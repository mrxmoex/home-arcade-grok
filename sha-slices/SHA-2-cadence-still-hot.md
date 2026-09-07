# SHA-2 — cadence still hot after SHA-1

**From:** `sessions/2026-09-07-post-sha1-poke/SESSION.md`  
**Tip base:** `1bd6f1e`  
**Keep:** density SHA-1 (crowding GOOD)  
**Problem:** skill picks still too quick with many orbs on field.

## Proposed dials (tune in CA if tests need)

Hypothesis: orb *count* floods XP — raise costs harder and/or cut absorb XP coef.

| Knob | SHA-1 now | Proposed |
|------|-----------|----------|
| `XP_PER_LEVEL` | 40 | **80** |
| `EARLY_XP_PER_LEVEL` | 60 | **100** |
| `EARLY_LEVEL_UPS` | 8 | **10** |
| `XP_PER_LEVEL_CAP` | 120 | **200** |
| post-early grow step | +10/level | **+15/level** |
| `ABSORB_XP_SIZE_COEF` (if live) | (check tip) | **cut ~30–40%** if still spam after cost raise |

## Hold

Density knobs · vacuum · tear · skilltree code · borders@100 system.

## Done when

One PR · tests lock new numbers · no Law7 dump · cite this slice + poke session.
