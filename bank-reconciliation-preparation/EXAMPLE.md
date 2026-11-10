# Bank reconciliation preparation: an invented example

*Illustrative example with invented data.* The business, the suppliers, the bank, every row and every figure below are invented. Tallow Street Bakery is an invented bakery with two shops and a wholesale round to local cafés. Its bookkeeper reconciles the operating account for October 2026, and its outside accountant reviews and signs. People are referred to by role and suppliers by letter.

The inputs come first, in full, so the template can be run on them. The reconciliation sheet follows.

## The inputs

### 1. Settings

```
Account: operating account, ending 4417.
Statement period: 1 to 31 October 2026.
Sheet prepared: Tuesday 3 November 2026.
Runs it: bookkeeper. Reviews and signs: outside accountant.
Codes and posts entries, marks items cleared: bookkeeper, after the
  outside accountant approves.
Answers questions: Shop 2 manager for Shop 2 cash takings; bookkeeper for
  supplier payments, checks and returned items; outside accountant for
  what happens to an old payment; owner for anything unexplained.
Bank's business days: Monday to Friday. No bank holidays in October.
(No date window, deposit check or old-payment limit given.)
```

### 2. Bank statement export, operating account ending 4417

```
Opening balance 1 October 2026: 18,450.00
Closing balance 31 October 2026: 25,511.08

Date,Description,Reference,Money out,Money in
2026-10-01,DEPOSIT,,,1240.00
2026-10-02,CARD SETTLEMENT MERCHANT 0091,,,3412.55
2026-10-05,ACH DEBIT SUPPLIER A FLOUR,,2180.00,
2026-10-06,CHECK 1182,1182,860.00,
2026-10-09,CARD SETTLEMENT MERCHANT 0091,,,4105.20
2026-10-12,PAYROLL SVC DD,,9640.00,
2026-10-14,CHECK 1191,1191,445.00,
2026-10-16,CARD SETTLEMENT MERCHANT 0091,,,3987.40
2026-10-19,ACH DEBIT SUPPLIER B DAIRY,,1326.75,
2026-10-20,ACH DEBIT SUPPLIER B DAIRY,,1326.75,
2026-10-23,CARD SETTLEMENT MERCHANT 0091,,,4230.10
2026-10-26,RETURNED DEPOSITED ITEM,RI0926,380.00,
2026-10-27,DEPOSIT,,,2050.00
2026-10-30,CARD SETTLEMENT MERCHANT 0091,,,4512.85
2026-10-30,MONTHLY SERVICE FEE,,35.00,
2026-10-30,MERCHANT DISCOUNT OCT,,287.64,
2026-10-30,INTEREST PAID,,,4.12
```

### 3. Ledger export, operating account

```
Opening balance 1 October 2026: 18,617.60
Closing balance 31 October 2026: 28,441.95

Date,Type,Number,Name,Memo,Amount
2026-10-01,Deposit,D-1001,Merchant card settlement,Card takings 24 to 30 Sep,3412.55
2026-10-01,Bill payment,ACH-1001,Supplier A (flour),September flour,-2180.00
2026-10-08,Deposit,D-1008,Merchant card settlement,Card takings 1 to 7 Oct,4105.20
2026-10-09,Check,1191,Supplier D (produce),Produce week to 9 Oct,-454.00
2026-10-12,Payroll,PR-1012,Payroll service,Payroll 12 Oct,-9640.00
2026-10-15,Deposit,D-1015,Merchant card settlement,Card takings 8 to 14 Oct,3987.40
2026-10-19,Bill payment,ACH-1019,Supplier B (dairy),October dairy,-1326.75
2026-10-20,Check,1194,Supplier E (cleaning),Cleaning October,-318.00
2026-10-21,Deposit,D-1021,Cash takings Shop 2,Cash takings 12 to 18 Oct,920.00
2026-10-22,Deposit,D-1022,Merchant card settlement,Card takings 15 to 21 Oct,4230.10
2026-10-23,Deposit,D-1023,Wholesale receipts,Checks from cafés,2050.00
2026-10-28,Check,1195,Supplier C (equipment repair),Oven repair,-1150.00
2026-10-29,Deposit,D-1029,Merchant card settlement,Card takings 22 to 28 Oct,4512.85
2026-10-30,Deposit,D-1030,Wholesale receipts,Checks from cafés,1675.00
```

