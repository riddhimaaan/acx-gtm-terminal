---
name: icp-builder
description: Takes the member's best clients and closed-won deals, finds the pattern, and writes down who to go after, what has to be happening in their world, and who to disqualify. Use when someone says "build my ICP", "pick my niche", "who should I target", "my ideal customer", or runs Module 2 Video 2 of the ACX program.
---

<!--
ACX fork. Source: https://github.com/zarif3624/gtm-skills (MIT), skill `define-icp`.
Rewritten for the ACX GTM Terminal: agency owners already at revenue. See forks/CREDITS.md.
-->

# ICP Builder

**The rule for everything you write:** an ICP is a filter, not a description. If the member could not plug a line into a search and get a finite list of companies back, that line does not belong in the ICP.

**Who this is for:** an agency owner with clients already closed. The answer is sitting in their own deals — you are reading it off, not guessing it.

## How the final answer should feel

Write for a busy business owner, using words a 10-year-old could understand. The deal review can be detailed; the final answer must be a short checklist they can use today.

- Put the chosen customer group first, in one plain sentence.
- Keep the main report to one page.
- Every company category, example, and location rule must be something the member can check in a list or find online.
- Use "buy now when" instead of "trigger events," and "do not contact" instead of "disqualifiers."
- Group company types into "strong fit," "adjacent fit," and "explicit non-focus" so the lead grader can use the rules directly.
- Include two or three real, verified company examples under each category when they make the category easier to recognise. Examples are not leads or proof that those companies will buy.
- Keep location rules in their own section.
- Show only the two strongest patterns from the member's own wins, losses, or churned clients.
- If the evidence is thin, say "first draft" at the top. Do not pretend the rules are certain.
- End with no more than three practical next actions.
- Do not use words such as "firmographic," "persona," or "segmentation." Say "company type," "buyer," and "the group we are going after."

## Step 0: Start from deals, not from wishes

Ask for their **best clients and recent wins** (five to ten is plenty), and read `ACX/my-business.md`. If they have fewer than five real wins, say so and treat everything below as a first draft to be corrected by the next ten deals.

## Step 1: Ask, two questions at a time

Keep it conversational. You want:

1. Where do you win easily?
2. Where do you struggle or lose?
3. Who was easiest to close?
4. Who has churned, refunded or gone quiet?
5. What was happening in their world right before they bought?

Question 4 matters as much as the rest. A group that buys fast and leaves in six months is a **not-a-fit** signal, not a win.

## Step 2: Find the pattern

Compare the wins against the losses and the churn. You are looking for what the wins have in common that the others do not: industry, company size, who signed, what triggered it, how long it took.

If nothing separates them, say that plainly. A pattern you invented is worse than no pattern.

## Step 3: Say the niche in one line

One line: which group they are going after, and why they win with them. Plain words, no jargon.

## Step 4: Write the ICP as a filter

Every line must be something you could search for. Keep each one short and checkable:

- industry
- company size
- country
- who signs (the role)
- what is happening in their world right now (below)

Then set the **disqualifiers** — who to skip. Include the churn pattern from Step 1. The disqualifiers save more time than the target list does.

## Step 5: Name the trigger events

Triggers are the things happening now that mean a company is ready to buy this month, not someday. Usual suspects: new funding, a new leader in the relevant seat, fast hiring, a launch, an acquisition, falling behind a competitor, a deadline or rule change.

Write them as things you could notice from the outside, because the member has to be able to spot them.

## Step 6: Sanity check

Run the finished ICP against two or three real accounts. If a client they love lands **outside** the lines, the lines are wrong — fix them.

## If the evidence is thin

Say so. Label it a first draft. Do **not** invent a scoring model with weights and numbers to make it look rigorous. A short honest list beats a made-up score.

## What to write

Save to `ACX/outputs/icp.md` using this exact shape:

```md
# Who should we sell to?

## Short answer
We should sell to [specific type of business] because they are most likely to need [result] and buy now.

## Company fit

### Strong fit
- [Specific company category]
  Examples: [Verified company], [Verified company]
- [Specific company category]
  Examples: [Verified company], [Verified company]

### Adjacent fit
- [Related company category worth considering]
  Examples: [Verified company], [Verified company]

### Explicit non-focus
- [Company category to skip]
  Examples: [Verified company], [Verified company]

## Location fit

### Priority locations
- [Country or region to focus on]

### Locations to skip
- [Country or region to avoid, only if the evidence supports it]

## Other rules
- Company size: [company size]
- Buyer: [job title]

## Buy now when
- [Clear event we can spot from the outside]
- [Clear event]
- [Clear event]

## Do not contact
- [Type of company to skip]
- [Type of company to skip]
- [Type of company to skip]

## Why this is the right group
- [Pattern from best clients]
- [Pattern from lost, churned, or poor-fit clients]

## What to do next
1. Find 10 companies matching these rules.
2. Check that they do not match the "do not contact" list.
3. Run `lead-grader` before sending.
```

Keep the full deal review in research notes. The main report should contain only the rules the member needs to find the right companies.

Then stop. The next step is checking a real list against this.

## Things you must never do

- Build the ICP from who they wish they sold to.
- Use a job title as the whole ICP.
- Leave out disqualifiers.
- Put numbers and weights on thin evidence.
- Ask the member for anything already in `ACX/my-business.md`.
