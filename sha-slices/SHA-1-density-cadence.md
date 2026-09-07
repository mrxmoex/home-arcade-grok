# SHA-1 — phone density + skill cadence

**From:** `sessions/2026-09-07-bh-knobs/SESSION.md`  
**Scope:** Survival feel only · one Origin PR · one SHA  
**Base tip:** Origin `18bd548` (ALL-IN SETUP)  
**Laws:** Law7 · unit≠accept · no new systems · dial values only

## Deltas (apply these)

| Knob | Current | Proposed |
|------|---------|----------|
| `SURVIVOR_PHONE_DENSITY_MUL` | 0.72 | **0.60** |
| `SURVIVOR_PHONE_DENSITY_FLOOR` | 14 | **11** |
| `SURVIVOR_PHONE_LARGE_MUL` | 0.58 | **0.52** |
| `XP_PER_LEVEL` | 20 | **40** |
| `EARLY_XP_PER_LEVEL` | 40 | **60** |
| `EARLY_LEVEL_UPS` | 5 | **8** |
| `xpToNextLevel` | flat 20 after early | **grow after early** (use existing helper; add a sane cap if none) |

## Hold this SHA

- `SURVIVOR_PHONE_VIEW_SOFT`
- tear chip amounts
- vacuum target set
- massWeight / xpWeight / skillWeight
- LevelPack rows / Arena
- any new RNG / spawn-director

## Done when

- Typecheck + package tests green
- Defaults in tests updated to the new numbers (feel lock = new dial, not old)
- PR body cites session + this sha-slice
- No hub CSS / Law7 violations

## Later (not this PR)

tiny absorb loosen · collision blink · vacuum food+loot · rare plant · pack deep/idle rows · Arena-fixed
