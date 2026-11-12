# Journal entry preparation: an invented example

*Illustrative example with invented data.* The studio, its suppliers and customers, every account, document and figure below are invented. Harrow Lane Studio is an invented 30-person brand and product design studio. Its staff accountant prepares the October 2026 entries; its controller reviews them, and its finance director approves the larger ones. People are referred to by role, suppliers and customers by letter.

The inputs come first, in full, so the template can be run on them. The package the workflow template should return follows; the trial record published with it shows what one run actually produced.

## The inputs

### 1. Settings

```
Organization: Harrow Lane Studio.
Period: October 2026, 1 to 31 October 2026. Status: open.
September 2026: closed.
Package prepared: Monday 2 November 2026.
Prepares entries: staff accountant. Reviews: controller.
Posts approved entries and sets up reversals: staff accountant.
Approval limits: entries up to $10,000.00, controller; entries above
  $10,000.00, finance director; any correction of an entry in a closed
  period, finance director, whatever the amount.
Depreciation start rule: depreciation starts in the first full calendar
  month an asset is in service.
Questions about freelance and project costs: studio lead.
Questions about accounting treatment: controller.
(No round-amount size, entry date or reversal date given.)
```

### 2. Entry request list

```
Ref,What it records,Kind,Debit,Credit,Basis,Support,Reverses
R1,IT support contractor October services; invoice not yet received,accrual,6420,2150,Monthly fee per agreement,S1,No
R2,October share of the annual insurance premium,prepaid release,6310,1410,Per prepaid schedule,S2,No
R3,October depreciation on computer equipment,depreciation,6510,1590,Per asset register,S3,No
R4,October share of the Client K retainer billed in advance,deferred revenue release,2300,4100,Per billing record,S4,No
R5,Software subscription posted to IT services in September,correction,6430,6420,Reverse JE-0917 and enter it on the right account,S5,No
R6,Freelance photographer for the October shoot; invoice not yet received,accrual,6260,2150,Estimate 2500.00,Email from the studio lead,Yes
R7,Utility U October electricity; bill not yet received,accrual,6440,2150,640.00 per last month's bill,S6,Yes
```

### 3. Chart of accounts export

```
Account,Name,Type,Status
1010,Operating bank,Asset,Active
1410,Prepaid expenses,Asset,Active
1510,Computer equipment,Asset,Active
1590,Accumulated depreciation,Asset,Active
2000,Accounts payable,Liability,Active
2150,Accrued expenses,Liability,Active
2300,Deferred revenue,Liability,Active
4100,Fee revenue,Revenue,Active
6260,Freelance production,Expense,Active
6310,Insurance,Expense,Active
6420,IT services,Expense,Active
6430,Software subscriptions,Expense,Active
6440,Utilities,Expense,Active
6450,Telephone,Expense,Inactive
6510,Depreciation,Expense,Active
```

### 4. Posted lines this period (revenue and expense accounts named on the requests)

```
Date,Entry,Account,Memo,Amount
2026-10-01,JE-0931R,6420,Reversal of JE-0931: Supplier T September support accrual,-4200.00
2026-10-05,BILL-1031,6420,Supplier T September support,4200.00
2026-10-14,BILL-1037,6430,Software vendor M monthly seats,312.00
2026-10-30,BILL-1043,6440,Utility U October electricity,640.00
```

### 5. Supporting documents

```
S1. IT support agreement with Supplier T (extract)
Services: helpdesk and device management for the studio.
Fee: $4,200.00 a month, invoiced in arrears by the 5th of the following
month.
October service log from Supplier T, sent 30 October 2026: 27 tickets
closed; on-site visits on 8 and 22 October.

S2. Prepaid schedule (extract)
Item: business insurance policy, annual premium.
Paid: 1 August 2026. Amount: $9,600.00.
Covers: 1 August 2026 to 31 July 2027, 12 months. Monthly: $800.00.
Released to 30 September 2026: $1,600.00.

S3. Asset register, computer equipment (extract)
Asset,Description,In service,Cost,Residual,Life (months),Accumulated to 30 Sep 2026,Method
CE-01,Design workstations (8),2025-03-01,19200.00,0.00,48,7600.00,Straight line
CE-02,Laptops (12),2026-02-01,21600.00,0.00,36,4800.00,Straight line
CE-03,Large-format plotter,2026-10-20,6300.00,300.00,60,0.00,Straight line
CE-04,File server,2021-09-01,4800.00,0.00,48,4800.00,Straight line

S4. Billing record
Invoice INV-2207 to Client K, dated 1 October 2026, $18,000.00.
Retainer for brand design services, October to December 2026, in three
equal months. Posted at billing to 2300 Deferred revenue.

S5. Posted entry JE-0917, dated 18 September 2026
Dr 6420 IT services        1,188.00
Cr 2000 Accounts payable   1,188.00
Memo: Supplier P rendering software, September usage. Invoice P-0918.

S6. Utility U bill for September 2026
Service period 1 to 30 September 2026. Amount due: $640.00.
```

## The package

