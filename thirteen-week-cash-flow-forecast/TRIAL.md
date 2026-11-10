# Thirteen-week cash flow forecast: trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5). It did not write the template.
- **Date:** 2026-11-09

The inputs for this run are the invented Kestrelmoor Signworks example in [`example.md`](example.md) (settings, receivables, paid invoices, committed sales, pipeline, payables, recurring list, other known items, card statements and paid bills). No client data was used. The run followed the instruction block and output format in the member template as written, using only those inputs. The example's own output was read only after this output was finished.

## What came out

Every required part of the output format was produced, and every check passed. The figures below are the whole of the substance; wording is shortened where the format only repeats a row.

**Thirteen-week cash flow forecast: Kestrelmoor Signworks, weeks of 9 November 2026 to 1 February 2027**

For: owner. Prepared by: bookkeeper on 9 November 2026. Opening cash: $96,500 at the close of Friday 6 November 2026 (no time of day was given), operating and savings accounts, as stated by the bookkeeper from online banking. Floor: $60,000, set by the owner. Not supplied: none. Defaults used: 16 days late for customers with fewer than three paid invoices (D, E and G), the average of all 20 paid invoices (301 days over 20, 15.05, rounded up), because the settings give no figure.

Status: Above zero in all 13 weeks; below the $60,000 floor in weeks 8, 10 and 11; lowest $46,665 in week 8.

Customer timing (days late): A 13, B 2, C 30, H 9, J 6; D, E and G 16 by default.

The grid (US dollars, negatives in brackets, - for nothing):

| | W1 9 Nov | W2 16 Nov | W3 23 Nov | W4 30 Nov | W5 7 Dec | W6 14 Dec | W7 21 Dec | W8 28 Dec | W9 4 Jan | W10 11 Jan | W11 18 Jan | W12 25 Jan | W13 1 Feb | Total |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Opening cash | 96,500 | 108,810 | 95,330 | 85,855 | 85,255 | 79,155 | 84,305 | 81,865 | 46,665 | 70,265 | 54,315 | 51,875 | 61,975 | (no total) |
| Invoices already issued | 28,150 | 21,900 | - | 35,800 | 7,900 | 40,900 | - | - | - | - | - | - | - | 134,650 |
| Committed sales | - | - | - | - | - | 12,800 | - | - | 16,200 | 35,600 | - | 38,500 | - | 103,100 |
| Recurring receipts | - | - | - | 7,400 | - | - | - | - | 7,400 | - | - | - | 7,400 | 22,200 |
| Other receipts | - | - | - | - | - | - | - | - | - | - | - | - | - | - |
| Total in | 28,150 | 21,900 | - | 43,200 | 7,900 | 53,700 | - | - | 23,600 | 35,600 | - | 38,500 | 7,400 | 259,950 |
| Supplier bills | 13,690 | 6,980 | 3,175 | 8,600 | - | - | - | - | - | - | - | - | - | 32,445 |
| Payroll | - | 28,400 | - | 28,400 | - | 36,900 | - | 28,400 | - | 28,400 | - | 28,400 | - | 178,900 |
| Rent | - | - | - | 6,800 | - | - | - | 6,800 | - | - | - | - | 6,800 | 20,400 |
| Loan and lease payments | 2,150 | - | - | - | - | 2,150 | - | - | - | 2,150 | - | - | - | 6,450 |
| Subscriptions | - | - | 1,340 | - | - | - | 1,340 | - | - | - | 1,340 | - | - | 4,020 |
| Insurance | - | - | - | - | - | - | - | - | - | - | - | - | - | - |
| Taxes | - | - | - | - | - | - | - | - | - | 9,000 | - | - | - | 9,000 |
| Card statements | - | - | 3,860 | - | - | - | - | - | - | - | - | - | - | 3,860 |
| Purchases for committed work | - | - | - | - | - | 9,500 | - | - | - | 12,000 | - | - | - | 21,500 |
| Other payments | - | - | 1,100 | - | 14,000 | - | 1,100 | - | - | - | 1,100 | - | - | 17,300 |
| Total out | 15,840 | 35,380 | 9,475 | 43,800 | 14,000 | 48,550 | 2,440 | 35,200 | - | 51,550 | 2,440 | 28,400 | 6,800 | 293,875 |
| Net change | 12,310 | (13,480) | (9,475) | (600) | (6,100) | 5,150 | (2,440) | (35,200) | 23,600 | (15,950) | (2,440) | 10,100 | 600 | (33,925) |
| Closing cash | 108,810 | 95,330 | 85,855 | 85,255 | 79,155 | 84,305 | 81,865 | 46,665 | 70,265 | 54,315 | 51,875 | 61,975 | 62,575 | (no total) |
| Closing, no new sales | 108,810 | 95,330 | 85,855 | 85,255 | 79,155 | 81,005 | 78,565 | 43,365 | 50,765 | 11,215 | 8,775 | (19,625) | (19,025) | (no total) |
| Closing, two largest customers four weeks late | 90,410 | 76,930 | 67,455 | 66,855 | 79,155 | 43,405 | 40,965 | 5,765 | 29,365 | 28,315 | 25,875 | (2,525) | (1,925) | (no total) |

