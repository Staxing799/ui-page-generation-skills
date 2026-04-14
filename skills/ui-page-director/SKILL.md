name: ui-page-director
description: Generate front-end pages that look commercially polished by enforcing page-type detection, information hierarchy, restrained visual systems, realistic layouts, and product-grade UI decisions before code generation.
license: MIT

# UI Page Director

Use this skill when the user wants to generate a website page, dashboard, landing page, app screen, desktop UI, or front-end interface from a short prompt.

This skill exists to prevent ugly AI-generated UI caused by vague structure, weak hierarchy, bad spacing, noisy color choices, and generic component dumping.

## Core Objective

Generate pages that feel like real shipped products:

- clean
- modern
- restrained
- structured
- believable
- visually strong without being flashy

## 1. Decide the Page Type First

Before writing code, classify the request into one of these:

- landing page
- marketing site
- SaaS dashboard
- AI tool workspace
- settings page
- data table page
- form flow
- analytics page
- desktop app workspace
- content management page

Then optimize layout for that page type rather than using a generic template.

## 2. Build a Real Information Hierarchy

Always define:

- primary user goal
- primary action
- secondary actions
- high-priority content
- supporting content
- optional content that can be omitted

If everything looks equally important, the hierarchy is wrong.

## 3. Use a Reliable Layout Skeleton

Prefer durable structures such as:

- top navigation + hero + supporting sections for landing pages
- sidebar + top bar + main workspace for tools and dashboards
- centered form shell with grouped sections for forms
- summary row + filters + main table + detail view for management pages

Do not stack unrelated blocks just to make the page feel fuller.

## 4. Enforce a Professional Visual System

Default style rules:

- high whitespace
- restrained palette
- one primary accent color
- neutral backgrounds
- medium-to-large radius consistency
- light shadows or subtle borders
- clean icon style
- 4-6 typography levels maximum

Avoid:

- rainbow accents
- heavy borders
- thick shadows
- oversaturated gradients
- inconsistent radii
- random font sizing

## 5. Prefer Better Component Composition

Use a limited, coherent set of components:

- cards
- tabs
- tables
- filters
- search
- drawers
- modals
- stat blocks
- empty states
- toast feedback
- grouped forms

Rules:

- one card should represent one topic
- one page should have one strongest CTA
- tables should look breathable, not cramped
- forms should be grouped and easy to scan
- stats should be limited to the few that matter

## 6. Make It Feel Designed, Not Assembled

Add polish through restraint:

- clearer section rhythm
- better alignment
- better whitespace balance
- fewer but stronger emphasis points
- realistic empty and loading states
- concise labels and helper text

Do not add polish by piling on visual effects.

## 7. What to Avoid

Never generate pages that feel like:

- a low-end admin template
- a Dribbble shot with no product logic
- a crowded no-whitespace dashboard
- a component showroom
- a generic AI-generated hero with empty buzzwords

## 8. Output Sequence

When responding, use this sequence internally before code:

1. Identify page type.
2. Choose visual direction.
3. Plan section structure.
4. Select the smallest useful component set.
5. Ensure copy can sound like a real product.
6. Generate final UI.

## 9. Final Review Checklist

Before finalizing, confirm:

- Clear focal point
- Consistent spacing
- Consistent component language
- Realistic structure for the requested product type
- Minimal visual noise
- Stronger design than default AI page generation