### 4. Open items from the September reconciliation

```
Date,Type,Number,Name,Amount
2026-08-18,Check,1176,Supplier F (packaging),-212.40
2026-09-24,Check,1182,Supplier C (equipment repair),-860.00
2026-09-30,Deposit,D-0930,Wholesale receipts,1240.00
```

## The reconciliation sheet

```
BANK RECONCILIATION: operating account, ending 4417, 1 to 31 October 2026

For: outside accountant. Prepared by: bookkeeper on 3 November 2026.
Sources: bank statement export, 17 rows, 1 to 31 October 2026; ledger export, 14 rows; last month's open items, 3, from September 2026.
Settings used: date window 3 business days; deposit check 5 business days; old-payment limit 60 days; business days Monday to Friday. Defaults used: date window, deposit check, old-payment limit.

RESULT
Proof agrees: difference $0.00.
Open items: 13. Flagged: 2. Entries to prepare: 4.

BALANCES
Statement: opening $18,450.00 + money in $23,542.22 - money out $16,481.14 = $25,511.08. Closing balance on the statement $25,511.08: agrees.
Ledger: opening $18,617.60 + money in $24,893.10 - money out $15,068.75 = $28,441.95. Closing balance in the ledger $28,441.95: agrees.

PROOF
Statement closing balance                          $25,511.08
  Add: ledger receipts the bank has not shown yet   $2,595.00
  Less: ledger payments the bank has not shown yet  ($3,007.15)
Adjusted statement balance                         $25,098.93
Ledger closing balance                             $28,441.95
  Add: bank receipts the ledger does not show       $4.12
  Less: bank payments the ledger does not show      ($3,356.14)
  Amount differences                                $9.00
Adjusted ledger balance                            $25,098.93
Difference                                         $0.00

MATCHED: 10 pairs. Money in $23,538.10. Money out $12,680.00.
By reference: statement 6 Oct "CHECK 1182" $860.00 out = ledger 24 Sep 1182 "Supplier C (equipment repair)", carried.
By amount and date: statement 1 Oct "DEPOSIT" = ledger 30 Sep D-0930 "Wholesale receipts", carried, $1,240.00 in, 1 business day apart, description not compared.
By amount and date: statement 2 Oct "CARD SETTLEMENT MERCHANT 0091" = ledger 1 Oct D-1001 "Merchant card settlement", $3,412.55 in, 1 business day apart.
By amount and date: statement 5 Oct "ACH DEBIT SUPPLIER A FLOUR" = ledger 1 Oct ACH-1001 "Supplier A (flour)", $2,180.00 out, 2 business days apart.
By amount and date: statement 9 Oct "CARD SETTLEMENT MERCHANT 0091" = ledger 8 Oct D-1008 "Merchant card settlement", $4,105.20 in, 1 business day apart.
By amount and date: statement 12 Oct "PAYROLL SVC DD" = ledger 12 Oct PR-1012 "Payroll service", $9,640.00 out, 0 business days apart.
By amount and date: statement 16 Oct "CARD SETTLEMENT MERCHANT 0091" = ledger 15 Oct D-1015 "Merchant card settlement", $3,987.40 in, 1 business day apart.
By amount and date: statement 23 Oct "CARD SETTLEMENT MERCHANT 0091" = ledger 22 Oct D-1022 "Merchant card settlement", $4,230.10 in, 1 business day apart.
By amount and date: statement 27 Oct "DEPOSIT" = ledger 23 Oct D-1023 "Wholesale receipts", $2,050.00 in, 2 business days apart, description not compared.
By amount and date: statement 30 Oct "CARD SETTLEMENT MERCHANT 0091" = ledger 29 Oct D-1029 "Merchant card settlement", $4,512.85 in, 1 business day apart.

OUTSTANDING PAYMENTS
18 Aug 1176 "Supplier F (packaging)" $212.40 out, 74 days, carried. FLAG: old payment.
20 Oct 1194 "Supplier E (cleaning)" $318.00 out, 11 days.
28 Oct 1195 "Supplier C (equipment repair)" $1,150.00 out, 3 days.

DEPOSITS IN TRANSIT
21 Oct D-1021 "Cash takings Shop 2" $920.00 in, 10 days. FLAG: not on the statement after 7 business days.
30 Oct D-1030 "Wholesale receipts" $1,675.00 in, 1 day.

ON THE STATEMENT ONLY
26 Oct "RETURNED DEPOSITED ITEM" RI0926 $380.00 out, 5 days. Kind: returned item.
30 Oct "MONTHLY SERVICE FEE" $35.00 out, 1 day. Kind: fee.
30 Oct "MERCHANT DISCOUNT OCT" $287.64 out, 1 day. Kind: fee.
30 Oct "INTEREST PAID" $4.12 in, 1 day. Kind: interest.

AMOUNT DIFFERS
Reference 1191: statement 14 Oct $445.00 out; ledger 9 Oct 1191 "Supplier D (produce)" $454.00 out. Gap $9.00. 22 days. Two digits may be swapped.

NEEDS A PERSON TO PAIR
Statement 19 Oct "ACH DEBIT SUPPLIER B DAIRY" $1,326.75 out, 12 days. Candidates: ledger 19 Oct ACH-1019.
Statement 20 Oct "ACH DEBIT SUPPLIER B DAIRY" $1,326.75 out, 11 days. Candidates: ledger 19 Oct ACH-1019.
Ledger 19 Oct ACH-1019 "Supplier B (dairy)" $1,326.75 out, 12 days. Candidates: statement 19 Oct and statement 20 Oct.

CARRIED FROM LAST MONTH
18 Aug 1176 "Supplier F (packaging)" $212.40: still open, now 74 days.
24 Sep 1182 "Supplier C (equipment repair)" $860.00: cleared on 6 Oct.
30 Sep D-0930 "Wholesale receipts" $1,240.00: cleared on 1 Oct.

AGEING
Within 30 days: 12. 31 to 60 days: 0. Over 60 days: 1.
Flags: check 1176: old payment. Deposit D-1021: not on the statement after 7 business days.

ENTRIES TO PREPARE FOR APPROVAL
1. 26 Oct "RETURNED DEPOSITED ITEM" $380.00 out. Kind: returned item.
2. 30 Oct "MONTHLY SERVICE FEE" $35.00 out. Kind: fee.
3. 30 Oct "MERCHANT DISCOUNT OCT" $287.64 out. Kind: fee.
4. 30 Oct "INTEREST PAID" $4.12 in. Kind: interest.
Coding: chosen by bookkeeper. Posted by bookkeeper after outside accountant approves.
Waiting on an answer: check 1191 (gap $9.00); Supplier B debits of $1,326.75 on 19 and 20 Oct against one ledger payment.

QUESTIONS
For bookkeeper: check 1191 to Supplier D is $454.00 in the ledger on 9 Oct but cleared the bank at $445.00 on 14 Oct; which amount is written on the check?
For bookkeeper: the statement shows Supplier B debits of $1,326.75 on 19 Oct and again on 20 Oct, while the ledger has one payment of $1,326.75 on 19 Oct; was a second payment due, or was the account debited twice?
For Shop 2 manager: Shop 2 cash takings of $920.00, recorded on 21 Oct as D-1021, are not on the statement by 31 Oct; were they banked, and on what date?
For bookkeeper: the statement shows a returned deposited item of $380.00 on 26 Oct, reference RI0926; whose payment was returned?
For outside accountant: check 1176 to Supplier F for $212.40, written on 18 Aug, is still not cashed after 74 days; what should happen to it?

IF THE PROOF DOES NOT AGREE: WHERE TO LOOK
Not needed.

SIGN-OFF
Prepared by: bookkeeper, 3 November 2026.
Reviewed by: ____________________  Date: ____________

Prepared for review. Nothing has been posted, cleared, written off or sent.
```

How the figures trace: money in on the statement is the eight receipts, money out the nine payments. Ledger receipts the bank has not shown yet are the two deposits in transit (\$920.00 + \$1,675.00). Ledger payments the bank has not shown yet are the three outstanding checks and the unpaired Supplier B ledger payment (\$212.40 + \$318.00 + \$1,150.00 + \$1,326.75). Bank payments the ledger does not show are the returned item, the two fees and both unpaired Supplier B debits (\$380.00 + \$35.00 + \$287.64 + \$1,326.75 + \$1,326.75). The amount difference is the statement's \$445.00 out less the ledger's \$454.00 out, which adds \$9.00 to the ledger side. The thirteen open items are three outstanding payments, two deposits in transit, four statement items, one amount difference and three rows waiting to be paired.
