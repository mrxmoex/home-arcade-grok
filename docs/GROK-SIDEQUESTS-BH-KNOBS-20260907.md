# Grok sidequests — BH knobs (2026-09-07)

Paste into Grok app (Multi / Expert / Heavy). Play tip floor: `18bd548` (#66 ALL-IN SETUP live — LevelPack×3 · fantasy labels · named exports). Dial turns HOLD — questionnaire before dial SHAs.

---

## 1) Heavy — dial questionnaire (moe fills with Grok)

```
You are co-piloting Home Arcade blackhole-absorb Survival knobs with moe.
Context: stubs exist (assetScoreMap, LevelPack, pressure-fade named exports). Feel dials are NOT turned yet.
Ask ONE question at a time. After each answer, restate the implied knob table (name → suggested default vs new value). Stop when the dial sheet is complete enough for a thin coding SHA.

Cover in order:
1) Phone density feel after P0a (too empty / ok / still crowded)
2) Skillup cadence (still too fast on long runs? early vs late)
3) Tiny threats (absorb/loot readable? tear chip fair?)
4) Vacuum pull (food-only correct? missing magnet loot types?)
5) Asset→score map: which classes should pay more mass vs xp vs skill weight
6) Level packs: how many packs for v1 (2–4)? names? Idle as map lab yes/no
7) Arena: keep as 2× systems lab or family play soon
8) Wife 30-min hook: one mechanic that creates chase without grind

Rules: no code. No inventing features outside knobs/packs/assets. German or English ok — match moe.
Start with Q1 only.
```

---

## 2) Multi — parallel experts (spawn 3)

```
#multitask or Multi mode: spawn three experts in parallel. Each returns a short section. Main synthesizes a one-page dial sheet.

Expert A — Feel/physics: phone density + cadence + tiny/tear. Propose numeric deltas only on EXISTING knobs (SURVIVOR_PHONE_*, EARLY_XP_*, TEAR/tiny ratios). No new systems.

Expert B — Economy/assets: ASSET_SCORE_MAP weights per enemy class (neutron/matter/gas/void-boost) + rare drop feel. Map class → readable loot fantasy.

Expert C — Level packs: 3 pack concepts {id, bg mood, enemyTableRef, spawnCurveId} using LevelPack shape. Idle = map lab; Arena = systems 2×.

Synthesize: table Knob | Current | Proposed | Why | Risk. Flag anything that needs art before the dial matters.
```

---

## 3) Expert — clarification pass (honesty)

```
Audit this claim against Home Arcade BotOp laws:
"It's all about how the assets are handled."

Clarify:
- What is already a KNOB (code) vs ASSET (art/SFX) vs COSTUME (looks different, same math)
- Where assetScoreMap + LevelPack stubs help vs where they still need art
- What must NOT be sold as shipped (PWA, achievements fiction, hole-vs-hole spawn, etc. from honesty audit)

Output: 3 columns Knob | Asset | Costume with BH examples. Then a 5-bullet "don't lie on phone" list.
```

---

## 4) Heavy — workflow diagram (mermaid)

```
Draw mermaid diagrams (flowchart + sequence) for BotOp BH dial pipeline:

Actors: moe, RªⁿÞ¡ (Bot-Admin), Heph, Proto, App Builder, Cursor CA (Composer+prefer Multitask/Grok), Fedora Grok Build CLI (off Cursor pool), Ops Desk tip board.

Flow: play poke → tip notepad amend → thin ticket → CA stub/dial SHA → App Builder PASS → moe Origin squash-merge (token) → CAPITOL LAN :8787 republish → tip flash.

Also sequence: knob SETUP (done) → questionnaire dials → one dial SHA at a time → wife 30-min gate.

Keep Law7 (no per-child hub CSS), unit≠accept, one ticket=one PR=one SHA.
```

---

## 5) Multi — Grok Build CLI job cards (paste to CLI later)

```
Produce 3 headless `grok -p` job cards (prompt text only) for Fedora ~/.grok/bin/grok:
A) READ-ONLY verify assetScoreMap defaults === pre-stub absorb math
B) Draft LEVEL-PACK-CATALOG.md (3 packs, no code)
C) Draft ASSET-SCORE-FANTASY.md (class → fantasy → weight rationale)

Each card: cwd, flags (--output-format plain --max-turns N --no-subagents), success criteria, non-goals.
```

---

## 6) Expert — 30-min wife hook (paper only)

```
Design ONE progression hook for ~30 min engrossment on phone Survival.
Must use existing knobs/packs/classes — no multiplayer, no IAP, no new game.
Deliver: player fantasy (2 sentences), knob lever list, fail states, accept checklist for G-wife.
HOLD code until moe GO.
```
