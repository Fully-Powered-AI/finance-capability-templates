# Annual operating budget: tried on its example

- **Product:** Claude, run in Claude Code

Model: Claude Sonnet 5.5 (model ID claude-sonnet-5-5). Date: 2026-11-10.

This run used the invented example's inputs (Company K, the invented sign maker). No client data was used. The run was done by an assistant that did not write the template. It read the template and the example's inputs first, produced the budget by following the instructions block and the output format, and only then compared its result with the example's published output and the reviewer checklist.

## Inputs used

The seven inputs in [the example](example.md), under "The inputs": settings, targets, this year's figures, budget submissions with custom phasing, headcount plan, capital purchases list and other cash items.

## What came out

Every part of the output format was produced, nothing made the assistant stop, and no flagged line was left without a question. The assistant worked the arithmetic out in a short script and then wrote the draft. The full draft follows.

```
ANNUAL OPERATING BUDGET: 2027, DRAFT

For: managing director, budget meeting on Thursday 3 December 2026, to settle the open questions and approve. Prepared by the finance lead on Tuesday 10 November 2026, for the finance lead's review.
Sources: this year's figures, as of 6 November 2026, actual January to October 2026 and an estimate for November and December; submissions from Sales (sales director, 3 November 2026), Production (production manager, 4 November 2026), Administration (office manager, 5 November 2026); headcount plan of 2 November 2026; capital purchases list of 5 November 2026; other cash items of 6 November 2026.
Settings used: change threshold $5,000 and 10%; capitalisation limit $2,500; collection lag 1 month; opening receivables $250,000; opening cash $320,000; minimum cash $150,000; downside 10% lower revenue; missing lines carried at this year's figure. Defaults used: none.

THE PICTURE
Revenue: budget $3,600,000; this year $3,240,000; change +$360,000 (11.1%). Target $3,700,000: $100,000 below.
Costs: budget $3,389,400; this year $3,066,000; change +$323,400 (10.5%). People costs $1,836,000, from the headcount plan.
Result: budget $210,600; this year $174,000; change +$36,600 (21.0%). Target $300,000: $89,400 below.
Capital purchases: $129,400, 3 items, outside costs and inside the cash check.
Cash: opening $320,000; closing $251,200; lowest $144,900 at the end of May. Below the $150,000 minimum: May. If revenue is 10% lower: lowest -$94,800 at the end of October; below the minimum: April to December; below zero: September to December.
Lines: 13. Flagged: 3. Questions for budget owners: 3. Open questions for leadership: 4.

TIE-OUT
This year: revenue lines add to Total revenue, $3,240,000; cost lines add to Total costs, $3,066,000. Headcount plan: each team's months add to its Total; total $1,836,000. Budget: by team, by month and in the cash check, revenue $3,600,000 and costs $3,389,400.

BUDGET BY TEAM
Sales (sales director). Submitted by the sales director on 3 November 2026.
Sign sales (Revenue). This year $2,880,000; next year $3,168,000; change +$288,000 (10.0%). Driver: 1,320 orders x 2,400 = $3,168,000. Phasing: custom, months as submitted (Jan 192,000 to Dec 264,000; adds to $3,168,000).
Installation fees (Revenue). This year $360,000; next year $432,000; change +$72,000 (20.0%). Driver: 480 installs x 950 = $456,000. Phasing: even, $36,000 a month. FLAG, driver does not give the amount: submitted $432,000, driver gives $456,000, difference $24,000. See question 1.
People costs (Cost). This year $420,000; next year $504,000; change +$84,000 (20.0%). Driver: headcount plan of 2 November 2026. Phasing: as the headcount plan (Jan and Feb 37,000; Mar to Dec 43,000).
Marketing (Cost). This year $96,000; next year $120,000; change +$24,000 (25.0%). Driver: 96,000 + 24,000 = $120,000. Phasing: custom, months as submitted (April 32,000; every other month 8,000; adds to $120,000).
Travel (Cost). This year $30,000; next year $30,000; no change. Driver: same as this year, $30,000. Phasing: even, $2,500 a month.
Team total: revenue $3,600,000; costs $654,000.

Production (production manager). Submitted by the production manager on 4 November 2026.
People costs (Cost). This year $960,000; next year $1,020,000; change +$60,000 (6.3%). Driver: headcount plan of 2 November 2026. Phasing: as the headcount plan (Jan to Jun 82,000; Jul to Dec 88,000).
Materials (Cost). This year $1,008,000; next year $1,108,800; change +$100,800 (10.0%). Driver: 35% of Sign sales, 35% x 3,168,000 = $1,108,800. Phasing: as Sign sales (35% of each month; Jan 67,200 to Dec 92,400).
Equipment upkeep (Cost). This year $48,000; next year $66,000; change +$18,000 (37.5%). Driver: 4,000 x 12 + 18,000 = $66,000. Phasing: custom, months as submitted (July 22,000; every other month 4,000).
Waste removal (Cost). This year $0; next year $12,000; new line. Driver: 1,000 x 12 = $12,000. Phasing: even, $1,000 a month.
Team total: revenue $0; costs $2,206,800.

Administration (office manager). Submitted by the office manager on 5 November 2026.
People costs (Cost). This year $300,000; next year $312,000; change +$12,000 (4.0%). Driver: headcount plan of 2 November 2026. Phasing: as the headcount plan (26,000 a month).
Rent (Cost). This year $144,000; next year $149,400; change +$5,400 (3.8%). Driver: 12,000 x 3 + 12,600 x 9 = $149,400. Phasing: custom, months as submitted (Jan to Mar 12,000; Apr to Dec 12,600).
Software (Cost). This year $36,000; next year $43,200; change +$7,200 (20.0%). Driver: 3,600 x 12 = $43,200. Phasing: even, $3,600 a month. FLAG, change past the threshold with no reason given: +$7,200 (20.0%). See question 2.
Insurance (Cost). This year $24,000; next year $24,000; no change. Driver: carried at this year's figure, not submitted. Phasing: even, $2,000 a month. FLAG, not submitted: carried at $24,000. See question 3.
Team total: revenue $0; costs $528,600.

BUDGET BY MONTH
Month | Revenue | People costs | Other costs | Result
Jan | 228,000 | 145,000 | 100,300 | -17,300
Feb | 252,000 | 145,000 | 108,700 | -1,700
Mar | 300,000 | 151,000 | 125,500 | 23,500
Apr | 324,000 | 151,000 | 158,500 | 14,500
May | 336,000 | 151,000 | 138,700 | 46,300
Jun | 324,000 | 151,000 | 134,500 | 38,500
Jul | 288,000 | 157,000 | 139,900 | -8,900
Aug | 264,000 | 157,000 | 113,500 | -6,500
Sep | 312,000 | 157,000 | 130,300 | 24,700
Oct | 336,000 | 157,000 | 138,700 | 40,300
Nov | 336,000 | 157,000 | 138,700 | 40,300
Dec | 300,000 | 157,000 | 126,100 | 16,900
Year | 3,600,000 | 1,836,000 | 1,553,400 | 210,600

COSTS BY TEAM BY MONTH
Month | Sales | Production | Administration | Total
Jan | 47,500 | 154,200 | 43,600 | 245,300
Feb | 47,500 | 162,600 | 43,600 | 253,700
Mar | 53,500 | 179,400 | 43,600 | 276,500
Apr | 77,500 | 187,800 | 44,200 | 309,500
May | 53,500 | 192,000 | 44,200 | 289,700
Jun | 53,500 | 187,800 | 44,200 | 285,500
Jul | 53,500 | 199,200 | 44,200 | 296,900
Aug | 53,500 | 172,800 | 44,200 | 270,500
Sep | 53,500 | 189,600 | 44,200 | 287,300
Oct | 53,500 | 198,000 | 44,200 | 295,700
Nov | 53,500 | 198,000 | 44,200 | 295,700
Dec | 53,500 | 185,400 | 44,200 | 283,100
Year | 654,000 | 2,206,800 | 528,600 | 3,389,400

LARGEST CHANGES FROM THIS YEAR
Sales, Sign sales: +$288,000 (10.0%). Reason given: second sales rep starts in March; orders up from 1,200 to 1,320 (sales director).
Production, Materials: +$100,800 (10.0%). Reason given: materials stay at 35% of sign sales (production manager).
Sales, People costs: +$84,000 (20.0%). Reason given: headcount plan of 2 November 2026.
Sales, Installation fees: +$72,000 (20.0%). Reason given: installs grow with orders (sales director).
Sales, Marketing: +$24,000 (25.0%). Reason given: spring trade show in April (sales director).
Production, Equipment upkeep: +$18,000 (37.5%). Reason given: press overhaul due in July (production manager).
Production, Waste removal: +$12,000 (new line). Reason given: the landlord's shared waste service ends in December; a contractor has quoted 1,000 a month (production manager).
Administration, Software: +$7,200 (20.0%). Reason given: none stated.

CAPITAL PURCHASES (outside costs)
Jan: Laptops (2), Administration, $2,400, owner office manager. Reason: for the two new starters. FLAG: under the capitalisation limit.
Mar: Van for installs, Sales, $42,000, owner sales director. Reason: second installation crew.
May: Flatbed printer, Production, $85,000, owner production manager. Reason: replaces the printer bought in 2016.
Total $129,400.

CASH CHECK
Month | Cash in | Costs paid | Capital | Other cash | Closing cash | Below minimum
Jan | 250,000 | 245,300 | 2,400 | -5,000 | 317,300 | no
Feb | 228,000 | 253,700 | 0 | -5,000 | 286,600 | no
Mar | 252,000 | 276,500 | 42,000 | -5,000 | 215,100 | no
Apr | 300,000 | 309,500 | 0 | -5,000 | 200,600 | no
May | 324,000 | 289,700 | 85,000 | -5,000 | 144,900 | yes
Jun | 336,000 | 285,500 | 0 | -5,000 | 190,400 | no
Jul | 324,000 | 296,900 | 0 | -5,000 | 212,500 | no
Aug | 288,000 | 270,500 | 0 | -5,000 | 225,000 | no
Sep | 264,000 | 287,300 | 0 | -45,000 | 156,700 | no
Oct | 312,000 | 295,700 | 0 | -5,000 | 168,000 | no
Nov | 336,000 | 295,700 | 0 | -5,000 | 203,300 | no
Dec | 336,000 | 283,100 | 0 | -5,000 | 251,200 | no
Year | 3,550,000 | 3,389,400 | 129,400 | -100,000 | 251,200 |
Lowest: $144,900, end of May. If revenue is 10% lower, everything else unchanged: lowest -$94,800, end of October; below the minimum: April to December; below zero: September to December.
(Downside month by month, closing cash: Jan 317,300; Feb 263,800; Mar 167,100; Apr 122,600; May 34,500; Jun 46,400; Jul 36,100; Aug 19,800; Sep -74,900; Oct -94,800; Nov -93,100; Dec -78,800.)

ASSUMPTIONS
Lines:
Sales, Sign sales: second sales rep starts in March; orders up from 1,200 to 1,320; average order held at 2,400 (sales director, 3 November 2026).
Sales, Installation fees: installs grow with orders (sales director, 3 November 2026).
Sales, People costs: headcount plan of 2 November 2026.
Sales, Marketing: spring trade show in April; everything else as this year (sales director, 3 November 2026).
Sales, Travel: none stated.
Production, People costs: headcount plan of 2 November 2026.
Production, Materials: materials stay at 35% of sign sales, as this year (production manager, 4 November 2026).
Production, Equipment upkeep: press overhaul due in July; service contract unchanged (production manager, 4 November 2026).
Production, Waste removal: the landlord's shared waste service ends in December; a contractor has quoted 1,000 a month (production manager, 4 November 2026).
Administration, People costs: headcount plan of 2 November 2026.
Administration, Rent: lease review in April adds 5% (office manager, 5 November 2026).
Administration, Software: none stated.
Administration, Insurance: none stated; carried at this year's figure.
Budget-wide:
This year's figures are actual for January to October 2026 and the finance lead's estimate for November and December (settings, 6 November 2026).
Customers pay one month after the sale; $250,000 was owed at 31 December 2026 and is collected in January (settings). December 2027 revenue is not collected within the year.
Costs are paid in the month they are budgeted.
The result is before depreciation, interest and tax.
Opening cash on 1 January 2027 is $320,000 (settings).
The downside lowers every month's budgeted revenue by 10%, rounded to whole dollars; costs, capital purchases, other cash items and opening receivables are unchanged.
Other cash items: loan repayment of $5,000 every month; tax payment on 2026 profits of $40,000 in September (other cash items, 6 November 2026).
Defaults used: none. Insurance is carried at this year's figure because the settings allow it.

QUESTIONS FOR BUDGET OWNERS
1. For the sales director: Sales, Installation fees: you submitted $432,000; 480 installs x 950 gives $456,000, which is $24,000 more. Which figure is right?
2. For the office manager: Administration, Software: the budget is $43,200 against $36,000 this year, up $7,200 (20.0%). The driver is 3,600 a month, with no reason given. What is behind the increase?
3. For the office manager: Administration, Insurance: no submission arrived. $24,000 was carried at this year's figure, $2,000 a month. What is next year's figure, and what is it based on?

OPEN QUESTIONS FOR LEADERSHIP
1. Budgeted revenue is $3,600,000 against the $3,700,000 target, $100,000 below. How should the gap be handled?
2. The budgeted result is $210,600 against the $300,000 target, $89,400 below. How should the gap be handled?
3. Closing cash in May is $144,900, $5,100 below the $150,000 minimum, in the month the $85,000 flatbed printer is bought. If revenue is 10% lower, cash is below the minimum from April to December, below zero from September to December, and lowest at -$94,800 at the end of October. What does leadership want to do about the minimum and the downside?
4. Which capital purchases are approved, and in which month: laptops (2), $2,400, January (under the capitalisation limit, for the finance lead's decision); van for installs, $42,000, March; flatbed printer, $85,000, May?

CHECKS FOR THE FINANCE LEAD
Submissions missing: Administration, Insurance. Carried at this year's figure: Administration, Insurance, $24,000.
Drivers that do not give the submitted amount: Sales, Installation fees, driver result $456,000, submitted $432,000.
Changes past the threshold with no reason given: Administration, Software, +$7,200. Nothing stated: none.
People costs found in submissions, left out: none.
Capital items flagged: Laptops (2), $2,400, under the capitalisation limit.

Draft for the finance lead's review and managing director's approval. No submitted figure has been changed, no target has been set or moved, and nothing has been approved, sent or entered in any system.
```