What the grid shows: lowest point week 8 (28 December to 3 January), $46,665, after payroll of $28,400 on 30 December and rent of $6,800 on 1 January, with no receipts. Below the floor: weeks 8 ($46,665), 10 ($54,315), 11 ($51,875). Below zero: none. No new sales: below the floor from week 8, below zero from week 12 (25 to 31 January), lowest (19,625) in week 12. Two largest customers four weeks late (C $64,800, A $59,000): below the floor from week 6, below zero in weeks 12 and 13, lowest (2,525) in week 12. Moved: A invoice 2291 $18,400 week 1 to 5; C invoice 2302 $26,300 week 6 to 10; A invoice 2308 $14,600 week 6 to 10; A retail rollout first seven stores $26,000 week 10 to after week 13; C hospital wayfinding phase 2 $38,500 week 12 to after week 13. Falling after week 13: $64,500.

Placed and not counted:
- Not counted, past its usual timing: Customer D invoice 2240, $4,200, due 9 August, expected 25 August by the rule.
- Not counted, after week 13: Customer A retail rollout, last seven stores, $26,000, expected 20 February 2027.
- Not counted, pipeline: Customer K, museum gallery signs, $45,000, proposal sent.
- Customer F invoice 2287 has nothing left to pay and is left out.
- Payments after week 13: none.

Checks: $96,500 + $259,950 - $293,875 = $62,575, week 13's closing cash. Each week opens at the previous week's closing. Invoices already issued: $138,850 = $134,650 placed + $0 after week 13 + $4,200 not counted, with one row of nothing left to pay. Committed sales: $129,100 = $103,100 + $26,000 + $0. Supplier bills: $32,445 = $32,445 + $0.

Questions for the owner:
1. Customer D invoice 2240, $4,200, is past its usual timing and not counted: has a payment date been agreed?
2. Supplier F (van leases) was paid $1,480 on 28 August, September and October and is not on the recurring list: if it continues it falls on 28 November (week 3), 28 December (week 8) and 28 January (week 12). Should it be added?
3. No line covers sales tax: is a payment due between 9 November and 7 February, and if so, how much and when?
4. No line covers insurance: the same question.

Decisions this forecast informs:
1. Week 8 (28 December to 3 January) closes at $46,665, $13,335 below the floor: payroll $28,400 on 30 December and rent $6,800 on 1 January, no receipts expected.
2. Weeks 10 and 11 (11 to 24 January) close at $54,315 and $51,875, below the floor by $5,685 and $8,125: payroll $28,400 on 13 January, purchases for committed work $12,000 on 12 January, the tax estimate $9,000 and the loan $2,150 on 15 January, against $35,600 of committed-sales receipts in week 10; week 11 has $2,440 of payments and no receipts.
3. With no sales beyond the invoices already issued, cash is below the floor from week 8 to week 13 and below zero in weeks 12 and 13 ((19,625) and (19,025)); payroll of $28,400 falls on 30 December, 13 January and 27 January.
4. If Customers C and A each pay four weeks later than their history, cash is below the floor from week 6 to week 13 and below zero in weeks 12 and 13 ((2,525) and (1,925)); $64,500 of their receipts falls after week 13.

The owner decides whether and how to act on each.

Next run: Monday 16 November 2026, from the opening balance at the close of Friday 13 November and fresh exports; week 1 drops off and a new week 13 (8 to 14 February 2027) is added. Assumptions A1 to A8, the full list of placed receipts and payments, and the closing line were also written, as the format requires; they are not repeated here.

## What was observed

Compared with the published example, the grid, every total, both cases, the status line, the checks and the four questions came out the same, figure for figure. The differences were small:

