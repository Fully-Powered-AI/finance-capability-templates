# Thirteen-week cash flow forecast: an invented example

*Illustrative example with invented data.* The company, the customers, the suppliers, the people and every figure below are invented. Kestrelmoor Signworks is an invented 24-person company that designs, makes and installs signs for shops, offices and hospitals. Its bookkeeper prepares the forecast on Monday 9 November 2026 for the owner. People are referred to by role, and customers and suppliers by letter.

The inputs come first, in full, so the template can be run on them. The forecast follows.

## The inputs

### Settings

```
Business: Kestrelmoor Signworks
Prepared by: bookkeeper, on Monday 9 November 2026. For: owner.
Forecast start: Monday 9 November 2026. Weeks run Monday to Sunday.
Currency: US dollars.
Opening cash: $96,500 at the close of Friday 6 November 2026, operating
  and savings accounts, read by the bookkeeper from online banking.
Floor: $60,000, set by the owner (about two payrolls).
Days late for customers with little history: not set.
```

### Open receivables export, as of 6 November 2026

```
Customer | Invoice | Invoice date | Due date | Balance due
Customer A | 2291 | 2026-10-02 | 2026-11-01 | 18,400
Customer B | 2296 | 2026-10-09 | 2026-11-08 | 9,750
Customer C | 2302 | 2026-10-20 | 2026-11-19 | 26,300
Customer D | 2240 | 2026-07-10 | 2026-08-09 | 4,200
Customer E | 2305 | 2026-10-28 | 2026-11-27 | 7,900
Customer A | 2308 | 2026-11-02 | 2026-12-02 | 14,600
Customer F | 2287 | 2026-09-30 | 2026-10-30 | 0
Customer H | 2299 | 2026-10-14 | 2026-11-13 | 21,900
Customer B | 2310 | 2026-11-04 | 2026-12-04 | 11,300
Customer J | 2304 | 2026-10-26 | 2026-11-25 | 24,500
```

### Paid invoices, last twelve months

```
Customer | Invoice | Due date | Paid date | Amount
Customer A | 2201 | 2026-05-01 | 2026-05-13 | 12,800
Customer A | 2224 | 2026-06-12 | 2026-06-27 | 16,400
Customer A | 2247 | 2026-07-24 | 2026-08-02 | 9,900
Customer A | 2268 | 2026-09-04 | 2026-09-18 | 15,200
Customer B | 2210 | 2026-05-22 | 2026-05-24 | 8,700
Customer B | 2233 | 2026-07-03 | 2026-07-03 | 10,450
Customer B | 2259 | 2026-08-14 | 2026-08-19 | 7,600
Customer B | 2279 | 2026-09-25 | 2026-09-26 | 9,200
Customer C | 2215 | 2026-06-05 | 2026-07-05 | 22,800
Customer C | 2251 | 2026-08-07 | 2026-09-02 | 31,500
Customer C | 2272 | 2026-09-18 | 2026-10-22 | 18,900
Customer D | 2190 | 2026-04-17 | 2026-06-01 | 3,800
Customer D | 2228 | 2026-06-19 | 2026-08-18 | 5,100
Customer E | 2262 | 2026-08-28 | 2026-08-31 | 6,300
Customer H | 2219 | 2026-06-01 | 2026-06-11 | 17,600
Customer H | 2244 | 2026-07-20 | 2026-07-28 | 20,300
Customer H | 2270 | 2026-09-07 | 2026-09-16 | 19,800
Customer J | 2222 | 2026-06-08 | 2026-06-14 | 14,200
Customer J | 2249 | 2026-07-27 | 2026-08-01 | 21,700
Customer J | 2276 | 2026-09-21 | 2026-09-28 | 18,300
```

### Committed sales not yet invoiced

```
Customer | Work | Amount | Invoice date | Terms (days) | Committed by
Customer C | Hospital wayfinding, phase 2 | 38,500 | 2026-11-27 | 30 | signed order
Customer G | Shopfront fascia and lettering | 12,800 | 2026-11-20 | 14 | deposit received
Customer B | Vehicle livery, six vans | 9,600 | 2026-12-11 | 30 | purchase order
Customer A | Retail rollout, first seven stores | 26,000 | 2026-12-04 | 30 | purchase order
Customer A | Retail rollout, last seven stores | 26,000 | 2027-01-08 | 30 | purchase order
Customer H | Office reception signs | 16,200 | 2026-11-27 | 30 | signed order
```

