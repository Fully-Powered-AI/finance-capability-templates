# Year-end tax packet for the accountant: an invented example

*Illustrative example with invented data.* The business, the contractors, the firms, every row and every figure below are invented. The business is an invented six-person sign and display studio in Oregon, called "the Studio" here, owned by one person and kept by a part-time bookkeeper. Contractors and firms are referred to by letter and people by role. The Studio's outside accountant has sent a request letter for the 2026 return, and the bookkeeper runs the packet on Monday 11 January 2027, the first working day after the books were closed.

The inputs come first, in full, so the template can be run on them. The packet follows.

## The inputs

### 1. Settings

```
Business: the Studio.
Country: United States. State: Oregon.
Tax year: 1 January 2026 to 31 December 2026. Currency: USD.
Business structure, as the owner states it: single-member LLC.
Accounting basis, as the owner states it: cash.
Prepares the packet: Bookkeeper. Approves it and sends it: Owner.
Requests missing W-9s: Owner.
Books closed: Friday 8 January 2027, by the bookkeeper. December bank
  and card accounts reconciled: yes.
Today: Monday 11 January 2027.
Service accounts: Contract labour; Professional fees.
Reporting threshold: from the accountant's request letter, item 4.
Form that reports contractors: 1099-NEC.
Form that records a contractor's tax details: W-9.
```

### 2. The accountant's request letter

```
Please send the packet by Friday 29 January 2027.
1. Profit and loss and balance sheet for 2026
2. December 2026 statements for every bank, card and loan account
3. The payroll year-end summary from your payroll provider
4. Everyone you paid $2,000 or more for services in 2026, by date paid,
   and whether you hold a W-9 for each. Tell us who was paid by card or
   through a payment platform.
5. Your 2026 federal and state estimated tax payments, with confirmations
6. Invoices for equipment bought in 2026 costing $2,500 or more
7. Your card processor's 2026 annual summary
8. Any letters from the IRS or the state during 2026
```

### 3. The closed year's reports

```
Profit and loss, 1 January to 31 December 2026, cash basis
Sales                          412,600.00
Total income                   412,600.00
Materials                       96,300.00
Contract labour                 41,850.00
Professional fees                9,200.00
Wages and payroll taxes        118,400.00
Rent                            36,000.00
Software and subscriptions       4,150.00
Other operating expenses        27,940.00
Total expenses                 333,840.00
Net profit                      78,760.00

Balance sheet at 31 December 2026 (cash, card and loan lines)
Checking account                58,420.17
Savings account                 30,000.00
Business card                   -3,184.55
Equipment loan                 -18,750.00
```

### 4. The vendor payments export (1 January 2026 to 11 January 2027)

```
Date,Payee,Account,Amount,Method,Reference
2026-02-13,Contractor A,Contract labour,4600.00,Bank transfer,A-0126
2026-03-06,Firm F LLC,Professional fees,1500.00,Bank transfer,F-311
2026-03-20,Contractor B,Contract labour,2250.00,Payment platform,B-01
2026-04-03,Firm G,Professional fees,5000.00,Cheque,1042
2026-04-10,Contractor C Fabrication Inc.,Contract labour,7800.00,Cheque,1043
2026-05-15,Contractor A,Contract labour,4600.00,Bank transfer,A-0426
2026-06-05,Contractor D,Contract labour,1200.00,Bank transfer,D-1
2026-06-19,Contractor B,Contract labour,2250.00,Payment platform,B-02
2026-07-17,Contractor C Fabrication Inc.,Materials,2880.00,Cheque,1051
2026-08-14,Contractor A,Contract labour,4600.00,Bank transfer,A-0726
2026-08-28,Contractor E,Contract labour,1800.00,Card,E-77
2026-09-04,Firm F LLC,Professional fees,2700.00,Bank transfer,F-342
2026-09-18,Contractor B,Contract labour,2250.00,Payment platform,B-03
2026-10-09,Contractor C Fabrication Inc.,Contract labour,4500.00,Cheque,1060
2026-11-13,Contractor A,Contract labour,4600.00,Bank transfer,A-1026
2026-12-30,Contractor D Metalwork,Contract labour,1400.00,Bank transfer,DM-12
2027-01-06,Contractor A,Contract labour,4600.00,Bank transfer,A-1226
```

