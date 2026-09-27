# ACX GTM Terminal

One install. Every ACX agent.

## Install (one command)

```
claude plugin marketplace add riddhimaaan/acx-gtm-terminal && claude plugin install acx@acx -y
```

**Claude Desktop:** Settings, then Plugins, then Add marketplace, and paste `riddhimaaan/acx-gtm-terminal`. Then install **ACX**.

## Start here

```
/acx:onboarding
```

This asks a few plain questions about the member's business and creates their shared ACX folder. If they opened Cowork in a specific folder, ACX saves there. If not, it creates `~/ACX` and tells them. No external tool or API key is needed to begin.

Then run:

```
/acx:start
```

That is the router. It reads what the member asks, chooses the right skill, and carries useful context into the next step.

## What is inside

| Skill | Use it when |
|---|---|
| `start` | always - the router that runs the rest |
| `market-scanner` | is my market still worth selling into, how crowded is it |
| `category-gap-finder` | where have competitors left a spot open |
| `icp-builder` | who should I sell to, pick my niche |
| `lead-grader` | check this list before I send it |
| `offer-architect` | fix my offer, make it easier to understand |
| `guarantee-designer` | make it safe to buy, risk reversal |
| `positioning-builder` | my positioning, my one-liner |
| `message-tester` | does this message land |
| `outlier-finder` | find LinkedIn content angles from posts already working in my niche |

## Where your files go

- `ACX/my-business.md` - the member's business details. Every agent reads it, and the router keeps it up to date. Asked once, never twice.
- `ACX/setup-status.md` - which optional tools are available. No keys are stored here.
- `ACX/outputs/` - one file per agent: `market-scan.md`, `gap-finder.md`, `icp.md`, `graded-list.csv`, `offer.md`, `guarantee.md`, `positioning.md`, `message-test.md`.

No API keys are stored in this repo.

## Provenance

Eight of the nine skills are forks of public MIT-licensed agent skills, renamed to the ACX agent names and given an ACX output contract. Sources, licences and what was changed are in [CREDITS.md](CREDITS.md); licence texts are kept verbatim in [`_licences/`](_licences/).