- The example's decisions section has one item covering weeks 8, 10 and 11. The template says one item for each run of weeks below the floor, so this run wrote week 8 and weeks 10 to 11 as two items.
- The example's first assumption says nothing moved over the weekend after the balance date. That is not in the inputs, and this run did not add it.
- The example's Questions 3 and 4 and this run's match; neither output adds any payment the inputs do not list.
- No fact appeared in this run's output that is not in the inputs. The example's A3 ("receipts thin out in the later weeks") and its A1 weekend statement are reasoning or assumption beyond the inputs, though harmless.

Nothing in the run called for a stop. Where the instructions were unclear and a guess was needed:

- Opening cash must be given with "date and time read"; the example gives a date and "close of Friday" but no time.
- The title line reads "weeks of [W1 date] to [W13 date]". It is not said whether W13's date is its first day (1 February) or its last (7 February); this run used the first day, as the example does.
- Nothing says what happens between the balance date (Friday 6 November) and the forecast start (Monday 9 November). The weekend's receipts and payments are in no week.
- A customer with fewer than three paid invoices takes the all-customer average. That gave Customer E, who paid 3 days late once, 16 days, and gave Customer D, who paid 45 and 60 days late, 16 days as well. The rule ignores a thin history that points the other way. Customer G has no paid invoices at all, which the rule does not name but plainly covers.
- "Rounded up" on 15.05 gives 16; a rounding rule that jumps a day on 0.05 is brittle. How to round a negative average (early payers) is not stated.
- "Largest single payroll payment" for the default floor is unclear when a bonus falls in the same week as regular payroll (28,400 or 36,900). The floor was set in the inputs, so it did not matter here.
- The monthly recurrence rule does not say what to do for a date such as the 31st.
- The "no new sales" case also removes already-won committed sales, so its name suggests less than it does; it means no sales beyond invoices already issued.
- The pasted instruction block leaves out the list of categories and the "Other payments" and "Other receipts" fallback, and the rule to list bills falling after week 13. They are in the template's Inputs and Procedure sections but not in the block an assistant would be given.
- Whether a case's decision item should be one item or two when it is below the floor and later below zero is not stated; this run used one item per case.
- The format shows grid rows as pipes without a header separator line, so a reader must add it to see a table.

The figures were worked out with a small throwaway script used as a calculator; the reading of the rules, and each placement, was the assistant's own. The template has not been tested in a client environment.

## Changed after this run, and not run again

Changed on 9 November 2026 after an independent review of the published template, and not run again. The output and the observations above are as recorded and describe the template and the example as they stood at the run:

- **The example's decisions.** Its single item for weeks 8, 10 and 11 is now two, week 8 and weeks 10 to 11, as the template asks and as this run wrote them. The example now has four decision items.
- **The weekend before the forecast start.** The procedure and the pasted instructions now ask for an assumption that nothing was received or paid between the time the opening cash was read and the forecast start, unless the person says otherwise. The example's first assumption now says this in those terms.
- **The opening cash's time.** The template now asks for the date it was read, with the time or "close of day" where known, so "the close of Friday 6 November" fits as given.
- **Customer timing.** Rounding up is now defined as moving toward later payment, early payers included (-2.3 becomes -2). The thin-history default now says it covers a customer with no paid invoices and one whose one or two paid invoices point another way, and its assumption names each such customer's own days late. The example's eighth assumption now lists Customer D (45 and 60 days), Customer E (3 days) and Customer G (none paid). No figure in the grid changes.
- **Monthly dates.** A monthly, quarterly or yearly date that does not exist in a month (the 29th to the 31st) now falls on that month's last day. No date in the example is affected.
- **The default floor.** It is now the largest single regular payroll payment from the recurring list, not a bonus or other one-off. The example sets its own floor, so nothing changes.
- **The "no new sales" case.** Its name is unchanged, but the procedure, the pasted instructions, the output format and the example now say it means no sales beyond the invoices already issued, so committed sales are removed too.
- **The pasted instructions** now carry the list of categories with the "Other payments" and "Other receipts" fallback, and the rule that a bill due after week 13 is listed under "Payments after week 13". One long line was rewrapped.
- **The output format.** The title now reads "weeks of [W1 first day] to [W13 first day]", and the grid has its header separator row.

The question this run raised about one decision item or two for a case that goes below the floor and later below zero is unchanged: the template still says one item for each case.
