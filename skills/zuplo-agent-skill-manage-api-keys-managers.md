---
name: zuplo-agent-skill-manage-api-keys-managers
description: Manage API Key managers for a consumer by listing existing managers, creating a new manager, and deleting a manager.
api: openapi/zuplo-api-keys-managers-api-openapi.yml
operations:
- ApiKeyConsumerManagers_list
- ApiKeyConsumerManagers_create
- ApiKeyConsumerManagers_delete
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/zuplo-api-keys-managers-api-openapi.yml ; every operationId checked against the contract
---

# zuplo-agent-skill-manage-api-keys-managers

Manage API Key managers for a consumer by listing existing managers, creating a new manager, and deleting a manager.

## Steps

1. 1. Call `ApiKeyConsumerManagers_list` with path parameters `accountName`, `bucketName`, and `consumerName`.
2. 2. Call `ApiKeyConsumerManagers_create` with path parameters `accountName`, `bucketName`, `consumerName` and a request body containing the manager details.
3. 3. Call `ApiKeyConsumerManagers_delete` with path parameters `accountName`, `bucketName`, `consumerName`, and `managerId`.

## Rules

- Include the `Authorization` header with the API key as defined by the `ApiKeyAuth` scheme.
- No rate‑limit information is provided; handle HTTP responses accordingly.
