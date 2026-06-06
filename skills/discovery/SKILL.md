---
name: discovery
description: >-
  Pressure-test a product idea or PR/FAQ with real research and sharpen it into a crisp
  problem statement and a defensible, falsifiable bet. Takes the future press release +
  FAQ produced by the product-idea skill (or any idea) and runs autonomous deep research
  to produce three artifacts — a research synthesis, an opportunity map, and assumption
  tests — then applies an exit gate: the problem and the bet must be sharp. Use this skill
  whenever the user wants to validate, de-risk, or pressure-test an idea or PR/FAQ; run
  product discovery; figure out whether a real problem and a winnable bet underpin a
  concept; build an opportunity map or opportunity-solution tree; identify and test the
  riskiest assumptions; or decide whether an idea is worth pursuing. Trigger on phrases
  like "is this idea real," "validate this," "pressure-test the PR/FAQ," "do discovery on
  this," "what are the riskiest assumptions," "map the opportunity," "should we build
  this," or when handed a PR/FAQ to scrutinize.
---

# Discovery → Sharp Problem + Bet

## What this skill does and why it works

Writing the PR/FAQ (the `product-idea` skill) is the easy part — it's a vision, and a
vision can be wrong. Discovery is where the vision meets reality. It takes the aspirational
press release and its internal FAQ — full of confident claims about the customer, the
problem, the TAM, the unit economics, and the risks — and asks the uncomfortable question:
**is any of this actually true, and is it the sharpest version of the bet we could make?**

Discovery's job is not to produce more documents. Its job is to produce **a decision backed
by evidence**: proceed, refine, pivot, or kill. The output is only "done" when two things
are sharp:

- **The problem** — stated as a specific customer's need/job (not a solution), backed by
  evidence, with current alternatives and why they fall short.
- **The bet** — the prioritized opportunity, the beachhead customer, our point of view on
  why we'll win, the single riskiest assumption, and the **falsification condition** (the
  evidence that would make us walk away).

The discipline that makes this work: **separate evidence from inference, prioritize the
problem before the solution, and test the riskiest assumption first with the cheapest
experiment.** A bet without a falsification condition is a hope, not a bet.

Read `references/discovery-methods.md` for the full frameworks, formulas, and templates
before your first run, and whenever you need the exact opportunity-score math, the
assumptions-map quadrants, or the experiment-card format.

## Pipeline position

`product-idea` (PR/FAQ) → **`discovery`** (this skill) → a sharp problem + bet that either
sends you back to revise the PR/FAQ or forward to build. Discovery normally runs *on* a
PR/FAQ, but it works on any raw idea — if there's no PR/FAQ, treat the user's description
as the vision and proceed.

## Workflow

### 1. Intake — extract the claims ledger

If the input is a PR/FAQ, read it in full (a file path, a pasted doc, or the most recent
`product-idea` output). Extract every load-bearing claim into a short **claims ledger** —
this is what discovery will test:

- **Customer**: who the PR/FAQ says the customer is.
- **Problem**: the pain/job it asserts, and the evidence it offers (often invented numbers
  in the press release — flag these as unverified).
- **Benefit & differentiation**: the core promise and why it beats alternatives.
- **Market / TAM**: the sizing claim and its arithmetic.
- **Economics**: unit cost, margin, pricing, CAC assumptions.
- **Internal-FAQ assumptions & risks**: the "what could go wrong," "what we're NOT doing,"
  feasibility, and dependency claims — these are pre-identified assumptions; harvest them.

If the input is a bare idea, build the same ledger from the user's description and your own
framing, marking everything as unverified.

State the ledger briefly so the user can see what you're about to scrutinize.

### 2. Research synthesis (artifact 1)

Run **autonomous deep research** to confirm, challenge, or refine the claims ledger. See
the **Research tooling** section below for what to invoke. Scope the research to the
highest-stakes claims first (problem reality, market size, competitive alternatives,
"why now") rather than boiling the ocean.

Structure the synthesis (full section list in the reference):
1. Question & scope (the problem area + the outcome the research informs)
2. Market context — size (TAM/SAM/SOM), trends, why now
3. Customer segments & their jobs/pains — segment → JTBD → desired outcomes → current
   satisfaction
4. Competitive / alternatives landscape — include non-consumption and manual workarounds,
   not just direct competitors
5. Regulatory / technical context — constraints bearing on feasibility/viability
6. **Evidence-vs-inference table** — every row tagged **Fact** (observed/cited, with a
   source) or **Inference** (our interpretation), with a **confidence rating** (High =
   multiple independent sources; Med = single source; Low = anecdote/assumption)
7. Key insights — the 3–5 "so-whats" that change the decision
8. Open questions → hand off to the assumption tests

The single most important discipline here: **cite every factual claim, and never let an
inference masquerade as a fact.** Triangulate — when multiple independent sources point the
same way, confidence rises. Where the PR/FAQ's invented numbers turn out wrong, say so
plainly; that's discovery working.

### 3. Opportunity map (artifact 2)

Build an **opportunity-solution tree**, then score it. Purpose: confirm the PR/FAQ is
chasing the *sharpest* opportunity, or surface a better-adjacent one.

- **Desired outcome (root)**: the business/customer outcome metric this is meant to move
  (an outcome, not a feature).
