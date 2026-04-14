---
name: ui-page-director
description: Plan and generate commercially believable UI pages before writing code. Use when Codex needs to turn a short product prompt into a landing page, dashboard, app screen, settings page, workspace, analytics view, table page, or other front-end interface with strong hierarchy, restrained styling, and realistic product structure.
---

# UI Page Director

Classify the page before generating code.

Pick the closest page type:

- landing page
- marketing site
- SaaS dashboard
- AI workspace
- settings page
- data table page
- analytics page
- form flow
- content management page
- desktop app workspace

State the primary user goal in one sentence and let that goal drive layout decisions.

Plan the information hierarchy before picking components.

Define:

- primary action
- secondary actions
- high-priority content
- supporting content
- optional content that can be omitted

Prefer a durable layout skeleton instead of a generic block stack.

Use patterns such as:

- top navigation + hero + supporting sections for landing pages
- sidebar + top bar + main workspace for dashboards and tools
- centered shell with grouped sections for forms
- summary row + filters + table + detail panel for management pages

Keep the visual system restrained and consistent.

Default style rules:

- high whitespace
- mostly neutral surfaces
- one primary accent color
- medium or large radius used consistently
- subtle borders or light shadows
- four to six typography levels at most
- one icon style and one density level across the page

Avoid:

- rainbow accents
- thick shadows
- heavy borders
- cramped layouts
- inconsistent radii
- decorative sections with no product logic

Compose a small, coherent component set.

Prefer:

- cards for distinct topics
- tabs for limited view switching
- filters and search for dense data pages
- grouped forms with clear section titles
- stat blocks only for the few metrics that matter
- empty, loading, and error states that fit the page

Do not turn the page into a component showroom.

Keep one strongest call to action. Let supporting actions stay visually secondary.

Add polish through structure and restraint.

Improve:

- spacing rhythm
- alignment
- section pacing
- emphasis hierarchy
- label clarity
- realistic placeholder and empty states

Do not add polish by piling on effects.

Before finalizing, review this checklist:

- page type is clear
- focal point is obvious
- structure matches the product context
- spacing feels breathable
- component language is consistent
- visual noise is low
- result feels like a shipped product, not a template dump
