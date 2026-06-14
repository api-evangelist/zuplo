# Zuplo GraphQL Schema

## Overview

This is a conceptual GraphQL schema for the Zuplo API management platform. Zuplo does not currently expose a public GraphQL endpoint; this schema models the platform's core resources—projects, deployments, API keys, consumers, rate limits, analytics, security, and developer portal management—as they are described in the Zuplo Developer API (ZAPI) and product documentation.

## Source

- **Provider**: Zuplo
- **Base URL**: https://dev.zuplo.com
- **Documentation**: https://zuplo.com/docs/articles/developer-api
- **API Reference**: https://zuplo.com/docs/api
- **Schema type**: Conceptual (derived from REST API surface and product documentation)
- **Schema file**: zuplo-schema.graphql

## Coverage

The schema covers 55 types spanning the full Zuplo platform surface:

| Domain | Types |
|---|---|
| Projects & Environments | APIProject, APIEnvironment, EnvironmentVariable, ProjectMember |
| Gateway & Routing | APIGateway, Route, RouteConfig, RequestHandler, ResponseTransformer |
| Policies | Policy, PolicyConfig, TrafficFilter |
| Authentication & Authorization | Authentication, OAuthProvider, JWTConfig, APIKeyAuth |
| API Keys & Consumers | APIKey, APIKeyBucket, APIConsumer, ConsumerGroup, ConsumerManager |
| Rate Limiting & Quotas | RateLimit, RateLimitWindow, Quota, QuotaUsage |
| Deployments | Deployment, DeploymentStatus, DeploymentLog, Redeploy |
| Custom Domains & TLS | CustomDomain, SSLCertificate, DomainVerification |
| Analytics & Observability | Analytics, RequestLog, ErrorLog, Usage, Bandwidth, Latency, P50Latency, P99Latency |
| Security | SecurityEvent, IPBlock, GeoBlock, BotProtection, WAFRule |
| Monetization | Plan, Feature, Subscription, ConsumerBilling |
| Developer Portal | DeveloperPortal, PortalConfig |
| Integrations & Events | Integration, Plugin, Webhook, EventLog |
| Tunnels | Tunnel, TunnelToken |
| Audit | AuditLog |

## Notes

- A live GraphQL introspection query against `https://api.zuplo.com/graphql` returned HTTP 404, confirming no public GraphQL endpoint exists as of June 2026.
- This schema is inferred from the REST API's resource model, the Zuplo JSON Schema artifacts in `json-schema/`, and the product feature set documented at https://zuplo.com/docs.
- All types, fields, and relationships represent the logical data model of the Zuplo platform and are suitable for GraphQL gateway design, federation planning, or client tooling scaffolding.
