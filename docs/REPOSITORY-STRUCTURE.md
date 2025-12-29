# Repository Structure

```
process-copilot/
├── services/           # Microservices
│   ├── api-gateway/
│   ├── workflow-engine/
│   └── observability/
├── frontend/           # Next.js app
├── infrastructure/     # Terraform/K8s
├── docs/               # Architecture, guides
└── ml-models/          # Evaluators
```

**Monorepo with Turborepo/Nx**

See [services/api-gateway/package.json](services/api-gateway/) for setup.