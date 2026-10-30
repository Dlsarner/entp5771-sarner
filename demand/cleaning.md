# Cleaning

Data: `responses.csv`. Instrument: yes/no demand, one PORTALO, maximum price including shipping (Q9). Identifying columns stripped: the form collected no names or emails, and I removed the exact submission times, keeping only the date.

## Summary

| | Count |
|---|---|
| Rows in the raw Google Forms export | 27 |
| Genuine rows | 26 |
| Failed the screen, dropped | 5 |
| Flagged but kept | 6 (see below) |



## Walking through the checks

**1. Failed the screen: 5 dropped.** One under 18 (S02) and four who said someone else pays for their outdoor gear (S01, S03, S04, S05). All five come from the 29 October Torrance session. They stay in responses.csv, marked as screened out, and are excluded from the curve.

**2. Quantity at max price exceeding quantity at zero.** Not applicable. Yes/no demand asks for one unit, so there is no quantity to be incoherent.

**3. Willingness to pay above any plausible bound.** None. The highest answer is $85 (R20), only $16 above the campaign's stated MSRP of about $69 and below the two-pack price of about $86. It is plausible and stays in. The lowest positive answer is $10.

**4. Straight-lining.** None in the sense of the same answer everywhere. Two responses are low-effort (R08: "It's w," "It's rad," and "Give it to my wife to deal with"; R14: "It's clean," "No logo," "Logo"), but each answers the questions. Kept.

**5. Duplicates.** None. No two rows match, and the closest timestamps (11:40, 11:41 and 11:42 on 29 October) have different answers from three people filling it in side by side.

**6. Units and period drift.** None visible. Every answer is a whole-dollar amount between $0 and $85, which fits a one-unit purchase. Nobody answered as if it were a subscription or a multipack. One feature: every price is a multiple of $5, and $30 appears four times. That is heaping, not drift (see curve.md).

**7. Blank cells, per question, among the 21 screened-in respondents.**

| Question | Blanks | Kind |
|---|---|---|
| Q1–Q4 screeners, Q5 appeal, Q9 price, Q10–Q12 | 0 | Required |
| Q6 like best | 0 | |
| Q7 dislike | 0 | |
| Q8 do better | 1 (R08) | Respondent skipped an optional question. Not used in the curve |
| Q13 current practice | 0 | |

Every blank in the 5 screen-out rows was created by my form's branching. "No" to the age question and "Someone else pays" both route straight to the end, so those people were never asked anything else. Those blanks are not zeros and not non-buyers. They are people outside the population, and they are dropped, not counted. **No blank was scored as zero anywhere.** The rule I gave Claude was to treat screen-out blanks as screen failures and to stop if any blank appeared in Q9 among screened-in respondents. None did.

**8. Zero willingness to pay.** One typed zero (R07, appeal 1/10, "looks so poorly made," already owns a pressurised rinse kit and uses free showers). They passed the screen honestly, so this is a real non-buyer and they stay in. They are what a non-customer in my population looks like.

## Flagged and kept

| Flag | Rows | Why | What keeping them does |
|---|---|---|---|
| Not from a planned channel | R02, R03 (my sibling and cousin) | Recruited through a personal tie, which can push answers up to be supportive | Kept. Dropping them leaves n = 19 and moves the share at $51 or more from 29% to 32%, because both answered below $51. They pull the estimate down slightly, not up |
| Deleted, then restored | R01, 30 September, $20, from Luke's group chat | I deleted this in Google Forms because I thought it was a bad answer. Deleting in Forms does not remove it from the linked Sheet, so it was still in the export. A low answer is evidence, not a reason to remove someone, so I have restored it | Kept. Dropping it would leave n = 20 and raise the share at $51 or more from 29% to 30%. Removing a low answer pushes the curve up, which is exactly why it shouldn't be done quietly |
| Did not understand the product | R09 ($10: "Idk what it is"), R18 ($55: "looks like something id use for a sports game to drink… explain what its meant for") | They valued something other than what I described | Kept, because the misreading is a finding about my instrument (see below). Dropping both gives n = 19 and 5 of 19 (26%) at $51 or more |
| Answer inconsistent with appeal | R20 (appeal 4/10, price $85) | The lowest appeal among the parents and the highest price in the sample | Kept. It is coherent once you read it: they already own a bigger rinse kit for their son. Dropping it removes the only answer above $75 |

**A finding about my instrument.** Several respondents read the product as a drinking bottle ("looks like a modern water bottle," "fit in my cup holder," "something id use for a sports game to drink"). My debranded photo shows a bottle, and the description says "refillable bottle." Two respondents said outright that they did not understand it. The description needed to say what it is for (rinsing sand off feet, gear and kids) before saying what it is.

## Three checks that are easy to skip

**Segment consistency.** My Week 3 customer was the surf parent, not the surfer. Splitting by Q10:

| Segment | n | Willingness to pay | Median |
|---|---|---|---|
| Surf themselves | 16 | $0, 10, 20, 25, 30, 30, 30, 30, 35, 35, 40, 40, 45, 45, 45, 55 | $32.50 |
| Household member surfs (parents) | 3 | $55, 75, 85 | $75 |
| Other outdoors | 2 | $55, 75 | $65 |

The distributions barely overlap. Every parent is at $55 or more, and only one surfer is, and that is R18, who thought it was a drinks bottle. That supports the bet I made in Week 3, that the parent is the buyer. It also means my sample is mostly the wrong segment. A surf contest put far more surfers than parents in front of me, so 16 of 21 respondents are from the segment with the lower willingness to pay. With only 3 parents, I cannot say how wide the parent distribution really is.

**Effective sample size by price region.** $0–29: 4 respondents. $30–49: 11. $50–85: 6. Above $55: 3. Anything I say above $55 rests on three people.

**Replication.** This is a single sample, not a replicated one. 18 of the 21 usable responses come from one morning at one beach. One fielding is one observation of the market.

## Is a sample of 21 still worth reading?

It is below 30, so here is the argument. The 18 Torrance responses are a fair picture of the adults at that beach that morning: they finished at 51% of approaches, and nobody dropped out midway, so the people who answered are not just the keenest few. It is not a picture of Southern California, and it under-represents parents, the segment I set out to sample. Read it as a measure of what adult surfers at Torrance would pay, plus three data points about parents.
