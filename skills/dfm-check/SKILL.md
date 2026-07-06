---
name: dfm-check
description: Design-for-manufacturability review for injection-molded plastic parts. Use when the user shares a part design, CAD description, or product idea headed for injection molding, before they pay for tooling.
---

# DFM Check — catch it before you pay for steel

A mold change after cutting steel costs 10–100× the same change on a screen.
Your job: review the design like a tooling engineer who has to quote it, and return
a written DFM report.

## What to ask for first (if not provided)

1. Part geometry: dimensions, or the CAD/screenshots/description you can get
2. Material (or intended use → you propose material)
3. Expected annual volume (drives cavity count and tooling class)
4. Cosmetic requirements: visible surfaces? gloss? texture?
5. Any mating parts / assembly method (snap fit, screws, ultrasonic welding)

## Review checklist — run every item

### Walls
- Typical wall thickness: **ABS/PC 1.5–3.0 mm, PP 1.0–2.5 mm**. Below 1.0 mm expect
  filling problems; above 3.5 mm expect sink marks and long cycle times.
- Uniformity beats thickness: keep variation within **±10–15%** of nominal. Sudden
  thick-to-thin transitions → sink, warp, voids. Core out thick sections.

### Draft
- Minimum **1° per side** on untextured walls; add roughly **1° per 0.025 mm of
  texture depth** (medium texture typically needs 3°+).
- Zero-draft faces are possible but cost you: hand-polishing, ejection marks, slower cycles.

### Ribs & bosses
- Rib thickness ≤ **60% of adjoining wall** (prevents sink on the cosmetic side);
  rib height ≤ 3× wall thickness; add 0.5–1° draft on ribs.
- Bosses: not free-standing when avoidable — tie to walls with gussets. Boss OD ≈ 2×
  the screw/insert diameter. Core them properly; a solid boss is a sink mark generator.

### Undercuts
- Every undercut = a slider, lifter, or hand-loaded insert = tooling cost + cycle time +
  a wear item. Ask for each one: *can this feature move to the parting line, or be
  redesigned as a pass-through?*
- Snap fits often CAN be molded without sliders using pass-through cores — flag when applicable.

### Tolerances
- Realistic general tolerance for injection molding: **±0.1–0.2 mm** on small features;
  tighter is quotable but priced accordingly. Anything specified at ±0.02 mm on a plastic
  drawing signals an inexperienced designer to the factory — and invites padded quotes.
- Critical-to-function dimensions: mark them explicitly (and only them).

### Surfaces & appearance
- Parting line and gate location: they WILL be visible somewhere. Decide where, on
  purpose, before the toolmaker decides for you.
- High-gloss cosmetic faces: specify mold steel and polish grade up front (see mold-quote skill).

### Material notes
- ABS: cheap, tough, paints well, yellows in UV. PC: strong, clear-capable, stress-cracks
  with wrong chemicals. PP: cheap, chemical-proof, living hinges — but shrinks ~1.5–2%
  and warps if ribbed badly. TPU/TPE overmolding: adds a second shot or second tool.
- Food/drink contact → flag FDA/LFGB/GB 4806 requirements early (see compliance skill).

## Output format

Produce a **DFM Report** with three sections:
1. **Blockers** — will fail or can't be molded as drawn (each with the fix)
2. **Cost drivers** — moldable but expensive (undercuts, zero draft, tight tolerances),
   each with the cheaper alternative
3. **Fine** — what's already production-ready, so the user knows what not to touch

Close with the three questions the user's toolmaker will ask that the design doesn't
answer yet.

⚠️ All numbers above are industry starting points. Resin datasheets and the toolmaker's
feedback on YOUR geometry are the final word.
