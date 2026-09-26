# CREDITS

This folder is the product: the single-plugin marketplace members install. `plugins/acx/`
holds all nine skills under one plugin, so the whole terminal installs in one command.

Eight of the nine are **forks of public agent skills**. `skills/start/` is ours — the
router that runs the other eight in order and carries context between them, because under
this design the individual skills do not read each other.

The ACX-authored versions of these agents live in `../plugins/` and are **not shipped**.

## What was changed in each fork

Every forked skill was rewritten for the ACX GTM Terminal, whose members are agency owners,
consultants and B2B service operators **already at revenue and already running outbound**.

In every one:

- renamed to the ACX agent name, and given a description that names the video that runs it
- rewritten in plain everyday words, in the member's voice, for someone who already sells
- the inputs changed to what an established business actually has (their clients, their
  closed deals, their current offer) rather than a founder's idea or a product repo
- one output file in `ACX/outputs/`, fixed name — no source-specific directory trees
- no scripts the member has to run, and no dependency on any particular model or tool
  beyond reading files and searching the web
- source-specific plumbing removed (their internal paths, their other skills, their APIs)
- ends at the handoff to the next video, with the one-liner the member writes down
- a "things you must never do" list, weighted towards not inventing data

| ACX agent | Forked from | Licence | What was kept from the source |
|---|---|---|---|
| market-scanner | [RohitWaghire/Deep-Market-Reasearch](https://github.com/RohitWaghire/Deep-Market-Reasearch) | MIT (stated in README prose; **no LICENSE file**) | the evidence-scored dimension tables and the concrete search patterns (`references/query-recipes.md`) |
| category-gap-finder | [mloki23/market-gap-finder](https://github.com/mloki23/market-gap-finder) | MIT | scored gap testing across demand, competition, revenue and timing; the "empty for a bad reason" test |
| icp-builder | [zarif3624/gtm-skills](https://github.com/zarif3624/gtm-skills) → `skills/define-icp` | MIT | ICP-as-filter; derivation from closed-won evidence, never aspiration |
| lead-grader | [LeadMagic/gtm-skills](https://github.com/LeadMagic/gtm-skills) → `skills/foundation/icp-scoring` | MIT | weighted scoring with hard disqualifiers separated from additive points; per-source pass rates |
| offer-architect | [cgallic/kai-cmo-harness](https://github.com/cgallic/kai-cmo-harness) → `harness/skills-v2/kai-offer-builder` | MIT (plugin payload — their `LICENSING.md` reads "Fork the plugin, modify the skills, and redistribute them — including inside a paid product of your own") | the four-lever scoring with a justified line per score; "no source, no row"; substantiation and compliance; keeping the value scores internal |
| guarantee-designer | [wondelai/skills](https://github.com/wondelai/skills) → `hundred-million-offers` | MIT | the five guarantee types, the decision keyed on cost to deliver, guarantee naming, and the ROI maths (`references/guarantees.md`, `references/naming-offers.md`) |
| positioning-builder | [zarif3624/gtm-skills](https://github.com/zarif3624/gtm-skills) → `skills/develop-positioning` | MIT | the ordered component sequence, the claim ladder, and the "never go from capability to guaranteed outcome" rule |
| message-tester | [takechanman1228/claude-persona](https://github.com/takechanman1228/claude-persona) | MIT | the persona panel, the concept-test structure, and the rule that each persona answers in isolation with no cross-contamination |

## Source licence texts

Kept verbatim in `_licences/`. Where a repo states a licence only in its README (no
`LICENSE` file), that is recorded in the table above rather than reproduced. Files a forked
skill carries that came with their own `LICENSE` keep it in place.

## Considered and rejected

| Source | Licence | Why not |
|---|---|---|
| [bookforge-ai/bookforge-skills](https://github.com/bookforge-ai/bookforge-skills) → `guarantee-design-and-selection` | **CC BY-SA 4.0** | Closest single match to our Guarantee Designer, but share-alike means our fork would have to carry the same licence; it also bundles a "we are a non-commercial project" posture and content distilled from a paid book with a takedown process. Used wondelai (MIT) instead. |
| [stage-2-capital/ICP-Builder](https://github.com/stage-2-capital/ICP-Builder) | **no licence, no statement anywhere** | Repo is two files; default is all rights reserved. No permission to redistribute, so not used. |
| [entpnomad/bootstrapper-toolkit](https://github.com/entpnomad/bootstrapper-toolkit) | **no licence, no statement anywhere** | Same. |
| [Claudient/Claudient](https://github.com/Claudient/Claudient) → `sdr-lead-scorer` | moved to `UitbreidenOS/UitKit`, no clear licence | Repo relocated; used LeadMagic (MIT) for lead-grader instead. |

## Removed on purpose during the trim

Source files that did not fit the member or the design:

- `lead-grader` — `scripts/check-output.py`, `templates/`, `references/framework-notes.md`
  (SPICED/MEDDICC/Gartner/SPIN — enterprise sales frameworks, not an agency owner's material)
- `market-scanner` — `references/scoring-rubric.md` and `references/report-template.md`
  (folded into the skill body and the single output file)
- `guarantee-designer` — nine of eleven references (bonus stacking, case studies, scarcity,
  pricing, etc. — other skills' subject matter)
- `icp-builder` and `positioning-builder` — the `assets/` templates and `references/` guides
  (evidence ledgers, approval owners, "falsifiable paragraph" — written for an enterprise
  GTM team, not for a member reading one file), plus `agents/openai.yaml` (a different runtime)
