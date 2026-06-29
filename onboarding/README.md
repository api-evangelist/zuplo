# Programmatic API Onboarding — Zuplo

A single-file, zero-dependency Node.js (18+) CLI that reproduces SoundCloud's
`sc-api-auth.mjs` pattern for Zuplo: register an application / obtain credentials
programmatically instead of clicking through a dashboard, so agents and developers
can onboard at the command line.

- Script: [`zuplo-api-auth.mjs`](zuplo-api-auth.mjs)
- Run `node zuplo-api-auth.mjs --help` for usage and the required environment variables.
- Story / rationale: https://apievangelist.com/2026/07/20/zuplo-has-the-onboarding-api-wrong-door/

Part of the API Evangelist "Programmatic API Onboarding for the Agentic Moment" series.
