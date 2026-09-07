# TICKET — CELESTIAL-STATIONARY-20260907 (paper · big body / orbit eat)

**Repo:** Origin `mrxmoex/home-arcade` · CAPITOL `~/src/wip/private/wife-home-gamebase/`  
**Kind:** PAPER ONLY · Law7 · **NO CA code**  
**Tip floor:** `0d01afd` · mint: marks-integrity-poke  
**Cite:** `ENEMY_CLASSES` / `ThreatKind` / `rareDrops` / level-pack hooks · silhouette readability paper  
**Parked:** skilltree  
**NON-GO:** no implement · no Arena rewrite as sneak-in · no dial turns · Origin only

## Intent

Add a **big stationary celestial** (planet / star / station) that structures a pocket of the field: player eats **surrounding / orbit fodder** before an **optional boss** engage. Size classes gate **drop quality**. Note path for **growing NPC enemies** later — not in V1 of this feature.

## Fantasy sketch

| Beat | Player reads |
|------|----------------|
| Approach | Huge body, nearly still (drift ≈ 0) — not a normal orb |
| Orbit layer | Moons / debris / class-tagged fodder circling or ring-spawned |
| Optional boss | Core engage only after orbit cleared or timer/HP gate |
| Reward | Drop quality scales with celestial **size class** |

## Size classes → drop quality (design table)

| Size class (id) | Scale vs player (spirit) | Orbit density | Drop quality band | Boss? |
|-----------------|--------------------------|---------------|-------------------|-------|
| `celestial-s` | Large landmark | Light ring | Common crumbs (`matter-crumb` spirit) | Optional skip |
| `celestial-m` | Screen-anchor | Medium ring | Mid crumbs / xp shards | Optional |
| `celestial-l` | Multi-screen threat | Heavy ring | High / void-support table spirit | Recommended |
| `celestial-xl` | Set-piece | Dense + elites | Boss table + rare bonus | Yes |

Map onto existing `rareDrops` kinds (mass / xp / bonus) — **new table rows later**, not a second currency.

## Systems touch (paper only)

| System | Hook |
|--------|------|
| Spawn | Authored or rare roll — not full T11 pressure owner |
| Class/threat | Orbit fodder still uses `EnemyClassId` × `ThreatKind` |
| Level pack | Optional `enemyTableRef` / spawn curve override for pocket |
| Silhouette | Stationary body ≠ gas swarm ≠ other-BH (rim/horizon language) |
| Integrity | Boss tear/core may chip integrity — regen paper is separate |

## Growing NPC enemies (note only)

Later plane: orbit NPCs that **gain mass over time** or when fed — not V1 celestial. Keep as backlog flag so boss design does not pretend NPCs are static forever.

## Done when (paper)

- [x] Stationary body + orbit-before-boss loop named  
- [x] Size class → drop quality bands  
- [x] Growing NPC note parked  
- [ ] Bot-Admin GO → implement ticket (separate)

## Accept

One set-piece readable on phone: big still body, orbit food, optional scary core. Skilltree PARKED.

## Dual-save

`docs/tickets/TICKET-CELESTIAL-STATIONARY-20260907.md` · Field-Proto `traces/` twin
