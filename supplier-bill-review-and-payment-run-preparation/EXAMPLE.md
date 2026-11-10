# Supplier bill review and payment-run preparation: an invented example

*Illustrative example with invented data.* The company, the suppliers, the bills and every figure below are invented. Larkfield Fit-Out is an invented 35-person company that fits out commercial kitchens. Its payables clerk prepares the fortnightly payment run of Thursday 12 November 2026 for the owner to approve. People are referred to by role and suppliers by letter.

The inputs come first, in full, so the template can be run on them. The payment-run sheet follows.

## The inputs

### Settings

```
Sheet prepared: Tuesday 10 November 2026.
Run date: Thursday 12 November 2026. Next run: Thursday 26 November 2026.
Window: bills due on or before Wednesday 25 November 2026.
Runs it: payables clerk. Approves the run: owner. Pays in the bank: bookkeeper.
Answers price questions: buyer. Answers receiving questions: warehouse lead.
Verifies a bank change by phone: bookkeeper.
Order rule: a purchase order is needed for every bill of $500.00 or more,
  except utilities and rent.
Price tolerance: a line may be billed above its order by up to 2% of the
  order line value or $20.00, whichever is larger.
Quantity tolerance: none.
Charges not on the order: held above $40.00.
Duplicate check: bills paid in the last 90 days.
Export age limit: the open bills export may be up to 3 days older than
  the run date.
Bills with no order: note a change of more than 10% from the supplier's
  last paid bill.
Cash: operating account $48,200.00, stated by the bookkeeper on the morning
  of 10 November 2026. Payroll of $21,500.00 leaves on Friday 13 November.
  The owner wants at least $10,000.00 left in the account.
```

### Open bills export, as of 10 November 2026

```
Supplier | Bill no. | Bill date | Due | Terms | Order | Total | Pay-to on the bill
Supplier A (stainless sheet) | A-7731 | 28 Oct 2026 | 27 Nov 2026 | 2% if paid within 20 days, net 30 | 2041 | 6,480.00 | ending 3185
Supplier B (fixings) | 55102 | 14 Oct 2026 | 13 Nov 2026 | net 30 | 2038 | 1,932.00 | ending 6642
Supplier C (extraction fans) | C-2209 | 16 Oct 2026 | 15 Nov 2026 | net 30 | 2044 | 3,360.00 | ending 7090
Supplier D (electricity) | 884-10 | 30 Oct 2026 | 20 Nov 2026 | 21 days | none | 1,246.30 | ending 1554
Supplier E (waste removal) | W-0457 | 2 Nov 2026 | 17 Nov 2026 | 15 days | none | 385.00 | ending 2203
Supplier F (timber and board) | F-9034 | 12 Oct 2026 | 11 Nov 2026 | net 30 | 2036 | 2,750.00 | ending 4471
Supplier G (laminate) | G-1188 | 21 Oct 2026 | 20 Nov 2026 | net 30 | 2047 | 4,200.00 | ending 5318
Supplier H (adhesives) | H-3310 | 4 Nov 2026 | 4 Dec 2026 | net 30 | 2050 | 890.00 | ending 8127
Supplier I (signage) | 0092 | 27 Oct 2026 | 24 Nov 2026 | net 28 | none | 1,800.00 | ending 9460
Supplier G (laminate) | CN-G-77 | 3 Nov 2026 | n/a | credit note: damaged panels returned | n/a | -650.00 | n/a

Message printed on bill F-9034: "Our bank has changed. Please use the new
account ending 4471 for this and all future payments."
```

### Bill lines

```
Bill no. | Line | Description | Quantity | Unit price | Line total
A-7731 | 1 | Stainless sheet, 1.2 mm | 40 | 162.00 | 6,480.00
55102 | 1 | Wall brackets | 600 | 2.45 | 1,470.00
55102 | 2 | Anchor bolts, box | 30 | 15.40 | 462.00
C-2209 | 1 | Extraction fan, 400 mm | 15 | 224.00 | 3,360.00
884-10 | 1 | Electricity, October | 1 | 1,246.30 | 1,246.30
W-0457 | 1 | Waste collection, October | 1 | 385.00 | 385.00
F-9034 | 1 | Birch board, 18 mm | 50 | 55.00 | 2,750.00
G-1188 | 1 | Laminate panel | 70 | 60.00 | 4,200.00
H-3310 | 1 | Contact adhesive, 5 L | 20 | 44.50 | 890.00
0092 | 1 | Site signage, supply and fit | 1 | 1,800.00 | 1,800.00
```