## What was observed

- **Every required part was produced.** All the sections in the output format are present, in order, ending with the status line. None of the stop conditions applied to these inputs, so the stop rules were not exercised. Nor were the refusals (change a figure, set a target, send) or the rule about names and pay.
- **The figures match the published example exactly.** Every total, every monthly figure, the cash check in both cases, the flags and the changes past the threshold agree. The tie-out passed. Three lines were flagged: the installation driver (480 x 950 gives $456,000, $432,000 submitted), the software increase with no reason, and the insurance line with no submission. The lowest cash is $144,900 at the end of May, and in the lower-revenue case it is -$94,800 at the end of October. The reviewer checklist's nine points could each be checked against the output and held.
- **Differences from the published example.** These are wording and choices, not figures:
  - Mine gave four open questions for leadership, splitting the revenue gap from the result gap. The example gave three and put both gaps in one.
  - The example's first leadership question adds that if the installation driver of $456,000 is right, revenue and the result are each $24,000 higher. Mine did not; the template does not ask for it.
  - The example's second leadership question asks whether leadership accepts the May position and what should happen if revenue runs below budget. Mine asked more narrowly what leadership wants to do about the minimum and the downside.
  - The example writes dollar signs in the tables and shows the monthly amounts of each phased line (for Materials, all twelve). Mine left the dollar signs out of the tables and gave the rule and the first and last amounts for most lines.
  - Mine added the lower-revenue case month by month in a line under the cash check, and listed the loan repayment and the tax payment among the assumptions. The example has neither.
  - Mine said the lower-revenue figures are rounded to whole dollars; the example does not say.
  - The example's questions say "The budget uses $432,000". Mine said the submitted figure stands in the flag and did not repeat it in the question.
