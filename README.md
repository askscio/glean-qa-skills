# glean-qa-skills

Frozen fixture repository for Glean's **Skills → Import from GitHub** browser tests
(`python_scio/scripts/tests/yoda_playwright_automation/component_tests/assistant/skills/`).

**Do not edit, rename, or delete anything here.** CI asserts on exact skill names, file
trees, and counts. Change the tests first if a layout change is ever required.

## Layout

| Path | Purpose |
|---|---|
| `skills/finance-skills/` | Single skill, `SKILL.md` only |
| `skills/saas-metrics-coach/` | Single skill with supporting files (`assets/`, `references/`, `scripts/`) |
| `skills/financial-analyst/` | Single skill, trimmed supporting files |
| `skills/month-end-close/` | Single skill including a binary (`assets/logo.png`) that import must skip |
| `skills/` | Folder import → 4 skills |
| `nested/outer/` | Skill whose folder contains another skill (`inner/`) |
| repository root | Root import → 6 skills |
| `empty/` | Folder with no `SKILL.md` → import error |

Refs used by tests: branch `main`, branch `feature/qa`, tag `v1` (all point at the same tree).

## Attribution

Files under `skills/` are adapted from [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills)
(`finance/skills/*`, commit `8f082544116fc0d014188e521ca40304cdfc86b0`, MIT). Frontmatter was rewritten with QA names and
descriptions; supporting files were trimmed. See `LICENSE`.
