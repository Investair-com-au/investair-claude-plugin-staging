# Staff tester marketplace

This repo is the **staff tester** Claude marketplace: the `investair-staging` plugin, pointed at the staging connector.

**This repository is publicly readable.** It has to be, because Claude's *Add marketplace, Add from a repository* flow only accepts public repos. "Staging" describes who it is for, not who can see it. Treat every file here as published to the open internet.

Full prose skills and recipes are fine here. Data internals are not.

## Never commit here

SQL, table or column names, `describe_table`, `list_allowed_tables`, schema, data-lake paths, or pre-built page assets that embed queries. Those stay in the private plugin.

## Before you push

```bash
rg -nE '(ASX_Market|Cashflow|Placement|Broker|Feed_Public|ATM_Screening)\.[A-Za-z_]+|\bSELECT\b|describe_table|list_allowed_tables' .
```

A clean result is required. CI runs the same check and fails the build on any hit.

Work in the private plugin first, then port here with the staging substitutions: connector name, slash-command prefix, and the tester disclaimers.
