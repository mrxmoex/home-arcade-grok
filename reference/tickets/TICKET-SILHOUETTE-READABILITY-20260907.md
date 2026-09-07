# TICKET — SILHOUETTE-READABILITY-20260907 (paper · tell bodies apart)

**Repo:** Origin `mrxmoex/home-arcade` · CAPITOL `~/src/wip/private/wife-home-gamebase/`  
**Kind:** PAPER ONLY · Law7 · **NO CA code** this ticket  
**Tip floor:** `2e21ef3` (BH-SHA2-CADENCE-STILL-HOT on main)  
**Cite live:** `ENEMY_CLASSES` (neutron / matter / gas / void-boost) · `ThreatKind` food/threat/elite · `ASSET_FANTASY_LABELS` · `rareDrops` · `visuals.ts` paint  
**Parked (not this paper):** skilltree · borders@100 code  
**Seats:** Writer paper → Bot-Admin later visual CA · App Builder / Frontend PASS on phone if coded  
**NON-GO:** no feel dials · no Wave A physics reopen · no STORED · no hub `:has()` · no EmulatorJS · no skilltree/borders@100 · Origin only

## Intent

At high spawn volume, wife/moe must **tell bodies apart in one glance**: what is food, what kills, what is loot, what is another hole. Today classes mostly share **circle + inner tint**; ThreatKind adds food/threat/elite paint; fantasy labels are **string keys only** (no sprites). This paper locks readability rules so a later art/visual SHA does not invent a second taxonomy.

## Problem (from live paint)

| Layer | What exists @ tip | Gap at high density |
|-------|-------------------|---------------------|
| Class | `ENEMY_CLASSES` inners + `driftScale` / `massGainScale` | Same disc silhouette; gas/matter/void blur together when small |
| Threat | `ThreatKind` food / threat / elite + elite gold ring | Size still primary; red/amber wash floods portrait |
| Fantasy | `ASSET_FANTASY_LABELS`: collapsed-star · standard-matter · swarm-cloud · void-shard | Labels not drawn — no shape language yet |
| Loot | `rareDrops` keyed by class (crumbs / shards / void bonus) | Drop is on orb or instant — **planted loot** not distinct from gas sparkle |
| Other BH | Hole-vs-hole / absorb path (BH-17) | Occasional other-hole must not read as big food orb |

## Readability rules (design law)

### 1. Orthogonal axes (do not collapse)

Keep **three orthogonal tags** — never overload one color for all meaning:

1. **ThreatKind** → danger grammar (food vs threat vs elite)  
2. **EnemyClassId** → fantasy/role grammar (tank / fuel / swarm / rare-support)  
3. **Loot state** → planted drop vs bare orb (when shown)

If two axes share a cue (e.g. both use green), the third axis must carry **shape or motion**.

### 2. Shape / size / motion / color (per class)

Targets are **phone-LAN readable** at survivor late mix (~VARIETY_GATE_SEC and after). Defaults = tip feel; **no dial numbers in this paper**.

| Class | Fantasy label | Role | Shape cue (proposed) | Size cue | Motion cue | Color cue (have → keep spirit) |
|-------|---------------|------|----------------------|----------|------------|--------------------------------|
| `neutron` | collapsed-star | dense-tank | Heavier disc / slight faceted rim | Reads **bigger mass per radius** (already slow drift) | Slower drift (`driftScale` 0.72) — keep | Cool blue inners (`#7aa0ff` family) |
| `matter` | standard-matter | baseline-fuel | Default circle (baseline) | Baseline | Baseline drift | Cyan food / rose threat / amber elite (current matter inners) |
| `gas` | swarm-cloud | swarm-pressure | **Soft / cloudy edge** or 2–3 micro-lobes — not a hard disc | Prefer **smaller** on-screen for same threat band | Faster drift (1.35) — keep as swarm tell | Lime family — **must not** equal loot sparkle |
| `void-boost` | void-shard | rare-support | **Shard / diamond** or broken ring — rare silhouette | Sparse count (late mix 6%) | Mid drift | Violet family — distinct from tear-core violet if possible |

**Elite ring** (T11 gold) stays ThreatKind elite telegraph — class does **not** invent a second elite language.

### 3. ThreatKind overlay (danger grammar)

| ThreatKind | Must read as | Live cue to preserve | Add only if needed |
|------------|--------------|----------------------|--------------------|
| `food` | Safe / eatable | Class `innerFood` | Soft outline OK; never red |
| `threat` | Danger if bigger | Class `innerThreat` + tear/core zones when bigger | Size literacy > tint flood |
| `elite` | High danger | Gold ring + amber body | Cap wash on small canvas (`senseStrokeAlpha` spirit) |

FAIL-TEACH spirit: red ≠ food; bigger eats you; small black ≠ automatically food.

### 4. Other-BH (occasional)

| Rule | Detail |
|------|--------|
| Silhouette | Other hole = **void disc with event-horizon rim**, not class orb inners |
| Frequency | Occasional — must not dominate spawn soup |
| Contact | Hole-vs-hole grammar stays BH-17 / absorb rules — readability only here |
| Anti-confusion | Never paint other-BH with matter/gas food inners |

### 5. Planted loot vs gas blur

| Rule | Detail |
|------|--------|
| Gas | Swarm body — cloudy, many, fast; **no** sparkle-as-loot |
| Planted loot | When rare drop is visible on field (if/when shown): **glyph or hard spark** on/near orb, tied to `rareDrops` id (`gas-shard`, `matter-crumb`, `neutron-crumb`, `void-pull` / `void-crumb`) |
| Timing | Prefer telegraph **before** absorb if drop is “planted”; instant-on-eat can stay invisible |
| Anti-blur | Gas elite lime ≠ void-shard violet ≠ loot spark white/gold |

## Mapping to live data (cite only)

- Classes: `games/blackhole-absorb/src/enemyClasses.ts` — `ENEMY_CLASSES`, `CLASS_MIX`, `VARIETY_GATE_SEC`  
- Threat: `difficulty.ts` — `ThreatKind`  
- Fantasy keys: `assetScoreMap.ts` — `ASSET_FANTASY_LABELS` / `fantasyLabelFor`  
- Loot tables: `rareDrops.ts` — `RARE_DROP_TABLES`  
- Paint: `visuals.ts` — class inners, elite ring, tear/core zones  

## Later coding SHA (NOT this paper)

When Bot-Admin names a visual CA:

1. Apply shape/motion/color rules above without retuning spawn counts / XP / Wave A physics.  
2. Optional planted-loot glyph path keyed to `rareDrops` ids.  
3. Other-BH rim distinct from orbs.  
4. Phone LAN check · unit ≠ accept · App Builder/Frontend PASS.  

**Out:** skilltree · borders@100 · dial turns · new classes · meta currency.

## Done when (paper)

- [x] Orthogonal axes + per-class shape/size/motion/color rules  
- [x] Other-BH + planted-loot vs gas blur called out  
- [x] Live cites @ tip `2e21ef3`  
- [x] Law7 · no CA code · parked skilltree/borders@100  
- [ ] Bot-Admin accept → named visual CA (separate)

## Accept

One portrait survivor late-field glance: food / threat / elite still clear **and** neutron / matter / gas / void-boost tell apart without reading HUD. Unit ≠ accept.

## Dual-save

- CAPITOL / Origin: `docs/tickets/TICKET-SILHOUETTE-READABILITY-20260907.md`  
- Field-Proto: `traces/TICKET-SILHOUETTE-READABILITY-20260907.md`