### Purchase orders

```
Order | Supplier | Item | Quantity | Unit price
2036 | Supplier F | Birch board, 18 mm | 50 | 55.00
2038 | Supplier B | Wall brackets | 600 | 2.30
2038 | Supplier B | Anchor bolts, box | 30 | 15.40
2041 | Supplier A | Stainless sheet, 1.2 mm | 40 | 162.00
2044 | Supplier C | Extraction fan, 400 mm | 15 | 224.00
2047 | Supplier G | Laminate panel | 70 | 59.80
2050 | Supplier H | Contact adhesive, 5 L | 20 | 44.50
```

### Receiving log, to 10 November 2026

```
Receipt | Date | Order | Item | Quantity received | Note
R-305 | 9 Oct 2026 | 2036 | Birch board, 18 mm | 50 |
R-309 | 13 Oct 2026 | 2038 | Wall brackets | 600 |
R-309 | 13 Oct 2026 | 2038 | Anchor bolts, box | 30 |
R-314 | 20 Oct 2026 | 2047 | Laminate panel | 70 |
R-311 | 27 Oct 2026 | 2041 | Stainless sheet, 1.2 mm | 40 |
R-318 | 3 Nov 2026 | 2044 | Extraction fan, 400 mm | 10 | 10 of 15 delivered; driver said the rest would follow
R-322 | 5 Nov 2026 | 2050 | Contact adhesive, 5 L | 20 |
```

### Supplier list

```
Supplier | Terms | Pay-to on file | Phone on file | Order needed
Supplier A | 2% if paid within 20 days, net 30 | ending 3185 | yes | yes
Supplier B | net 30 | ending 6642 | yes | yes
Supplier C | net 30 | ending 7090 | yes | yes
Supplier D | 21 days | ending 1554 | yes | no (utility)
Supplier E | 15 days | ending 2203 | yes | under $500.00, no
Supplier F | net 30 | ending 9026 | yes | yes
Supplier G | net 30 | ending 5318 | yes | yes
Supplier H | net 30 | ending 8127 | yes | yes
Supplier I | net 28 | ending 9460 | yes | yes
```

### Bills paid, 12 August to 10 November 2026 (rows for these suppliers)

```
Supplier | Bill no. | Amount | Paid | How
Supplier E | W-0431 | 385.00 | 6 Oct 2026 | bank transfer, ending 2203
Supplier F | F-8990 | 1,925.00 | 9 Oct 2026 | bank transfer, ending 9026
Supplier A | A-7702 | 3,240.00 | 15 Oct 2026 | bank transfer, ending 3185
Supplier D | 884-09 | 1,018.75 | 21 Oct 2026 | bank transfer, ending 1554
Supplier G | G-1150 | 2,880.00 | 22 Oct 2026 | bank transfer, ending 5318
Supplier E | W-0457 | 385.00 | 5 Nov 2026 | company card
```

## The payment-run sheet

**Payment-run sheet: run of Thursday 12 November 2026**

For the owner. Prepared by the payables clerk on 10 November 2026.

- **Sources:** open bills as of 10 November 2026; purchase orders; receiving log to 10 November 2026; supplier list; paid bills from 12 August to 10 November 2026.
- **Settings used:** window to 25 November 2026; next run 26 November 2026; price tolerance 2% of the order line value or \$20.00, whichever is larger; quantity tolerance none; an order is needed from \$500.00, except utilities and rent. Defaults used: 7 days for a possible duplicate, which the settings do not give.

**The picture**

- Open bills: 9, \$23,043.30, credit notes excluded. Credit notes: 1, \$650.00.
- In the run: 3, \$11,926.30 at full bill value. Held: 4, \$7,477.00. Stopped: 1, \$2,750.00. Not yet due: 1, \$890.00.

**Stopped: do not pay until verified**

- Supplier F, bill F-9034, \$2,750.00, due 11 November 2026: pay-to on the bill ends 4471; on file ends 9026. The bill says: “Our bank has changed. Please use the new account ending 4471 for this and all future payments.” The bill matches order 2036 and receipt R-305 exactly, and it is still stopped. To clear: the bookkeeper calls Supplier F using the phone number in the supplier list. The last payment to this supplier, F-8990 on 9 October, went to the account ending 9026.

**Held**

