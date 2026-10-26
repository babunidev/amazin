# Development rules — amazin

**Author:** Babuni.dev

Preserve project-specific player experience and source comments. Human direction belongs to Babuni.dev; credit AI separately. Existing code is evidence of an approach, not proof of historic approval or runtime verification. Record proposed, implemented and tested separately. With material edits update README, CONCEPT, ROADMAP, CHANGELOG and docs/DEVLOG. Preserve third-party credits.

## Evidence and maintenance rules

- Read the actual branch, Lua, TOC, README and relevant dated diffs before editing. Keep source behavior, proposals and tested results separate.
- Preserve Babuni.dev as project author; identify AI drafting, analysis or code assistance separately. Preserve historical records, aliases, license terms and third-party credit.
- Never treat a comment, version label or manifest interface as proof of runtime compatibility. Never claim tests were run without recording the command, environment and outcome.
- For material changes update README, CONCEPT, ROADMAP, CHANGELOG and docs/DEVLOG, plus architecture/design/content where affected. Link evidence and retain uncertainty.
- Documentation-only work must not change Lua, TOC, tests or assets. Check the diff and all relative documentation links before publishing.

## Repository-specific constraints

- Resolve Lua v1.2.4 versus TOC v1.1.0 and stale TOC command descriptions before a release; do not silently choose a version.
- Verify 1.12 event callback conventions, login/logout persistence and logout before lazy hydration.
- Check watched-slot presses with failed casts, bar paging and another UseAction wrapper.
- Exercise 0%/100% chance, cooldown boundaries, startup uptime, reset and rested-XP edge cases.
- Validate all 12 built-in tokens and fallback behavior on intended locales; prior README compatibility claims are not test results.