- **Facts not in the inputs.** None in either output. Both contain figures worked out from the inputs (the totals, the gaps, the $24,000 effect, December 2027 revenue still owed at year end). Both reword the owners' reasons without adding to them.
- **Where the instructions were ambiguous and the assistant had to choose:**
  1. In the first month with a one-month lag, "the opening receivables collected in the first month" can be read as replacing the previous month's revenue or adding to it. The assistant took it as replacing, since the receivables are the previous month's revenue. The example does the same.
  2. The rounding of the lower-revenue case is not stated. The assistant rounded each month's revenue to whole dollars. It made no difference here.
  3. The rounding of an "as:" line is described as "rounded to whole units" without saying how a half is rounded. No half arose in this example.
  4. "Flagged: [n]" does not say whether flagged capital items count with flagged lines. The assistant counted lines only (3), which matches the example.
  5. "Largest changes from this year" does not say how many to list or which lines. The assistant listed every line that passed the threshold, largest first, as the example did.
  6. The count of open questions for leadership depends on whether the two target gaps are one question or two. The template's order ("any gap to a target") does not settle it.
  7. "Per item" in the settings against "Laptops (2), $2,400" in the list: the limit is per item, but the list gives one amount for two laptops, so it is unclear whether $2,400 or $1,200 is compared with the limit. The flag follows either way, and the template's own acceptance test treats the pair as one item.
  8. The format says the draft is "prepared by the [role] ... for the [finance lead role]'s review". Here the finance lead prepares it, so the line reads as preparing it for their own review. The example repeats it unchanged.
  9. The format shows amounts in brackets without saying whether to write a currency symbol in the tables; the example uses dollar signs, mine did not.
  10. In the instructions block, the recompute rule drops the "same as this year" and "a change on this year's figure" driver forms that the procedure lists, so an assistant using only the block might write "not recomputed" for them.
