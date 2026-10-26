# amazin — development journal

**Project author and creative direction:** Babuni.dev

## Evidence-based retrospective — 2026-10-26

- **2025-08-22** — [c9d9b9f](https://github.com/babunidev/amazin/commit/c9d9b9f0df1501c9eacc9f9718d7fbc241d6cd03): Lua first added; commit-list evidence.
- **2025-08-22** — [8792a2b](https://github.com/babunidev/amazin/commit/8792a2b8cffa118059dd6b62bb9c8154c9f5696b): Inspected diff removes earlier aura/general-emote paths and simplifies toward watched-slot stealth emotes.
- **2025-08-23** — [9a3ead5](https://github.com/babunidev/amazin/commit/9a3ead5100f246b625093735b635ea6f14fc3809): Inspected diff labels Lua v1.2.4, adds rested-XP reporting and replaces formatted info output with concatenation.
- **2025-09-11** — [79c3265](https://github.com/babunidev/amazin/commit/79c3265e3c193c08b9422e868a5e39d62e522ebf): Inspected diff adds ROAR and LICK to the emote pool.

## Present implementation and interpretation

A stealth-themed emote addon that watches one configured action-bar slot. Pressing that slot may play a random built-in emote after a cooldown, then delegates to the original action. It does not detect successful Stealth casts or actual stealth state. A separate command reports rested XP.

The small interaction gives a stealth-themed action a comic character reaction. This reading follows current source and prior README, not a recovered design discussion. Slot watching avoids dependence on aura/icon detection, but pressing the slot is not proof that Stealth succeeded. Moving or paging action bars can change what the selected slot means.

Chance and cooldown offer two independent controls over frequency. Watch mode helps discover slot numbers, but prints every action while enabled. The addon wraps a global function, so other action-bar addons and load order need a combined test. Historical claims that it works on every locale remain unverified in this pass.

## Evidence and status

Reviewed on 2026-10-26 against `main` at [e96070a](https://github.com/babunidev/amazin/commit/e96070a7cf16ed4605caafaf018a566f74d63207). Current Lua, TOC, README and dated commit history were inspected. Source describes implementation; it does not establish successful operation. Historical intent is reconstructed only where labeled. No in-client test or automated test was executed during this documentation pass.

## Documentation authorship

Babuni.dev retains project authorship and creative direction. AI assistance in this pass inspected files and selected commit diffs, identified inconsistencies and drafted documentation. Historical conversations, personal motives, prior approvals and any earlier AI involvement were not recovered or invented.

## Preserved earlier documentation

The following earlier record is retained verbatim. Statements about unavailable history or pending verification describe that earlier snapshot; the dated evidence above supplements it.

# amazin — development journal

**Author:** Babuni.dev

## Retrospective reading — 2026-10-26

A Vanilla 1.12 stealth-themed emote addon with cooldown, random chance, watched action slot and rested-experience reporting. The inspected material demonstrates a concrete direction: Amazin.lua hooks action-slot use, chooses built-in emotes, stores AmazinDB; README documents /amazin watch, slot, chance, scd, rexp. Stealth is inferred from the watched button rather than a buff/icon, which avoids fragile client aura checks.

This narrative is a reconstruction of the existing source, not a recovered original conversation. It does not establish when or why individual changes were accepted. Babuni.dev retains credit for the work and artistic direction; AI's contribution in this session was to organize and interpret the repository evidence. No in-client test was performed.

## Open verification

README describes version 1.2.4 while the inspected TOC declared 1.1.0; confirm version before release.
