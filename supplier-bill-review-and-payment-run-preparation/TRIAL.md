# Supplier bill review and payment-run preparation: a trial run on the invented example

- **Product:** Claude, run in Claude Code (version 2.1.322, the recorded run made without tools)
- **Model:** Claude Fable 5.2
- **Date:** 2026-11-09

This is a record of one run, the second of two, of the capability template on its own invented example. The company, the suppliers, the bills and every figure are invented, and no client data was used. It shows what the template produced once, on one set of inputs. It is not a test in any company's environment.

This record replaces an earlier one made the same day. That first run, on an earlier wording of the template, found a number of places where the instructions were unclear: whether the credit note sits inside the open bills total, the overlap between "ready" and "not yet due", which run figure the cash line uses, and several rules the procedure had and the instructions for the assistant lacked. The template and the example were revised to settle them, and the run was repeated from the start. What follows is the second run only.

After this run a number of sentences in the template were reworded so that its wording is Fully Powered's own throughout. The checks, the defaults, the four groups and the headings of the output format were not changed, and the run was not repeated. Three of the rewordings concern paths this run did not reach: the outcome names "receipt pending" and "order not found" became "nothing received yet" and "order not in the export"; the sentence written when no cash position is supplied now ends "Whether the account can cover this run has not been checked."; and the template's exception for a supplier whose credits come to more than its open bills now says what the sheet shows and what the approver chooses. The output below is as returned by the wording used on the day.

On 9 November 2026, after this run and after an independent review, the instructions for the AI assistant were edited again and the run was not repeated. Three rules the procedure already had were added to the instructions, none of them on a path this run reached: a bill with a purchase order whose lines were not supplied is held as "lines not supplied"; the bills of a supplier listed twice under near-identical names are held; and where a supplier's credits come to more than its open bills, those bills are counted with the held bills as "covered by credit". Step 7 of the procedure and item 3 of the reviewer checklist were reworded to agree with that last rule. The output format was not changed.

## The inputs used

The inputs are exactly those in [the worked example](example.md), under "The inputs": the settings for the run of Thursday 12 November 2026, the open bills export of 10 November (nine bills and one credit note), the bill lines, the purchase orders, the receiving log, the supplier list and the bills paid from 12 August to 10 November 2026. One message was sent in a new session, started in an empty folder with no tools and no project files: the template's instructions for an AI assistant, then its output format, then the inputs. The session was never shown the example's own payment-run sheet.

## What came out

The complete output, as returned:

