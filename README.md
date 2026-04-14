# UI Page Generation Skills

Turn vague UI prompts into cleaner, more believable product pages.

This repository packages a small skill system for front-end page generation:

- one root skill as the main entry
- one sub-skill for layout and visual structure
- one sub-skill for natural, product-like copy

The goal is simple: make generated pages feel more like shipped software and less like generic AI mockups.

## What This Solves

Most raw UI generations fail in predictable ways:

- weak information hierarchy
- noisy layouts
- random component stacking
- inconsistent visual systems
- too much decoration
- AI-sounding headings, buttons, and helper text

This repository adds opinionated constraints before the final page is generated.

## Repository Design

The repo uses a single main entry skill at the root:

- [`SKILL.md`](./SKILL.md)

That root skill acts as an orchestrator and routes work to the specialized skills in [`skills/`](./skills).

## Structure

```text
.
├── SKILL.md
├── agents/
│   └── openai.yaml
└── skills/
    ├── ui-page-director/
    │   ├── SKILL.md
    │   └── agents/openai.yaml
    └── product-copy-natural-tone/
        ├── SKILL.md
        └── agents/openai.yaml
```

## Skills

### Main Entry: `ui-page-generation`

The root [`SKILL.md`](./SKILL.md) is the only entry you need to think about first.

It is responsible for:

- deciding whether a request is a UI/page-generation task
- routing work to the right sub-skill
- enforcing the execution order for full-page generation

### Sub-skill: `ui-page-director`

Use [`skills/ui-page-director/SKILL.md`](./skills/ui-page-director/SKILL.md) for:

- page type classification
- layout planning
- information hierarchy
- component selection
- restrained visual direction
- stronger product realism before code generation

### Sub-skill: `product-copy-natural-tone`

Use [`skills/product-copy-natural-tone/SKILL.md`](./skills/product-copy-natural-tone/SKILL.md) for:

- headings
- labels
- buttons
- helper text
- empty states
- onboarding copy
- landing-page copy
- cleanup of AI-sounding wording

## How It Works

For most page-generation tasks, the intended flow is:

1. Enter through the root `SKILL.md`.
2. Apply `ui-page-director` to define structure and visual logic.
3. Apply `product-copy-natural-tone` to refine visible copy.
4. Generate the final page or code.

If the task is copy-only, the copy skill can be used on its own.

If the task is layout-only, the UI direction skill can be used on its own.

## Example Prompts

These examples are useful for showing how the repository is meant to be used.

### Full Page Generation

```text
Use $ui-page-generation to build a SaaS analytics dashboard for a video localization tool.
The page should feel clean, credible, and ready for a real product.
```

### Landing Page

```text
Use $ui-page-generation to design a landing page for an AI meeting assistant.
Keep the layout restrained and make the copy sound like a real startup site, not a hype page.
```

### Layout-Only Improvement

```text
Use $ui-page-director to improve the structure of this settings page.
Reduce clutter, create a clearer hierarchy, and keep the UI commercially believable.
```

### Copy-Only Improvement

```text
Use $product-copy-natural-tone to rewrite these dashboard headings, buttons, and empty states.
Remove AI filler and make the wording feel product-native.
```

## Installation

Place this repository where your skill system can read it, or copy the root skill and the `skills/` directory into your local skills workspace.

If you are using a Codex-style local skill setup, the important files are:

- root `SKILL.md`
- root `agents/openai.yaml`
- all skill folders inside `skills/`

## Why A Root Skill

Without a main entry, multi-skill repositories are harder to use consistently.

The root skill solves that by:

- giving the repo one obvious entry point
- making routing explicit
- keeping sub-skills focused and reusable
- reducing ambiguity for future maintenance

## Design Principles

This repository is biased toward:

- design before code
- simple, commercially realistic page structure
- restrained visual systems
- consistency over novelty
- product-like copy instead of AI-flavored language

## Good Fit

- SaaS dashboards
- AI tool workspaces
- internal tools
- analytics pages
- settings pages
- landing pages
- data-heavy interfaces

## Not The Best Fit

- highly experimental visual design
- game UI
- brand-led art direction work
- intentionally loud or novelty-first layouts

## Status

This repository is organized as a standard skill set with:

- a valid root skill
- valid sub-skills
- per-skill `agents/openai.yaml` metadata

You can keep extending it by adding more specialized skills under `skills/` while preserving the root entry pattern.
