# AI supervision log, Milestone II

Tool: Claude. I pasted the Milestone II instructions and asked for help building the six files. Claude read my files directly from this repository: project/decision.md, profit/cost-structure.md, and demand/responses.csv, funnel.md, cleaning.md and curve.md.

## Dead ends and things that went wrong

**My Week 6 scale.md was never committed.** Claude found that profit/ has cost-structure.md and a funnel.md, but no scale.md. I had uploaded the funnel there by mistake in Week 6. Claude recovered my Week 6 N (700–2,000, mostly the Wedge) from our earlier conversation, and inputs.md restates it so the comparison is visible. The funnel.md sitting in profit/ also still has my wrong Week 6 Torrance numbers.

**The survey never named a period.** My instrument notes said I would name the period inside the price question. Checking the live Q9 wording showed it says "if it were available to buy today." Neither Claude nor I had caught this until the reconciliation forced us to read the actual question.

**The return rate looked consequential and wasn't.** Claude's first draft of sensitivity.md said the return rate mattered because it is part of what separates low c from high c. When we tested it on its own, going from 2% to 6% adds about $1.16 per unit and doesn't flip anything. The input that does flip is landed cost, at $23.08. That draft sentence was wrong, and testing one input at a time is what caught it.

**The band nearly read robust.** Read from its outer edges, the best case's positive band runs from $27.35 to $55, which is 32.5% of the range and "robust." It is actually two pieces with a loss from $45 to $52.40, so it is 23.8% and "fragile." The arithmetic for the outer-edge version is valid. Only the meaning is wrong, which is the kind of error Prof. Hatch warned a tool would carry forward without comment.

**My Week 6 N would have made it look robust.** At N = 2,000 and low costs, the reading is robust at 67.8%. That N rested mostly on the Wedge, which I never sampled, so I dropped it rather than keep the better answer.

**The hours on site came from Claude, not my tally, and they were wrong.** Claude estimated about 6 hours at Torrance on 29 October from the response times in our earlier chat, which ran until about 2:45 pm. I was actually there from just before 9:00 to about 10:30, about 1.5 hours. Some responses came in after I left, probably from parents using the coach's email. The correction cut the effort per response from about 20 minutes to about 5. It also moved the acquisition threshold from $12.63 an hour to about $50, which changed the belief the decision rests on: in the first draft it was acquisition effort, and after the correction it is reach (N). One wrong input from the tool changed a conclusion, not just a number.

## Checked against something I already knew, before trusting it

- **The staircase.** The model's share willing at $35 (13 of 21) and at $51 (6 of 21) matches the table in demand/curve.md, which I had already checked against responses.csv in Milestone I.
- **Variable cost.** The new price-dependent c gives $8.36 and $18.55 at $51, the same as cost-structure.md.
- **Break-even.** The model's break-even at $51 and low costs is 106 buyers. My Week 6 scale.md said 107, from the same numbers rounded up.
- **One profit number, step by step.** I asked Claude to show the arithmetic for the best case at $35 rather than just the answer: 13 ÷ 21 × 360 = 222.9 units; c = $6.88 + 0.029 × $35 = $7.90; profit = 222.9 × ($35 − $7.90) − $4,525 = $1,516, which matches the model.

## What I did with it

I kept the counted staircase rather than the fitted line, because the line failed in Milestone I. I accepted the revised N of 170–360, with the Wedge removed. Whether the Week 3 answer changed what I would do, the exposure choice, and the call (sign for 1,000) are my decisions. I gave them to Claude in my own words, and it wrote them into the files.