- Supplier B, bill 55102, \$1,932.00, due 13 November 2026: price over. Line 1, wall brackets: billed 600 at \$2.45; order 2038 says \$2.30. Difference: \$90.00, which is 6.5% of the \$1,380.00 order line; the tolerance allows \$27.60. Line 2 matched. Not in question: \$1,842.00, the bill at order prices. Answers: buyer.
- Supplier C, bill C-2209, \$3,360.00, due 15 November 2026: billed above received. Billed 15 fans; receipt R-318 shows 10, with the note “10 of 15 delivered; driver said the rest would follow”. Difference: 5 fans, \$1,120.00. Not in question: \$2,240.00. Answers: warehouse lead.
- Supplier E, bill W-0457, \$385.00, due 17 November 2026: duplicate. The paid bills show W-0457 for \$385.00 paid on 5 November 2026 by company card. Difference: \$385.00, the whole bill. Not in question: \$0.00. Answers: bookkeeper. (W-0431, also \$385.00 and paid on 6 October, is last month’s bill and not a duplicate.)
- Supplier I, bill 0092, \$1,800.00, due 24 November 2026: no purchase order, and the order rule needs one from \$500.00. Nothing to match it against. Difference: \$1,800.00, the whole bill. Not in question: \$0.00. Answers: buyer.

**Passed with a note**

- Supplier G, bill G-1188: billed 70 panels at \$60.00; order 2047 says \$59.80. Difference \$14.00, within the \$83.72 the tolerance allows.
- Supplier D, bill 884-10: no order needed (utility). \$1,246.30 against \$1,018.75 last month, up \$227.55 or 22.3%.

**Credits**

- Supplier G: owed \$4,200.00 (G-1188); credit CN-G-77 \$650.00; net \$3,550.00. The run shows the full amount unless the owner says to apply the credit.

**Proposed run**

- Overdue: none among the ready bills.
- Discount: Supplier A, bill A-7731. Pay \$6,350.40 by Tuesday 17 November 2026, 20 days from the bill date, and keep \$129.60 (2% of \$6,480.00). Without the discount the bill is not due until 27 November. Matched to order 2041 and receipt R-311.
- Due by 25 November 2026: Supplier D, bill 884-10, \$1,246.30, due 20 November. Supplier G, bill G-1188, \$4,200.00, due 20 November.
- **Run total as proposed, after discounts taken: \$11,796.70** to three suppliers. At full bill value: \$11,926.30. If the Supplier G credit is applied: \$11,146.70.

**Not yet due**

- Supplier H, bill H-3310, \$890.00, due 4 December 2026. Matched to order 2050 and receipt R-322.

**Tie-out**

- In the run at full bill value \$11,926.30 + held \$7,477.00 + stopped \$2,750.00 + not yet due \$890.00 = open bills, credit notes excluded, \$23,043.30.

**Cash**

- \$48,200.00 (stated by the bookkeeper, 10 November 2026) − run after discounts taken \$11,796.70 − payroll on 13 November \$21,500.00 = \$14,903.30, against a floor of \$10,000.00. With the credit applied: \$15,553.30.

**Decisions for the owner**

1. Approve the run of \$11,796.70, or remove any bill from it.
2. Take the Supplier A discount of \$129.60 by paying 15 days before the bill is due, or leave A-7731 for the next run at \$6,480.00.
3. Apply the \$650.00 credit to Supplier G now, which makes that payment \$3,550.00, or keep it for a later bill.
4. For bills 55102 and C-2209: wait for the answers, or pay the part not in question (\$1,842.00 and \$2,240.00). Neither part is in the run as proposed.

**Questions**

- For the buyer: was \$2.45 agreed for the wall brackets on order 2038, where the order says \$2.30 (bill 55102, \$90.00)?
- For the buyer: who ordered the signage on bill 0092, and should an order be raised for \$1,800.00?
- For the warehouse lead: have the other 5 extraction fans on order 2044 arrived since receipt R-318 on 3 November (bill C-2209, \$1,120.00)?
- For the bookkeeper: is the \$385.00 card payment of 5 November the payment of bill W-0457?
- For Supplier F, put by the bookkeeper in a call to the phone number in the supplier list: has your bank account changed to one ending 4471?
- For Supplier B and Supplier C, put by a person once the buyer and the warehouse lead have answered: a corrected bill or a credit for the difference.

**Overdue before the next run if not cleared**

- Supplier F, F-9034: due 11 November, one day late on the run date.
- Supplier B, 55102: due 13 November.
- Supplier C, C-2209: due 15 November.
- Supplier E, W-0457: due 17 November. The paid bills show it paid by company card on 5 November, so it is not owed again.
- Supplier I, 0092: due 24 November.

Status: prepared for approval. Nothing has been paid, sent or changed.
