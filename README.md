# Amazin

**Author:** Babuni.dev

A stealth-themed emote addon that watches one configured action-bar slot. Pressing that slot may play a random built-in emote after a cooldown, then delegates to the original action. It does not detect successful Stealth casts or actual stealth state. A separate command reports rested XP.

## Installation and use

Install `Amazin.lua` and `Amazin.toc` under `Interface/AddOns/Amazin/`, restart the client and enable it. Run `/amazin watch`, press the intended button, note its slot, set `/amazin slot <n>`, then toggle watch off.

| Command | Source behavior |
| --- | --- |
| `/amazin slot <n>` | Saves watched numeric slot |
| `/amazin watch` | Toggles local slot reports |
| `/amazin chance <0-100>` | Sets probability; default 100% |
| `/amazin scd <0-60>` | Sets cooldown seconds; default 6 |
| `/amazin rexp` | Reports rested XP and rounded bubbles, capped at 30 |
| `/amazin info` | Shows slot, chance, cooldown and pool size |
| `/amazin reset` | Clears only the watched slot |
| `/amazin save` | Copies current settings to the DB |

**Version discrepancy:** Lua labels itself v1.2.4; the actual TOC declares v1.1.0. TOC notes list obsolete commands including `emote`, `stealth`, `debug` and omit `rexp`. This documentation records the discrepancy without modifying metadata. The [historical README](docs/HISTORICAL_README.md) includes a suggested v1.2.4 TOC block, not the committed manifest.

## Limitations and verification

- Resolve Lua v1.2.4 versus TOC v1.1.0 and stale TOC command descriptions before a release; do not silently choose a version.
- Verify 1.12 event callback conventions, login/logout persistence and logout before lazy hydration.
- Check watched-slot presses with failed casts, bar paging and another UseAction wrapper.
- Exercise 0%/100% chance, cooldown boundaries, startup uptime, reset and rested-XP edge cases.
- Validate all 12 built-in tokens and fallback behavior on intended locales; prior README compatibility claims are not test results.

## Evidence and status

Reviewed on 2026-10-26 against `main` at [e96070a](https://github.com/babunidev/amazin/commit/e96070a7cf16ed4605caafaf018a566f74d63207). Current Lua, TOC, README and dated commit history were inspected. Source describes implementation; it does not establish successful operation. Historical intent is reconstructed only where labeled. No in-client test or automated test was executed during this documentation pass.

## Documentation

- [Concept](CONCEPT.md) · [Design](docs/DESIGN.md) · [Content](docs/CONTENT.md)
- [Architecture](docs/ARCHITECTURE.md) · [Decisions](docs/DECISIONS.md)
- [Roadmap](ROADMAP.md) · [Changelog](CHANGELOG.md) · [Development journal](docs/DEVLOG.md)
- [AI collaboration](docs/AI_COLLABORATION.md) · [Contributor instructions](AGENTS.md)

The [historical README](docs/HISTORICAL_README.md) is retained verbatim as prior documentation, including any outdated claims. Current source and the qualifications above take precedence.
