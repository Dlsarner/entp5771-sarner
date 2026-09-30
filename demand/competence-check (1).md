# Estimation competence check

Data: muscle-cola.csv, 46 respondents, protein cola sold through gyms.
Path: how-many demand, three anchors, built by counting.

## Part 1. Tool check

All five values matched on the first run. I did not adjust anything to make them fit.

| Check | Expected | Mine |
|---|---|---|
| n | 46 | 46 |
| respondents with wtp of 0 | 11 | 11 |
| respondents who would take none even at zero | 12 | 12 |
| highest wtp | $3.51 | $3.51 |
| median wtp among those who would pay something | $1.99 | $1.99 |
| units per month at $1.00 | about 998 | 997.9 |
| units per month at $2.00 | about 419 | 419.0 |

Two things I checked deliberately before trusting the run, because they are the failure modes named in the assignment. There are no blank cells in wtp, quantity, or quantity_at_P0, so nothing could have been silently read as missing instead of zero. And all 46 rows survived loading, including the 11 respondents with a wtp of zero, so nobody was dropped.

Note that 11 and 12 are different numbers and both are correct. Eleven people would pay nothing for one. Twelve would take none even if it were free. Those are not the same group. The one-person gap turned out to be a product of the doubled column, not of how people behave (see the log).

## Part 2. The curve

Each respondent's three anchors give a line: quantity_at_P0 units at a price of zero, quantity units at their own maximum, and nothing above it. Summing those 46 lines horizontally, adding up quantities at each price, gives the curve below. Every respondent is used and nothing is discarded.

| Price | Units per month, whole sample | Counting or fitting |
|---|---|---|
| $0.00 | 1,402 | Counting |
| $0.50 | 1,206 | Counting |
| $1.00 | 998 | Counting |
| $1.50 | 770 | Counting |
| $2.00 | 419 | Counting |
| $2.50 | 255 | Counting |
| $3.00 | 108 | Counting |
| $3.51 | 60 | Counting |

Every number above comes from counting. No line was fitted, no shape was assumed, and no behaviour was invented at prices nobody was asked about. The one modelling choice inside the construction is that each respondent's demand is treated as a straight line between their two known points, at zero and at their own maximum, which is the standard three anchor construction rather than something I added.

The four read-offs the assignment asks for:

**$0.50 — 1,206 units per month.** Counting.
**$1.50 — 770 units per month.** Counting.
**$2.50 — 255 units per month.** Counting.
**$3.00 — 108 units per month.** Counting.

**Quantity at a price of zero — 1,402 units per month.** Counting. This number is the sum of the quantity_at_P0 column across all 46 respondents, the quantity each would take per month if the drink were permanently free. It involves no interpolation, but it is not assumption-free. After I built this, Prof. Hatch announced that a student had found every quantity_at_P0 is exactly double that respondent's quantity at their own maximum, because the column was generated arithmetically, not collected. So 1,402 is 2 × 701, and this point, along with the low-price end of the curve that it anchors, rests on that doubling, not on anything respondents said. I did not catch this myself.

![Demand curve](demand-curve.png)

## Part 3. What I notice

[YOUR PARAGRAPH HERE — delete this line. What the pattern is, what causes it, what it does to a profit estimate.]

## Part 4. The log

See demand/ai-log-week5.md.
