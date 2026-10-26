# cursor-skills

Cursor adaptations of a few of Matt Pocock's agent skills, for vendoring into project repos.

Source: https://github.com/mattpocock/skills at commit [`5beb35b`](https://github.com/mattpocock/skills/tree/5beb35b). MIT licensed; see `LICENSE`.

## What's here

Slash commands (`.cursor/commands/`):

- `/grill-me`: relentless interview to sharpen a plan or design.
- `/grill-with-docs`: the same, while updating `GLOSSARY.md` and ADRs in `docs/adr/`.
- `/tdd`: test-first red→green development.
- `/to-spec`: turn the conversation into a spec, published as a GitHub issue labeled `ready-for-agent`.
- `/improve-codebase-architecture`: find deepening opportunities, write an HTML report to `docs/architecture-reports/`, then grill through the one you pick.

Rules (`.cursor/rules/`, `alwaysApply: false`): `grilling`, `domain-modeling`, `codebase-design`, `tdd`, each with helper files in a folder of the same name.

## Changes from upstream

- "Call the Skill tool with X" became "read and follow `.cursor/rules/X.mdc`".
- Sub-agent dispatches are done inline.
- `/to-spec` publishes straight to the repo's GitHub issues; no `setup-matt-pocock-skills` or `docs/agents/issue-tracker.md`.
- The architecture report goes to `docs/architecture-reports/` (or a cloud-agent artifact) instead of `$TMPDIR`.
- `disable-model-invocation` and `agents/openai.yaml` were dropped.

## Use in a project

1. Copy this repo's `.cursor/` folder contents into the project's `.cursor/` folder. Use real copies, not symlinks, so cloud agents see them.
2. Paste `AGENTS-snippet.md` into the project's `AGENTS.md`.
3. Commit.
