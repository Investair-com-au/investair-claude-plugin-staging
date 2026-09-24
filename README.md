# Investair staging tester (staff only)

**This is not the production Investair plugin.** Do not give this repo to customers or brokers.

Staff-only Claude marketplace for the **staging** MCP. No API keys in this repo.

| | Production (customers) | This repo (staff testers) |
|--|--|--|
| Marketplace | `Investair-com-au/investair-claude-marketplace` | `Investair-com-au/investair-claude-plugin-staging` |
| Plugin | `investair` | `investair-staging` |
| Connector | `Investair_data` | `Investair_data_staging` |
| MCP URL | `https://mcp.investair.com.au/mcp/prefect-v1` | tester gateway below |

This org also hosts the public product marketplace. Add **that** repo for live `Investair_data`. Add **this** repo only if you are testing staging.

## Install (staff)

1. Claude → **Add marketplace** → paste **exactly** one of:
   - `Investair-com-au/investair-claude-plugin-staging`
   - `https://github.com/Investair-com-au/investair-claude-plugin-staging.git`
2. Install plugin **investair-staging** (not `investair`).
3. Sign in with your **@investair.com.au** email when prompted.
4. Use connector **`Investair_data_staging`**, not production `Investair_data`.

If login says staff-only, ask Terry to add you to Clerk org **Investair staging testers**.

## Custom connector (if Add marketplace fails)

1. Keep production `Investair_data` as-is.
2. Add custom MCP connector `Investair_data_staging`.
3. URL (no Bearer key):

   `https://investair-mcp-gateway-staging-production-ff8dc0f.zuplo.app/mcp/prefect-v1`

4. Sign in with the staging Clerk app (not the production connector session).

## What is public vs secret

| In this repo | On the server only |
|--------------|--------------------|
| Tester gateway URL | Horizon `fmcp_` key |
| Plugin name | Clerk OAuth client secret |
| | Clerk org gate |

Anyone can install the plugin. They cannot read Investair data without a Clerk login in **Investair staging testers**.
