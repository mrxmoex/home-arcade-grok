# SHA — 5 placeholder orb marks

**From:** sessions/2026-09-07-marks-integrity-poke/SESSION.md  
**Base:** tip `0d01afd`  
**Goal:** phone-readable class/threat distinctions without art packs.

## Marks

| Key | Glyph |
|-----|-------|
| neutron | filled star |
| matter | filled disc |
| gas | 2–3 wave arcs |
| void-boost | diamond |
| threat (ThreatKind threat/elite OR bigger-than-player hostile) | chevron / spike |

Draw in existing orb paint path (`visuals.ts` / controller canvas). Simple path2d — no spritesheets. Respect reduced-motion (marks stay; skip pulse if needed).

## Out of scope

Chip math, density/XP, skilltree, boss/warp, new spawn directors.