```
JOURNAL ENTRIES FOR REVIEW: Harrow Lane Studio, October 2026

For: controller. Prepared by: staff accountant on 2 November 2026. Entry date: 31 October 2026. Reversal date: 1 November 2026.
Sources: entry requests, 7; chart of accounts, 15 accounts; posted lines this period, 4; supporting documents, 6: S1, S2, S3, S4, S5, S6.
Settings used: round-amount size $500.00; depreciation start rule: first full calendar month an asset is in service; approval limits: as supplied. Defaults used: round-amount size; entry date; reversal date.

SUMMARY
Requests: 7. Ready for review: 5 (R1, R2, R3, R4, R5). Held: 1 (R6). No entry needed: 1 (R7).
Ready for review: debits $14,376.00, credits $14,376.00.
Entries flagged: 3 (R1, R5, R6). Questions: 3.

ENTRY R1: IT support contractor October services; invoice not yet received
Status: Ready for review.
Kind: accrual. Date: 31 October 2026. Reverses: no.
Lines:
  Dr 6420 IT services             $4,200.00
  Cr 2150 Accrued expenses        $4,200.00
  Totals: debits $4,200.00, credits $4,200.00.
Memo: October 2026: IT support from Supplier T for October, invoice not yet received. Per S1.
Calculation: monthly fee $4,200.00 (S1). Already booked $0.00. $4,200.00 - $0.00 = $4,200.00.
Already booked this period: none. Not counted: JE-0931R (-$4,200.00) and BILL-1031 ($4,200.00) in 6420, both for September's service.
Support: S1: the agreement with Supplier T sets a fee of $4,200.00 a month, invoiced in arrears; its October service log shows 27 tickets closed and visits on 8 and 22 October.
Checks: balanced yes; one side per line, no negative amounts yes; accounts in the chart and active yes; accounts fit the kind yes.
Flags: accrual not set to reverse: the request says No, while last month's accrual for the same supplier, JE-0931, reversed on 1 October (JE-0931R).
Approver: controller, under the limit for entries up to $10,000.00. Posted by: staff accountant, after approval.

ENTRY R2: October share of the annual insurance premium
Status: Ready for review.
Kind: prepaid release. Date: 31 October 2026. Reverses: no.
Lines:
  Dr 6310 Insurance               $800.00
  Cr 1410 Prepaid expenses        $800.00
  Totals: debits $800.00, credits $800.00.
Memo: October 2026: one month of the business insurance premium paid on 1 August 2026. Per S2.
Calculation: premium $9,600.00 / 12 months (1 August 2026 to 31 July 2027) = $800.00 (S2). Released to 30 September $1,600.00; after October $2,400.00; remaining $7,200.00. Already booked $0.00. $800.00 - $0.00 = $800.00.
Already booked this period: none.
Support: S2: the prepaid schedule line for the business insurance policy.
Checks: balanced yes; one side per line, no negative amounts yes; accounts in the chart and active yes; accounts fit the kind yes.
Flags: none.
Approver: controller, under the limit for entries up to $10,000.00. Posted by: staff accountant, after approval.

ENTRY R3: October depreciation on computer equipment
Status: Ready for review.
Kind: depreciation. Date: 31 October 2026. Reverses: no.
Lines:
  Dr 6510 Depreciation              $1,000.00
  Cr 1590 Accumulated depreciation  $1,000.00
  Totals: debits $1,000.00, credits $1,000.00.
Memo: October 2026: depreciation on computer equipment, assets CE-01 to CE-04. Per S3.
Calculation: CE-01 ($19,200.00 - $0.00) / 48 = $400.00. CE-02 ($21,600.00 - $0.00) / 36 = $600.00. CE-03 in service 20 October 2026; under the start rule its first month is November: $0.00. CE-04 accumulated $4,800.00 equals cost less residual, fully depreciated: $0.00. Total $1,000.00. Already booked $0.00. $1,000.00 - $0.00 = $1,000.00.
Already booked this period: none.
Support: S3: the asset register extract for computer equipment, four assets.
Checks: balanced yes; one side per line, no negative amounts yes; accounts in the chart and active yes; accounts fit the kind yes.
Flags: none.
Approver: controller, under the limit for entries up to $10,000.00. Posted by: staff accountant, after approval.

ENTRY R4: October share of the Client K retainer billed in advance
Status: Ready for review.
Kind: deferred revenue release. Date: 31 October 2026. Reverses: no.
Lines:
  Dr 2300 Deferred revenue        $6,000.00
  Cr 4100 Fee revenue             $6,000.00
  Totals: debits $6,000.00, credits $6,000.00.
Memo: October 2026: one month of Client K's retainer billed in advance on INV-2207. Per S4.
Calculation: INV-2207 $18,000.00 / 3 months (October to December 2026) = $6,000.00 (S4). Already booked $0.00. $6,000.00 - $0.00 = $6,000.00.
Already booked this period: none.
Support: S4: the billing record for INV-2207, a retainer for October to December 2026 in three equal months, posted at billing to 2300.
Checks: balanced yes; one side per line, no negative amounts yes; accounts in the chart and active yes; accounts fit the kind yes.
Flags: none.
Approver: controller, under the limit for entries up to $10,000.00. Posted by: staff accountant, after approval.

ENTRY R5: Software subscription posted to IT services in September
Status: Ready for review.
Kind: correction. Date: 31 October 2026. Reverses: no.
Lines:
  Part A, reversing JE-0917 in full:
  Dr 2000 Accounts payable        $1,188.00
  Cr 6420 IT services             $1,188.00
  Part B, as it should have been:
  Dr 6430 Software subscriptions  $1,188.00
  Cr 2000 Accounts payable        $1,188.00
  Totals: debits $2,376.00, credits $2,376.00.
Memo: October 2026: corrects JE-0917 of 18 September 2026, Supplier P rendering software for September, invoice P-0918, posted to IT services instead of Software subscriptions. Per S5.
Calculation: JE-0917 carries $1,188.00 on each side (S5). Part A reverses both lines; Part B enters $1,188.00 on 6430. Already booked $0.00. Total $2,376.00 each side.
Already booked this period: none. No posted line this period refers to JE-0917 or Supplier P. Not counted: BILL-1037 in 6430, Software vendor M, a different supplier.
Support: S5: posted entry JE-0917 with its memo naming Supplier P's invoice P-0918 for September usage.
Checks: balanced yes; one side per line, no negative amounts yes; accounts in the chart and active yes; accounts fit the kind yes: Parts A and B net to Dr 6430, Cr 6420, as requested.
Flags: corrects a closed period: JE-0917 is dated 18 September 2026, and September is closed.
Approver: finance director, under the rule for any correction of an entry in a closed period. Posted by: staff accountant, after approval.

ENTRY R6: Freelance photographer for the October shoot; invoice not yet received
Status: Held: support named but not supplied.
Kind: accrual. Date: 31 October 2026. Reverses: on 1 November 2026.
Lines:
  Dr 6260 Freelance production    $2,500.00
  Cr 2150 Accrued expenses        $2,500.00
  Totals: debits $2,500.00, credits $2,500.00.
  These lines are as requested and are not ready for review.
Memo: October 2026: freelance photographer for the October shoot, invoice not yet received. Per email from the studio lead (not supplied).
Calculation: estimate $2,500.00, as given on the request; estimate, no calculation supplied. Already booked $0.00. $2,500.00 - $0.00 = $2,500.00.
Already booked this period: none.
Support: named but not supplied: "Email from the studio lead".
Checks: balanced yes; one side per line, no negative amounts yes; accounts in the chart and active yes; accounts fit the kind yes.
Flags: round estimate: $2,500.00 is a whole multiple of $500.00 with no calculation behind it.
Approver: controller, under the limit for entries up to $10,000.00, once the hold is cleared. Posted by: staff accountant, after approval.

ENTRY R7: Utility U October electricity; bill not yet received
Status: No entry needed: already booked in full by BILL-1043.
Kind: accrual. Date: 31 October 2026. Reverses: not applicable, no entry.
Lines: none.
Memo: none.
Calculation: request $640.00, from last month's bill (S6). Already booked $640.00 (BILL-1043). $640.00 - $640.00 = $0.00.
Already booked this period: BILL-1043, 30 October 2026, $640.00, "Utility U October electricity".
Support: S6: Utility U's bill for 1 to 30 September 2026, $640.00.
Checks: balanced not run, no lines; one side per line, no negative amounts not run, no lines; accounts in the chart and active yes; accounts fit the kind yes.
Flags: none.
Approver: not needed. Posted by: not needed.

QUESTIONS
1. For controller: R1, the $4,200.00 accrual for Supplier T's October support is set not to reverse, while last month's accrual for the same supplier reversed on 1 October (JE-0931R); should this one reverse on 1 November 2026?
2. For controller: R5 corrects JE-0917, $1,188.00 dated 18 September 2026 in a closed period, by reversing it in full and entering it on 6430 Software subscriptions on 31 October 2026; is a correction in October the treatment you want?
3. For studio lead: R6, the $2,500.00 accrual for the photographer's October shoot is a round estimate and its support, your email, was not supplied; can you send the email with the agreed fee, or the day rate and the days worked?

SIGN-OFF
R1: Reviewed by ____________ Date ______  Approved by ____________ Date ______
R2: Reviewed by ____________ Date ______  Approved by ____________ Date ______
R3: Reviewed by ____________ Date ______  Approved by ____________ Date ______
R4: Reviewed by ____________ Date ______  Approved by ____________ Date ______
R5: Reviewed by ____________ Date ______  Approved by ____________ Date ______

Prepared for review. Nothing has been posted, approved, reversed or sent.
```

How the figures trace: the $14,376.00 ready for review is R1 $4,200.00 + R2 $800.00 + R3 $1,000.00 + R4 $6,000.00 + R5 $2,376.00. R6 is held until the studio lead's email arrives, so its $2,500.00 is not in that total. R7 needs no entry because Utility U's October bill, BILL-1043, was posted on 30 October for the same $640.00. Plotter CE-03 starts depreciating in November under the studio's start rule, and file server CE-04 was fully depreciated before October.
