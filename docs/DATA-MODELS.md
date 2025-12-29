# Data Models

## Core Schemas

### Organization & User
```sql
Organization (
  id UUID PRIMARY KEY,
  name VARCHAR,
  subscription_tier ENUM,
  billing_info JSONB
)

User (
  id UUID PRIMARY KEY,
  organization_id UUID,
  email VARCHAR UNIQUE,
  role ENUM
)
```

### Workflow & Agent
```json
{
  "workflow": {
    "id": "uuid",
    "definition": {
      "agents": [],
      "connections": [],
      "triggers": []
    }
  },
  "agent": {
    "configuration": {
      "model": "gpt-4o",
      "tools": [],
      "memory": {}
    }
  }
}
```

### Execution Tracking
```sql
WorkflowExecution (
  id UUID,
  status ENUM,
  input_data JSONB,
  output_data JSONB,
  token_usage JSONB
)

AgentMetrics (
  metric_type ENUM,
  value FLOAT,
  dimensions JSONB
)
```

Full schemas in [shared/data-models](shared/data-models/)