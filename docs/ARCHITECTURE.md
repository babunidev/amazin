# amazin — architecture

**Project author and creative direction:** Babuni.dev

The file captures `UseAction` in `_Orig_UseAction` and replaces it with a wrapper. Every invocation lazily calls `ensureLoaded()`, optionally prints a watched slot, and calls `doStealthEmoteNow()` when the slot matches. The original action is invoked afterward with its original arguments.

`doStealthEmoteNow()` compares `GetTime()` with `LAST_STEALTH_EMOTE_TIME`, then records the time **before** the chance roll. Thus an unsuccessful roll still consumes the cooldown. Selection uses `table.getn` and `math.random`; `DoEmote` has a German text fallback. `LAST_STEALTH_EMOTE_TIME` starts at zero, so initial eligibility depends on client uptime.

`AmazinDB` is declared account-wide in the TOC, holding `slot`, `stealth_chance`, `stealth_cd`. Watch mode and last-emote time are transient. `PLAYER_LOGIN` seeds randomness and `PLAYER_LOGOUT` copies current settings. Lazy hydration occurs on action use or a slash command; logout before hydration should be checked for overwriting saved settings with defaults. There is no per-frame loop or automated test file.

## Evidence and status

Reviewed on 2026-10-26 against `main` at [e96070a](https://github.com/babunidev/amazin/commit/e96070a7cf16ed4605caafaf018a566f74d63207). Current Lua, TOC, README and dated commit history were inspected. Source describes implementation; it does not establish successful operation. Historical intent is reconstructed only where labeled. No in-client test or automated test was executed during this documentation pass.

## Preserved earlier documentation

The following earlier record is retained verbatim. Statements about unavailable history or pending verification describe that earlier snapshot; the dated evidence above supplements it.

# amazin — architecture

**Author:** Babuni.dev

Amazin.lua hooks action-slot use, chooses built-in emotes, stores AmazinDB; README documents /amazin watch, slot, chance, scd, rexp.

Evidence: README.md, main addon Lua file and .toc manifest. Code inspection describes implementation intent, not verified behavior on a running client.
