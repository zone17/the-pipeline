# Product Discovery — Methods, Formulas & Templates

Reference for the `discovery` skill. Frameworks synthesized from the canonical sources:
Teresa Torres (Continuous Discovery Habits), Marty Cagan / SVPG, Eric Ries (Lean Startup),
David Bland & Alex Osterwalder (Testing Business Ideas), Tony Ulwick (Outcome-Driven
Innovation / JTBD), and Rob Fitzpatrick (The Mom Test).

## Table of contents
1. Opportunity-Solution Trees (Torres) — the opportunity map backbone
2. The four big risks (Cagan) — what discovery de-risks
3. Assumptions map + experiment library + experiment card (Bland/Osterwalder/Ries)
4. JTBD + ODI opportunity score — prioritization math
5. The Mom Test — truthful customer research
6. The research synthesis — what it contains
7. The exit gate — sharp problem + sharp bet templates + checklist
8. Anti-patterns and counters
9. Artifact → framework quick map

---

## 1. Opportunity-Solution Trees (Torres)

Four hierarchical layers, root at top:

1. **Desired Outcome (root)** — a single product-level metric that scopes discovery. An
   *outcome* (measure of impact), not an output (feature shipped). E.g. "increase
   first-time activation from 22% to 25%."
2. **Opportunity Space** — customer needs, pains, desires that would drive the outcome.
   Always *problems*, never solutions. Organized as a tree; big opportunities decompose
   into sub-opportunities.
3. **Solution Space** — products/features/workflows addressing a *specific target
   opportunity*. Generate **3+ competing solutions** per opportunity so decisions are
   "compare and contrast," not "whether or not."
4. **Assumption Tests** — small experiments validating the assumptions a solution depends
   on.

**Opportunity vs. solution litmus test:** if there's only *one* way to address a statement,
it's a solution in disguise. A true opportunity admits multiple solutions. Phrase
opportunities in the customer's voice ("I don't have time to cook"), surfaced from
story-based interviews ("Tell me about a time when…"), not brainstormed (which imports
bias). Support tickets/sales calls are inspiration for interview topics, not direct
opportunity sources.

**Torres's four sizing/prioritization factors:** (1) opportunity sizing — how many
customers, how often; (2) market factors — competitive positioning; (3) company factors —
fit with mission/strategy; (4) customer factors — importance × satisfaction (the ODI hook,
§4). **Effort/feasibility is deliberately excluded** at opportunity-prioritization stage —
any opportunity has both easy and hard solutions; effort is assessed later.

**Five assumption types (Torres):** Desirability, Viability, Feasibility, Usability,
Ethical (potential for harm). For a target solution ask: what must be true for this to
succeed? Which assumption is most uncertain/scary? How might we test it with a real
customer before building?

---

## 2. The four big risks (Cagan / SVPG)

*"Before we build, we must address four big risks."*

| Risk | Definition | Owner |
|------|-----------|-------|
| **Value** | whether customers will buy it / users will choose to use it | Product Manager |
| **Usability** | whether users can figure out how to use it | Product Designer |
| **Feasibility** | whether engineers can build it with the time, skills, tech we have | Lead Engineer |
| **Business viability** | whether it works for the business — GTM/sales channel, legal/compliance, partners, CAC, monetization, brand | Product Manager |

De-risk: value → interviews, demand tests, prototype reactions; usability → usability
testing; feasibility → engineering spikes/feasibility prototypes; viability → stakeholder
review with legal/finance/sales/marketing. Tackle the big risks **early** — especially
value and viability — and **collaboratively** (eng + design + product together).

**Discovery vs. delivery:** discovery answers "are we building the right thing?" — its
output is *confidence and a decision* (proceed/pivot/kill). Delivery answers "can we build
it right?" Discovery exists to kill the four risks before delivery starts.

---

## 3. Assumptions map + experiment library + experiment card

**Riskiest-assumption-first:** isolate the single belief that, if false, sinks the idea,
and test it first, as cheaply as possible. Bland's question: *"Which hypothesis, if proven
wrong, will cause our business idea to fail?"*

**Assumptions mapping (2×2):**
- Extract every assumption: "What must be true for this to work?" Write each as a
  hypothesis ("We believe that…") — testable, precise, discrete.
- Classify each: **Desirability** (does the market want it?), **Feasibility** (can we
  build/deliver at scale?), **Viability** (profitable/sustainable?), and optionally
  **Adaptability** (survives a changing environment?).
- **Y axis = Importance** (if wrong, does the idea fail?). **X axis = Evidence** (observable
  evidence, qualitative or quantitative — not opinion or seniority).
- **Quadrant action:**
  - **Top-right (Important + No evidence) → TEST NOW** (leap-of-faith assumptions).
  - Top-left (Important + Have evidence) → monitor.
  - Bottom-right (Unimportant + No evidence) → park.
  - Bottom-left (Unimportant + Have evidence) → ignore.

