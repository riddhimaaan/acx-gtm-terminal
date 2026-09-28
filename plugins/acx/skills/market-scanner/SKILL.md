---
name: market-scanner
description: "Uses Prospeo's company search to count companies matching the member's target market. Use when someone says \"scan my market\", \"how many companies match my target\", \"is this market big enough\", or runs Module 1 Video 2 of the ACX program."
---

<!--
ACX fork. Source: https://github.com/RohitWaghire/Deep-Market-Reasearch (MIT, stated in README).
Rewritten for the ACX GTM Terminal: the member is an agency owner already at revenue.
See forks/CREDITS.md.
-->

# Market Scanner

**The rule for everything you write:** report only the company count Prospeo actually returns. Never turn a database count into a claim that companies are ready to buy.

**Who this is for:** an agency owner, consultant, or service operator who wants to know how many companies match their target before they spend time chasing that market.

## How the final answer should feel

Write for a busy business owner, using words a 10-year-old could understand. The research can be detailed; the final answer must not be.

- Put the answer first.
- Keep the main report to one page.
- Use one idea per sentence and short headings that ask a real question.
- Show the count and the filters used.
- Explain what the count does and does not mean in plain words.
- End with no more than three actions the member can take next.
- Do not use words such as "TAM," "market saturation," or "demand signals."

## Step 0: Get the company filters

Read `ACX/my-business.md` and `ACX/setup-status.md` first. You need all three facts below:

- the type of company to find
- the country or region
- the company size

Use the saved `## Company search filters` section when it exists. If one fact is missing, ask only for that fact and save the answer there.

Check that Prospeo company search is marked `available`. If it is not, stop and say: `Market Scanner needs the Prospeo company-search connection. Run /acx:onboarding to connect it.` Do not replace it with people search or broad web research.

## Step 1: Prepare the search

Read `references/prospeo-company-search.md`.

Use only these company filters:

- company type, industry, or keywords
- company headquarters location
- company size

Use Prospeo's search suggestions to select its exact industry and location values. Show the member the filters in plain language, then ask: `Prospeo may use one credit to run this company search. Should I run it?` Wait for a clear yes.

## Step 2: Run one company search

Use only Prospeo's company-search tool. Never use people search, contact search, enrichment, email lookup, or phone lookup.

Run one approved company search. Read the returned `pagination.total_count` as the count. If Prospeo does not return a reliable total, say that it did not return a reliable total. Do not estimate.

## Step 3: Explain the count honestly

Say that the count is the number of companies matching the saved filters in Prospeo right now. It does **not** tell us how many are ready to buy, prove demand, or prove that the filters are perfect.

## Step 4: Choose the next move

Offer no more than two choices:

1. Narrow or widen one filter, then run a new search only after approval.
2. Run `category-gap-finder` to look for a clearer angle inside this company group.

## What to write

Save to `ACX/outputs/market-scan.md` using this exact shape:

```md
# How many companies match my target?

## Short answer
Prospeo found [company count] companies matching [short description].

## What we searched for
- Company type: [filter used]
- Location: [filter used]
- Company size: [filter used]

## What this means
These are companies that match the filters in Prospeo. This is not a count of companies ready to buy.

## What to do next
1. [Narrow or widen one filter, if needed.]
2. Run `category-gap-finder` to find a clearer angle for these companies.
```

Save the result to `ACX/outputs/market-scan.md`. Keep any raw Prospeo response outside the member report.

## Things you must never do

- Search for people, contacts, emails, or phone numbers.
- Run Prospeo before the member clearly approves the search.
- Guess a filter value or a company count.
- Call the count demand, TAM, or proof that companies will buy.
- Hide a missing filter. Ask for it instead.
