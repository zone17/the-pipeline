# Working Backwards & the PR/FAQ — Full Reference

Reference material for generating a future press release + FAQ. Everything here is
drawn from authoritative sources (Bryar & Carr's `workingbackwards.com` and their book
*Working Backwards*, Colin Bryar's published "Melinda" example, Ian McAllister's
canonical template, Commoncog, and theprfaq.com).

## Table of contents
1. The philosophy (why this works)
2. Press release — annotated structure & order
3. FAQ — external vs. internal
4. The five customer questions
5. Rules, constraints, best practices
6. Anti-patterns (the self-review checklist, expanded)
7. The "Melinda" worked example
8. Fill-in-the-blank templates

---

## 1. The philosophy

**The core inversion.** Most companies start "skills-forward" — from a capability they
already have — and bolt customers on. Amazon starts from the customer's problem and
works *backwards* to the product. It's rooted in the first Leadership Principle,
Customer Obsession: *customers don't care what you're building; they care only about how
your product makes their lives better.*

**What the PR/FAQ actually solves.** Slide decks, SWOTs, and P&Ls let teams hide weak
ideas behind bullet points. The PR/FAQ exposes weak thinking *before* a line of code is
written. It (a) forces reasoning from the customer's view, (b) forces clarity and
intellectual honesty before resources are committed, (c) aligns stakeholders on *vision
and strategy*, not just a plan, and (d) lets leadership compare and kill ideas cheaply —
"a great product development process should be a funnel, not a tunnel."

**The emotional-honesty mechanism** (the most important and least-discussed point). The
PR/FAQ is a signalling device. As Commoncog puts it bluntly: if you attempt one, "the
dominant feeling you'll experience is discovering just how shitty your new idea really
is." If writing it feels like pulling teeth, the document is telling you that you haven't
done the customer research yet. People skip the PR/FAQ precisely to avoid confronting
weak ideas — that avoidance is the anti-pattern.

**Narrative over PowerPoint.** Bezos banned slide decks in senior meetings in 2004 in
favor of six-page narrative memos (the PR/FAQ is the variant used for *new* product
proposals). The reasoning: bullet points let you hide gaps; prose forces complete
thoughts and logical connections. *Good writing is good thinking.*

**The silent reading meeting.** Meetings open with 15–20 minutes of total silence while
everyone — including the most senior person — reads and annotates the printed memo, then
~40 minutes of debate. Tone is "truth-seeking vs. selling, improving vs. deciding."

**Velocity vs. speed.** Moving fast ≠ moving toward the right goal. The AWS team spent
over a year iterating PR/FAQs before launching in 2006; that upfront thinking is credited
with AWS's growth.

---

## 2. Press release — annotated structure & order

Strictly **one page**. Written **as if already launched** — future-dated dateline,
present/past tense.

| # | Component | What it must accomplish |
|---|-----------|------------------------|
| 1 | **Heading / Title** | Name the product so the *target customer* instantly gets it. Pattern: "[Company] announces [Product] to enable [customer segment] to [benefit]." One line. |
| 2 | **Subheading** | One sentence under the heading: who the market is and the single key benefit. Specific segment, not "everyone." |
| 3 | **Dateline + summary (lede)** | Opens `CITY, STATE — [future launch date] —`. Then a few sentences giving the whole story. "Assume the reader will not read anything else, so make this paragraph good." |
| 4 | **Problem** | The problem from the *customer's* point of view. Top 3–4 pains, ranked by severity, quantified. Do **not** mention your solution here. |
| 5 | **Solution** | How the product *elegantly* solves each pain. May run 2–3 paragraphs for complex products. Include differentiation: what people use today, why it falls short, how you're better/cheaper/faster. |
| 6 | **Leader quote** | One quote from your exec/spokesperson on *why* you tackled this and how it works at a high level. |
| 7 | **How to get started** | Show how *easy* the first step is — the customer's first 1–3 actions, with enough specificity to build confidence. |
| 8 | **Customer quote** | A fictional-but-realistic, named delighted customer naming their original pain and the benefit they now get. |
| 9 | **Call to action / closing** | The single first place a customer goes — a URL. |
| 10 | **Closing mark** | `# # #` (press-industry end-of-release marker). |

