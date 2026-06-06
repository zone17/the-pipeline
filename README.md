# The Pipeline

A collection of [Claude Code](https://claude.com/claude-code) skills that move a product
idea from **raw thought to shipped reality**. Each stage of the pipeline is its own skill;
this repo is the home — and the installable marketplace — for all of them.

The philosophy: do the thinking *before* the building. Write the launch announcement
first, then pressure-test it with real research, and only then commit to code. Most of the
value is in killing or sharpening weak ideas cheaply, before they cost you a sprint.

---

## Skills

| Stage | Skill | What it does |
|-------|-------|--------------|
| 1 — Vision | [`product-idea`](skills/product-idea/SKILL.md) | Turns any product or feature idea into a future-dated Amazon **Working Backwards** PR/FAQ — a one-page mock press release plus a rigorous external + internal FAQ — written in the fused voice of **Ivy Lee** (clarity, credibility, brevity) and **Edward Bernays** (psychology, narrative framing). |
| 2 — Reality check | [`discovery`](skills/discovery/SKILL.md) | Takes that PR/FAQ and **pressure-tests it with autonomous deep research**, producing three artifacts — a research synthesis, an opportunity map, and assumption tests — and exits only when the **problem and the bet are sharp** (a falsifiable bet with a named riskiest assumption and a walk-away condition). |

**The loop:**

```
        ┌──────────────────────────────────────────┐
        ▼                                            │
   product-idea  ──►  discovery  ──►  sharp problem + bet
   (the vision)      (validate &       │         │
                      sharpen)         │         │
                                refine PR/FAQ   build
```

`product-idea` gives you a confident vision. `discovery` asks whether any of it is true and
whether it's the sharpest version of the bet — then sends you back to revise the PR/FAQ or
forward to build.

_(More stages coming as the pipeline grows toward "shipped.")_

---

## Install

### From GitHub (recommended — gets updates)

In Claude Code:

```
/plugin marketplace add zone17/the-pipeline
/plugin install the-pipeline@the-pipeline
```

Pull future updates with:

```
/plugin marketplace update the-pipeline
```

### From a local clone

```bash
git clone https://github.com/zone17/the-pipeline.git
```

Then, in Claude Code:

```
/plugin marketplace add /path/to/the-pipeline
/plugin install the-pipeline@the-pipeline
```

After installing, the two skills appear in your skill list and trigger automatically when
your request matches them (see **Usage** below). No restart needed in recent Claude Code
versions; reload if they don't show up.

### In Claude Cowork / Claude Desktop

The same plugin works in Claude Cowork (Claude Desktop for macOS/Windows, paid plans). No
repackaging needed — it installs from this GitHub repo:

1. Open the **Cowork** tab, then **Customize** in the left sidebar.
2. Open the **Plugins** tab → add a marketplace from a **GitHub repository / git URL**:
   `https://github.com/zone17/the-pipeline`
3. **Install** `the-pipeline`.

You can also share it with a colleague by sending them the plugin file to upload directly.
`product-idea` runs identically; `discovery` adapts to Cowork's native web search and any
research **MCP connectors** you've added (its research instructions are environment-aware).

---

## Usage

The skills are model-invoked: describe what you want in natural language and Claude routes
to the right one. You can also invoke them explicitly.

### `product-idea` — write the vision

Triggers on things like *"write a press release for my idea," "do a working-backwards doc,"
"PRFAQ," "draft the launch announcement," "pitch this product," "is this idea worth
building."*

> **You:** I want to build a tool that auto-generates release notes from merged PRs.
> Write the PR/FAQ.

It produces a future-dated mock press release plus an external + internal FAQ (customer,
problem, the single most important benefit, evidence of demand, experience, market size,
unit economics, risks, and what you're deliberately *not* building). Where you left gaps,
it invents realistic specifics and lists them under "Assumptions I made" so you can correct
them.

### `discovery` — pressure-test the vision

Triggers on things like *"is this idea real," "validate this," "pressure-test the PR/FAQ,"
"do discovery on this," "what are the riskiest assumptions," "map the opportunity," "should
we build this."*

> **You:** Run discovery on that PR/FAQ.

It extracts a claims ledger from the PR/FAQ, runs autonomous deep research, and produces:

- a **research synthesis** (separating evidence from inference),
- an **opportunity map** (prioritized problems / opportunity-solution tree), and
- **assumption tests** (the riskiest assumptions, each with the cheapest experiment to
  falsify it).

It only declares done when both the **problem** (a specific customer job, backed by
evidence, with current alternatives and why they fall short) and the **bet** (beachhead
customer, point of view on why you win, riskiest assumption, and the falsification
condition that would make you walk away) are sharp.

### Running the full loop

1. `product-idea` → draft the PR/FAQ.
2. `discovery` → pressure-test it.
3. Use the verdict — **proceed, refine, pivot, or kill** — to revise the PR/FAQ or move on
   to build.

---

## Layout

```
the-pipeline/
├── .claude-plugin/
│   ├── plugin.json          # plugin manifest (name, version, keywords)
│   └── marketplace.json     # marketplace manifest — makes the repo installable
├── skills/
│   ├── product-idea/
│   │   ├── SKILL.md         # the skill: trigger description + workflow
│   │   └── references/
│   │       ├── working-backwards.md     # Amazon Working Backwards method
│   │       └── press-release-craft.md   # Ivy Lee + Bernays craft principles
│   └── discovery/
│       ├── SKILL.md
│       └── references/
│           └── discovery-methods.md     # frameworks, scoring math, templates
├── LICENSE
└── README.md
```

Claude Code auto-discovers anything under `skills/`, so each `SKILL.md` is the unit of
behavior and the `references/` files hold the heavier craft/method docs the skill pulls in
on demand.

---

## Adding a new stage

1. Create `skills/<skill-name>/SKILL.md` with YAML frontmatter (`name`, `description`).
   The `description` is what Claude uses to decide when to trigger the skill — make it
   specific and list trigger phrases.
2. Put any heavy reference docs in `skills/<skill-name>/references/`.
3. Bump `version` in **both** `.claude-plugin/plugin.json` and
   `.claude-plugin/marketplace.json` (keep them in sync).
4. Commit, push, and run `/plugin marketplace update the-pipeline`.

---

## Contributing

Issues and PRs welcome. Keep skill descriptions trigger-oriented and reference docs
self-contained, and bump the version in both manifests with any behavior change.

## License

[MIT](LICENSE) © 2026 Matt Wollschleger