### 5. The contractor details list

```
Payee,Legal name,Entity type,Tax details form on file,Tax ID on file
Contractor A,Contractor A,Individual,yes,yes
Contractor B,Contractor B,Individual,no,no
Contractor C Fabrication Inc.,Contractor C Fabrication Inc.,Corporation,yes,yes
Contractor D,Contractor D,Individual,no,no
Contractor E,Contractor E,Individual,yes,yes
Firm F LLC,Firm F LLC,LLC,yes,yes
Firm G,Firm G,,no,no
```

### 6. Estimated tax payments

```
Date paid,Authority,Period,Amount,Confirmation held
2026-01-15,Federal,2025 Q4,3800.00,yes
2026-04-15,Federal,2026 Q1,4500.00,yes
2026-04-15,State,2026 Q1,1200.00,yes
2026-06-15,Federal,2026 Q2,4500.00,yes
2026-06-15,State,2026 Q2,1200.00,no
2026-09-15,Federal,2026 Q3,4500.00,yes
2026-09-15,State,2026 Q3,1200.00,yes
2027-01-08,Federal,2026 Q4,4500.00,yes
```

### 7. Documents on hand (typed by the bookkeeper)

```
- Profit and loss 2026: have. From the closed books.
- Balance sheet at 31 December 2026: have. From the closed books.
- December statement, checking account: have. Closing balance 58,420.17.
- December statement, savings account: missing. Not yet downloaded.
- December statement, business card: have. Closing balance 3,184.55 owed.
- December statement, equipment loan: have. Balance 18,750.00.
- Payroll year-end summary: missing. The payroll provider sends it on
  20 January 2027.
- Estimated payment confirmations: have, except the state 2026 Q2
  confirmation, which I cannot find.
- Equipment invoices: have. Vinyl printer, bought 14 May 2026,
  18,900.00. No other equipment over 2,500 this year.
- Card processor annual summary: missing. Expected by 31 January 2027.
```

### 8. Notes on the year (typed by the owner)

```
- Bought a vinyl printer in May for $18,900, paid for with the equipment
  loan.
- Since September I have worked from a home office two days a week. Can
  I deduct the home office?
- No letters from the IRS or the state this year.
- The state estimated payment for 2026 Q4 has not been made yet.
- My other question: should the Studio become an S corporation for 2027?
```

## The output