**Experiment library:**

| Experiment | Tests | Cost | Evidence |
|-----------|-------|------|----------|
| Customer interviews (Mom Test) | desirability / problem existence | very low | weak–moderate (says) |
| Landing page / smoke test | value prop, demand | low–moderate | moderate |
| Fake door | demand for a specific feature | low | moderate |
| Paid-ads campaign | messaging + CPC viability | moderate | moderate–strong |
| Concierge (manual, user knows) | value + usability + demand | moderate–high | strong |
| Wizard of Oz (manual back-end, user unaware) | demand + behavior | moderate–high | strong |
| Piecemeal / no-code MVP | end-to-end experience | low–moderate | moderate |
| Pre-sales / crowdfunding | demand with real money | moderate–high | strong (money) |

Register the metric and pass/fail threshold **before** launch. Behavior (a click, a
payment) beats stated intent. **XYZ hypothesis:** "At least X% of [Y population] will [Z
observable action]."

### Experiment card template

```
EXPERIMENT CARD
─────────────────────────────────────────────
Assumption ID:        [A-03]   Type: ☐Desirability ☐Viability ☐Feasibility ☐Usability ☐Ethical
Riskiest? (top-right quadrant): ☐Yes
Assumption:           "We believe that [target customer] [needs / will do X]."
Hypothesis (XYZ):     "At least [X%] of [Y segment] will [Z observable action]."
Test / method:        [Landing page | Fake door | Concierge | Wizard of Oz | Interview | Pre-sale]
Setup:                [exactly what we build/do, traffic source, sample size, duration]
Metric:               [the single measured number]
Success criterion:    [PASS if ≥ X% | FAIL if < threshold]   (set BEFORE running)
Cost:                 [$ / person-hours]      Time: [e.g. 3 days]
Evidence strength:    ☐Weak (says) ☐Strong (does)
Estimated resolution: [likely true / uncertain / likely false] — confidence [H/M/L], because […]
Result & decision:    [data] → ☐Proceed ☐Iterate ☐Pivot ☐Kill
─────────────────────────────────────────────
```

---

## 4. JTBD + ODI opportunity score

**Functional job statement (Ulwick):** `[verb] + [object] + [contextual clarifier]`,
solution-free. E.g. "minimize the time it takes to prepare a healthy meal."

**Narrative JTBD (Klement):** "When [situation/trigger], I want to [motivation], so I can
[expected outcome]." One job executor, no solution referenced.

**Desired-outcome statement (4 parts):** `[minimize/maximize] + [metric] + [object of
control] + [context]`. E.g. "Minimize the time it takes to determine what nutrition is
needed to address the pet's existing health issues."

**Opportunity Score (the opportunity algorithm):**
```
Opportunity = Importance + max(Importance − Satisfaction, 0)
```
Customers rate each desired outcome on Importance and Satisfaction, 1–10. Thresholds:
**≥15 highly attractive (under-served); 10–15 attractive; <10 over-served (don't invest).**
Example: Importance 10, Satisfaction 3 → 10 + 7 = 17. This is the defensible, quantified
backbone for Torres's "customer factors."

---

## 5. The Mom Test (Fitzpatrick)

Three rules:
1. **Talk about their life, not your idea.**
2. **Ask about specifics in the past, not generics/hypotheticals about the future.**
3. **Talk less, listen more** (customer talks ~80%).

Opinions and compliments are worthless ("fluff"); facts, specifics, commitments are signal.
Questions that always fail (seek validation): "Do you think this is a good idea?", "Would
you use this?", "How much would you pay?" Good questions: "Talk me through the last time
this happened." "What have you tried to solve it?" "How much does it cost you today?"
**Commitment/advancement signal:** real interest = giving up something valued — time (a
follow-up), reputation (an intro), or money (a pre-order, LOI). Compliments ≠ commitment.

---

## 6. The research synthesis — sections

1. **Question & scope** — problem area + the desired outcome the research informs.
2. **Market context** — TAM/SAM/SOM, trends, why now.
3. **Customer segments & jobs/pains** — segment → JTBD → desired outcomes → current
   satisfaction.
4. **Competitive / alternatives landscape** — include non-consumption and manual
   workarounds, not just direct competitors.
5. **Regulatory / technical context** — constraints bearing on viability/feasibility.
6. **Evidence-vs-inference table** — each row tagged **Fact** (observed/cited + source) or
   **Inference** (interpretation), with **confidence** (High = multiple independent
   first-hand signals; Med = single source; Low = anecdote/assumption).
7. **Key insights** — the 3–5 "so-whats" that change a decision.
8. **Open questions / assumptions to test** — hands off into the assumptions map.

Good practices: cite every claim; label assumptions as assumptions; triangulate (multiple
methods agreeing → trust); prefer behavioral evidence over stated opinion; flag
recency/staleness.

---

## 7. The exit gate — sharp problem + sharp bet

### Sharp problem statement
```
WHO:         [specific customer/segment + job executor]
STRUGGLE:    When [situation/trigger], they are trying to [job-to-be-done],
             but [obstacle/pain] — phrased as a need, NOT a solution.
CONTEXT:     This happens [frequency] in [context/environment].
ALTERNATIVES: Today they cope by [workarounds / competing solutions],
             which fall short because [gap].
WHY IT MATTERS: It costs them [time/money/risk]; matters to us because [link to outcome/strategy].
EVIDENCE:    We know this because [N interviews / data / behavioral signal], confidence = [H/M/L].
```
Solution-agnostic test: a good problem admits *multiple* solutions. "Users want to find and
buy items they saw in real life" (good) vs. "users can't visually search in the app" (bad —
presupposes the solution).

