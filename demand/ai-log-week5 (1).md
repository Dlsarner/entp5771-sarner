# AI log, Week 5

## What I asked

I handed the raw muscle-cola.csv to Claude and asked it to run the five Part 1 checks before computing anything else, explicitly telling it not to adjust any result to match the expected values.

## What came back, in order

**First look at the raw file.** Before any computation I had it print the header row and the first few lines rather than jumping straight to an answer. This turned up two things worth knowing. The file has 17 columns, of which only three matter, and the line ending count was 46 including the header, which initially suggested 45 respondents rather than the 46 the assignment expects. That was the first thing I made it resolve, and it turned out to be a missing trailing newline rather than a missing respondent. Loading the file properly gave 46 rows.

That was a small thing but it is exactly the kind of small thing the assignment is about. If I had accepted 45 and gone looking for the missing person, I would have wasted an hour on a file that was fine.

**Checked the two named failure modes before trusting anything.** The assignment lists the common causes of a wrong answer here: blank cells read as missing instead of zero, and respondents with zero silently dropped. I had it check both directly rather than assume. There are no blank cells in wtp, quantity, or quantity_at_P0, and all 11 respondents with a wtp of zero are present in the loaded data. So neither failure mode was available to happen in this file. I would not have known that without looking.

**Part 1, all five checks.** n = 46, eleven respondents with a wtp of zero, twelve who would take none even at zero, highest wtp $3.51, median wtp among payers $1.99. All five matched on the first run with nothing adjusted.

I asked it to confirm the median was taken among those who would pay something rather than across all 46, because including the eleven zeros would have pulled it down and still returned a plausible looking number. It was computed correctly. This is the kind of error that would not announce itself.

**The two curve points.** $1.00 gave 997.9 and $2.00 gave 419.0, against the expected 998 and 419. Only after both matched did I let it proceed to Part 2.

## Dead ends and things I had to push on

**The wtp = 0 edge case.** The three anchor construction says each respondent's line runs from their quantity at a price of zero to their quantity at their own maximum. For the eleven respondents whose maximum is zero, those two points are the same point and there is no line to draw. I had to decide explicitly what happens to them. The answer used is that they contribute their quantity_at_P0 at a price of exactly zero and nothing at any positive price, which is the only reading consistent with a maximum of zero meaning they will not pay. I recorded it as a judgement inside the method. Later I realised it made no difference in this file, because all 11 of those respondents also take zero when it is free, so they contribute nothing at any price however they are handled. Making the judgement explicit was still right. It just turned out not to matter here.

**A number I chased that turned out to be nothing.** I noticed the counts 11 and 12 and assumed one of them was an error, since I expected the people who would pay nothing and the people who want none to be the same group. They are not. I had it list the overlap directly. Nobody with a wtp of zero would take a positive quantity for free, but there is exactly one respondent with a positive wtp who says they would take none even at zero. So the two counts differ by one respondent rather than by a computation error. That respondent is row 37: a maximum of $0.50 and a quantity of zero at every price including free. At the time I read this as a quirk of human behaviour, someone contradicting themselves. It was not. After the assignment, Prof. Hatch announced that a student had found every quantity_at_P0 in the file is exactly double the quantity at that respondent's maximum, a column he generated years ago to test code. Row 37 gave a quantity of 0 at its maximum, and double 0 is 0. The "contradiction" was the doubling rule, not the person. I had the clue in front of me and explained it away instead of asking whether quantity_at_P0 ÷ quantity varied between respondents, which is a one-line check. Neither I nor the tool ran it.

**Concentration, which I went looking for and found.** After the read-offs I asked how the volume at each price was distributed across respondents, because the curve alone does not show it. That produced the material for Part 3.

## What I did with it

I used the Part 1 result to decide whether to trust Part 2 at all, which is the point of the exercise. All the read-off numbers in competence-check.md come from the verified run. The figure is plotted from the same construction rather than redrawn by hand.

Part 3 is mine. I asked for the distribution behind the curve and for anything unusual in the data, and I got several candidate observations back with numbers attached, but the paragraph about what it means and what it does to a profit estimate is my own reading of it.

## The honest summary

The tool was right the first time on this file, which is a less interesting log than one where it was wrong. What I actually got out of it was the discipline of checking two specific failure modes before trusting an output that looked correct, and a lesson I learned the hard way: the 11 versus 12 discrepancy I decided was a real feature of the data was actually a manufactured column that I never tested. Matching the answer key proved my tool does the arithmetic correctly. It did not prove the data was real. In Week 8 I will check that relationships which should vary between people actually do, before building anything on them. In Week 8 there will be no answer key, and the only thing carrying over is the habit.
