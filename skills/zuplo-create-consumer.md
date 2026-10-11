---
name: zuplo-create-consumer
description: Create a new API key consumer, retrieve its details, and optionally roll its key.
api: openapi/zuplo-api-keys-consumers-api-openapi.yml
operations:
- ApiKeyConsumersService_create
- ApiKeyConsumersService_read
- ApiKeyConsumersService_rollKey
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/zuplo-api-keys-consumers-api-openapi.yml ; every operationId checked against the contract
---

# zuplo-create-consumer

Create a new API key consumer, retrieve its details, and optionally roll its key.

## Steps

1. 1. Use `ApiKeyConsumersService_create` with body fields `consumerName`, `description` (if any) and header `Authorization`.
2. 2. Use `ApiKeyConsumersService_read` with path parameters `accountName`, `bucketName`, `consumerName` and header `Authorization` to get the consumer details.
3. 3. (Optional) Use `ApiKeyConsumersService_rollKey` with the same path parameters and header `Authorization` to rotate the consumer's key.

## Rules

- Authentication: Include the API key in the `Authorization` header as defined by the `ApiKeyAuth` scheme.
- Idempotency: The `ApiKeyConsumersService_create` operation is not idempotent; repeat calls will create duplicate consumers unless a unique `consumerName` is provided.
- Errors: The API returns standard HTTP error codes; on missing or invalid `Authorization` a 401 is returned, and on not found resources a 404.