- **Opportunity space**: customer needs/pains/desires that would drive the outcome, framed
  as problems with *multiple possible solutions* (the litmus test — if there's only one way
  to address it, it's a solution in disguise). Decompose big opportunities into children.
- **Solution space**: for the target opportunity, sketch 3+ competing solutions so the
  decision is "compare and contrast," not "whether or not." (The PR/FAQ's product is one
  of these — show its rivals.)
- **Score and prioritize** each opportunity with the ODI **Opportunity Score**:
  `Importance + max(Importance − Satisfaction, 0)` (each rated 1–10; ≥15 highly attractive
  / under-served, 10–15 attractive, <10 over-served). Deliberately **exclude effort** at
  this stage — any opportunity has both easy and hard solutions. Also weigh sizing,
  market/competitive position, and strategic fit.

Output the tree (as a nested list) plus a scored opportunity table and a one-line verdict:
is the PR/FAQ's bet on the best-scoring opportunity, or should it pivot?

### 4. Assumption tests (artifact 3)

Harvest every assumption the bet depends on — from the claims ledger, the synthesis's open
questions, and the internal FAQ. Classify each across the risk types: **desirability /
value, usability, feasibility, business viability, ethical**.

Map them on the **assumptions 2×2** (Y = importance: if wrong, does the idea fail?; X =
evidence: do we have observable evidence, not opinion?). The **top-right (important + no
evidence)** assumptions are the leap-of-faith ones — these get tested first.

For each top-right assumption, write an **experiment card** (full template in the
reference): assumption → XYZ hypothesis ("at least X% of [Y] will [Z]") → test method
(interview / landing page / fake door / concierge / Wizard of Oz / pre-sale) → metric →
pass/fail threshold set *before* running → cost & time → evidence strength.

Because real customer testing isn't possible from here, **also estimate how each assumption
would most likely resolve** based on the research synthesis — give a directional call
(likely true / uncertain / likely false) with an explicit **confidence flag** and the
evidence behind it. Be honest where the estimate is weak; the estimate never replaces the
test, it prioritizes it. Prefer experiments that measure real behavior (a click, a payment)
over stated intent, and tell the human how to run interviews truthfully (Mom Test: ask
about past specifics, never pitch, listen more than you talk).

### 5. Exit gate — sharpen the problem + bet (the brief)

Synthesize everything into the **discovery brief**: a sharp problem statement and a sharp
bet, using the templates in the reference. The bet **must** include the single riskiest
assumption and a falsification condition (metric, threshold, date).

Then run the **"is it sharp enough to exit discovery?" checklist** (full version in the
reference) — problem-as-need not solution, named target customer, first-hand-ish evidence
with confidence, measurable outcome, prioritized opportunity with rationale, explicit point
of view, named riskiest assumption, falsification condition, riskiest assumption tested or
cheaply testable with real behavior.

Close with an explicit verdict and the handoff:
- **Proceed** — problem + bet are sharp; ready to build or to firm up the PR/FAQ.
- **Refine** — send specific corrections back to the `product-idea` PR/FAQ (e.g. wrong
  customer, inflated TAM, weak differentiation) and note what changed.
- **Pivot** — a different opportunity scored higher; restate the bet.
- **Kill** — the problem isn't real or the bet can't be made sharp; say why, plainly.

## Research tooling

Use the best research capability available, in this order:

1. **The `deep-research` skill** — preferred for the synthesis. Hand it a *sharply scoped*
   question (e.g. "How large and underserved is [specific problem] for [specific segment],
   who are the real alternatives, and why now?"), not the whole idea. It fans out searches,
   fetches sources, adversarially verifies, and returns a cited report. Run it once per
   major research thread (problem reality, market/TAM, competition) rather than one giant
   query.
2. **The `ce-web-researcher` agent** (compound-engineering) — strong structured web
   research if `deep-research` isn't available; spawn it per thread.
3. **`jina` and `firecrawl` tools, plus WebSearch/WebFetch** — for targeted lookups,
   reading specific competitor pages/docs, recent-news scans, and pulling concrete numbers.
4. **`last30days`** — when recency matters (fast-moving markets, "why now").

Always cite sources in the synthesis. If no research tooling is reachable, say so, proceed
from reasoning and the user's input, and mark the synthesis confidence as Low throughout.

## Output format

Write four Markdown files into a `discovery/` folder next to the input (or a sensible
project location), so the artifacts can be reviewed and handed off independently:

- `00-discovery-brief.md` — the tying-together brief: the sharp **problem statement**, the
  sharp **bet** (with falsification condition), the exit-gate checklist, and the verdict.
  This is the file that hands back to `product-idea` or forward to build.
- `01-research-synthesis.md`
- `02-opportunity-map.md`
- `03-assumption-tests.md`

The brief should stand on its own; the other three are its evidence. Render the brief inline
for quick one-offs if the user prefers not to create files.

## Self-review pass

Before handing over, reread with a cold eye for the discovery anti-patterns (expanded in the
reference):

- **Solution-first / confirmation bias** — did you frame the problem first, or just
  rationalize the PR/FAQ's solution? Generate genuine competing opportunities/solutions.
- **Inference dressed as fact** — every factual claim cited; interpretations clearly marked.
- **Desirability-only validation** — assumptions cover value *and* usability, feasibility,
  and viability, not just "do people want it."
- **Opinions as evidence** — behavioral/observed evidence weighted over stated intent and
  HiPPO opinion.
- **A soft bet** — confirm the riskiest assumption is named and the falsification condition
  has a real metric, threshold, and date. A bet you can't lose isn't a bet.
- **Analysis paralysis** — the brief ends in a decision, not "more research needed" without
  saying which single test would unblock it.

## Reference file

- `references/discovery-methods.md` — the full frameworks and reusable templates: Teresa
  Torres opportunity-solution trees, Marty Cagan's four big risks, the Lean Startup /
  Testing Business Ideas assumptions map and experiment library + experiment-card template,
  JTBD/ODI desired-outcome statements and the opportunity-score formula, the Mom Test rules,
  the sharp-problem and sharp-bet templates, the exit-gate checklist, and the anti-pattern
  table with counters. Read it before your first run.
