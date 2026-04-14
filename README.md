# UI Page Generation Skills

A lightweight skill folder inspired by the structure used in `forrestchang/andrej-karpathy-skills`:

- `CLAUDE.md` at the repo root
- `skills/<skill-name>/SKILL.md`
- optional `.claude-plugin/` directory placeholder

## Included skills

- `ui-page-director`: forces stronger UI structure and better visual decisions before code generation
- `product-copy-natural-tone`: removes heavy AI tone from UI copy and keeps product text grounded

## Suggested usage

Put this folder into your project, then let your coding agent load the root `CLAUDE.md` and the skills under `skills/`.

Use both skills together when you want:

- one-sentence page generation
- better visual hierarchy
- less template-like UI
- less AI-sounding copy
