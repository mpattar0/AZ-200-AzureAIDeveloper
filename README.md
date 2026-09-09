# AI-200: Developing AI Cloud Solutions on Azure

Personal hands-on learning workspace for the AI-200 exam, organized into **9 topic areas and 26 labs**.

## Official resources

- [Microsoft lab repository](https://github.com/MicrosoftLearning/mslearn-azure-ai)
- [Complete lab instructions](https://microsoftlearning.github.io/mslearn-azure-ai/)
- [AI-200 course and learning paths](https://learn.microsoft.com/en-us/training/courses/ai-200t00/)
- [AI-200 exam study guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/ai-200)

## How to use this workspace

1. Open a lab README below and follow its official instructions.
2. Check the lab's current prerequisites, subscription requirements, permissions, and costs before deploying resources.
3. Add your implementation files inside that lab's folder. No Microsoft starter code has been downloaded or copied into this workspace.
4. Record setup decisions, implementation notes, validation results, and resource cleanup in the lab README.
5. Mark the checkbox below when the lab is complete.

**Cost reminder:** These labs can create billable Azure resources. Follow each lab's cleanup instructions and verify that resources are removed when no longer needed. The ACR Tasks exercise currently requires a paid subscription rather than Azure free credits.

## Terraform structure

Infrastructure code belongs in the single repository-level [Terraform directory](terraform/README.md), separate from the lab exercises. It contains **16 reusable service-module scaffolds**, TEST/UAT/PROD environment folders, and the five root Terraform files. See the [module catalogue and all 26 lab mappings](terraform/Modules/README.md). The files are placeholders only; no Azure resources or backend are configured.

Local Terraform runs are limited to formatting, validation, and planning. All apply and destroy operations must use GitHub Actions with OIDC; deployment workflows have not been implemented yet.

## Folder structure

Each lab folder contains a README with its official exercise link and space for notes. Add code and other files as you work through the lab; do not commit credentials, connection strings, or other secrets.

```text
labs/
├── 01-container-hosting/
│   ├── 01-acr-tasks/
│   ├── 02-app-service-container/
│   └── 03-app-service-sidecar/
├── 02-container-apps/
│   ├── 01-deploy-backend-api/
│   ├── 02-troubleshoot-deployment/
│   └── 03-keda-autoscaling/
├── 03-azure-kubernetes-service/
│   ├── 01-deploy-inference-api/
│   ├── 02-configure-apps/
│   └── 03-troubleshoot-apps/
├── 04-cosmos-db/
│   ├── 01-rag-document-store/
│   ├── 02-semantic-search/
│   └── 03-optimize-vector-indexes/
├── 05-postgresql/
│   ├── 01-agent-tool-backend/
│   ├── 02-vector-search/
│   └── 03-optimize-vector-search/
├── 06-managed-redis/
│   ├── 01-data-operations/
│   ├── 02-publish-subscribe/
│   └── 03-semantic-search/
├── 07-integrate-services/
│   ├── 01-service-bus-messages/
│   ├── 02-event-grid-events/
│   ├── 03-functions-mcp-server/
│   └── 04-durable-functions-workflow/
├── 08-secrets-configuration/
│   ├── 01-key-vault-secrets/
│   └── 02-app-configuration/
└── 09-monitoring/
	├── 01-opentelemetry/
	└── 02-kql-queries/
```

## Lab checklist

### 01. Container hosting

- [ ] [Build and run a container image with ACR Tasks](labs/01-container-hosting/01-acr-tasks/README.md)
- [ ] [Deploy a container to Azure App Service](labs/01-container-hosting/02-app-service-container/README.md)
- [ ] [Deploy an AI API with a local model-serving sidecar](labs/01-container-hosting/03-app-service-sidecar/README.md)

### 02. Azure Container Apps

- [ ] [Deploy a containerized backend API](labs/02-container-apps/01-deploy-backend-api/README.md)
- [ ] [Diagnose and fix a failing deployment](labs/02-container-apps/02-troubleshoot-deployment/README.md)
- [ ] [Configure autoscaling using KEDA](labs/02-container-apps/03-keda-autoscaling/README.md)

### 03. Azure Kubernetes Service

- [ ] [Deploy an AI inference API to AKS](labs/03-azure-kubernetes-service/01-deploy-inference-api/README.md)
- [ ] [Configure apps on AKS](labs/03-azure-kubernetes-service/02-configure-apps/README.md)
- [ ] [Troubleshoot apps on AKS](labs/03-azure-kubernetes-service/03-troubleshoot-apps/README.md)

### 04. Azure Cosmos DB for NoSQL

- [ ] [Build a RAG document store](labs/04-cosmos-db/01-rag-document-store/README.md)
- [ ] [Build a semantic search application](labs/04-cosmos-db/02-semantic-search/README.md)
- [ ] [Optimize query performance with vector indexes](labs/04-cosmos-db/03-optimize-vector-indexes/README.md)

### 05. Azure Database for PostgreSQL

- [ ] [Build an agent tool backend](labs/05-postgresql/01-agent-tool-backend/README.md)
- [ ] [Implement vector search](labs/05-postgresql/02-vector-search/README.md)
- [ ] [Optimize vector search performance](labs/05-postgresql/03-optimize-vector-search/README.md)

### 06. Azure Managed Redis

- [ ] [Perform data operations](labs/06-managed-redis/01-data-operations/README.md)
- [ ] [Publish and subscribe to events](labs/06-managed-redis/02-publish-subscribe/README.md)
- [ ] [Implement semantic search](labs/06-managed-redis/03-semantic-search/README.md)

### 07. Integrate backend services

- [ ] [Process messages with Azure Service Bus](labs/07-integrate-services/01-service-bus-messages/README.md)
- [ ] [Publish and receive events with Azure Event Grid](labs/07-integrate-services/02-event-grid-events/README.md)
- [ ] [Create an MCP server with Azure Functions](labs/07-integrate-services/03-functions-mcp-server/README.md)
- [ ] [Build a document-processing workflow with Azure Durable Functions](labs/07-integrate-services/04-durable-functions-workflow/README.md)

### 08. Secrets and configuration

- [ ] [Manage secrets with Azure Key Vault](labs/08-secrets-configuration/01-key-vault-secrets/README.md)
- [ ] [Retrieve settings and secrets from Azure App Configuration](labs/08-secrets-configuration/02-app-configuration/README.md)

### 09. Monitoring and troubleshooting

- [ ] [Instrument an app with the OpenTelemetry SDK](labs/09-monitoring/01-opentelemetry/README.md)
- [ ] [Query logs with KQL](labs/09-monitoring/02-kql-queries/README.md)

The exercise list was checked against Microsoft's lab index on **2026-09-09**. Exercises may change; use the official course and study guide to confirm current exam coverage.

---
*AI disclosure: This README and the initial lab README templates were generated by GitHub Copilot. Lab implementation and completion are left to the learner.*
