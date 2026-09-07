# TICKET — LEVEL-PACK-CATALOG-20260907 (paper · catalog after stub)

**Repo:** Origin `mrxmoex/home-arcade` · CAPITOL `~/src/wip/private/wife-home-gamebase/`  
**Kind:** PAPER ONLY · catalog / fantasy plan · **dials HOLD** · no code in this ticket  
**Tip floor:** `74cf37c` (knob stubs — `levelPack.ts` + `assetScoreMap.ts`)  
**Cite:** knob board SoT Field-Proto `e801bbb` · home-arcade docs `7677646` · `TICKET-bh-knob-board-20260907.md` §6  
**Seats:** Writer paper → Bot-Admin later content/CA · App Builder PASS if UI  
**NON-GO:** no dial turns · no Arena rewrite · no Idle UI · no Wave A physics reopen · no STORED · no hub `:has()` · Origin only

## Intent

Code stub shipped at `74cf37c`: `LevelPack { id, bg, enemyTableRef, spawnCurveId }`. This paper **catalogs** live packs + empty fantasy slots so content can fill without redesigning the shape. **Do not turn dials here.**

## HAVE (live @ tip)

| Pack / path | Shape | Notes |
|-------------|-------|-------|
| `DEFAULT_SURVIVOR_LEVEL_PACK` | `id: survivor-calm-default`, `bg: calm`, `enemyTableRef: enemy-classes-default`, `spawnCurveId: survivor` | Survivor always resolves here; gameplay still calm tune/palette |
| Session-level synthetic pack | `id: level-<sessionLevelId>`, `bg: sessionLevelId`, default enemy table, `spawnCurveId: modeKind` | Non-survivor when session seeds a level |
| Manifest levels | `calm`, `deep` | Hub chrome; unlock stub deep←calm mass |
| Manifest modes | classic · survivor · timed-swarm · zen · beam-arena | Arena uses `arenaChamber`, **not** this table (comment in `levelPack.ts`) |
| Pressure curves | `MODE_DIFFICULTY.*` + named fade coefs | Referenced by `spawnCurveId` |

Cite: `games/blackhole-absorb/src/levelPack.ts`, `manifest.ts`, `difficulty.ts`, `physics.ts` `LEVEL_TUNE` / `tuneForLevel`.

## Catalog slots (fantasy · empty / later)

| Slot id (proposed) | bg | enemyTableRef | spawnCurveId | Status |
|--------------------|-----|---------------|--------------|--------|
| `survivor-calm-default` | calm | enemy-classes-default | survivor | **LIVE** |
| `survivor-deep` | deep | enemy-classes-default (or deep mix later) | survivor | **EMPTY** — deep palette only when GO |
| `classic-calm` | calm | enemy-classes-default | classic | **EMPTY** — classic still session/legacy path |
| `idle-*` | TBD | TBD | TBD | **PARK** — Idle hook comment only |
| `arena-*` | — | — | — | **OUT** — chamber packs, not this table |

Future rows may add: bg art key · music · spawn seed · class-mix override — **schema widen needs Bot-Admin GO**.

## Done when (paper)

- [x] Live pack + empty slots listed  
- [x] Arena/Idle boundaries explicit  
- [x] Dials HOLD stamped  
- [ ] Bot-Admin accept → content fill or coding widen (separate tickets)

## Accept

Catalog is enough to fill one pack row without reshaping `LevelPack`. **No dial values in this paper.**

## Dual-save

- `docs/tickets/TICKET-LEVEL-PACK-CATALOG-20260907.md`  
- Field-Proto `traces/TICKET-LEVEL-PACK-CATALOG-20260907.md`