### Pipeline

```
Customer | Work | Amount | Stage
Customer K | Museum gallery signs | 45,000 | proposal sent
```

### Open payables export, as of 6 November 2026

```
Supplier | Bill | Due date | Balance due
Supplier A (acrylic and aluminium sheet) | A-5521 | 2026-11-12 | 11,240
Supplier B (LED modules) | 88140 | 2026-11-20 | 6,980
Supplier C (vinyl and film) | C-3307 | 2026-11-03 | 2,450
Supplier D (installation crew) | D-118 | 2026-12-05 | 8,600
Supplier E (powder coating) | E-2049 | 2026-11-26 | 3,175
```

### Recurring list

```
Item | In or out | Category | Amount | Frequency | Next date | Source
Payroll (net pay, payroll taxes, benefits) | out | payroll | 28,400 | every 2 weeks | 2026-11-18 | payroll records
Rent | out | rent | 6,800 | monthly | 2026-12-01 | lease
Equipment loan | out | loan or lease | 2,150 | monthly | 2026-11-15 | loan statement
Software subscriptions | out | subscriptions | 1,340 | monthly | 2026-11-23 | card and bank statements
Utilities and phones | out | other | 1,100 | monthly | 2026-11-24 | bank statements
Maintenance plans, collected by direct debit | in | recurring receipt | 7,400 | monthly | 2026-12-05 | bank statements
```

### Other known items

```
Item | In or out | Category | Amount | Date
Deposit on a new wide-format printer | out | other | 14,000 | 2026-12-10
Year-end staff bonus | out | payroll | 8,500 | 2026-12-18
Materials and installers for committed orders (owner's estimate) | out | purchases for committed work | 9,500 | 2026-12-15
Materials and installers for committed orders (owner's estimate) | out | purchases for committed work | 12,000 | 2027-01-12
Estimated tax payment, fourth quarter | out | taxes | 9,000 | 2027-01-15
```

### Card statements not yet paid

```
Card | Amount | Payment date
Company card, November statement | 3,860 | 2026-11-25
```

### Paid bills, August to October 2026

```
Supplier | Amount | Paid date
Supplier A | 7,320 | 2026-08-14
Supplier F (van leases) | 1,480 | 2026-08-28
Supplier A | 9,870 | 2026-09-14
Supplier F (van leases) | 1,480 | 2026-09-28
Supplier A | 12,410 | 2026-10-13
Supplier F (van leases) | 1,480 | 2026-10-28
```

## The forecast

**Thirteen-week cash flow forecast: Kestrelmoor Signworks, weeks of 9 November 2026 to 1 February 2027**

- **For:** Owner. **Prepared by:** Bookkeeper on Monday 9 November 2026.
- **Opening cash:** \$96,500 at the close of Friday 6 November 2026, operating and savings accounts, as stated by the bookkeeper from online banking.
- **Floor:** \$60,000, set by the owner.
- **Sources:** settings of 9 November 2026; open receivables as of 6 November 2026 (10 rows); paid invoices for the twelve months to 6 November 2026 (20 rows); committed sales (6 rows); pipeline (1 row); open payables as of 6 November 2026 (5 rows); recurring list (6 rows); other known items (5 rows); card statements (1 row); paid bills, August to October 2026 (6 rows).
- **Not supplied:** none.
- **Defaults used:** 16 days late for customers with fewer than three paid invoices (Customers D, E and G), the average across all 20 paid invoices supplied, rounded up, because the settings give no figure.

**Status**

Above zero in all 13 weeks; below the \$60,000 floor in weeks 8, 10 and 11; lowest \$46,665 in week 8.

**The grid**

Amounts in US dollars, whole units. Negative amounts in brackets. A cell with nothing in it shows -.