- **Shortcomings of this trial.** It is one run on one invented example with no stop condition, refusal, people-cost-in-submission case or header mismatch in it, so those parts of the template are untried. The acceptance tests in the template have not been run. The arithmetic was done in a script written for the run, not by the model alone, so this does not show how the model does the sums without one. The run was by the product named above only.

## Changed after this run, and not run again

Changed on 10 November 2026 after an independent review of the template, and not run again. No figure, rule of arithmetic or example input that changes a figure was altered. The output and the observations above are as recorded and describe the template and the example as they stood at the run:

- **Driver forms in the pasted instructions** (item 10 above). The recompute step now lists the same forms as the procedure, including "a change on this year's figure" and "same as this year".
- **The first month's cash in with a one-month lag** (item 1 above). The procedure and the pasted instructions now say that in the first month cash in is the opening receivables only, as the run and the example already did.
- **The target gaps** (item 6 above). The revenue gap and the result gap now go in one open question for leadership, as in the example. On the revised instructions, the run's two gap questions would be one, and its count of open questions three, not four.
- **"Flagged" and "Largest changes from this year"** (items 4 and 5 above). The format now says "Flagged" counts lines only, not flagged capital items, and that every line past the change threshold is listed under largest changes, largest change first, ignoring sign. Both the run and the example already did this.
- **Rounding** (items 2 and 3 above). Each month's lower revenue in the downside, and each month of an "as:" line, is now rounded to whole currency units with halves rounded away from zero. No figure in the run or the example changes.
- **Currency symbol** (item 9 above). Every amount now carries the currency symbol, in the tables too, as in the example. The run's tables, without dollar signs, would not meet the revised format.
- **Defaults in the procedure.** The Inputs section now gives every setting's default, including a collection lag of 0 and missing lines not carried, which appeared before only in the pasted instructions.
- **The opening line** (item 8 above). The format now leaves out "for the finance lead's review" when the finance lead prepares the draft, and the example's opening line was shortened to match. The run kept the clause.
- **The capitalisation limit** (item 7 above). It is now compared with each row's amount on the capital purchases list, as listed; the example's setting says so in place of "per item". The laptops are still flagged.
- **The example's first open question for leadership** no longer adds that revenue and the result would each be $24,000 higher if the installation driver is right, since the template does not ask for it (the second difference listed above). The run did not add it either.
