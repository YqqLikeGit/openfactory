---
name: bom-cost
description: Build a bill of materials and full cost stack for a physical product, including landed cost and retail-price back-calculation. Use when the user asks "what will this cost to make", needs a BOM, or is setting a retail price.
---

# BOM Cost — the spreadsheet that decides if the product lives

Most first-time hardware products die of arithmetic, not engineering: the maker prices
from factory cost, forgets the five other layers, and discovers at retail that the
margin was never there. Build the whole stack every time.

## The cost stack (never quote fewer than all seven)

```
1. Materials        every part, fastener, label, and the resin in the sprue
2. Process          molding minutes, machining, finishing, assembly labor
3. Scrap/yield      nothing yields 100%; 2–5% typical for mature processes, worse early
4. Packaging        unit box, insert, master carton, manual — physical AND printed
5. Factory margin   the factory is not a charity; it's in the quote whether itemized or not
6. Logistics        freight + duty + insurance = the difference between EXW and landed
7. Amortization     tooling / certifications / NRE spread over realistic volume
```

Lines 1–5 ≈ your **FOB price**. Add line 6 → **landed cost**. Forgetting line 7 is how
people conclude they're profitable while still underwater on the mold.

## Building the BOM

One row per part: part name · material/spec · supplier (or "TBD") · qty per unit ·
unit cost at THIS volume tier · extended cost · MOQ · lead time · notes.

Rules:
- **Cost changes with volume — a BOM without a stated quantity tier is fiction.**
  Build three columns: e.g. 1k / 10k / 50k units.
- Include the boring rows: screws, foam, desiccant, warning label, the manual, tape.
  The boring rows are reliably 8–15% and reliably forgotten.
- Electronics: price the BOM the week you buy, not the week you designed — chip pricing
  moves. Note single-source parts; each one is a future crisis.

## The retail back-calculation (run it in both directions)

Standard consumer-hardware channel math:

```
retail price ≈ landed cost × 4 to 5     (traditional retail, distributor + store margin)
retail price ≈ landed cost × 2.5 to 3   (DTC only — but you're paying ads instead)
```

So run it backwards FIRST: target retail $29.9 at retail multiple 4 → landed must be
≤ ~$7.5 → FOB ≤ ~$6 after freight/duty → and now every BOM line has a budget.
If the backwards pass fails at target volume, the product needs a redesign or a
different channel — better to learn that on the spreadsheet.

## Landed cost quick math

- Sea freight China→US/EU on small consumer goods: often $0.10–0.60/unit at container
  or shared-container scale — but a full 40' of air-filled product is real money; cube
  efficiency (units per carton, cartons per pallet) is a design decision.
- Duty: look up the actual HS code — rates vary hugely by product and destination;
  never assume zero. Add customs brokerage and inland trucking.
- Air freight is 4–8× sea: it's for samples and emergencies, not for your margin model.

## Output format

Deliver: (1) BOM table at three volume tiers, (2) cost stack summary FOB → landed,
(3) retail back-calculation with pass/fail verdict at the user's target price,
(4) top three cost risks (single-source parts, volatile materials, low-cube packaging).

⚠️ Every figure here is a planning range. Real numbers come from supplier quotes at
your actual volumes — this skill's job is making sure no layer is missing when they arrive.
