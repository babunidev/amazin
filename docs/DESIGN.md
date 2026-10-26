# amazin — experience design

**Project author and creative direction:** Babuni.dev

The small interaction gives a stealth-themed action a comic character reaction. This reading follows current source and prior README, not a recovered design discussion. Slot watching avoids dependence on aura/icon detection, but pressing the slot is not proof that Stealth succeeded. Moving or paging action bars can change what the selected slot means.

Chance and cooldown offer two independent controls over frequency. Watch mode helps discover slot numbers, but prints every action while enabled. The addon wraps a global function, so other action-bar addons and load order need a combined test. Historical claims that it works on every locale remain unverified in this pass.

## Verification priorities

- Resolve Lua v1.2.4 versus TOC v1.1.0 and stale TOC command descriptions before a release; do not silently choose a version.
- Verify 1.12 event callback conventions, login/logout persistence and logout before lazy hydration.
- Check watched-slot presses with failed casts, bar paging and another UseAction wrapper.
- Exercise 0%/100% chance, cooldown boundaries, startup uptime, reset and rested-XP edge cases.
- Validate all 12 built-in tokens and fallback behavior on intended locales; prior README compatibility claims are not test results.
