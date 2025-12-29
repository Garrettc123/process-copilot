# System Architecture

## Multi-Layer Design [web:1][web:19]

### Layer 1: Data Foundation
- Data Integration Hub (Kafka event-driven) [web:58]
- PostgreSQL + Redis + MongoDB
- API Gateway (rate limiting, auth)

### Layer 2: Agent Orchestration
- Multi-Agent Coordinator (hierarchical) [web:13]
- Temporal.io Workflow Engine [web:23]
- Dynamic Task Graph Manager [web:12]

### Layer 3: Execution
- Containerized Agent Runtime (Kubernetes)
- Tool Integration Framework
- Bidirectional Reflection Protocol [web:10]

### Layer 4: Observability [web:27][web:61]
- OpenTelemetry + Jaeger
- Langfuse for agent traces [web:69]
- Custom evaluators (relevancy, completion)

### Layer 5: UI/UX
- Next.js + React Flow workflow builder
- Role-based dashboards

## Tech Stack
**Backend:** Node.js/Python, FastAPI, Temporal.io
**Data:** PostgreSQL, Redis, Pinecone
**Frontend:** Next.js 14, Shadcn/ui
**Observability:** Prometheus, Grafana, ELK

[Full details →](https://github.com/Garrettc123/process-copilot/tree/main/docs)