| | W1 9 Nov | W2 16 Nov | W3 23 Nov | W4 30 Nov | W5 7 Dec | W6 14 Dec | W7 21 Dec | W8 28 Dec | W9 4 Jan | W10 11 Jan | W11 18 Jan | W12 25 Jan | W13 1 Feb | Total |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Opening cash | 96,500 | 108,810 | 95,330 | 85,855 | 85,255 | 79,155 | 84,305 | 81,865 | 46,665 | 70,265 | 54,315 | 51,875 | 61,975 | |
| Invoices already issued | 28,150 | 21,900 | - | 35,800 | 7,900 | 40,900 | - | - | - | - | - | - | - | 134,650 |
| Committed sales | - | - | - | - | - | 12,800 | - | - | 16,200 | 35,600 | - | 38,500 | - | 103,100 |
| Recurring receipts | - | - | - | 7,400 | - | - | - | - | 7,400 | - | - | - | 7,400 | 22,200 |
| Other receipts | - | - | - | - | - | - | - | - | - | - | - | - | - | - |
| **Total in** | 28,150 | 21,900 | - | 43,200 | 7,900 | 53,700 | - | - | 23,600 | 35,600 | - | 38,500 | 7,400 | 259,950 |
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
| **Total out** | 15,840 | 35,380 | 9,475 | 43,800 | 14,000 | 48,550 | 2,440 | 35,200 | - | 51,550 | 2,440 | 28,400 | 6,800 | 293,875 |
| Net change | 12,310 | (13,480) | (9,475) | (600) | (6,100) | 5,150 | (2,440) | (35,200) | 23,600 | (15,950) | (2,440) | 10,100 | 600 | (33,925) |
| **Closing cash** | 108,810 | 95,330 | 85,855 | 85,255 | 79,155 | 84,305 | 81,865 | 46,665 | 70,265 | 54,315 | 51,875 | 61,975 | 62,575 | |
| Closing, no new sales | 108,810 | 95,330 | 85,855 | 85,255 | 79,155 | 81,005 | 78,565 | 43,365 | 50,765 | 11,215 | 8,775 | (19,625) | (19,025) | |
| Closing, two largest customers four weeks late | 90,410 | 76,930 | 67,455 | 66,855 | 79,155 | 43,405 | 40,965 | 5,765 | 29,365 | 28,315 | 25,875 | (2,525) | (1,925) | |

**What the grid shows**

- **Lowest point:** week 8 (28 December to 3 January), \$46,665. Payments that week: payroll \$28,400 on 30 December; rent \$6,800 on 1 January. Receipts expected that week: none.
- **Weeks below the floor:** week 8 (\$46,665), week 10 (\$54,315), week 11 (\$51,875).
- **Weeks below zero:** none.
- **No new sales** (no sales beyond the invoices already issued, so committed sales are removed too): below the floor from week 8; below zero from week 12 (25 to 31 January); lowest (19,625) in week 12.
- **Two largest customers four weeks late** (Customer C, \$64,800; Customer A, \$59,000 expected in the 13 weeks): below the floor from week 6; below zero in weeks 12 and 13; lowest (2,525) in week 12. Moved: Customer A, invoice 2291, \$18,400, week 1 to week 5; Customer C, invoice 2302, \$26,300, week 6 to week 10; Customer A, invoice 2308, \$14,600, week 6 to week 10; Customer A, retail rollout, first seven stores, \$26,000, week 10 to after week 13; Customer C, hospital wayfinding, phase 2, \$38,500, week 12 to after week 13. Falling after week 13: \$64,500.

**Assumptions**

