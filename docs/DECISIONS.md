# amazin — decisions and evidence

**Project author and creative direction:** Babuni.dev

| Implemented choice | Evidence | Interpretation boundary |
| --- | --- | --- |
| Observe a slot press | `UseAction` wrapper | Not successful Stealth detection |
| Consume cooldown before roll | `doStealthEmoteNow` assignment order | No recorded rationale for this order |
| Store account-wide settings | `AmazinDB` and TOC | Different characters may need different slots |
| Parse with `string.find` | `split_cmd` | Lua 5.0 intent is not a live-client test |
| Keep version mismatch visible | Lua header and TOC | Documentation does not reconcile release identity |

## Open verification

- Resolve Lua v1.2.4 versus TOC v1.1.0 and stale TOC command descriptions before a release; do not silently choose a version.
- Verify 1.12 event callback conventions, login/logout persistence and logout before lazy hydration.
- Check watched-slot presses with failed casts, bar paging and another UseAction wrapper.
- Exercise 0%/100% chance, cooldown boundaries, startup uptime, reset and rested-XP edge cases.
- Validate all 12 built-in tokens and fallback behavior on intended locales; prior README compatibility claims are not test results.

These are source-observed choices and proposed checks, not invented historical approvals or an approved feature backlog.

## Preserved earlier documentation

The following earlier record is retained verbatim. Statements about unavailable history or pending verification describe that earlier snapshot; the dated evidence above supplements it.

# amazin — decisions and evidence

**Author:** Babuni.dev

## Current implementation choices (not confirmed historical approvals)

Stealth is inferred from the watched button rather than a buff/icon, which avoids fragile client aura checks.

## Unresolved

README describes version 1.2.4 while the inspected TOC declared 1.1.0; confirm version before release.
