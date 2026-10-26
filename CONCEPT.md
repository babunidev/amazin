# amazin — concept

**Project author and creative direction:** Babuni.dev

A stealth-themed emote addon that watches one configured action-bar slot. Pressing that slot may play a random built-in emote after a cooldown, then delegates to the original action. It does not detect successful Stealth casts or actual stealth state. A separate command reports rested XP.

The small interaction gives a stealth-themed action a comic character reaction. This reading follows current source and prior README, not a recovered design discussion. Slot watching avoids dependence on aura/icon detection, but pressing the slot is not proof that Stealth succeeded. Moving or paging action bars can change what the selected slot means.

Chance and cooldown offer two independent controls over frequency. Watch mode helps discover slot numbers, but prints every action while enabled. The addon wraps a global function, so other action-bar addons and load order need a combined test. Historical claims that it works on every locale remain unverified in this pass.

## Evidence and status

Reviewed on 2026-10-26 against `main` at [e96070a](https://github.com/babunidev/amazin/commit/e96070a7cf16ed4605caafaf018a566f74d63207). Current Lua, TOC, README and dated commit history were inspected. Source describes implementation; it does not establish successful operation. Historical intent is reconstructed only where labeled. No in-client test or automated test was executed during this documentation pass.

## Preserved earlier documentation

The following earlier record is retained verbatim. Statements about unavailable history or pending verification describe that earlier snapshot; the dated evidence above supplements it.

# amazin — concept

**Author:** Babuni.dev

A Vanilla 1.12 stealth-themed emote addon with cooldown, random chance, watched action slot and rested-experience reporting.

## Design visible in the repository

Stealth is inferred from the watched button rather than a buff/icon, which avoids fragile client aura checks.

This concept is reconstructed from README.md, main addon Lua file and .toc manifest; original idea and authorship belong to Babuni.dev. No unrecorded decisions are invented.
