# Prospeo Company Search

Use only Prospeo's company-search capability for this skill.

## What you may use

- Prospeo search suggestions for industry and location
- Prospeo company search
- The returned `pagination.total_count`

## What you must never use

- People search
- Person enrichment
- Email or mobile lookup
- Contact reveal
- More than one company-search page unless the member separately approves it

## Turn the business profile into filters

| Business detail | Prospeo filter |
|---|---|
| Company type or industry | `company_industry` or `company_keywords` |
| Country or region | `company_location_search` |
| Company size | `company_headcount_range` or `company_headcount_custom` |

Use Prospeo's search suggestions before searching. Use the exact industry and location values it returns. Do not guess a value.

## Cost and approval

A company-search page that returns companies may use one Prospeo credit. The first page normally includes the total company count, so it is enough for this skill.

Before searching, say: `Prospeo may use one credit to run this company search. Should I run it?` Wait for a clear yes.

## Read the result

Use the exact `pagination.total_count` returned by Prospeo. Do not estimate, turn it into a market size, or call it proof of demand.

## Official documentation

- [Prospeo MCP](https://prospeo.io/api-docs/mcp)
- [Search Company](https://prospeo.io/api-docs/search-company)
- [Company filters](https://prospeo.io/api-docs/filters-documentation)