### Sharp bet
```
THE OPPORTUNITY:  We're pursuing [prioritized opportunity / under-served outcome],
                  because Opportunity Score = [N] (importance [x], satisfaction [y]).
TARGET CUSTOMER:  [the beachhead segment we bet on first].
POINT OF VIEW:    We'll win because [unique insight / unfair advantage / why now].
                  Differentiated approach: [angle].
DESIRED OUTCOME:  Success = moving [metric] from [A] to [B] by [when].
RISKIEST ASSUMPTION: The single belief most likely wrong and most fatal is [assumption]
                  (top-right of the assumptions map).
FALSIFICATION:    We KILL/PIVOT if [specific test] shows [metric] < [threshold] by [date].
```
The falsification condition is what separates a sharp bet from a vague aspiration.

### "Is it sharp enough to exit discovery?" checklist
- [ ] Problem stated as a **customer need/job**, not a solution (passes multiple-solutions test).
- [ ] We can name the **specific target customer** (not "users").
- [ ] Problem backed by **evidence**, with evidence separated from inference + confidence rating.
- [ ] There is a **measurable desired outcome** tied to strategy.
- [ ] The opportunity is **prioritized with a rationale** (opportunity score / sizing).
- [ ] We have an explicit **point of view** on why we'll win.
- [ ] The **single riskiest assumption** is named and sits in "important + no evidence."
- [ ] There is a **falsification condition** with metric, threshold, and date.
- [ ] The riskiest assumption is tested, or cheaply testable, with **real behavior**.

---

## 8. Anti-patterns and counters

| Anti-pattern | Looks like | Counter |
|--------------|-----------|---------|
| Solution-first / confirmation bias | entering with a pet solution, researching to confirm it | frame the problem first (OST); 3+ competing solutions; pre-register what would disprove you |
| Confirmation bias in tests | tests that can only confirm | define pass *and* fail thresholds up front; skeptic review; triangulate |
| Leading questions | "Would you use this?" | Mom Test: past specifics, never pitch, listen 80% |
| Analysis paralysis | endless research, no decision | time-box; output is a decision; test riskiest assumption with cheapest experiment |
| Desirability-only validation | proving want, ignoring feasibility/viability | map assumptions across all four risks |
| Opinions as evidence | "HiPPO says…"; relying on what people *say* | only observable evidence; weight behavior over intent |
| Vanity research/metrics | impressive dashboards that change no decision | tie every item to an open question + a decision; prefer commitment signals |
| Opinion battles | "whether-or-not" debates | OST reframes as compare-and-contrast across opportunities/solutions |

---

## 9. Artifact → framework quick map

| Artifact | Primary frameworks | Exit-gate contribution |
|----------|--------------------|------------------------|
| **Research Synthesis** | desk research structure + Mom Test interviews + JTBD/ODI segmentation; evidence-vs-inference + confidence | evidence behind the sharp **problem** |
| **Opportunity Map** | OST (outcome→opportunities→solutions) + ODI Opportunity Score + Torres's 4 sizing factors | selects/justifies **the opportunity** in the bet |
| **Assumption Tests** | assumptions map 2×2 + experiment library + experiment card + Cagan's four risks + Mom Test | names the **riskiest assumption** + defines **falsification** |

**Load-bearing items to reuse verbatim:**
- Opportunity Score: `Importance + max(Importance − Satisfaction, 0)` (≥15 attractive, <10 over-served).
- Desired-outcome statement: `[minimize/maximize] + [metric] + [object] + [context]`.
- Narrative JTBD: "When [situation], I want to [motivation], so I can [outcome]."
- XYZ hypothesis: "At least X% of [Y] will [Z]."
- Assumptions-map rule: test the top-right quadrant first, cheapest experiment per assumption.
- Mom Test: their life not your idea; past specifics not hypotheticals; listen 80%.
