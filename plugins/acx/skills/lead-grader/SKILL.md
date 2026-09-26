---
name: lead-grader
description: Grades every row of a lead list against the member's best-fit rules. Adds pass or fail, a one-line reason, a confidence level and what is missing to each row, then says what the result means and where the bad rows came from. Use when someone says "grade my list", "check this list", "score my leads", "is this list any good", "clean my list before sending", or runs Module 2 Video 3 of the ACX program.
---

<!--
ACX fork. Source: https://github.com/LeadMagic/gtm-skills (MIT), skill `foundation/icp-scoring`.
Rewritten for the ACX GTM Terminal: agency owners already at revenue. See forks/CREDITS.md.
-->

# Lead Grader

**The rule for everything you write:** grade on what is actually in the row. Anything missing gets flagged as missing — never filled in with a guess.

**Who this is for:** an agency owner with a list in hand and about to spend money and time sending to it. This is the check that happens *before* the send.

## Step 0: Load the rules and the list

Read the ICP in `ACX/my-business.md`. If there is no ICP yet, stop and say so — grading against nothing is guesswork.

Then take the list: a CSV, a paste, however they have it.

## Step 1: Turn the ICP into a checklist

Two short lists before touching a single row:

- **Must have** — the lines that make someone a fit.
- **Hard no** — the disqualifiers. Any of these means fail, no matter how good the rest looks.

Show the member the two lists and get a yes before grading. This is the bar everything is scored against.

## Step 2: Practice round

Grade **10 rows first** and show them. If the bar is off, fix it now rather than after 500 rows.

## Step 3: Only fill gaps with a yes

Some rows will be missing a company size or an industry. Filling those in usually costs money (enrichment credits, a paid lookup). **Ask first, name the cost, then do it.** Never enrich silently.

## Step 4: Grade every row

Each row gets four things:

| Field | What goes in it |
|---|---|
| **Pass or fail** | against the checklist from Step 1 |
| **Why** | one line, plain |
| **Confidence** | high, medium or low — how much of the row was actually there to judge |
| **Missing** | what was absent and mattered |

Low confidence is not a fail. It means the row needs data before anyone decides.

## Step 5: Tally it

- How many passed, out of how many.
- **Where the fails came from.** If there is a source column, give the pass rate per source. That answer is usually worth more than the grades themselves — a source that fails two rows in three should be dropped.

## Step 6: Say what it means

| Result | What it means |
|---|---|
| Most rows pass | The targeting is right. Move on to the message. |
| Half pass | Send to the passes first. Then rework where the other half came from. |
| Most rows fail | The list came from the wrong place. Fix the source before writing anything. |

## What to write

Save to `ACX/outputs/graded-list.csv`: the list with the four columns added. Then say out loud how many passed and where the failed rows came from — that is the line they write down.

Then stop. The next step is the offer.

## Things you must never do

- Invent a company size, industry, revenue or job title.
- Score a row on missing data without flagging it.
- Treat a pass as a promise that they will buy. A pass means fit, not intent.
- Enrich, scrape or spend anything without a yes first.
- Bury the source breakdown. It is the most useful line in the whole report.
