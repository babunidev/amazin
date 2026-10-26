# amazin — content inventory

**Project author and creative direction:** Babuni.dev

The current 12-token pool is `ROFL`, `LAUGH`, `GIGGLE`, `STARE`, `GRIN`, `SMIRK`, `CHUCKLE`, `WINK`, `SHUSH`, `SNICKER`, `ROAR`, `LICK`. The older README listed only ten. These are built-in WoW emote identifiers, not original animation assets. The fallback is the German text `kichert leise...` sent as EMOTE.

Other text includes the blue `Amazin:` prefix, command help, slot/chance/cooldown status and rested-XP reports. `rexp` calculates `floor(restedXP * 20 / maxXP + 0.5)` and caps at 30; missing exhaustion or zero XP maximum produces a local message. Token availability and localization require client tests.

Game names and built-in game content remain separate from project authorship. No source strings or assets were changed in this documentation pass.
