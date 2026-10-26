# amazin — roadmap

**Project author and creative direction:** Babuni.dev

## Current implementation

A stealth-themed emote addon that watches one configured action-bar slot. Pressing that slot may play a random built-in emote after a cooldown, then delegates to the original action. It does not detect successful Stealth casts or actual stealth state. A separate command reports rested XP.

## Proposed verification work

- [ ] Resolve Lua v1.2.4 versus TOC v1.1.0 and stale TOC command descriptions before a release; do not silently choose a version.
- [ ] Verify 1.12 event callback conventions, login/logout persistence and logout before lazy hydration.
- [ ] Check watched-slot presses with failed casts, bar paging and another UseAction wrapper.
- [ ] Exercise 0%/100% chance, cooldown boundaries, startup uptime, reset and rested-XP edge cases.
- [ ] Validate all 12 built-in tokens and fallback behavior on intended locales; prior README compatibility claims are not test results.

No new gameplay feature or release is approved by this documentation pass. Resolve compatibility findings in a separately scoped implementation change and update this record with actual test results.

## Preserved earlier documentation

The following earlier record is retained verbatim. Statements about unavailable history or pending verification describe that earlier snapshot; the dated evidence above supplements it.

# amazin — roadmap

**Author:** Babuni.dev

## Present

Source and addon metadata exist. No live-game test was conducted during this documentation pass.

## Verification work, not approved new features

README describes version 1.2.4 while the inspected TOC declared 1.1.0; confirm version before release.

## Future development

No additional feature is approved by this reconstruction. Record new direction before implementation.
