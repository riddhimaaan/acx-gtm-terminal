---
name: market-scanner
description: Checks if a market is worth selling into. Gives back 3 scores (demand, competition, open gaps) with proof and a one-line verdict. Use when someone says "scan my market", "is my market still buying", "check demand for X", "how crowded is my market", or runs Module 1 Video 2 of the ACX program.
---

<!--
ACX fork. Source: https://github.com/RohitWaghire/Deep-Market-Reasearch (MIT, stated in README).
Rewritten for the ACX GTM Terminal: the member is an agency owner already at revenue.
See forks/CREDITS.md.
-->

# Market Scanner

**The rule for everything you write:** every score needs evidence underneath it. If you cannot point at something you actually found, do not give the score.

**Who this is for:** an agency owner, consultant or service operator who is already making money. Work has stopped paying off and they want to know whether the problem is them or the market. They are not a beginner and they do not need the basics explained.

## Step 0: Get the two things you need

You need the member's **market** and **who they sell to**. Both live in `ACX/my-business.md`. Read it first. Only ask for what is genuinely missing, and write what you learn back into that file.

## Step 1: Write the scope down in one line

One line: what they sell, who they sell it to, which country. If you cannot write that line, you do not have enough to scan anything.

## Step 2: Check demand — are buyers already paying?

> Search patterns for every step below are in `references/query-recipes.md`.

You are looking for **money already moving**, not interest. Signals that count:

- competitors quietly charging for this and staying in business
- job posts that mention the problem, or a role hired to fix it
- buyers describing the problem in their own words somewhere public
- an existing budget line they would pull from

Search for these things: `[problem] "struggling with"`, `[market] agencies`, `[competitor] pricing`, `[problem] costs`, `[market] trends 2026`. Use whatever search you have.

**Interest is not demand.** Likes, views, "this is interesting" comments — none of that is evidence anyone pays. If they only have interest, say so.

## Step 3: Check crowding — how many are selling the same thing to the same people?

Signals:

- a growing number of people in the same space saying the same thing
- everyone using the same words in their marketing
- buyers complaining that their inbox is full of this pitch
- the same playbook that worked last year now getting silence

Crowded is not the end. It means effort alone is no longer enough — they need an angle instead of more volume.

## Step 4: Look at the open gaps (first pass)

Where is nobody standing? This is only a first look — the **Category Gap Finder** goes deep on it as the next step. Note what you see and move on.

## Step 5: Check the two traps

- **The empty market trap.** "Nobody is doing this" is usually a warning. Ask: is nobody doing it, or is nobody paying for it? Look for the money.
- **The wave going out.** Demand arrives in waves — a funding cycle, a new platform, a tool that changed what buyers expect. Name what drove their last good stretch. If that wave is going out, working harder will not bring it back.

## Step 6: Score the three things

Score each 0–10 and say in one line what evidence earned the score.

| Score | What it measures | 9–10 | 5–6 | 0–2 |
|---|---|---|---|---|
| **Demand** | are buyers already paying | already paying, several of them | some money moving, patchy | nobody pays for this |
| **Competition** | how much room is left | huge gaps to attack | several players with real weaknesses | dominated, buyers happy |
| **Open gaps** | how many spots are genuinely open | clear unmet need | a couple of soft spots | nothing left |

## Step 7: Give the verdict

One line: **can this market take me to the next level, yes or no — and why.** Then say which of the three it is.

## How the member reads the result

| Result | What it means |
|---|---|
| High demand, low competition | Go. Fix the work, not the market. |
| High demand but crowded | They need an angle, not more effort. |
| Low demand | That is the ceiling. Change the market before changing the tactics. |

## What to write

Save to `ACX/outputs/market-scan.md`: the scope line, the three scores with their evidence, the two traps, and the verdict. Put the member's one-liner at the top: **can this market take me to the next level — yes or no, and why.**

Then stop. The next step is finding where the openings are.

## Things you must never do

- Invent a market size, a growth rate or a competitor's revenue. If you could not find it, say it is missing.
- Report interest as demand.
- Call a market crowded without naming who is in it.
- Hand over a score with no evidence under it.
- Tell them their market is fine because they seem to want to hear it.
