---
name: mold-quote
description: Decode, sanity-check, and compare injection-mold tooling quotes. Use when the user receives a mold/tooling quote, needs to budget tooling, or asks why quotes differ wildly.
---

# Mold Quote — read a tooling quote like a factory owner

Two suppliers quote the same part at $4,000 and $18,000. Usually neither is lying —
they're quoting different molds. Your job: make the differences visible, then help the
user match the mold to their actual volume.

## The five levers that set a mold's price

1. **Cavity count** — 1 cavity = cheapest steel, highest per-part cost. Rule of thumb:
   annual volume under ~10k: single cavity; 50k–200k: 2–4 cavities; beyond that,
   multi-cavity or family molds. More cavities = more steel, more precision, more money,
   cheaper parts.
2. **Steel grade** — P20/718 (pre-hardened): standard for most work, roughly 300k–500k
   shots. H13 (hardened): abrasive/glass-filled resins or million-shot life. S136
   (stainless, polishable): clear parts and high-gloss cosmetics. A quote that doesn't
   name the steel isn't a quote.
3. **Runner system** — cold runner: cheaper tool, wastes material each shot, visible
   gate trim. Hot runner: adds thousands to the tool, pays back on high volume and big
   parts. Below ~50k/year the hot runner rarely pays.
4. **Actions** — every slider/lifter for an undercut adds cost and a wear item.
   (If the DFM pass didn't kill the undercuts, this is where they send the bill.)
5. **Texture & polish** — VDI/MT texture spec and mirror polish are line items.
   High-gloss S136 polish is skilled-labor-hours, priced as such.

## What a complete quote must contain

Cavity count · steel grades (cavity/core separately) · runner type · guaranteed shot
life · cycle time estimate · T1 sample date · what's included (texture? first samples?
DFM feedback?) · mold ownership terms · maintenance responsibility.

Missing items are negotiating room they kept for later. Ask for all of them in writing.

## Timeline reality

Typical simple-to-medium tool from a Chinese shop: **T1 samples in 25–45 days** from
final CAD. Then expect T2 (fixes) and often T3. Budget 2–3 sample loops before
production-ready; a vendor promising first-shot-perfect is selling something.

## The amortization math (always run this)

```
tooling_cost / expected_lifetime_units = tooling cost per part
```

- $8,000 mold ÷ 20,000 units = $0.40/part buried in every unit
- Same mold ÷ 200,000 units = $0.04/part
- This one line answers "should I pay more for a better tool?" — a $12k 4-cavity tool
  that cuts part price by $0.15 beats an $6k single-cavity tool after ~40k units.

## Negotiation notes (from the factory side of the table)

- Quotes swing with the shop's order book. A slow month buys you 20% — a full one adds it.
- "Free mold" offers bury the steel in the part price with an MOQ handcuff. Run the
  amortization math both ways before accepting; sometimes it's genuinely fine, sometimes
  you're financing their machine at loan-shark rates.
- Mold ownership: get it in writing that the tool is yours, with the right to move it.
  Expect friction moving a tool a shop built cheap — the discount was the lock-in.

## Output format

Return a **Quote Review**: (1) what this quote actually specifies, (2) what's missing,
(3) amortization at the user's real volume, (4) the three questions to send back before
paying any deposit. Standard deposit structure: 50% down / 50% at T1 approval — flag
anything demanding 100% up front.

⚠️ Ranges above are starting points for budgeting, not prices. Geometry, resin, and the
month's order book set real numbers — get three quotes and make them explain each other.
