---
name: use-staging-mcp
description: >
  Use the Investair_data_staging connector (staff tester MCP), never
  production Investair_data. For Investair staff testing staging only.
metadata:
  version: "0.18.11"
---

# Use Investair staging MCP

This plugin is a **staff tester**. It is not the production Investair plugin.

- Call tools through connector **`Investair_data_staging`**.
- Do **not** use production **`Investair_data`** / `mcp.investair.com.au` in this plugin.
- Skills are the public v0.18.11 set (snapshot, initiation, sector, peers, digests). They are not the private v0.19 plugin.
- Do not tell customers or brokers to install this marketplace.
- If the connector is missing, ask the user to add the custom MCP URL from this repo's README, then sign in with Clerk org **Investair staging testers**.
