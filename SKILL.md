---
name: ui-page-generation
description: Orchestrate high-quality front-end page generation from short product prompts. Use when Codex needs a single main skill that coordinates UI structure, visual hierarchy, and natural product copy for landing pages, dashboards, app screens, workspaces, settings pages, analytics views, tables, and similar interfaces.
---

# UI Page Generation

Use this file as the main entry for the repository.

Treat this skill as the coordinator for the specialized skills under `skills/`.

Bias toward design quality, restraint, and product realism over raw speed.

## Workflow

Start by deciding whether the request is a front-end page or interface generation task.

Typical matches:

- landing page
- marketing site
- dashboard
- workspace
- settings page
- analytics page
- data table page
- form flow
- internal tool UI
- desktop-style app screen

If the request is not primarily about generating or refining a UI page, do not force this workflow.

Do not jump straight into code.

Before implementation:

- identify the page type first
- state the primary user goal in one sentence
- plan the information hierarchy before choosing components
- if the request is ambiguous, choose the simplest commercially realistic structure
- if a design choice is debatable, prefer the cleaner and more restrained option

## Skill Routing

Use `skills/ui-page-director/SKILL.md` when the task needs:

- page type classification
- layout planning
- information hierarchy
- component selection
- restrained visual direction
- stronger product realism before code generation

Use `skills/product-copy-natural-tone/SKILL.md` when the task needs:

- headings
- labels
- buttons
- helper text
- empty states
- onboarding copy
- landing-page copy
- cleanup of AI-sounding wording

In most page-generation tasks, use both skills:

1. Apply `ui-page-director` first to decide structure and visual logic.
2. Apply `product-copy-natural-tone` second to refine interface and marketing copy.
3. Generate the final UI only after both structure and copy quality are aligned.

If the user only asks for copy, use `product-copy-natural-tone` without forcing layout work.

If the user only asks for visual/layout improvement, use `ui-page-director` without rewriting copy unnecessarily.

## Global Constraints

Keep the page product-grade by default.

Default style:

- modern
- minimal
- high whitespace
- strong hierarchy
- unified spacing
- restrained color usage
- professional, not flashy

Keep the design system consistent across the page:

- color
- typography
- radius
- border treatment
- shadow treatment
- icon style
- component density

Use one main accent color and mostly neutral surfaces unless the user explicitly asks otherwise.

Build structured layouts, not feature piles.

- keep a clear main task
- make one focal action visually dominant
- reduce visual competition between components
- avoid speculative sections the user did not ask for

Prefer simplicity over decoration.

- avoid decorative gradients everywhere
- avoid oversized shadows
- avoid colorful buttons competing for attention
- avoid excessive badges, charts, or cards without product logic
- remove sections that only make the page look busier

## Output Order

When generating a page, follow this order:

1. Identify the page type.
2. State the primary user goal.
3. Plan information hierarchy.
4. Choose a restrained visual direction.
5. Decide the smallest useful component set.
6. Refine visible copy with natural product tone.
7. Produce the final code or page output.

## Quality Bar

Before finalizing, verify:

- structure matches the product context
- hierarchy is obvious
- layout feels breathable
- component choices are coherent
- copy sounds product-native
- result feels like a shipped product, not a generic AI mockup
