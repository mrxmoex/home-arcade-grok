# TICKET — WARP-LAYER-20260907 (paper · screenwarp / warphole options)

**Repo:** Origin `mrxmoex/home-arcade` · CAPITOL `~/src/wip/private/wife-home-gamebase/`  
**Kind:** PAPER ONLY · Law7 · **NO CA code** · options only  
**Tip floor:** `0d01afd` · mint: marks-integrity-poke  
**Cite:** level-pack `bg` / `spawnCurveId` · modes · run-end / skill-pick pause patterns  
**Parked:** skilltree  
**NON-GO:** no implement · no hub mode sheet row yet · no EmulatorJS · Origin only

## Intent

Explore **screenwarp / warphole** as a layer switch for **boss pockets** or **level-up moments** — without implementing. Pick one option later; do not ship all.

## Options (choose later)

### Option W1 — Boss warphole (spatial)

| | |
|--|--|
| Trigger | Rare void-looking hole or celestial core interact |
| Effect | Brief warp VFX → load boss pocket (celestial paper) or Fixed-chamber-like arena |
| Exit | Boss clear / fail / voluntary eject → return to prior field seed |
| Pros | Clear fantasy; contains boss pressure |
| Cons | State save of field; phone perf |

### Option W2 — Level-up layer flash (temporal)

| | |
|--|--|
| Trigger | On skill level-up (after or instead of full pick overlay weight) |
| Effect | Short warp chrome → “layer N” tint / pack `bg` swap · same run continuity |
| Exit | Automatic after pick resolves |
| Pros | Cheap; ties to existing cadence |
| Cons | Must not feel like death; reduced-motion path required |

### Option W3 — Soft screenwarp only (presentation)

| | |
|--|--|
| Trigger | Boss telegraph or last-pick / run-end beat |
| Effect | Camera/shader warp **without** world swap |
| Exit | N/A |
| Pros | Lowest risk; helps readability |
| Cons | No real layer gameplay |

### Option W4 — Pack swap mid-run (data)

| | |
|--|--|
| Trigger | Authored gate (mass / time / celestial clear) |
| Effect | `resolveLevelPack` → new `LevelPack` row (`bg`, `enemyTableRef`, `spawnCurveId`) |
| Exit | Sticky until next gate or run end |
| Pros | Reuses tip `levelPack.ts` shape |
| Cons | Needs catalog rows; test matrix grows |

## Shared laws (all options)

- Pause-safe with skill-pick / death overlays  
- `reducedMotion` / mute: warp is optional chrome, not required for fairness  
- No second skilltree UI  
- Integrity / tear rules unchanged unless Bot-Admin ties regen/heal to warp exit  

## Done when (paper)

- [x] ≥3 concrete options (W1–W4) with trigger/effect/exit  
- [x] Link to celestial + level-pack without requiring them  
- [ ] Bot-Admin pick option → implement ticket (separate)

## Accept

Bot-Admin can name W1/W2/W3/W4 without redesigning mid-PR. **No implement in this paper.**

## Dual-save

`docs/tickets/TICKET-WARP-LAYER-20260907.md` · Field-Proto `traces/` twin
