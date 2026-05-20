---
title: "Rate Limit LLM APIs by Tokens Not Requests"
url: "https://zuplo.com//blog/rate-limit-llm-apis-by-tokens-not-requests"
date: "2026-05-12T00:00:00.000Z"
author: ""
feed_url: "https://zuplo.com/blog/atom.xml"
---
Requests-per-minute is the wrong meter for LLM endpoints. One call can be 50 tokens or 50,000. Rate limit on input and output tokens with Zuplo's complex-rate-limit-inbound policy and the real counts from each upstream response.
