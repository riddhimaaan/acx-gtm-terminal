# Optional tools for ACX

You do not need any external tool, MCP server, or API key to use the core ACX skills. They work with normal web research and files in the member's working folder.

## Use only when needed

| Tool | Use it when | Do not use it when |
|---|---|---|
| Google Drive or Sheets | The member's lead list or report already lives in Google Drive. | They gave you a CSV or pasted the list in chat. |
| Apify | The member wants Outlier Finder to collect recent LinkedIn posts from chosen public profiles or normal web research cannot collect enough public information. | A few web pages, reviews, job posts, or competitor sites answer the question. |
| Prospeo MCP | The member runs Market Scanner. It counts companies matching their target company filters. | You need people, emails, phone numbers, or a broad web search. Market Scanner never uses those. |

## Not needed for this plugin

This plugin does not require a sending tool, email-enrichment tool, email-verification tool, CRM, or automation platform. Prospeo is required for Market Scanner and is connected as an MCP server. The member signs in through their chat-app connector settings; never save a Prospeo key in the ACX folder. Apify is optional, and Outlier Finder uses only `harvestapi/linkedin-profile-posts`.

## Safety rule

Before using any paid API, scraper, enrichment service, or sending tool, tell the member what it will do, what it may cost, and ask for a clear yes. Never save credentials in the ACX folder.
