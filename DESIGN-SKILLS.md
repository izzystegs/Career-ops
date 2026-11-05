# Design skills

Design skills installed on top of career-ops, for building the internship tracker UI.
All are MIT-licensed; each keeps its own LICENSE file.

| Skill(s) | Location | Source |
|---|---|---|
| `hallmark` | `.claude/skills/hallmark/` | [Nutlope/hallmark](https://github.com/Nutlope/hallmark) @ de4999e |
| `refactoring-ui` | `.claude/skills/refactoring-ui/` | [edisonmbli/refactoring-ui-skill](https://github.com/edisonmbli/refactoring-ui-skill) @ 4459662 |
| `data-dashboard`, `design-screen`, `design-component`, `design-tokens`, `design-qa`, `a11y-audit`, `critique`, `redesign`, `ux-writing` | `.claude/skills/<name>` → symlinks into `vendor/ux-ui-agent-skills/` | [plugin87/ux-ui-agent-skills](https://github.com/plugin87/ux-ui-agent-skills) @ def84a7 |

## Notes

- The ux-ui-agent-skills skills read shared files from the kit (`tokens/`, `scripts/`, `taste/`, ...),
  so the full kit lives in `vendor/ux-ui-agent-skills/` and only a subset of its skills is linked in.
  Link more with: `ln -s ../../vendor/ux-ui-agent-skills/.claude/skills/<name> .claude/skills/<name>`.
- Left out of the vendored kit: its tests/evals, its `.claude/settings.json` (hooks and permissions),
  and the 40 MB `design-systems/library/` (its `library.mjs` fetches specs on demand).
- Hallmark's optional image generation only runs if `TOGETHER_API_KEY` is set.
