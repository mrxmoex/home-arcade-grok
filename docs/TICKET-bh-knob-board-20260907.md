# TICKET — BH-KNOB-BOARD-20260907 (setup knobs · HAVE vs NEED)

**Repo:** Origin `mrxmoex/home-arcade` · CAPITOL `~/src/wip/private/wife-home-gamebase/`  
**Depends on:** play tip floor `fce60f3` (P0a CLOSED · #62–#64)  
**Status:** PAPER · **Writer refine** of Proto draft · coding CA **HOLD** until Bot-Admin names it · unit ≠ accept · Origin only  
**Law:** Law7 · **setup only — no feel dials** · missing boards = exported consts/tables with **neutral defaults** (= live behavior) · one ticket = one SHA when coded  
**Seats:** Proto draft → **Writer refine (this)** → Bot-Admin CA → App Builder PASS  
**NON-GO:** no product code in this paper pass · no LAN churn · no Wave A physics reopen · no moe dial values · no STORED code SHA · no hub `#game-root:has(.blackhole…)` · no EmulatorJS / ads / accounts

## Intent

One board so moe can turn dials later without hunting magic numbers. **SETUP inventory + scaffold names** — not a feel pass. Neutral default = today’s tip `fce60f3` behavior (identity / no-op).

## Tip floor

`fce60f3` — pull / tiny-tier absorb / survivor phone density+cadence live. Paths under `games/blackhole-absorb/src/` unless noted.

---

## HAVE vs NEED (by lane)

### 1. Collect (XP / pick pacing)

| | Item | Cite |
|--|------|------|
| **HAVE** | `XP_PER_LEVEL=20`, `EARLY_LEVEL_UPS=5`, `EARLY_XP_PER_LEVEL=40`, `xpToNextLevel`, `levelFromXp`, `absorbXp` | `xp.ts` |
| **HAVE** | `EARLY_PICK_WINDOW=3`, `EARLY_DISTINCT_SKILL_CAP=2`, `offerChoices` | `skillOffer.ts` |
| **HAVE** | Overlay: `SKILL_PICK_SCRIM`, `SKILL_PICK_SCRIM_PORTRAIT`, `SKILL_PICK_PORTRAIT_MQ`, `SKILL_PICK_CHOICE_MIN_PX=56` | `skillPick.ts` |
| **NEED** | Optional `COLLECT_KNOBS` (or re-export board) grouping the above — **values unchanged**. No new cadence numbers. |

### 2. Score

| | Item | Cite |
|--|------|------|
| **HAVE** | Bests keys + mass/time climb | `bests.ts` (`BEST_MASS_KEY`, `BEST_TIME_KEY`) |
| **HAVE** | Session metrics: mass, time, eaten, bestMass, bestTime, xp, level | `manifest.ts` / controller metrics |
| **NEED** | Exported **run-score weights / formula table** with neutral defaults that reproduce today’s HUD metrics (no leaderboard, no meta currency). Placeholder ids OK. |

### 3. Feedback (skill / contact punch)

| | Item | Cite |
|--|------|------|
| **HAVE** | Punch: `SKILL_PICK_PUNCH_S`, pulse/sfx ids, verb map | `skillPickPunch.ts` |
| **HAVE** | Stack chrome + FX↔skill tags; mute / reduced-motion gates | `skillStack.ts`, `fxTags.ts`, `contactFeedback.ts` |
| **HAVE** | Tear/core contact scales (integrity / chip) | `contact.ts` (`TEAR_*`, `CORE_*`, `START_INTEGRITY`) |
| **NEED** | Exported **feedback timing/intensity board** (punch duration, ring scale) defaults = current consts. No new VFX system. |

### 4. Classes (enemy) + rare drops

| | Item | Cite |
|--|------|------|
| **HAVE** | `ENEMY_CLASS_IDS`, `ENEMY_CLASSES`, `CLASS_MIX`, `VARIETY_GATE_SEC=90`, `CLASS_PICK_ORDER` | `enemyClasses.ts` |
| **HAVE** | `RARE_DROP_TABLES` by class | `rareDrops.ts` |
| **NEED** | Thin **file-of-record export / alias** only if coding SHA wants one import path — tables already data. Optional: document which rolls feed class vs drop (**no behavior change**). |

### 5. Phone (density + steer)

| | Item | Cite |
|--|------|------|
| **HAVE** | Classic phone: `CLASSIC_PHONE_VIEW_SOFT=480`, `EARLY_SEC=40`, `EARLY_MASS=36`, `LARGE_MUL=0.48`, `DENSITY_MUL=0.64`, `DENSITY_FLOOR=12` | `difficulty.ts` |
| **HAVE** | Survivor phone: `SURVIVOR_PHONE_VIEW_SOFT=480`, `DENSITY_MUL=0.72`, `LARGE_MUL=0.58`, `DENSITY_FLOOR=14` + weight helpers | `difficulty.ts` |
| **HAVE** | Steer feel fine/coarse: `STEER_ACCEL_*`, `STEER_MAX_SPEED_*`, `STEER_DRAG*`, `STEER_FEEL_FINE/COARSE` | `steerFeel.ts` |
| **HAVE** | Grow ease (not phone-only but live): `GROW_EASE_RATE`, `GROW_MAX_PX_PER_S`, `GROW_SNAP_PX` | `world.ts` |
| **NEED** | `PHONE_KNOBS` (+ optional `STEER_KNOBS` re-export) grouping the above — **do not retune**. Setup for later moe dials only. |

### 6. Level packs / long-run pressure

| | Item | Cite |
|--|------|------|
| **HAVE** | Manifest levels `calm` / `deep`; modes survivor / arena / timed / zen | `manifest.ts` |
| **HAVE** | Private `LEVEL_TUNE` calm `{orbTarget:24,speed:1,largeBias:0.15}` · deep `{32,1.25,0.22}` via `tuneForLevel` | `physics.ts` |
| **HAVE** | Mode pressure tables `MODE_DIFFICULTY` + `PRESSURE_CAP=104` + elite gates | `difficulty.ts` |
| **HAVE** | Hub level chrome only (`levelSelect.ts`); play resolves calm unless session seeded | hub |
| **NEED** | **Export `LEVEL_TUNE` / `LEVEL_PACKS` table** — rows: id · orbTarget · speed · largeBias · (optional) bg + enemy-table + spawn-id hooks. Neutral = calm/deep today. Scaffold empty slots for future map-lab packs **without** content fill. Arena = noted testbed — **no Arena rewrite**. |

### 7. Asset → score map (P0c)

| | Item | Cite |
|--|------|------|
| **HAVE** | Class mass/xp scales + rare-drop amounts; skill effects via ranks — **no** single asset→score registry | classes / rareDrops / skills |
| **NEED** | New exported `ASSET_SCORE_MAP` (name flexible): asset/class/drop id → score contribution fields. Neutral zeros **or** current rare-drop amounts. **Scaffold + types this SHA**; wire later. |

### 8. Hub settings (adjacent — do not reinvent)

| | Item | Cite |
|--|------|------|
| **HAVE** | `mute`, `reducedMotion`, `profileName` on `home-arcade:hub-settings` | `packages/save`, `apps/hub/src/settings.ts` |
| **HAVE** | Handicap `gentle` in physics/difficulty scales | `physics.ts` / `difficulty.ts` |
| **NEED** | Out of BH-KNOB-BOARD coding SHA unless Bot-Admin widens — BH-SETTINGS-DIFF (wife translate T2) is a **later** expose-UI ticket. List here so dials don’t fork a second settings store. |

---

## Coding SHA (NOT this paper) — Bot-Admin fire later

Priority align (Bot-Admin warm note):

1. **P0c** — scaffold `ASSET_SCORE_MAP` (+ types); neutral defaults.  
2. **P1** — export `LEVEL_PACKS` / `LEVEL_TUNE` shape (bg + enemy table + spawn ids hooks; empty future rows OK).  
3. Re-export / group **PHONE_KNOBS** (+ steer if named) and optional **COLLECT_KNOBS** / feedback board — values = live tip.  
4. Long-run dials already in `MODE_DIFFICULTY` — export/alias only if still “buried”; **no retune**.  
5. Typecheck + tests · **unit ≠ accept** · no feel retune · no asset art · no STORED · Law7.

## Paper done when

- [x] HAVE vs NEED for collect / score / feedback / classes / phone / level-packs / asset→score (+ hub adjacent)  
- [x] Writer refine (paths + steerFeel / MODE_DIFFICULTY / contact / P0c·P1 coding order)  
- [ ] Bot-Admin paper accept → named coding CA  
- [ ] App Builder PASS on coding PR (later)

## Accept (paper)

Bot-Admin can fire one coding CA from this board without redesign mid-PR. **This file is not a code GO.**

## Cite

Tip `fce60f3` · Proto draft · TIP-NOTEPAD / P0a CLOSED · Law7 · TICKET-11 · TICKET-18 · Wave B cadence/feedback · wife translate BH-SETTINGS-DIFF (later)

## Dual-save

- CAPITOL / Origin: `docs/tickets/TICKET-bh-knob-board-20260907.md`  
- Field-Proto: `traces/TICKET-bh-knob-board-20260907.md`  
- Box artifact (optional): `/workspace/artifacts/TICKET-bh-knob-board-20260907.md`
