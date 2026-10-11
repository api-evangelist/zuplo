---
name: zuplo-tunnel-create-and-list
description: Create a new tunnel and then list all tunnels for the account.
api: openapi/zuplo-tunnels-api-openapi.yml
operations:
- TunnelService_create
- TunnelService_list
generated: '2026-10-04'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/zuplo-tunnels-api-openapi.yml ; every operationId checked against the contract
---

# zuplo-tunnel-create-and-list

Create a new tunnel and then list all tunnels for the account.

## Steps

1. 1. Call `TunnelService_create` with the required request body fields for creating a tunnel.
2. 2. Call `TunnelService_list` with the required path parameter `accountName` and optional query parameters for pagination if needed.

## Rules

- Auth: Include an `Authorization` header with the API key (ApiKeyAuth).
- Pagination: `TunnelService_list` supports pagination via standard query parameters as defined in the contract.
