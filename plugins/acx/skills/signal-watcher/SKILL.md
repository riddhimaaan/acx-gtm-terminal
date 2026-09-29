---
name: signal-watcher
description: "Watches for companies that match the member's target and just showed a sign they may buy now: raised money, hiring for a role, a new leader, a launch, a new office, a new partner, or a new tool. For each matching company it also finds the right person (the new hire, or the member's buyer) with a verified work email, so the sheet's Leads tab can go straight into Smartlead, Aimfox or Gojiberry. Set up once, then runs every day and adds only what is new to the member's own Google Sheet, with the cost shown before and after each run. Uses Treg for signals, Prospeo, Icypeas and MillionVerifier for companies, people and emails, and Composio for Google Sheets. It never sends outreach. Use when someone says \"watch for signals\", \"trigger events\", \"buying signals\", \"who just raised\", \"who is hiring\", \"set up my signal watch\", or \"run my signals\"."
---

# Signal Watcher

**The rule for everything you write:** add only signals Treg actually returned, for companies that actually match the member's target. A signal is a reason to reach out now. It is not proof that the company will buy.

**Who this is for:** an agency owner who knows who they sell to and wants one Google Sheet that fills up every day with the companies that just did something worth reaching out about, and the right person to contact at each one, ready to drop into a campaign.

## How it should feel

Write for a busy business owner, using words a 10-year-old could understand.

- The Google Sheet is the output. It is where the member works: they sort it, filter it, and mark who they contacted.
- The **Leads** tab must be ready to import as it is. Its first columns use Smartlead's own field names, so the member can export it as a CSV and upload it without mapping anything.
- Signal Watcher stops at the sheet. It never adds leads to a campaign, sends a message, or starts a LinkedIn sequence. The member does that.
- The chat reply after each run is short: how many new rows were added, the cost, and the sheet link.
- Show the cost at the start and at the end of every run.
- Do not use words such as "intent data," "trigger events," or "firmographics." Say "signal," "what happened," and "company type."

## Two modes

Check for `ACX/signals/watch-setup.md`.

- **It does not exist:** run **Setup** (Steps 0 to 6), then the first **Daily run**.
- **It exists:** skip straight to the **Daily run** (Steps 7 to 12). Do not ask the setup questions again. If the member says "change my signals" or "change my targets", run only the setup step that changes, then update `watch-setup.md` and the sheet's Setup tab.

---

## Setup

### Step 0: Check both connections

Signal Watcher needs two connections:

1. **Treg** finds the signals. If the Treg tools are not in this chat, stop and say:
   `Signal Watcher needs the Treg connection. Connect the Treg MCP server in your chat-app connector settings, then sign in there. ACX never asks for or saves your key.`
2. **Composio with Google Sheets** holds the results. Read `references/google-sheet.md`. If the Composio tools are not in this chat, stop and say:
   `Signal Watcher saves your signals to a Google Sheet through Composio. Connect the Composio MCP server in your chat-app connector settings, then connect Google Sheets inside Composio.`
   If Composio is there but Google Sheets is not connected, use Composio's connection tool to start the Google Sheets sign-in. Show the member the sign-in link and wait until they say it is done.
   If more than one Google Sheets account is connected, list their email addresses and ask: `Which Google account should your signal sheet live in?` Save the chosen account's email and Composio account id in `watch-setup.md` (Step 6), and pass that account on every Google Sheets call from then on.

When both work, mark `Treg` and `Google Sheets (Composio)` as `available` in `ACX/setup-status.md`.

Then check the member's own lead tools, which Signal Watcher uses to look up companies, find people and check emails. Read `references/people-and-emails.md`. For each of **Prospeo**, **Icypeas** and **MillionVerifier**, find how it can be reached, in this order:

1. The member's own connection in this chat (its MCP server).
2. The member's own key registered in Treg (it shows in Treg's `my_tools`). These calls use the member's own credits and Treg does not charge for them.
3. Treg's catalog, which works without the member's account but is paid from the Treg balance.

Save the route for each tool in `watch-setup.md` (Step 6), and tell the member in one line which ones will spend Treg balance.

Read `references/treg-signals.md` before choosing any Treg endpoint. Use only the endpoints it lists.

### Step 1: Input one: which companies to watch

Read `ACX/outputs/icp.md` and `ACX/my-business.md` first.

If `icp.md` exists, pull these out and show them back in plain words:

- **Company type:** the strong-fit categories, plus adjacent fit if the member wants it
- **Where:** the priority locations and the locations to skip
- **Size:** the company-size rule
- **Skip:** the "Do not contact" list

Ask: `I will look for companies like this. Is that right, or should I change anything?`

If `icp.md` does not exist, ask only what is missing, two questions at a time:

