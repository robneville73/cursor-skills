## Agent skills

- Slash commands live in `.cursor/commands/`: `/grill-me`, `/grill-with-docs`, `/tdd`, `/to-spec`, `/improve-codebase-architecture`.
- Supporting rules live in `.cursor/rules/`: `grilling.mdc`, `domain-modeling.mdc`, `codebase-design.mdc`, `tdd.mdc`. When a command or task says to read and follow one, read it and its helper files.
- Domain language: `GLOSSARY.md` at the repo root. Use its terms; update it when a term is settled.
- Decisions: ADRs in `docs/adr/`. Respect them; do not re-litigate without a reason.
- Specs and tickets are GitHub issues in this repo; agent-ready ones carry the `ready-for-agent` label.