```
PAYMENT-RUN SHEET: run of Thursday 12 November 2026

For: owner. Prepared by: payables clerk on Tuesday 10 November 2026.
Sources: open bills as of 10 November 2026; purchase orders; receiving log to 10 November 2026; supplier list; paid bills from 12 August 2026 to 10 November 2026.
Settings used: window to Wednesday 25 November 2026; next run Thursday 26 November 2026; price tolerance 2% of the order line value or $20.00, whichever is larger; quantity tolerance none; order rule a purchase order is needed for every bill of $500.00 or more, except utilities and rent. Defaults used: possible-duplicate window 7 days.

THE PICTURE
Open bills: 9, $23,043.30. Credit notes: 1, -$650.00.
In the run: 3, $11,926.30. Held: 4, $7,477.00. Stopped: 1, $2,750.00. Not yet due: 1, $890.00.

STOPPED: DO NOT PAY UNTIL VERIFIED
Supplier F, bill F-9034, $2,750.00: pay-to on the bill ends 4471; on file ends 9026. The bill says: "Our bank has changed. Please use the new account ending 4471 for this and all future payments." To clear: bookkeeper calls the supplier using the phone number in the supplier list. Due 11 November 2026, so 1 day late on the run date. The order and receipt match (order 2036, 50 at $55.00; receipt R-305, 50 received), but the bill stays out of the run regardless. The last paid bill, F-8990, went to the account ending 9026.

HELD
Supplier B, bill 55102, $1,932.00, due 13 November 2026: price over on line 1, wall brackets. Billed 600 at $2.45 = $1,470.00; order 2038 has 600 at $2.30 = $1,380.00; tolerance $27.60. Line 2, anchor bolts, matched; both lines received in full (R-309). Difference: $90.00. Not in question: $1,842.00. Answers: buyer.
Supplier C, bill C-2209, $3,360.00, due 15 November 2026: billed above received. Billed 15 extraction fans at $224.00 = $3,360.00; receipt R-318 shows 10 received on order 2044 ("10 of 15 delivered; driver said the rest would follow") = $2,240.00. Difference: $1,120.00. Not in question: $2,240.00. Answers: warehouse lead.
Supplier E, bill W-0457, $385.00, due 17 November 2026: duplicate. Open bills row: Supplier E, W-0457, $385.00, bill date 2 November 2026. Paid bills row: Supplier E, W-0457, $385.00, paid 5 November 2026 by company card. Already paid, so not owed again. Difference: $385.00. Not in question: $0.00. Answers: bookkeeper.
Supplier I, bill 0092, $1,800.00, due 24 November 2026: no purchase order. Billed $1,800.00 for site signage, supply and fit; the order rule needs an order at $500.00 or more and none is quoted. Difference: $1,800.00. Not in question: $0.00. Answers: buyer.

PASSED WITH A NOTE
Supplier G, bill G-1188: within tolerance. Billed 70 laminate panels at $60.00 = $4,200.00; order 2047 has 70 at $59.80 = $4,186.00; difference $14.00 against a tolerance of $83.72. 70 received (R-314).
Supplier D, bill 884-10: movement note. Billed $1,246.30; last paid bill 884-09 was $1,018.75; up $227.55, or 22.3%, against a note level of 10%. No order needed (utility).

CREDITS
Supplier G: owed $4,200.00; credit CN-G-77 -$650.00; net $3,550.00. The run shows the full amount unless the approver says to apply the credit.

PROPOSED RUN
Overdue: none among the ready bills.
Discount: Supplier A, bill A-7731, pay $6,350.40, discount $129.60, pay by 17 November 2026 (2% within 20 days of the bill date, 28 October 2026; full amount $6,480.00, due 27 November 2026).
Due by 25 November 2026: Supplier D, bill 884-10, $1,246.30, due 20 November 2026.
Due by 25 November 2026: Supplier G, bill G-1188, $4,200.00, due 20 November 2026.
Run total as proposed, after discounts taken: $11,796.70. At full bill value: $11,926.30. If the credit is applied: $11,146.70.

NOT YET DUE
Supplier H, bill H-3310, $890.00, due 4 December 2026.

TIE-OUT
In the run at full bill value $11,926.30 + held $7,477.00 + stopped $2,750.00 + not yet due $890.00 = open bills, credit notes excluded $23,043.30.

CASH
$48,200.00, as stated by the bookkeeper on the morning of 10 November 2026 - run after discounts taken $11,796.70 - payroll, Friday 13 November 2026, $21,500.00 = $14,903.30, against a floor of $10,000.00. The run as proposed leaves the account $4,903.30 above the floor. If the stopped bill and the three held bills other than the duplicate ($9,842.00 in total) were all cleared and paid in full before the next run, the balance would be $5,061.30, below the floor.

DECISIONS FOR THE APPROVER
1. Approve or change the proposed run: 3 bills, $11,796.70 after the discount ($11,926.30 at full bill value).
2. Take the Supplier A discount on A-7731: pay $6,350.40 instead of $6,480.00, saving $129.60. The payment has to be made by 17 November 2026, and the discount will have expired by the next run.
3. Apply credit CN-G-77 (-$650.00) to G-1188 or not: pay $4,200.00 in full, or $3,550.00 net. The run total is $11,796.70 without the credit and $11,146.70 with it.
4. Supplier F, F-9034, $2,750.00: stays out until the bookkeeper has verified the bank change by phone. Decide whether, once verified, it is paid ahead of the 26 November run, as it is already past due.
5. Supplier B, 55102, and Supplier C, C-2209: both are held whole. Decide whether to wait for the answers or to release the amounts not in question ($1,842.00 and $2,240.00); that is the owner's decision.
6. Supplier E, W-0457, $385.00: the paid bills show it paid by company card on 5 November 2026. Confirm it is not to be paid again and have the open row cleared by a person in the accounting system.
7. Supplier I, 0092, $1,800.00: decide whether it can go forward once the buyer has said who ordered the work, or whether an order must be raised first.

QUESTIONS
For the buyer: did you agree $2.45 instead of the order price of $2.30 for the 600 wall brackets on Supplier B bill 55102 ($1,470.00 billed against $1,380.00 ordered, $90.00 over)?
For the buyer: who ordered the site signage on Supplier I bill 0092 ($1,800.00), which has no purchase order?
For the warehouse lead: have the remaining 5 extraction fans on order 2044 arrived since receipt R-318 recorded 10 of 15, given that Supplier C bill C-2209 charges for all 15 ($3,360.00)?
For the warehouse lead: which delivery do the damaged panels on Supplier G credit note CN-G-77 (-$650.00) come from, given that the receiving log shows 70 panels received on R-314 and no return?
For the bookkeeper: will you call Supplier F on the phone number in the supplier list to verify the change from the account ending 9026 to the account ending 4471 on bill F-9034 ($2,750.00)?
For the bookkeeper: can you confirm that the company card payment of $385.00 on 5 November 2026 settled Supplier E bill W-0457?
For Supplier B (for the buyer to put): will you issue a credit or corrected bill for the $90.00 on bill 55102 if the order price of $2.30 stands?
For Supplier C (for the buyer or warehouse lead to put): when will the remaining 5 fans be delivered, or will you reissue bill C-2209 for the 10 received ($2,240.00)?
For Supplier G (for the buyer to put): which bill does credit note CN-G-77 (-$650.00) relate to?

OVERDUE BEFORE THE NEXT RUN IF NOT CLEARED
Supplier F, bill F-9034, due 11 November 2026 (stopped; already 1 day late on the run date).
Supplier B, bill 55102, due 13 November 2026 (held).
Supplier C, bill C-2209, due 15 November 2026 (held).
Supplier E, bill W-0457, due 17 November 2026 (held as a duplicate). The paid bills show W-0457, $385.00, paid 5 November 2026 by company card; it is not owed again.
Supplier I, bill 0092, due 24 November 2026 (held).

Status: prepared for approval. Nothing has been paid, sent or changed.
```

