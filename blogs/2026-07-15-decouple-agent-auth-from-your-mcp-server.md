---
title: "Decouple Agent Auth From Your MCP Server"
url: "https://zuplo.com//blog/decouple-agent-auth-mcp-server"
date: "2026-07-15"
feed_url: "https://zuplo.com/blog/atom.xml"
---
Your agent's cloud identity shouldn't be wired straight into your MCP server. Put a gateway in the middle to translate auth, hand the upstream a scoped token, and enforce role-based access on every tool.
