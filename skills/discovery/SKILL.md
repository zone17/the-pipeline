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

Run discovery the way an **elite, multidisciplinary research team** would — never one search
summarized off the first page. **Fan out multiple independent threads in parallel**, each
owned by a different specialist lens and pulling from a different *class* of source, then
**converge, triangulate, and adversarially verify**. Breadth across domains and source types
is what separates a sharp, defensible bet from a confident guess. The orchestration below is
the same in every environment; only the tools change.

### The research threads (one per "specialist" — run them in parallel, not in sequence)

Scope each thread to a *sharp* question, never the whole idea. At minimum cover the threads
that bear on the load-bearing claims:

- **Problem & JTBD reality** — is the pain real, frequent, and urgent for the named segment?
  Jobs-to-be-done, real workflows, switching triggers.
- **Customer voice** — first-hand signal from where the segment actually talks: forums,
  Reddit/HN, app-store and G2/Capterra reviews, support threads, community Discords, social.
  Weight observed behavior and complaints over stated opinion.
- **Market & sizing** — TAM/SAM/SOM with real arithmetic, growth rate, adjacent-market
  spillover; industry/analyst reports where they exist.
- **Competitive & alternatives** — direct competitors *and* non-consumption, manual
  workarounds, and incumbents' roadmaps. Read primary sources (their docs, pricing,
  changelogs, job posts), not listicles.
- **Technology & feasibility — the cutting edge** — the current frontier and what *just*
  became newly possible: academic & preprint literature (arXiv/SSRN/scholar), patents,
  technical blogs, open-source state of the art. "Why now" is usually won or lost here.
- **Timing / "why now"** — shifts in the last 6–18 months (regulatory, cost-curve,
  behavioral, platform) that open the window *now* rather than two years ago or two from now.
- **Economics & pricing** — unit-cost drivers, comparable pricing/margins/CAC benchmarks,
  willingness-to-pay signals.
- **Regulatory / ethical / risk** — constraints, compliance, data/privacy, and failure
  modes that could kill the bet.

Add **domain-specific threads** whenever the bet lives in a vertical (e.g. clinical evidence
for health, on-chain & market data for fintech, scientific literature for deep tech,
procurement cycles for govtech). An elite team brings in the right specialist per domain.

### Source modalities to span (don't over-index on any one)

General web search · academic & preprint (arXiv, SSRN, scholar) · patents · primary
competitor docs / pricing / changelogs / job posts · industry & analyst reports · news &
recency scans · practitioner & expert long-form · community & review sites · and **domain
data sources** (financial, scientific, government/statistics) when relevant. A claim that
survives across *multiple* modalities is far stronger than one that appears in many pages of
the same kind.

### Tooling by environment

Use the strongest stack available — the thread plan above does not change.

**In Claude Code (full power — orchestrate a real fan-out):**
1. **`deep-research` skill** — the workhorse for each major thread. Hand it ONE *sharply
   scoped* question per thread (problem reality, sizing, competition, frontier-tech,
   why-now) — never the whole idea. It fans out searches, fetches sources, adversarially
   verifies, and returns a cited report. **Run several in parallel**, one per thread, like a
   team working concurrently.
2. **Parallel research agents / `Workflow` fan-out** — spawn multiple `ce-web-researcher`
   agents (or author a `Workflow` that pipelines thread → verify) so threads run
   concurrently and independently. Give each agent a **distinct lens** so they don't
   converge on the same handful of sources — diversity of angle is the point.
3. **`jina`** — `parallel_search_web` for broad multi-query sweeps, `search_arxiv` /
   `search_ssrn` for the academic/frontier thread, `parallel_read_url` to pull many primary
   sources at once, `search_images` / screenshots for product teardowns.
4. **`firecrawl`** — crawl and scrape competitor sites, docs, and pricing pages for
   primary-source numbers rather than secondary summaries.
5. **`last30days`** — the recency / "why now" thread in fast-moving markets.
6. **Domain MCP servers** — when the bet is vertical, pull *real data* (e.g. financial-data,
   scientific, or government-statistics MCP) instead of relying on prose.
7. **`WebSearch` / `WebFetch`** — targeted gap-filling and reading specific pages.

Default to running the threads **concurrently** (parallel agents or a `Workflow`), then
synthesize once all return — that is what makes this an elite *team* rather than one
researcher doing serial lookups.

**In Claude Cowork / Claude Desktop:**
- Lead with Cowork's **native web search + fetch** (server-side; works on search results and
  shared URLs). Run the same multi-thread plan — issue many scoped searches across the
  threads above rather than one broad query.
- Add **MCP connectors** for heavier research where connected (e.g. `jina`, `firecrawl`, or
  domain-data servers) via **Customize → Connectors** — this is how you recover
  academic/parallel-read/crawl power and domain data.
- The Claude-Code-only skills and agents above (`deep-research`, `last30days`,
  `ce-web-researcher`, `Workflow`) **do not exist here.** Replicate their effect by running
  the thread plan yourself across many native searches plus connectors, and keep the exact
  same triangulation and verification discipline.

**Anywhere else (API / Agent SDK):** use the `WebSearch` tool plus any attached MCP research
servers, following the same thread plan.

### Cross-cutting discipline (non-negotiable, every environment)

- **Triangulate** — a claim earns "Fact / High confidence" only with ≥2 *independent*
  sources; a single source → Med; anecdote or assumption → Low.
- **Adversarially verify the load-bearing claims** — for anything the bet depends on,
  actively try to **refute** it (search for disconfirming evidence and the strongest
  counter-case); don't just collect confirmations.
- **Separate fact from inference**, and **cite every factual claim** with a source + date.
- **Check recency** — flag stale sources; for "why now," prefer the last 6–18 months.
- **Prefer primary and behavioral sources** over secondary summaries and stated intent.
- **Span domains** — if every source is the same type (all blogs, or all vendor pages), the
  thread isn't done; pull at least one orthogonal modality before trusting it.

If no research tooling is reachable at all, say so explicitly, proceed from reasoning and the
user's input, mark the synthesis confidence **Low** throughout, and tell the user exactly
which searches would raise it.

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
