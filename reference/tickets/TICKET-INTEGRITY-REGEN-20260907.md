# TICKET — INTEGRITY-REGEN-20260907 (paper · regain design)

**Repo:** Origin `mrxmoex/home-arcade` · CAPITOL `~/src/wip/private/wife-home-gamebase/`  
**Kind:** PAPER ONLY · Law7 · **NO CA code**  
**Tip floor:** `0d01afd` (BH-TEAR-COLLISION-BLINK) · mint: marks-integrity-poke  
**Cite HAVE:** integrity HUD · tear chip · `START_INTEGRITY` / `TEAR_HP_CHIP` / `applyTearChip` · `hud-integrity` / `hud-tear-chip`  
**Parked:** skilltree  
**NON-GO:** no implement · no Wave A physics reopen · no STORED · no hub `:has()` · Origin only

## Intent

Integrity today only **goes down** (tear chips → Torn at 0). Design **regain** so long runs are not a one-way drain. This paper names knobs only — **no values, no code**.

## HAVE (live @ tip)

| Piece | Cite |
|-------|------|
| Start pool | `contact.ts` `START_INTEGRITY = 100` |
| Tear damage | `TEAR_HP_CHIP` (+ survivor scale via `survivorTearHpScale`) · `applyTearChip` |
| Exhaust | `isIntegrityExhausted` → finish `tear-exhaust` / overlay Torn |
| HUD | `.hud-integrity` shows rounded integrity; `.hud-tear-chip` pulse on chip |
| I-frames | `TEAR_IFRAMES_S` after chip |
| Feedback | tear flash / blink raised @ `0d01afd` |

No regen path exists today.

## Regain channels (design · pick later)

Three channels — may combine; Bot-Admin chooses which ship first.

### A. Over time (`INTEGRITY_REGEN_OVER_TIME`)

| Knob name (export later) | Role |
|--------------------------|------|
| `INTEGRITY_REGEN_PER_SEC` | Passive while alive / not in i-frames |
| `INTEGRITY_REGEN_DELAY_S` | Pause after last tear before regen starts |
| `INTEGRITY_REGEN_CAP` | Ceiling (usually `START_INTEGRITY`) |
| `INTEGRITY_REGEN_PAUSE_ON_PICK` | Whether skill-pick pause freezes regen |

### B. Collectibles (`INTEGRITY_REGEN_COLLECT`)

| Knob name | Role |
|-----------|------|
| `INTEGRITY_PICKUP_HEAL` | Integrity restored per pickup |
| `INTEGRITY_PICKUP_SPAWN_WEIGHT` | How often heal orbs appear (data table row) |
| `INTEGRITY_PICKUP_CLASS_REF` | Optional tie to class/loot id (not gas blur — see silhouette paper) |

Prefer distinct silhouette from gas / planted score loot.

### C. On level-up (`INTEGRITY_REGEN_LEVEL_UP`)

| Knob name | Role |
|-----------|------|
| `INTEGRITY_ON_LEVEL_UP` | Flat heal when skill level increases |
| `INTEGRITY_ON_LEVEL_UP_FRAC` | Alternate: fraction of missing integrity |
| `INTEGRITY_ON_LEVEL_UP_ONLY_SURVIVOR` | Mode gate |

Pairs with existing XP / pick cadence — **do not** retune XP knobs here.

## Done when (paper)

- [x] HAVE integrity HUD/tear chip cited  
- [x] Three regain channels + knob names only  
- [ ] Bot-Admin pick channel(s) → named CA (separate)

## Accept

Design is enough to implement one channel without inventing a second HP system. Skilltree PARKED.

## Dual-save

`docs/tickets/TICKET-INTEGRITY-REGEN-20260907.md` · Field-Proto `traces/` twin