1. What kind of companies do you want to find? Say it the way you would describe them to a friend.
2. Which countries or regions, and roughly what size (number of employees)?
3. Which companies should never show up, such as existing clients, competitors, or a type you avoid?

Then offer the optional list: `Do you also have specific companies you want me to keep an eye on? Paste their websites or give me a CSV. You can skip this, and you can add more later in the sheet.`

Tell the member the difference in one line: **finding new companies** searches the whole market for signals, while **watching named companies** checks only the companies on their list. Watching named companies costs money for each company every day, so keep the list under 50 unless they approve more.

Then settle **who to reach** at each matching company:

- **Buyer titles:** read `Buyer` from the ICP's `## Other rules`. Show it back with the usual variants, e.g. `Head of Marketing, VP Marketing, Marketing Director, CMO`, and ask the member to add or remove titles. These are the people found for every signal except "New leader".
- **New hires:** for the "New leader" signal, the person to reach is the one who was just hired. Ask how recent counts: `How recently must they have started? I suggest 90 days.`

If the member gives a durable new fact about their market, add it to `my-business.md` under `## What we learned later`.

### Step 2: Input two: which signals to watch

Show this menu. Pre-select every signal that matches a line in the ICP's `## Buy now when` section, and say which ICP line it came from.

| # | Signal | Plain meaning | Needs from the member |
|---|---|---|---|
| 1 | Raised money | announced a funding round | nothing |
| 2 | Hiring for a role | posted a job you care about | the job titles, e.g. "SDR", "Head of Marketing" |
| 3 | New leader | hired a new senior person, and Signal Watcher finds that person | which seats matter, e.g. "Head of Sales", "Head of Marketing" |
| 4 | Launched something | released a product or feature | nothing |
| 5 | Growing into new places | opened a new office or location | nothing |
| 6 | New partner | announced a partnership | nothing |
| 7 | Started using a tool | a new tool showed up on their site | the tools, e.g. "HubSpot", "Salesforce" |

Ask: `Which of these should I watch? Pick as many as you like.` Then ask for anything in the last column.

For signal 7 across the whole market, warn the member in one line: it is the priciest and noisiest signal. It costs the same whether results come back or not, it cannot filter by country or company type, and a loose tool name can match the wrong tool.

If the member wants a signal that is not on the menu, say that Signal Watcher cannot watch it yet, and do not invent a way to fake it.

### Step 3: Show the daily cost and set a limit

Work out the daily cost from the prices in `references/treg-signals.md` and `references/people-and-emails.md`, the chosen signals, the number of named companies, and the result caps. Add the lead-finding cost: about 5 matching companies a day unless the member expects more, each with one company lookup and up to 2 people. Check the live balance with Treg's `balance` tool. Google Sheets through Composio adds no cost. Show costs paid from the member's own Prospeo, Icypeas or MillionVerifier credits on a separate line, since they do not come out of Treg.

Show it like this:

```text
What this will cost each day
- Finding new companies that raised money: free (up to 5 checks a day)
- Finding new companies hiring "SDR" in 2 countries: about $0.03
- Watching 20 named companies for news: 20 × $0.04 = $0.80
- Finding people and emails for about 5 matching companies: about $0.25
Total from Treg: about $1.08 a day, about $32 a month.
From your own accounts instead: [only if routed there, e.g. "Icypeas and MillionVerifier credits for about 10 people a day"]
Your Treg balance right now: $12.40, which covers about 15 days.
```

Then ask: `Should I set a daily spend limit of $[total rounded up]? I will never spend more than that in one day without asking you.` Wait for a clear yes. If the balance covers fewer than 7 days, say so plainly.

### Step 4: Offer the daily schedule

If a scheduling tool is available in this chat, offer: `Do you want me to run this every morning at [time]?` Create the scheduled task only after a clear yes. The task runs `/acx:signal-watcher`.

If no scheduling tool is available, tell the member to run `/acx:signal-watcher` each day, or set up a scheduled task in their chat app.

### Step 5: Create the Google Sheet

Only now, after every answer is in, build the sheet. Follow `references/google-sheet.md` for the tool names, the tab layout and the column order.

1. If `watch-setup.md` already has a sheet link, use that sheet. Never create a second one.
2. Create one spreadsheet named `ACX Signals: [business name from my-business.md]`.
3. Rename the first tab to **Signals**, then add **Leads**, **Watch list**, **Run log** and **Setup** one at a time, in that order. Adding tabs at the same time puts them in a random order.
4. Write the header row on each tab, make it bold, and freeze it.
5. Make the Signals tab's Fit column a dropdown with only two choices: `ICP match` and `No ICP match`. Add the dropdowns on the Leads tab listed in `references/google-sheet.md`.
6. Fill the **Watch list** tab with any named companies from Step 1.
7. Fill the **Setup** tab with the answers from Steps 1 to 4.
8. Read the headers back once to check they landed in the right place.

