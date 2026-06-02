---
title: "Never Ship an MCP Server Without a Rate Limit"
url: "https://zuplo.com//blog/never-ship-mcp-server-without-rate-limit"
date: "2026-05-18"
feed_url: "https://zuplo.com/blog/atom.xml"
---
GitHub's MCP server inherits the 5,000/hour REST API limit, and that's the only thing standing between an agent and a suspended account. Most public MCP servers either have no limit, the wrong limit, or one so tight it breaks their own protocol. Put a real rate limit on every MCP route you publish.
