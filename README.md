# The Pipeline

A collection of Claude Code skills that move an idea from raw thought to shipped
reality. Each stage of the pipeline is its own skill; this repo is the home for all of
them.

## Skills

| Stage | Skill | What it does |
|-------|-------|--------------|
| 1 | `product-idea` | Turns any product or feature idea into a future-dated Amazon **Working Backwards** PR/FAQ — a one-page mock press release plus a rigorous external + internal FAQ — written in the fused voice of **Ivy Lee** (clarity, credibility, brevity) and **Edward Bernays** (psychology, narrative framing). The vision. |
| 2 | `discovery` | Takes the PR/FAQ and **pressure-tests it with autonomous deep research**, producing three artifacts — research synthesis, opportunity map, assumption tests — and exits only when the **problem and the bet are sharp** (a falsifiable bet with a named riskiest assumption). The reality check. |

**The loop:** `product-idea` (vision) → `discovery` (validate & sharpen) → back to refine the PR/FAQ, or forward to build.

_(More stages coming.)_

## Layout

```
the-pipeline/
├── .claude-plugin/
│   ├── plugin.json         # plugin manifest
│   └── marketplace.json    # lets you install it as a local marketplace
├── skills/
│   ├── product-idea/
│   │   ├── SKILL.md
│   │   └── references/
│   │       ├── working-backwards.md
│   │       └── press-release-craft.md
│   └── discovery/
│       ├── SKILL.md
│       └── references/
│           └── discovery-methods.md
└── README.md
```

Claude Code auto-discovers anything under `skills/`, so adding a new stage is just a
matter of creating `skills/<new-skill>/SKILL.md`.

## Install (local marketplace)

From Claude Code:

```
/plugin marketplace add /Users/fp/Documents/Claude Optimization/the-pipeline
/plugin install the-pipeline@the-pipeline
```

Then restart or reload, and the skills appear in your skill list. To update after
editing, run `/plugin marketplace update the-pipeline`.

## Adding a new skill

1. Create `skills/<skill-name>/SKILL.md` with YAML frontmatter (`name`, `description`).
2. Put any heavy reference docs in `skills/<skill-name>/references/`.
3. Bump `version` in `.claude-plugin/plugin.json`.
4. Run `/plugin marketplace update the-pipeline`.