Give the member the link: `Your signal sheet is ready: [link]. Companies with a new signal show up in the Signals tab, and the people to contact, with checked emails, in the Leads tab. You can add companies to the Watch list tab any time.`

### Step 6: Save the setup

Create `ACX/signals/watch-setup.md` using this exact shape:

```md
# Signal watch setup

Last changed: [date]
Last run: never

## Google Sheet
- Link: [spreadsheet link]
- Spreadsheet ID: [id]
- Google account: [email] (Composio account: [account id])

## Companies to watch
- Company type: [from Step 1]
- Where: [locations]
- Skip these locations: [or none]
- Size: [employee range, or Not known yet]
- Do not show: [list]

## Named companies
Kept in the sheet's Watch list tab.

## Who to reach
- Buyer titles: [list]
- New hires: started within the last [90] days, in these seats: [list]

## Lead tools
- Prospeo: [own connection, own key in Treg, or Treg catalog]
- Icypeas: [own connection, own key in Treg, or Treg catalog]
- MillionVerifier: [own connection, own key in Treg, or Treg catalog]

## Signals
- [Signal name]: [details such as job titles or seats] | [finding new, watching named, or both]

## Daily spend limit
$[amount] a day, approved on [date]

## Schedule
[Every day at 08:00, or: run by hand]
```

Also create `ACX/signals/seen.csv` with only this header:

```csv
first_seen,signal_id,company,website,signal
```

And create `ACX/signals/leads-seen.csv` with only this header:

```csv
first_seen,company_domain,person,linkedin_url,email
```

These two files are Signal Watcher's memory. They stop a signal or a person from coming back if the member deletes a row from the sheet.

Then go straight to the first Daily run.

---

## Daily run

### Step 7: Before spending: show the cost

1. Read `ACX/signals/watch-setup.md`, `ACX/signals/seen.csv` and `ACX/signals/leads-seen.csv`.
2. Read the sheet's **Watch list** tab. The member may have added or removed companies since the last run.
3. Check the balance with Treg's `balance` tool.
4. Work out today's estimate from the setup and today's Watch list.
5. Show it: `Today's run: about $[estimate] (your limit is $[limit]). Treg balance: $[balance].`
6. If the estimate is above the daily limit, or above the balance, stop and ask the member. Do not trim the setup or the Watch list silently.

The member approved the daily limit in setup, so a run within the limit does not need a new yes.

If the sheet cannot be reached, stop before spending anything and tell the member. Do not collect signals that have nowhere to go.

### Step 8: Look back to the last run

Use `Last run` as the start date for every "since" filter in `references/treg-signals.md`. If it says `never`, look back 7 days. If the last run was more than 7 days ago, look back only 7 days and say so in the chat reply.

### Step 9: Collect the signals

Run only the calls the setup needs. Follow `references/treg-signals.md` for which endpoint, which filters, and which result caps.

- One news call per named company covers signals 1, 3, 4, 5 and 6 together. Never make a separate call for each of those signals.
- Add up the `cost_usd` of every call as you go. If the running total reaches the daily limit, stop calling and note which checks were skipped.
- If a call fails, try once more. A Treg error with no charge costs nothing. If it fails again, note it as a check that did not run.

### Step 10: Clean, match and drop repeats

For every result:

1. **Is it a real company?** Drop headlines, investment funds raising their own fund, and rows with no clear company name. Count them as "not a company".
2. **Drop the obvious misses for free.** If the source already shows a clear miss (wrong country, clearly the wrong industry, on the "Do not show" list), drop it now, before paying for any lookup.
3. **Look the company up.** Every company left needs a domain, a headcount and an industry. If the source already gave all three (LinkedIn job results do), use them. Otherwise run one company lookup with Prospeo, following `references/people-and-emails.md`. If Prospeo does not know the company, try the source article or a quick web search for the domain. Store the domain in plain form, e.g. `checkmarble.com`, never `https://www.checkmarble.com/`.
4. **Does it match the target?** Check it against company type, location, size and the "Do not show" list in the setup. Judge only from the lookup, the source, or the company's own site.
   - Clear match on every rule: keep it, with Fit `ICP match`.
   - Clear miss (wrong industry, wrong country, wrong size, on the "Do not show" list): drop it and count the reason.
   - A real company in the right space, but a rule still cannot be confirmed after the lookup: keep it with Fit `No ICP match`, and say in "Fits because" what could not be confirmed. Never guess an industry or size to turn it into a match.