- **A1.** Opening cash is \$96,500, read by the bookkeeper from online banking at the close of Friday 6 November, operating and savings accounts. Nothing is assumed to have been received or paid between then and the forecast start on Monday 9 November. Affects: every week.
- **A2.** Each invoice arrives on its due date plus the customer's average days late over its last six paid invoices (all of them where it has fewer), rounded up to a whole day. Customers with fewer than three paid invoices (D, E and G) use the default of 16 days. Affects: receipts in weeks 1, 2, 4, 5, 6, 9, 10 and 12.
- **A3.** Only the six orders on the committed list count as sales, each invoiced on the date given and due on its terms; the \$45,000 pipeline proposal is not counted. Work not yet won is not in the forecast, so receipts thin out in the later weeks. Affects: weeks 6, 9, 10 and 12.
- **A4.** Supplier bills are paid on their due dates; C-3307, already past due, is paid in week 1. Affects: weeks 1 to 4.
- **A5.** Recurring payments and receipts follow the recurring list's amounts and dates; payroll is the payroll records' figure, including payroll taxes and benefits. Affects: every week.
- **A6.** Other known items and the card statement are paid on the dates given; the purchases for committed work are the owner's estimate. Affects: weeks 3, 5, 6 and 10.
- **A7.** Payments on no list are not in the forecast, including those raised under Questions. Affects: every week.
- **A8.** Default: 16 days late for customers with fewer than three paid invoices, the average across all 20 paid invoices supplied, rounded up. Their own paid invoices: Customer D, 45 and 60 days late; Customer E, 3 days late; Customer G, none paid. Affects: receipts in weeks 5 and 6.

**Receipts placed**

- **Invoices already issued:**
  - Customer A, invoice 2291, \$18,400, due 1 November: 13 days late (average of 4 paid invoices), expected 14 November, week 1.
  - Customer B, invoice 2296, \$9,750, due 8 November: 2 days late (average of 4 paid invoices), expected 10 November, week 1.
  - Customer H, invoice 2299, \$21,900, due 13 November: 9 days late (average of 3 paid invoices), expected 22 November, week 2.
  - Customer J, invoice 2304, \$24,500, due 25 November: 6 days late (average of 3 paid invoices), expected 1 December, week 4.
  - Customer B, invoice 2310, \$11,300, due 4 December: 2 days late (average of 4 paid invoices), expected 6 December, week 4.
  - Customer E, invoice 2305, \$7,900, due 27 November: 16 days late (fewer than three paid invoices, default), expected 13 December, week 5.
  - Customer C, invoice 2302, \$26,300, due 19 November: 30 days late (average of 3 paid invoices), expected 19 December, week 6.
  - Customer A, invoice 2308, \$14,600, due 2 December: 13 days late (average of 4 paid invoices), expected 15 December, week 6.
- **Committed sales:**
  - Customer G, shopfront fascia and lettering, \$12,800, invoiced 20 November on 14 days, due 4 December: 16 days late (fewer than three paid invoices, default), expected 20 December, week 6.
  - Customer H, office reception signs, \$16,200, invoiced 27 November on 30 days, due 27 December: 9 days late (average of 3 paid invoices), expected 5 January, week 9.
  - Customer B, vehicle livery, six vans, \$9,600, invoiced 11 December on 30 days, due 10 January: 2 days late (average of 4 paid invoices), expected 12 January, week 10.
  - Customer A, retail rollout, first seven stores, \$26,000, invoiced 4 December on 30 days, due 3 January: 13 days late (average of 4 paid invoices), expected 16 January, week 10.
  - Customer C, hospital wayfinding, phase 2, \$38,500, invoiced 27 November on 30 days, due 27 December: 30 days late (average of 3 paid invoices), expected 26 January, week 12.
- **Recurring receipts:** maintenance plans, collected by direct debit, \$7,400, monthly: 5 December (week 4), 5 January (week 9), 5 February (week 13).
- **Other receipts:** none.

**Not counted**

- **Past its usual timing:** Customer D, invoice 2240, \$4,200, due 9 August 2026, expected 25 August 2026 by the rule.
- **After week 13:** Customer A, retail rollout, last seven stores, \$26,000, invoiced 8 January on 30 days, expected 20 February 2027.
- **Pipeline:** Customer K, museum gallery signs, \$45,000, proposal sent.
- **Rows with a blank or nothing to say they are firm:** none.

**Payments placed**

- **Supplier bills:**
  - Supplier A, A-5521, \$11,240, due 12 November, week 1.
  - Supplier C, C-3307, \$2,450, due 3 November, past due, week 1.
  - Supplier B, 88140, \$6,980, due 20 November, week 2.
  - Supplier E, E-2049, \$3,175, due 26 November, week 3.
  - Supplier D, D-118, \$8,600, due 5 December, week 4.