Ordering note: some templates place the leader quote with the customer quote near the
end. The order above (leader quote after solution, then getting-started, then customer
quote, then CTA) reads as the most natural narrative arc and is the recommended default.

**Length norm:** one page, full stop. If the benefit can't be made exciting in one page,
the idea isn't strong enough — this is itself an early innovation filter.

---

## 3. FAQ — external vs. internal

Much longer than the release. Two clearly-labeled sections.

### External FAQ (customer- & press-facing — the easy ones)
- What is it / how does it work?
- What does it cost? (pricing model)
- When and where is it available? (regions, channels, rollout)
- What platforms/devices does it support?
- How do I get support?
- How is my data / privacy handled?
- Other obvious product-specific questions.

### Internal FAQ (the hard questions — where the honesty lives)
Deliberately adversarial; anticipates what senior leaders will ask. This is much longer
and is where weak ideas die.

- **Customer & demand:** Who exactly is the customer, and what proof do we have they
  have this problem? Would customers change current behavior to adopt? How will we test
  and measure success?
- **Market sizing (TAM):** market size = (# customers with the problem) × (what each
  will pay). Show the arithmetic. Is it large enough to justify the investment?
- **Unit economics:** per-unit cost, gross margin, upfront investment, timeline to
  profitability.
- **Competition / build-vs-buy:** what customers use today; why we're meaningfully
  better/cheaper/faster; build, buy, or partner?
- **Feasibility:** what new capability/technology must we invent or acquire? What's
  never been done before?
- **Dependencies:** which teams, partners, or infrastructure do we rely on?
- **Risks / what could go wrong:** the top three reasons this could fail; legal and
  regulatory concerns.
- **Scope — what we are NOT doing:** explicit out-of-scope boundaries for this version.
- **Cross-functional:** questions finance, legal, ops, marketing, and HR would each raise.

The press release answers "is this worth wanting?" The internal FAQ answers "is it worth
— and possible — to build?" The solution must be **valuable, viable, and feasible** at
once (customer need, business impact, team sustainability).

---

## 4. The five customer questions

Guidelines, not an ordered checklist. The release implicitly answers Q1–4; Q5's TAM
piece usually lives in the FAQ.

1. Who is the customer?
2. What is the customer problem or opportunity?
3. What is the most important customer benefit (the solution, explained to the customer)?
4. How do you know what customers need/want — and would they change behavior to adopt it?
5. What does the experience look like, and is the TAM large enough?

**Reviewer evaluation criteria** (what readers grade against): customer clearly defined?
problem clearly defined? solution actually addresses the problem? would customers change
behavior? in what dimension is it better/cheaper/faster, and is the market sufficient?

---

## 5. Rules, constraints, best practices

- **Write as if already launched.** Future-dated dateline; product in present/past tense.
- **"Oprah-speak," not "geek-speak."** Imagine explaining it on Oprah's couch. Plain,
  accessible language. No jargon, buzzwords, acronyms, code names, or marketing fluff.
- **Quantify everything.** Concrete numbers over vague claims — specificity builds
  credibility and forces real thinking.
- **One page.** The constraint forces prioritization; you must choose the single most
  important benefit.
- **First draft fast** (a few hours, not days), then iterate through review cycles.
- **The "if it's not exciting, don't build it" test.** If the benefit can't be expressed
  excitingly in mock-press-release form, the idea probably isn't worth investing in.
- **Don't let the process drive you.** Write multiple competing PRs early; write a
  FAQ-only doc to resolve one issue; separate docs per customer segment. Use the process
  to solve the problem in front of you.

---

## 6. Anti-patterns (expanded self-review checklist)

- **Feature-listing** instead of one compelling customer benefit.
- **Hype / "Oprah-speak gone wrong"** — superlatives with no substance ("revolutionary,"
  "world-class," "seamless," "game-changing").
- **Internal jargon / geek-speak** — acronyms, code names, technical framing the customer
  wouldn't use.
- **Vague benefits** — "makes things easier" with no number.
- **Burying the lede** — failing to give the whole story in the summary paragraph.
- **Solution-first problem paragraph** — describing your product where you should be
  describing the customer's pain.
- **Skipping the hard internal FAQ** — the cardinal sin; it defeats the whole purpose.
- **Treating it as a spec/PRD** — it's a vision-and-strategy alignment tool, not a
  requirements document.
- **Customer value without viability** — ignoring business impact and team sustainability.