```
YEAR-END TAX PACKET: the Studio, tax year 2026

Draft packet for the accountant to review. It is not tax advice: it works out no tax and says nothing about how any item should be treated.
For: the accountant. Packet wanted by: Friday 29 January 2027. Prepared by: Bookkeeper, Monday 11 January 2027. Approves: Owner.
Jurisdiction: United States, Oregon. Tax year: 1 January 2026 to 31 December 2026. Currency: USD.
Business structure: single-member LLC, as the owner states. Accounting basis: cash, as the owner states.
Books closed: Friday 8 January 2027, by the bookkeeper. Year-end bank and card accounts reconciled: yes, as stated.
Sources: settings; the accountant's request letter, 8 items; profit and loss for 2026; balance sheet lines at 31 December 2026, 4 accounts; vendor payments export, 17 rows; contractor details list, 7 payees; estimated tax payments, 8 rows; documents on hand, 10 lines; notes on the year, 5 lines.

ASSUMPTIONS
1. Contractor payments are counted by the date paid in the export. Payments dated after 31 December 2026 are not counted. Counted payments are shown as totals by payee, without each payment's date, which stays in the vendor payments export.
2. Only payments in Contract labour and Professional fees are counted as payments for services, as the settings say.
3. Payees are matched on the exact name in the export. Similar names are shown as possible duplicates, not merged.
4. Each estimated payment is put in the period written in its Period column.
5. The reporting threshold of $2,000 is the accountant's, from item 4 of the request letter, and "$2,000 or more" is read as at or above $2,000.
6. The business structure and the accounting basis are as the owner states them; they have not been checked.
7. The balance sheet shows the business card as -3,184.55 and the loan as -18,750.00; both are read as amounts owed, matching the card statement's 3,184.55 owed and the loan statement's balance of 18,750.00.

1. THE YEAR IN FIGURES
Total income: $412,600.00 (profit and loss).
Total expenses: $333,840.00 (profit and loss).
Net profit: $78,760.00 (profit and loss).
Contract labour: $41,850.00 (profit and loss).
Professional fees: $9,200.00 (profit and loss).
Checking account at 31 December 2026: $58,420.17 (balance sheet).
Savings account at 31 December 2026: $30,000.00 (balance sheet).
Business card at 31 December 2026: $3,184.55 owed (balance sheet).
Equipment loan at 31 December 2026: $18,750.00 owed (balance sheet).
Check: total income $412,600.00 less total expenses $333,840.00 = $78,760.00. The report prints net profit $78,760.00: agrees.
Check: checking account at 31 December 2026: balance sheet $58,420.17, statement $58,420.17: agrees.
Check: savings account at 31 December 2026: balance sheet $30,000.00, statement not supplied.
Check: business card at 31 December 2026: balance sheet $3,184.55 owed, statement $3,184.55 owed: agrees.
Check: equipment loan at 31 December 2026: balance sheet $18,750.00 owed, statement $18,750.00 owed: agrees.

2. DOCUMENTS FOR THE ACCOUNTANT
List used: the accountant's request list, 8 items.
Have 2. Partly 2. Missing 2. In this packet 1. Nothing to send 1. Not stated 0.
1. Profit and loss and balance sheet for 2026: have. Both from the closed books.
2. December 2026 statements for every bank, card and loan account: partly: the savings account statement is missing, not yet downloaded. Checking account, business card and equipment loan statements: have.
3. The payroll year-end summary from your payroll provider: missing, expected 20 January 2027.
4. Everyone you paid $2,000 or more for services in 2026, by date paid, and whether you hold a W-9 for each. Tell us who was paid by card or through a payment platform: in this packet, section 3.
5. Your 2026 federal and state estimated tax payments, with confirmations: partly: the confirmation for the state 2026 Q2 payment cannot be found. The payments are in section 4.
6. Invoices for equipment bought in 2026 costing $2,500 or more: have. One invoice: vinyl printer, bought 14 May 2026, $18,900.00. No other equipment over $2,500, as the bookkeeper states.
7. Your card processor's 2026 annual summary: missing, expected by 31 January 2027. FLAG, after the accountant's date: expected 31 January 2027; the packet is wanted by 29 January 2027.
8. Any letters from the IRS or the state during 2026: nothing to send, as the owner states.

3. CONTRACTORS
Reporting rule: $2,000 or more for services in 2026, reported on form 1099-NEC, tax details recorded on form W-9, from the accountant's request letter, item 4, and the settings.
Counted: 15 payments, $51,050.00, in Contract labour and Professional fees, dated 1 January 2026 to 31 December 2026.
Shown, not counted: Contractor C Fabrication Inc., 17 July 2026, Materials, $2,880.00, not a service account. Contractor A, 6 January 2027, Contract labour, $4,600.00, paid after the year end.
At or above $2,000: 5 payees, $46,650.00.
Contractor A (Contractor A): $18,400.00 in 4 payments, Contract labour. Paid by: bank transfer. Entity type: individual. Tax details form: on file.
Contractor C Fabrication Inc. (Contractor C Fabrication Inc.): $12,300.00 in 2 payments, Contract labour. Paid by: cheque. Entity type: corporation. Tax details form: on file. FLAG, entity type: stated as a corporation.
Contractor B (Contractor B): $6,750.00 in 3 payments, Contract labour. Paid by: payment platform. Entity type: individual. Tax details form: not on file. FLAG, no form on file, payment platform: every payment went through a payment platform, as the accountant asked to be told.
Firm G (Firm G): $5,000.00 in 1 payment, Professional fees. Paid by: cheque. Entity type: not stated. Tax details form: not on file. FLAG, no form on file, entity type not stated.
Firm F LLC (Firm F LLC): $4,200.00 in 2 payments, Professional fees. Paid by: bank transfer. Entity type: LLC. Tax details form: on file. FLAG, entity type: stated as an LLC, with its tax treatment not stated.
Below $2,000: Contractor E $1,800.00, paid by card, tax details form on file, FLAG, card: paid by card, as the accountant asked to be told. Contractor D Metalwork $1,400.00, paid by bank transfer, tax details form not stated, FLAG, not on the contractor details list. Contractor D $1,200.00, paid by bank transfer, tax details form not on file, FLAG, no form on file.
Possible duplicates: Contractor D ($1,200.00) and Contractor D Metalwork ($1,400.00): combined $2,600.00, which reaches the threshold. For the owner to confirm; not merged.
Missing tax details forms: 3. Contractor B, $6,750.00. Firm G, $5,000.00. Contractor D and Contractor D Metalwork, combined $2,600.00, if they are the same payee. The owner requests each form; nothing has been sent.
Check: Contract labour counted $41,850.00; profit and loss $41,850.00: agrees.
Check: Professional fees counted $9,200.00; profit and loss $9,200.00: agrees.

4. ESTIMATED TAX PAYMENTS
For tax year 2026:
2026-04-15  Federal  2026 Q1  $4,500.00  Confirmation: held
2026-04-15  State    2026 Q1  $1,200.00  Confirmation: held
2026-06-15  Federal  2026 Q2  $4,500.00  Confirmation: held
2026-06-15  State    2026 Q2  $1,200.00  Confirmation: not held
2026-09-15  Federal  2026 Q3  $4,500.00  Confirmation: held
2026-09-15  State    2026 Q3  $1,200.00  Confirmation: held
2027-01-08  Federal  2026 Q4  $4,500.00  Confirmation: held  (paid after the year end)
Total for 2026: Federal $18,000.00 in 4 payments. State $3,600.00 in 3 payments.
Paid during 2026 for an earlier period:
2026-01-15  Federal  2025 Q4  $3,800.00  Confirmation: held
These are the payments as recorded. Whether they are enough is for the accountant.

5. QUESTIONS FOR THE ACCOUNTANT
1. Contractor C Fabrication Inc. is stated as a corporation and was paid $12,300.00 for contract labour in 2026, with a W-9 on file. How should these payments be handled for reporting? (From: section 3.)
2. Contractor B was paid $6,750.00 for contract labour in 2026, all through a payment platform, and no W-9 is on file. How should these payments be handled for reporting? (From: section 3.)
3. Firm F LLC is stated as an LLC, with its tax treatment not stated, and was paid $4,200.00 in professional fees in 2026, with a W-9 on file. How should these payments be handled for reporting? (From: section 3.)
4. Contractor D ($1,200.00) and Contractor D Metalwork ($1,400.00) may be the same payee; this has not been confirmed (action 4). If they are, the combined $2,600.00 reaches your $2,000 line. How should they be handled for reporting? (From: section 3.)
5. The Studio bought a vinyl printer in May 2026 for $18,900.00, paid for with the equipment loan. How should it be treated on the 2026 return? (From: notes on the year.)
6. "Can I deduct the home office?" The owner has worked from a home office two days a week since September 2026. (From: notes on the year, the owner's own question.)
7. The owner notes that the state estimated payment for 2026 Q4 has not been made yet. What do you advise? (From: notes on the year.)
8. "Should the Studio become an S corporation for 2027?" (From: the owner's own question.)

6. BEFORE THE PACKET GOES
1. Download the December 2026 savings account statement and check its closing balance against the balance sheet's $30,000.00. (Bookkeeper.)
2. Request a W-9 from Contractor B. (Owner.)
3. Request a W-9 from Firm G, and confirm its entity type, which the contractor details list leaves blank. (Owner.)
4. Confirm whether Contractor D and Contractor D Metalwork are the same payee. Contractor D Metalwork is not on the contractor details list, and no W-9 is on file for Contractor D. If they are the same, request a W-9. (Owner.)
5. Find the confirmation for the state 2026 Q2 payment of $1,200.00, paid 15 June 2026. (Owner.)
6. Add the payroll year-end summary when it arrives, expected 20 January 2027. (Bookkeeper.)
7. Add the card processor's 2026 annual summary when it arrives, expected by 31 January 2027, after the accountant's date of 29 January 2027. (Bookkeeper.)

Draft for the owner's approval. Nothing has been sent, filed, paid or changed.
```
