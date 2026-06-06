---
name: product-idea
description: >-
  Turn a raw product or feature idea into a future-dated mock press release plus a
  rigorous FAQ, using Amazon's Working Backwards method and the writing craft of the
  greatest PR minds (Ivy Lee's clarity and credibility, Edward Bernays's psychology and
  narrative framing). Use this skill whenever the user wants a PR/FAQ, a "working
  backwards" doc, a future press release, a launch announcement written before building,
  a vision doc for a new product/feature/startup, or wants to pressure-test an idea by
  imagining its launch — even if they don't say "PR/FAQ" by name. Trigger on phrases like
  "write a press release for my idea," "do a working-backwards doc," "PRFAQ," "draft the
  launch announcement," "pitch this product," or "is this idea worth building."
---

# Product Idea → PR/FAQ

## What this skill does and why it works

Amazon builds products by writing the launch announcement **first** — before any code,
before any spec. If you can't make the idea sound compelling and honest in a one-page
press release, you probably shouldn't build it. The press release forces you to start
from the customer's problem and the single most important benefit, not from the
features you happen to be able to build. The FAQ that follows forces intellectual
honesty: it answers the questions a delighted customer would ask *and* the brutal
questions a skeptical executive would ask (unit economics, market size, what could go
wrong, what we're deliberately not doing).

So this is not a marketing exercise. It's a **thinking tool disguised as a press
release.** The document's job is to expose weak thinking cheaply, align people on a
vision, and earn the right to build. Treat writing it as a way to discover whether the
idea is any good — not to dress up an idea you've already decided on.

The writing voice fuses the two people who invented modern public relations:
- **Ivy Lee** gives the credible spine — lead with the news, plain declarative
  sentences, every claim grounded in a verifiable fact, no spin.
- **Edward Bernays** gives the resonant frame — tie the product to a larger human
  desire (freedom, security, status, belonging, ease), and let third-party voices
  (customers, experts, data) carry the persuasion.

The fusion: **a verifiable fact delivered inside a frame that makes the reader feel why
it matters to them.** Frame the truth; never manufacture it. Read
`references/press-release-craft.md` for the full craft principles before writing your
first PR/FAQ, and revisit it whenever the prose feels flat or hype-y.

## Workflow

### 1. Intake — adaptive, not interrogative

Read the user's idea and decide how much you actually know. The five questions a
PR/FAQ must answer are:

1. **Who is the customer?** (specific segment, not "everyone")
2. **What is their problem or unmet need?**
3. **What is the single most important benefit** of the solution?
4. **How do we know customers want this?** (and would they change behavior to adopt it?)
5. **What does the experience look like, and is the market big enough to matter?**

If the idea already implies confident answers to most of these, **proceed and generate
the full PR/FAQ immediately** — invent realistic specifics where the user left gaps,
then surface them in a short "Assumptions I made" list at the top so the user can
correct anything that's off. People move faster correcting a concrete draft than
answering an abstract questionnaire.

Only stop to ask questions when the idea is **critically underspecified** — when you
genuinely cannot tell who the customer is or what problem is being solved, and any guess
would be a coin flip. In that case ask the two or three questions you truly can't
proceed without, not a full interview.

When in doubt, lean toward generating. A flagged assumption is more useful to the user
than a question.

### 2. Write the press release (one page, future-dated, already-launched voice)

Write it as if the product shipped — future dateline, present/past tense ("Melinda *is*
a smart mailbox… *costs* just $299"). One page is a hard constraint; the constraint is
the point, because it forces you to choose the one benefit that matters most.

Use this canonical structure and order (full annotated template and a complete worked
example are in `references/working-backwards.md`):

1. **Headline** — one line: `[Company] announces [Product] to enable [customer] to [benefit]`, in words the customer would use.
2. **Subheading** — one sentence: who it's for and the single key benefit.
3. **Dateline + summary (the lede)** — `CITY, STATE — [future date] —` then 2–4 sentences giving the whole story. Assume the reader reads nothing else.
4. **Problem** — the top 3–4 pain points, ranked, **from the customer's point of view**, with concrete/quantified evidence. Do not mention your product here.
5. **Solution** — how the product elegantly solves each pain point; note what people use today and why it falls short; state how you're better/cheaper/faster.
6. **Leader quote** — one quote from a company spokesperson on why you built it and how it works at a high level.
7. **Getting started** — how easy the first step is (the first 1–3 actions a customer takes).
8. **Customer quote** — a realistic, named (fictional) customer naming their old pain and the benefit they now enjoy.
9. **Call to action** — the single first place to go (a URL).
10. Close with `# # #`.

While drafting, hold both voices: Lee decides the structure (news first, facts before
interpretation, plain language, quantified claims); Bernays decides the *angle* (which
larger human stake leads, what the product lets the customer *become*).

### 3. Write the FAQ (external + internal — full rigor)

The FAQ is where the real work happens and is much longer than the release. Split it
explicitly into two labeled sections.

**External FAQ** — what a customer or journalist would ask: what it is and how it
works, pricing, availability and rollout, supported platforms/devices, support, privacy
and data handling, plus anything obviously product-specific.

**Internal FAQ** — the hard questions a skeptical leadership team would ask. This is the
section that separates a real PR/FAQ from a press release with questions stapled on, so
do not soften it. Always cover, at minimum:

- **Customer & demand** — who exactly is the customer, what evidence do we have they
  have this problem, and would they change current behavior to adopt this?
- **Market size (TAM)** — number of customers with the problem × what each will pay.
  Show the arithmetic. Is it big enough to justify the investment?
- **Unit economics** — per-unit cost, gross margin, upfront investment, path to profit.
- **Competition / build-vs-buy** — what people use today, why we're meaningfully
  better, and whether we should build, buy, or partner.
- **Feasibility & dependencies** — what new capability or technology we must create or
  acquire; what teams, partners, or infrastructure we depend on.
- **Top 3 risks** — the three most likely reasons this fails, stated plainly, plus any
  legal/regulatory concerns.
- **What we are NOT doing** — explicit scope boundaries for this version.

Answer these honestly with concrete, quantified estimates (clearly framed as estimates).
If an honest answer is uncomfortable or exposes a real weakness, **say so** — that
discomfort is the document doing its job. A PR/FAQ that hides the hard answers is
worthless.

### 4. Self-review pass before you hand it over

Reread the draft once with a cold eye and fix these failure modes — they are the
difference between a Lee/Bernays-grade document and generic AI marketing copy:

- **Hype / empty superlatives** — "revolutionary," "world-class," "seamless,"
  "game-changing," "cutting-edge." Cut every one and replace with a concrete, quantified
  fact. If a sentence would survive being read aloud by a skeptical journalist, keep it.
- **Feature-listing** instead of one compelling benefit. Lead with what the customer
  *gains*, not what the product *has*.
- **Jargon / geek-speak / internal code names** — apply the "Oprah test": would this
  make sense to a general TV audience? If not, rewrite in plain language.
- **Vague benefits** — "makes life easier" with no number. Quantify it.
- **Buried lede** — the summary paragraph must contain the whole story.
- **Solution leaking into the problem paragraph** — the problem is the customer's, told
  without reference to your product.
- **A soft internal FAQ** — confirm TAM math, unit economics, top-3 risks, and
  "what we're not doing" are all present and honest.
- **Frame without truth** — confirm the resonant framing rides on real, checkable facts,
  not invented claims. Bernays's persuasion only holds on Lee's foundation.

## Output format

Produce a single clean Markdown document with two top-level sections — the press
release, then the FAQ — preceded by a short "Assumptions I made" list if you invented
specifics during intake. Save it to a sensibly named `.md` file when the user is working
in a project, or render it inline for a quick one-off. If the user later asks for a
`.docx`, PDF, or other format, produce it then; default to Markdown.

## Reference files

- `references/working-backwards.md` — the full annotated press-release and FAQ
  templates, the canonical "Melinda" worked example, the philosophy behind the method
  (silent reading meetings, narrative over slides, velocity vs. speed), and the complete
  anti-pattern list. Read it before your first PR/FAQ and whenever you need the exact
  template or example wording.
- `references/press-release-craft.md` — the writing craft of Ivy Lee and Edward Bernays:
  their principles, famous examples and the lesson each teaches, the 12 fused writing
  principles, and the ethical line (persuasion grounded in truth vs. manipulation
  through concealment). Read it to get the voice right.