---

## 7. The "Melinda" worked example (Colin Bryar's published sample)

The cleanest full template-in-action. Verbatim fragments:

- **Summary/lede:** "Today Blue Corp. announced the launch of Melinda, a smart mailbox
  that ensures secure and properly chilled delivery and storage for your online purchases
  and groceries. With Melinda, you no longer need to worry about getting your deliveries
  stolen from your doorstep or spoiled groceries. Plus, you're notified as soon as your
  packages are delivered. Packed with smart technology, Melinda costs just $299."
- **Dateline:** PR Newswire, Atlanta, GA, November 5, 2019.
- **Problem (quantified):** "23 percent of online shoppers report having packages stolen
  from their front porch, and 19 percent complain of grocery deliveries being spoiled."
- **Solution (concrete features):** camera, speaker, fingerprint reader, built-in scale,
  two-inch insulation; verifies deliveries via barcode scan; keeps groceries cool up to
  12 hours.
- **Leader quote:** "Melinda is a breakthrough in safety and convenience for online
  shoppers… we combined a number of the latest technologies at the low price of just
  $299." — Lisa Morris, CEO of Blue Corp.
- **Customer quote:** "Melinda is a lifesaver… I love knowing that they are kept cool and
  secure in my Melinda." — Janet Thomas, Instacart customer.
- **CTA:** "To order your Melinda, simply visit keepitcoolmelinda.com, or visit
  amazon.com, walmart.com, Walmart stores, and other leading retailers."

Note: Kindle, Prime, AWS, Prime Video, Amazon Music, and Alexa were all developed via
Working Backwards, but their original PR/FAQs are not public — Melinda plus McAllister's
template are the canonical public artifacts.

---

## 8. Fill-in-the-blank templates

### A. Press release

```
[COMPANY] Announces [PRODUCT NAME] to Enable [CUSTOMER SEGMENT] to [PRIMARY BENEFIT]
(Heading — one line, in language the target customer understands)

[One-sentence subheading: who the product is for and the single key benefit.]

[CITY, STATE] — [FUTURE LAUNCH DATE] — [Summary / lede: 2–4 sentences giving the whole
story. What it is, who it's for, the headline benefit, often the price. Assume the reader
reads nothing else.]

[Problem paragraph: from the CUSTOMER'S point of view, the top 3–4 pains, ranked, with
concrete/quantified evidence. Do NOT mention your product here.]

[Solution paragraph(s): how [PRODUCT] elegantly solves each pain. What customers use
today and why it falls short; how you're better/cheaper/faster. Concrete and quantified.]

"[Leader quote: why [COMPANY] took this on and how it works at a high level.]"
— [Name, Title, Company]

Getting started is easy. [The customer's first 1–3 steps and how simple it is.]

"[Customer quote: a realistic, named (fictional) customer naming their old pain and the
benefit they now enjoy.]"
— [Customer Name, descriptor/role]

To get started, visit [URL — the single first place a customer should go].

# # #
```

### B. FAQ

```
FREQUENTLY ASKED QUESTIONS

--- External FAQ (customer- & press-facing) ---
Q: What is [PRODUCT] and how does it work?
Q: How much does it cost? / What's the pricing model?
Q: When and where will it be available? (regions, channels)
Q: What platforms/devices does it support?
Q: How do I get support if something goes wrong?
Q: How is my data and privacy handled?
Q: [Other obvious product-specific questions]

--- Internal FAQ (the hard questions) ---
Customer & demand
Q: Who exactly is the customer, and what proof do we have they have this problem?
Q: Would customers change current behavior to adopt this? What change is required?
Q: How will we test the solution and measure success?

Market & economics
Q: What is the TAM? (# customers with the problem × what each will pay — show the math)
Q: What are the per-unit economics and gross margin?
Q: What upfront investment is required, and what's the path to profitability?

Competition & approach
Q: What do target customers use today, and why are we meaningfully better/cheaper/faster?
Q: Should we build, buy, or partner?

Feasibility & dependencies
Q: What new capabilities or technology must we create or acquire?
Q: What teams, partners, or infrastructure does this depend on?

Risk & scope
Q: What are the top 3 reasons this could fail?
Q: What legal, regulatory, or compliance concerns exist?
Q: What are we explicitly NOT doing in this version? (scope boundaries)
```
