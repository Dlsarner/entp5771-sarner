# Cost structure

Product: PORTALO, one unit (bottle, spray head, hose, strap).
Decision: sign a 1,000-unit production order in October 2026. 755 units are owed to Kickstarter backers, and 245 are speculative stock to sell in the first 12 months (October 2026 to September 2027).
Price used for the calculations: $51, the campaign price and the price in my question. The survey asks for a maximum **including shipping**, so shipping is a cost I carry, not something added on top.

The backers' 755 units are outside this analysis. Their pledges are already collected and the order has to cover them whatever I decide. The question is whether the extra 245 pay for themselves.

## Part 1. Variable cost

### The walk-through

A customer orders on my online store. The payment processor takes its cut. I (or a fulfilment company) take one unit off the shelf, put it in a mailer, print a label, and hand it to USPS. It arrives a few days later. A few units come back faulty, and each one costs a return label, a replacement unit and a second shipment.

**The surprise from walking it through: making the unit is not a variable cost here.** On a normal product, one more sale triggers one more unit being made. Here, all 245 speculative units are paid for in October, before I know whether anyone will buy them. A sale does not trigger manufacturing; it uses up a unit I have already bought. So the landed cost of the stock belongs in Part 2 as a fixed commitment, and it is the biggest one I have. A category list would have filed it under "cost of goods, variable" without anyone noticing.

### Table

| Trigger | Low | High | Source |
|---|---|---|---|
| One unit manufactured | $0 | $0 | Not triggered by a sale. The 245 units are prepaid in the October order, so they sit in fixed commitments (Part 2) |
| Packaging (shipping mailer) | $0.50 | $1.20 | Padded mailer versus a small box. Assumes the retail box comes from the factory inside the landed cost |
| Shipping to the customer | $5.50 | $9.00 | USPS Ground Advantage for a package of about 12 oz with packaging. Low is within Southern California, high is cross-country |
| Payment processing | $1.78 | $2.27 | Low: Shopify Payments, 2.9% + $0.30 on $51. High: PayPal, 3.49% + $0.49 |
| Pick and pack | $0 | $3.50 | Low: I pack orders myself, which costs time but no cash. High: typical per-order fee from a fulfilment company |
| Expected returns and replacements | $0.58 | $2.58 | Low: 2% of orders × ($17 unit + $12 two-way shipping). High: 6% × ($25 + $18). A pressurised plastic part with a pump, a seal and a magnet is the kind of thing that fails early |
| **Total c per unit sold** | **$8.36** | **$18.55** | |

Not included: sales tax, which the customer pays and I pass on, and paid advertising, which is a budget I commit in advance and is therefore in Part 2.

### Which of these are decisions

Almost all of them.

- **Pick and pack** is a choice between my time and $3.50 an order.
- **Shipping** depends on where I sell. Selling locally in person (Torrance, the Wedge) cuts it to zero, but then I carry stock around.
- **Payment processor** is a choice of platform.
- **The channel itself** is the biggest decision and is not in the table. Selling through surf shops instead of direct means the shop keeps about half the $51, so I receive about $25.50. Shipping and payment fees mostly disappear, but my margin per unit roughly halves. I test this in scale.md.

### The three-group sort

**Clearly low enough to work at plausible prices:** packaging and payment processing. Together they are under $3.50 even at the high end, and a large error in either would not change anything.

**Clearly too high:** nothing in the direct channel. The wholesale route is the one that fails on margin, as shown in scale.md.

**Decisive, where a small error would change what I do:**
1. **Pick and pack** ($0 or $3.50). Doing it myself or outsourcing moves c by about 40% of its low value.
2. **Shipping** ($5.50 to $9.00). This depends on how many orders come from outside California, which I don't know yet.
3. **Return rate** (2% or 6%). No backer has received a unit, so there is no field data at all.

These three account for most of the $10 gap between my low and high c. Of the three, the return rate is the one I can do least about before signing, so it is the one to research first. Reviews from the first batch sold at Concours Lépine in Paris are the only real evidence that exists.

**Floor.** My variable cost of $8.36 to $18.55 per unit is the floor under the price of units I already hold: selling below it means each sale loses money. For the decision to order the 245 in the first place, the floor also has to include what each unit costs to buy, $17 to $25 landed, **which puts the price floor for signing the order at about $25 to $44.** My $51 clears it at both ends, though at the high end the margin left over is thin.

## Part 2. Fixed commitments

These are what I am on the hook for before knowing how many of the 245 will sell.

| Commitment | Low | High | When I am committed | Reversible? |
|---|---|---|---|---|
| Speculative stock: 245 units × landed cost | $4,165 | $6,125 | At signing, October 2026. Suppliers typically take a 30–50% deposit at signing and the balance before shipment | **No.** Once production starts, the units are mine whether or not they sell. This is the only commitment that really matters |
| Online store | $60 | $468 | Monthly | Yes, cancel within 30 days |
| Product liability insurance | $300 | $900 | Annual policy, bought before the first sale | Partly. Pro-rata refunds are common but not guaranteed. A pressurised container makes this hard to skip |
| Product photos and listing | $0 | $300 | Once, before launch | No, but small. Low assumes the creator lets me reuse campaign photos |
| Demo presence (contest booth, permits) | $0 | $500 | Per event, booked ahead | Mostly no once booked |
| Storage | $0 | $600 | Monthly | Yes. Low is my garage |
| Committed ad budget | $0 | $1,000 | When I set the budget | Yes, stoppable at any time, but money already spent is gone |
| **Total f** | **$4,525** | **$9,893** | | |

**One-off or recurring.** The stock is a one-off. The store, storage and insurance recur monthly or annually, and I've converted them all to **12 months**. That matches the period in my question, which asks about selling the 245 in the first season. It also matches the survey, which asks for a single unit that someone would buy once and keep for years, so there's one purchase per buyer in the period.

**The honest summary of Part 2.** Between 62% and 92% of my fixed commitments are the stock itself, and it is the only line I can't undo. Everything else can be cancelled within a month. The decision in October is therefore not "can I afford a store"; it is "am I willing to own 245 sprayers."

One more thing Part 2 changes: any demo units I give away at Torrance or the Wedge come out of the 245. If I use 15 for demos, only **230** are left to sell, and that is the ceiling I use in scale.md.