- **Recurring:**
  - Payroll, \$28,400, every 2 weeks: 18 November (week 2), 2 December (week 4), 16 December (week 6), 30 December (week 8), 13 January (week 10), 27 January (week 12).
  - Rent, \$6,800, monthly: 1 December (week 4), 1 January (week 8), 1 February (week 13).
  - Equipment loan, \$2,150, monthly: 15 November (week 1), 15 December (week 6), 15 January (week 10).
  - Software subscriptions, \$1,340, monthly: 23 November (week 3), 23 December (week 7), 23 January (week 11).
  - Utilities and phones, \$1,100, monthly: 24 November (week 3), 24 December (week 7), 24 January (week 11).
- **Other known items:**
  - Deposit on a new wide-format printer, \$14,000, 10 December, week 5.
  - Year-end staff bonus, \$8,500, 18 December, week 6 (in the Payroll row).
  - Materials and installers for committed orders, \$9,500, 15 December, week 6 (in the Purchases for committed work row).
  - Materials and installers for committed orders, \$12,000, 12 January, week 10 (in the Purchases for committed work row).
  - Estimated tax payment, fourth quarter, \$9,000, 15 January, week 10 (in the Taxes row).
- **Card statements:** company card, November statement, \$3,860, 25 November, week 3.
- **Payments after week 13:** none.

**Checks**

- **Tie-out:** \$96,500 + \$259,950 − \$293,875 = \$62,575, week 13's closing cash.
- **Each week opens at the previous week's closing cash:** yes.
- **Invoices already issued:** \$138,850 = \$134,650 placed + \$0 after week 13 + \$4,200 not counted; 1 row with nothing left to pay left out (Customer F, invoice 2287).
- **Committed sales:** \$129,100 = \$103,100 placed + \$26,000 after week 13 + \$0 not counted.
- **Supplier bills:** \$32,445 = \$32,445 placed + \$0 after week 13.

**Owner's cases**

None requested.

**Questions for the owner**

1. Customer D's invoice 2240, \$4,200, was due on 9 August and is past its usual timing, so it is not counted: has a payment date been agreed?
2. Supplier F (van leases) was paid \$1,480 on 28 August, 28 September and 28 October and is not on the recurring list: if it continues, it falls on 28 November (week 3), 28 December (week 8) and 28 January (week 12). Should it be added?
3. No line covers sales tax: is a sales tax payment due between 9 November 2026 and 7 February 2027, and if so, how much and when?
4. No line covers insurance: is an insurance premium due between 9 November 2026 and 7 February 2027, and if so, how much and when?

**Decisions this forecast informs**

1. Week 8 (28 December to 3 January) closes below the \$60,000 floor at \$46,665, with payroll of \$28,400 on 30 December and rent of \$6,800 on 1 January and no receipts expected.
2. Weeks 10 and 11 close below the \$60,000 floor: week 10 (11 to 17 January) at \$54,315, with payroll of \$28,400, \$12,000 of purchases for committed work, the \$9,000 tax estimate and the \$2,150 loan payment, against \$35,600 of committed-sales receipts; week 11 (18 to 24 January) at \$51,875, with software subscriptions of \$1,340 and utilities and phones of \$1,100 and no receipts expected.
3. With no sales beyond the invoices already issued, cash falls below the floor from week 8 and below zero from week 12 (25 to 31 January), lowest (19,625) in week 12; the payroll of \$28,400 on 27 January falls in that week.
4. If Customer C and Customer A each pay four weeks later than their history shows, cash falls below the floor from week 6 and below zero in weeks 12 and 13, lowest (2,525) in week 12, and \$64,500 of their receipts falls after week 13.

The owner decides whether and how to act on each.

**Next run**

Monday 16 November 2026, from the opening balance at the close of Friday 13 November and fresh exports. Week 1 drops off and a new week 13 (8 to 14 February 2027) is added.

Prepared for the owner. It informs a decision and makes none. Nothing has been paid, moved, sent or changed. Where it will back a loan, a payment to the owners or a decision to take on staff, the company's accountant reviews it first.
