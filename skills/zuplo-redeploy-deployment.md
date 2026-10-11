---
name: zuplo-redeploy-deployment
description: Redeploy an existing deployment and verify its status.
api: openapi/zuplo-deployments-api-openapi.yml
operations:
- DeploymentsService_read
- DeployService_redeploy
- V1_deploymentStatus
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/zuplo-deployments-api-openapi.yml ; every operationId checked against the contract
---

# zuplo-redeploy-deployment

Redeploy an existing deployment and verify its status.

## Steps

1. 1. `DeploymentsService_read` – provide `deploymentName` path parameter.
2. 2. `DeployService_redeploy` – provide `deploymentName` path parameter and include any required request body (none specified).
3. 3. `V1_deploymentStatus` – provide `accountName`, `projectName`, and `statusId` path parameters to retrieve the deployment status.

## Rules

- Auth: Include an `Authorization` header with the API key (ApiKeyAuth).
- Idempotency: The `DeployService_redeploy` operation is not documented as idempotent; avoid repeated calls without checking status.
- Pagination: Not applicable to these operations.
- Errors: Follow standard HTTP error responses; no specific error codes are documented.
