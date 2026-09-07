# TICKET — ASSET-SCORE-FANTASY-20260907 (paper · fantasy after stub)

**Repo:** Origin `mrxmoex/home-arcade` · CAPITOL `~/src/wip/private/wife-home-gamebase/`  
**Kind:** PAPER ONLY · fantasy / content map · **dials HOLD** · no code in this ticket  
**Tip floor:** `74cf37c` (knob stubs — `assetScoreMap.ts` wired on absorb)  
**Cite:** knob board SoT Field-Proto `e801bbb` · home-arcade docs `7677646` · `TICKET-bh-knob-board-20260907.md` §7 P0c  
**Seats:** Writer paper → Bot-Admin later content/CA · App Builder PASS if chrome  
**NON-GO:** no dial turns · no new meta currency · no leaderboard · no rareDrops rewrite · no Wave A reopen · no STORED · Origin only

## Intent

Code stub shipped at `74cf37c`: per-class `ASSET_SCORE_MAP` with `massWeight` / `xpWeight` / `skillWeight`. Defaults lock to current feel (`massWeight` ≡ `classMassGainScale`; XP/skill weights = 1; rare drops still additive in `rareDrops.ts`). This paper sketches **fantasy fill** (what assets mean to score) without turning knobs.

## HAVE (live @ tip)

| Class id | massWeight | xpWeight | skillWeight | Fantasy read (neutral today) |
|----------|------------|----------|-------------|------------------------------|
| `neutron` | 1.55 | 1 | 1 | Dense tank — more mass per eat |
| `matter` | 1 | 1 | 1 | Baseline fuel |
| `gas` | 0.55 | 1 | 1 | Swarm pressure — lighter mass |
| `void-boost` | 0.85 | 1 | 1 | Rare-support class |

Cite: `games/blackhole-absorb/src/assetScoreMap.ts`, `enemyClasses.ts`, `rareDrops.ts`, controller absorb path.

## Fantasy lanes (later · dials HOLD)

| Lane | Idea | Maps onto | Status |
|------|------|-----------|--------|
| Class mass skew | Family “food vs rock” readability | `massWeight` | LIVE defaults — **do not retune here** |
| Class XP skew | Prefer eating X for level pace | `xpWeight` | All 1 — fantasy only until GO |
| Skill-offer hint | Class eats bias future offers | `skillWeight` | All 1 — unused in offer today |
| Named assets | Silhouette/OSS ids → score row | Extend map beyond class ids | **EMPTY** — needs schema GO |
| Rare-drop bridge | Drop id → score fields | Keep `rareDrops.ts` additive | **HOLD** — do not merge tables blindly |
| Funny absorbables | Wife W8 cast | Asset ids + weights | Wave C / ABSORB-CAST — not this paper’s code |

## Done when (paper)

- [x] Live class rows documented  
- [x] Fantasy lanes named without dial values  
- [x] Rare-drop boundary explicit  
- [ ] Bot-Admin accept → dial GO or asset-id schema ticket (separate)

## Accept

Fantasy map is enough to brief one content pass without changing numbers. **Dials HOLD.**

## Dual-save

- `docs/tickets/TICKET-ASSET-SCORE-FANTASY-20260907.md`  
- Field-Proto `traces/TICKET-ASSET-SCORE-FANTASY-20260907.md`
