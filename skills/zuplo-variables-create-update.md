---
name: zuplo-variables-create-update
description: Create a new variable and then update it in a specific branch of a project.
api: openapi/zuplo-variables-api-openapi.yml
operations:
- VariablesService_create
- VariablesService_update
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/zuplo-variables-api-openapi.yml ; every operationId checked against the contract
---

# zuplo-variables-create-update

Create a new variable and then update it in a specific branch of a project.

## Steps

1. 1. Call `VariablesService_create` with the required request body fields for the variable and include the `Authorization` header.
2. 2. Call `VariablesService_update` with the `variableName` path parameter, the updated request body fields, and include the `Authorization` header.

## Rules

- Auth: Provide an API key in the `Authorization` header (ApiKeyAuth).
- No idempotency key is required.
- No pagination applies.
- Errors follow standard HTTP error responses; no specific error codes are documented.
