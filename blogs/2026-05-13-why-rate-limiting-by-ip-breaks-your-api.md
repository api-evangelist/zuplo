---
title: "Why Rate Limiting by IP Breaks Your API"
url: "https://zuplo.com//blog/dont-rate-limit-by-ip"
date: "2026-05-13T00:00:00.000Z"
author: ""
feed_url: "https://zuplo.com/blog/atom.xml"
---
Carrier-grade NAT, cloud egress reuse, and shared proxies put unrelated callers behind one IP address, so an IP-based rate limit punishes the wrong people. Rate-limit by API key or JWT subject with Zuplo's rate-limit-inbound policy instead.
