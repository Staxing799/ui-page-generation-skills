# CLAUDE.md

Behavioral guidelines for generating beautiful, production-style front-end pages from short prompts.
Merge with project-specific instructions as needed.

Tradeoff: These guidelines bias toward design quality, restraint, and product realism over raw speed.

## 1. Design Before Code

Do not jump straight into code.

Before implementing:

- Identify the page type first: landing page, SaaS dashboard, AI tool, data view, settings page, form flow, workspace, desktop app screen.
- State the primary user goal for the page in one sentence.
- Plan the information hierarchy before choosing components.
- If the request is ambiguous, choose the simplest commercially realistic page structure rather than inventing extra features.
- If a design choice is debatable, prefer the cleaner and more restrained option.

## 2. Product-Grade UI by Default

Default style:

- modern
- minimal
- high whitespace
- strong hierarchy
- unified spacing
- restrained color usage
- card-based where appropriate
- professional, not flashy

Do not generate pages that feel like low-quality templates, crowded admin demos, or random component dumps.

## 3. Structured Layout, Not Feature Piles

- Build pages as clear sections with a visible main task.
- Prefer a stable layout skeleton: top bar, sidebar when needed, main work area, secondary panel only when justified.
- Keep alignment consistent.
- Use a limited set of spacing values.
- Make one focal action visually dominant.
- Reduce visual competition between components.

## 4. Consistent Design System

Keep these systems consistent across the page:

- color
- typography
- radius
- border treatment
- shadow treatment
- icon style
- component density

Use one main accent color and mostly neutral surfaces unless the user explicitly asks otherwise.

## 5. Natural Product Copy

Do not write copy that sounds AI-generated, generic, inflated, or empty.

Avoid patterns like:

- "empower your workflow"
- "unlock infinite possibilities"
- "redefine productivity"
- "seamlessly transform your experience"
- vague marketing filler with no concrete meaning

Prefer copy that is:

- short
- specific
- grounded
- believable
- product-like
- written as if it belongs in a real shipped interface

Buttons, headings, labels, helper text, empty states, and onboarding text should sound like real product copy, not prompt-engineered copy.

## 6. Simplicity Over Decoration

- No decorative gradients everywhere.
- No oversized shadows.
- No colorful buttons fighting each other.
- No excessive badges, charts, or cards unless the task needs them.
- No speculative widgets or panels the user did not ask for.

If removing one section improves the page, remove it.

## 7. Output Requirements

When generating a page, do this order:

1. page type
2. visual direction
3. information architecture
4. key components
5. interaction priorities
6. final code

If code is requested, default to React + Tailwind + shadcn-style patterns unless the project context says otherwise.

## 8. Quality Check Before Finalizing

Before final output, verify:

- The page has a clear visual hierarchy.
- The layout breathes.
- The interface feels commercially believable.
- The copy sounds human and product-native.
- No section exists only because AI page generators often add it.
- The result looks like a focused product page, not a component showcase.