5. **Is it the same news twice?** The same event often arrives from two sources, or from both a market-wide check and the Watch list (for example, one funding round reported by two news sites). When the company, the signal and the date match within a few days, keep one row. Use the most detailed source, and put every record id in Signal ID, separated by ` / `.
6. **Is it new?** Drop any result whose id is already in `seen.csv`. A known company with a new signal still counts as new.
7. **Drop weak news.** Drop news events with a confidence below 0.7.

### Step 11: Find the people and their emails

Only for companies marked `ICP match`. Never spend on people at a `No ICP match` company. Follow `references/people-and-emails.md` for every call.

1. **Pick who to find.**
   - "New leader" signal: the person who was just hired.
   - Every other signal: people whose current title matches the buyer titles. Up to 2 per company, most senior first.
2. **Find them.**
   - If the news names the new hire, search for that name at the company's domain.
   - If it does not, search the company's domain for the chosen seat's titles.
   - For buyers, search the company's domain for the buyer titles.
3. **Check each person before keeping them.**
   - Their current company must be this company (same domain or same LinkedIn company page).
   - Their current title must match what the member asked for.
   - For a new hire, their start date in this role must fall inside the member's window (for example, 90 days). If it is older, this is not the new hire: drop them.
   - If two people could be the new hire and nothing tells them apart, keep both and set Lead status to `Needs check`. Never guess.
   - Drop anyone already in `leads-seen.csv`.
4. **Find the work email** from first name, last name and company domain. Work emails only. Never a personal email and never a phone number.
5. **Check the email.** Map the result to Email status:
   - `ok` → `valid`
   - `catch_all` or `unknown` → `risky`
   - `invalid` or `disposable`, or a shared inbox like `info@` → drop the email. Email status `LinkedIn only`.
   - No email found → `LinkedIn only`.
6. **Write the personal line:** one plain sentence, under 20 words, built only from the real signal. For example: `Congrats on stepping in as Head of Sales at Reco.` or `Saw the €6.5M Series A led by Smartfin, congrats.` No flattery, no guesses, no claims about the company that the source does not support.
7. **When nobody can be found:** add no lead. Note the company in the Run log's "Companies with no lead found" count. The company still stays in the Signals tab.

Add up every cost as you go, together with the signal costs. If the running total reaches the daily limit, stop finding people and say how many companies were left without leads.

### Step 12: Update the sheet, then show the cost again

1. **Signals tab:** append one row per new signal, in the column order from `references/google-sheet.md`. Set Status to `New`. Put companies with more than one signal today next to each other.
2. **Leads tab:** append one row per person, in the column order from `references/google-sheet.md`. Put people with a `valid` email first, then `risky`, then LinkedIn only.
3. **Never change rows that are already in the sheet.** The Status and Notes columns belong to the member.
4. Add every new signal to `ACX/signals/seen.csv`, including every id of a merged row, and every new person to `ACX/signals/leads-seen.csv`.
5. Check the balance with Treg's `balance` tool again.
6. **Run log tab:** append one row with today's date, the estimate, the actual spend, the balance before and after, the counts, and any checks that did not run.
7. Set `Last run` in `watch-setup.md` to today.
8. End the chat reply with:

```text
Added [number] new signals from [number] companies, and [number] leads ([number] with a valid email, [number] risky, [number] LinkedIn only): [link]
Skipped [number]: [short reasons, e.g. "4 outside your countries, 2 were investment funds"]
This run cost $[actual] (estimated $[estimate]). Treg balance: $[before] → $[after].
Next: filter the Leads tab to Email status = valid, export it as a CSV and upload it to Smartlead. Send the LinkedIn-only rows to Aimfox or Gojiberry.
```

If nothing new came in, still add the Run log row and say: `Nothing new today. This run cost $[actual].` A quiet day is a real result.

## Things you must never do

- Spend more than the daily limit, or run any paid call before the limit is approved.
- Create a second spreadsheet when one is already saved in `watch-setup.md`.
- Edit, reorder or delete rows the member already has in the sheet.
- Look up people at a company that is not an `ICP match`.
- Look up personal emails, phone numbers or home addresses. Work emails only.
- Mark an email `valid` unless the email check returned `ok`.
- Add leads to a campaign, send any message, or start a LinkedIn sequence. The member does that.
- Use an endpoint that is not in `references/treg-signals.md` or `references/people-and-emails.md`.
- Put a guess in the personal line. It says only what the signal says.
- Invent a signal, a date, a funding amount, a company size, an industry, a person, a title or an email.
- Add a company from the "Do not show" list.
- Add the same signal twice.
- Call a signal proof that a company will buy.
- Save a Treg key, a Google password, or any key in the ACX folder or the sheet.