## What was observed

**What worked**

- Every part of the output format was produced, in order, ending with the status line.
- The tie-out holds: $11,926.30 + $7,477.00 + $2,750.00 + $890.00 = $23,043.30, the nine open bills with the credit note left out, as the instructions now say.
- The six things planted in the example were all caught: the changed bank details (stopped although the bill matches its order and receipt exactly), the price over, the fans billed above what was received, the bill already paid by card, the bill with no purchase order, and the early-payment discount on a bill due outside the window.
- The credit was shown apart and not subtracted; the run total is given after the discount, at full bill value and with the credit applied.
- The points the first run had to guess were read one way without comment: "In the run" at full bill value, the run total and the cash line after the discount, the discount period counted from the bill date, the amount not in question on the price hold ($1,842.00, the bill at order prices), $0.00 not in question where the whole bill is held, the buyer asked who ordered the signage, the preparation date taken from the settings, and the 7-day window for a possible duplicate reported as a default.
- The duplicate W-0457 is listed under the last heading with what the paid bills show, as the instructions ask.
- No stop condition applied. All four required exports were present, the open bills export was two days older than the run date against a limit of three, the tie-out passed, and nothing in the inputs asked the assistant to pay or change anything. The message printed on bill F-9034 was treated as information about the bill.
- Against the template's reviewer checklist, items 1 to 9 hold on reading the sheet. The approval and the payment are people's steps and were not carried out.
- Every figure agrees with the published example: the same sorting of all nine bills, the same run total, tie-out and cash line.

**Where the instructions were unclear or a guess was needed**

- **What to check a credit note against.** The instructions say how to show a credit and nothing about checking one. The run asked the warehouse lead which delivery the damaged panels came from, since the receiving log shows no return, and wrote a question for Supplier G about which bill the credit relates to. Both are reasonable; neither is asked for.
- **Who puts a question to a supplier.** The instructions say such a question is for a person to put and do not say which person. The run chose the buyer or the warehouse lead.
- **The question about the bank change.** The run addressed it to the bookkeeper ("will you call Supplier F...") and wrote no question under Supplier F's own name. The published example words it as the question the bookkeeper puts to the supplier.
- **Where the due date of a stopped bill goes.** The output format gives a stopped bill no due date. The run added it at the end of the line.
- **Settings with no place on the sheet.** The "Settings used" line has no slot for the limit on charges not on the order, the movement note, the duplicate lookback or the export age limit, and the run left them out. The sheet therefore does not show that the export's age was checked.
- **How much belongs in the cash line and the decisions.** The run added a what-if to the cash line (the balance if every stopped and held bill but the duplicate were cleared and paid before the next run, which would fall below the floor) and wrote seven decisions, three of them about held or stopped bills. The instructions set no limit, and an approver might prefer the shorter list.
- **The sign of a credit.** The run wrote the credit note total as -$650.00; the format does not say whether to show the sign.

**Differences from the published example**

- The example's sheet is laid out with bold headings and bullets. The run kept the plain layout of the output format, as its instructions require.
- The run has seven decisions for the approver and the example has four. The example has no decision lines for the stopped bill, the duplicate or the bill with no purchase order.
- The run asks two questions about the credit note that the example does not ask.
- The run writes the bank-change question to the bookkeeper; the example writes it as the question for Supplier F. The example asks Supplier B and Supplier C in one line; the run asks each separately.
- The example asks the buyer whether an order should be raised for the signage; the run asks only who ordered it and leaves the order to the approver's decisions.
- The run adds the what-if to the cash line. The example gives the cash line with and without the credit applied; the run gives it without.
- The run writes the credit note total as -$650.00; the example writes $650.00.
- The example notes that W-0431, last month's bill for the same amount, is not a duplicate. The run did not say so.
- The example repeats "credit notes excluded" beside the open bills total in "The picture"; the run says it on the tie-out line only.

**Shortcomings of this trial**

- One run, one model, one product, on the inputs the template's own example was written around. It says nothing about messier exports, different column names or a longer list of bills.
- It is a second run after the template was revised in answer to the first. It shows the revised wording was read as intended once; it does not show the wording is clear to every reader or every product.
- Several paths were not exercised: a missing export, an export past the age limit, a failed tie-out, a bill whose lines do not add up, a supplier missing from the supplier list, a possible duplicate with no bill number, a charge not on the order, an order not found, a cash line below the floor or not supplied, a credit larger than what is owed, and a request to pay or to change bank details.
- The inputs were pasted as text. Nothing was read from a spreadsheet file, where arithmetic over many rows is more likely to go wrong.
- The instructions and output format were followed as written text in a session, not installed as a packaged version.
- Nobody played the owner, the buyer, the warehouse lead or the bookkeeper, so the approval, the phone check and the answers were not carried out.
