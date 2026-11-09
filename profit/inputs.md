# Inputs, reconciled

Week 6 inputs are in profit/cost-structure.md and profit/scale.md. The demand curve is in demand/curve.md (21 usable responses). This file lines them up and records what changed.

**Two problems I found in my own Week 6 folder first.** profit/scale.md was never committed in Week 6. I uploaded funnel.md to profit/ by mistake instead. The Week 6 figures from scale.md are restated below so the comparison is still visible. profit/funnel.md is that Week 6 funnel, and its Torrance numbers (9 started, 5 finished) are wrong. The corrected funnel is demand/funnel.md, and everything in this milestone uses the corrected one.

## 1. The period

**Fixed commitments:** 12 months, October 2026 to September 2027 (cost-structure.md). The stock is a one-off. The store, insurance and storage were converted to 12 months.

**Survey:** Q9 asks the most someone would pay for one PORTALO "if it were available to buy today." It names no period. My instrument notes said I would name the period inside the valuation question. The live question doesn't. So the survey measures a single purchase decision, not purchases per year.

**Reconciled:** I treat each respondent who names a maximum at or above the price as one purchase within the 12-month window, and nobody as buying twice. That fits a durable product someone buys once and keeps. It is generous in one way, because "would buy today" becomes "will buy sometime this year," and adoption is not penetration. The sensitivity file tests how much that generosity matters (the conversion threshold). Week 3 assumed 0.5 purchases per buyer per year, but that was about repurchase over several years. In the first selling year, each buyer buys at most once, which is what cost-structure.md already assumed.

One more mismatch: the units arrive in November and December, so the real selling window is about ten months, and it starts in winter. I have kept the 12-month cost period and noted this rather than shortening the costs.

## 2. The unit

Q9 asks for one unit, **including shipping**: the bottle, spray head, hose and strap, which is what the description says comes in the box. c in cost-structure.md is the cost of exactly that unit delivered, with shipping to the customer included. The units match.

One change from Week 6: c was computed at $51, but the payment fee is a percentage of price, so c moves slightly with price. I now use:

- Low: c = $6.88 + 2.9% of price
- High: c = $16.77 + 3.49% of price

At $51 these give $8.36 and $18.55, the same as Week 6.

## 3. N, revised

| Channel | Week 6 N (scale.md) | Milestone I funnel evidence | Revised N |
|---|---|---|---|
| Torrance Beach lot | 150–400 adult regulars | 35 adults approached on 29 October. 5 of the 23 who started (22%) screened out as under 18 or "someone else pays" | 117–313 (Week 6 range × 78% who pass the screen) |
| The Wedge / Newport | 500–1,400 | Never ran. Zero approached | **0** |
| Cal Poly SLO surf team | 50–200 | Luke's group chat is about 50 people. 1 response | 50 |
| Personal network (sibling, cousin) | not in Week 6 | 2 responses | 0. Not a population |
| **N** | **700–2,000** | | **about 170–360** |

**What changed and why.**

- **The Wedge is gone.** I never sampled it, and Week 6 told me to set N to the population I actually sampled. It was 70% of my Week 6 N, so dropping it is the biggest change in this milestone.
- **Torrance is screened.** The demand curve is a share of screened-in people, so N has to be screened-in people too. Week 6 counted all adults.
- **Cal Poly narrowed** to the size of the group Luke posted in.

The Torrance range is still my own estimate, not a count. The only hard number I have is 35 adults approached on one contest morning.

**Multiplier:** N ÷ n = 170/21 to 360/21, so each respondent stands for about **8 to 17 people**. The assumption it carries is that the adults who stopped for my survey behave like the ones who didn't. In my sample that matters in a specific way: 16 of 21 are surfers, but parents have higher willingness to pay (cleaning.md). If the people I didn't reach are mostly parents, I understate demand. If they're mostly surfers like the ones I did reach, the curve holds.

demand/comparison.md scaled willingness to the Week 6 N of 700 to 2,000. That figure is superseded by this revision.

## 4. The ranges, carried forward

| Input | Low | High | Source |
|---|---|---|---|
| c, per unit sold (at $51) | $8.36 | $18.55 | cost-structure.md Part 1, with the payment fee scaled to price |
| f, 12 months | $4,525 | $9,893 | cost-structure.md Part 2. 62–92% of it is the 245 speculative units |
| N | 170 | 360 | Section 3 above |
| Units available to sell | 230 | 230 | 245 speculative minus 15 used for demos (cost-structure.md) |

I pair low c with low f and high c with high f, because both rest on the same landed cost per unit ($17 at the low end, $25 at the high end): it sets the cost of the stock in f and the cost of replacements in c. Mixed pairs are also reported in profit-model.md. Everything is computed at both ends of N.
