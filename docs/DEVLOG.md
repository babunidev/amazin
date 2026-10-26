# amazin — development journal

**Author:** Babuni.dev

## Retrospective reading — 2026-10-26

A Vanilla 1.12 stealth-themed emote addon with cooldown, random chance, watched action slot and rested-experience reporting. The inspected material demonstrates a concrete direction: Amazin.lua hooks action-slot use, chooses built-in emotes, stores AmazinDB; README documents /amazin watch, slot, chance, scd, rexp. Stealth is inferred from the watched button rather than a buff/icon, which avoids fragile client aura checks.

This narrative is a reconstruction of the existing source, not a recovered original conversation. It does not establish when or why individual changes were accepted. Babuni.dev retains credit for the work and artistic direction; AI's contribution in this session was to organize and interpret the repository evidence. No in-client test was performed.

## Open verification

README describes version 1.2.4 while the inspected TOC declared 1.1.0; confirm version before release.
