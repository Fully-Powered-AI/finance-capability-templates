# Bank reconciliation preparation: trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-09

The inputs are the invented example in `public/example.md` (Tallow Street Bakery, operating account ending 4417, October 2026): its settings, the bank statement export, the ledger export and the September open items. No client data was used. The model that ran this did not write the template. It read the template and the example's inputs only, followed the instruction block and the output format, and compared its sheet with the example's sheet afterwards.

**Edited after this run, 9 November 2026.** Following the independent review, the template and the example were edited after the run recorded here, and the run was not repeated. The output and the observations below are left as recorded, so where they describe the template or the example they describe them as they were at the time of the run. What changed:

- The "two digits may be swapped" test is now on the gap in cents (a $0.09, $4.50 or $9.00 gap qualifies), in the procedure, the instructions for the AI assistant and the where-to-look list. This settles the dollars-or-cents point below.
- Business days are now counted from the day after the earlier date up to and including the later date, both for the date window and for the deposit flag. This is how this run counted (21 Oct to 30 Oct = 7), and it settles the start-day point below.
- "Open items" is now defined in one sentence: every outstanding payment, deposit in transit and row on the statement only, plus each Amount differs pair once and each row under Needs a person to pair once. This is the reading this run took (13).
- The proof step now says that an unresolved Needs-a-person-to-pair group shows on both sides until a person decides, and that this is expected.
- The kind of a statement-only row now comes from a fixed list: fee, interest, returned item, direct debit, or "kind not clear". The example's sheet was changed to match ("returned item", "fee", "fee", "interest"). The comparison below is with the example's earlier wording. Under the fixed list, this run's "fee (merchant discount)" would read "fee".
- The instructions for the AI assistant now carry four things the procedure already had: counting the rows in each export for the Sources line, asking the user to confirm the sign before using Debit and Credit columns, the optional column map as an input, and repeating no password or login code that appears in a file and telling the user to remove it. None of these changes the result on this example.
- Reviewer checklist item 6 was reworded. Two factual slips in the observations below were also corrected: the comparison now lists every wording difference, and the last line no longer says the template was written for one product.

## What came out

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
30 Oct "MERCHANT DISCOUNT OCT" $287.64 out, 1 day. Kind: fee (merchant discount).
30 Oct "INTEREST PAID" $4.12 in, 1 day. Kind: interest.

AMOUNT DIFFERS
Reference 1191: statement 14 Oct $445.00 out; ledger 9 Oct 1191 "Supplier D (produce)" $454.00 out. Gap $9.00. 22 days. Two digits may be swapped.

NEEDS A PERSON TO PAIR
Statement 19 Oct "ACH DEBIT SUPPLIER B DAIRY" $1,326.75 out, 12 days. Candidates: ledger 19 Oct ACH-1019.
Statement 20 Oct "ACH DEBIT SUPPLIER B DAIRY" $1,326.75 out, 11 days. Candidates: ledger 19 Oct ACH-1019.
Ledger 19 Oct ACH-1019 "Supplier B (dairy)" $1,326.75 out, 12 days. Candidates: statement 19 Oct, statement 20 Oct.

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
3. 30 Oct "MERCHANT DISCOUNT OCT" $287.64 out. Kind: fee (merchant discount).
4. 30 Oct "INTEREST PAID" $4.12 in. Kind: interest.
Coding: chosen by bookkeeper. Posted by bookkeeper after outside accountant approves.
Waiting on an answer: check 1191 (gap $9.00); the Supplier B debits of $1,326.75 on 19 and 20 Oct and ledger ACH-1019.

QUESTIONS
For bookkeeper: check 1191 to Supplier D is $454.00 in the ledger on 9 Oct but cleared the bank at $445.00 on 14 Oct; which amount is on the check?
For bookkeeper: the statement shows Supplier B debits of $1,326.75 on 19 Oct and 20 Oct against one ledger payment of $1,326.75 on 19 Oct (ACH-1019); was a second payment due?
For Shop 2 manager: the $920.00 of Shop 2 cash takings recorded on 21 Oct (D-1021) is not on the statement by 31 Oct; was it banked, and on what date?
For bookkeeper: the statement shows a returned deposited item of $380.00 on 26 Oct, reference RI0926; which deposit does it relate to?
For outside accountant: check 1176 to Supplier F for $212.40, dated 18 Aug, is uncashed after 74 days; what should happen to it?

IF THE PROOF DOES NOT AGREE: WHERE TO LOOK
Not needed.

SIGN-OFF
Prepared by: bookkeeper, 3 November 2026.
Reviewed by: ____________________  Date: ____________

Prepared for review. Nothing has been posted, cleared, written off or sent.
```

## What was observed

- **Every required part was produced.** All sections of the output format appear in order. Nothing in the run told it to stop: both exports foot to their own closing balances, every heading matched, one account, every row inside the period.
- **The proof agrees at $0.00.** Both sides arrive at $25,098.93. The opening balances also differ by $167.60, which equals the three carried items (-$212.40, -$860.00, +$1,240.00), a useful independent check.
- **Compared with the published example, the figures, pairings, counts, ages, flags and entries are identical.** The differences are wording only: the kind given to the returned item (here "returned item", there "returned deposited item"), the two fees (here "fee" and "fee (merchant discount)", there "service fee" and "merchant discount"), the wording of all five questions and of the "Waiting on an answer" line, and how the two candidates are joined in one line (here a comma, there "and"). The trial and the example agree on 10 pairs, 13 open items, 2 flags and 4 entries.
- **No fact appears in either sheet that is not in the inputs.** In both, the kinds are taken from the statement descriptions. The example's closing paragraph ("How the figures trace") is explanation, not part of the sheet.
- **Where the instructions needed a judgment:**
  - The proof's handling of "Needs a person to pair" rows is literal but odd. The one ledger payment goes on the statement side as a payment the bank has not shown, and both statement debits go on the ledger side as payments the ledger does not show. It balances, but the same $1,326.75 appears on both sides, and the template does not say that this is expected.
  - "Open items" is not defined. It was taken to include the statement-only rows, which gives 13. A reader who counts only outstanding payments and deposits in transit would get 5.
  - Counting business days for the deposit flag does not say whether the start day counts. It was counted from the day after the deposit date to the last business day (21 Oct to 30 Oct = 7).
  - "A gap divisible by 9" does not say whether the test is on dollars or cents. Taken as whole dollars here ($9.00); a gap such as $4.50 would be ambiguous.
  - The settings gave no date window, deposit check or old-payment limit. The three defaults were used and listed. The instruction block still contains literal bracketed placeholders ("[your date window, default 3]"), which read correctly here only because the default is stated inside the brackets.
  - The instruction block's "Kind" wording lets the model choose how to label a statement row ("fee" or "service fee"); two runs will differ in wording.
- **No unfamiliar payee** appeared, so the owner-first question was not triggered. That branch, and every stop condition, was not exercised by this input. Only the clean-proof path ran.
- **Shortcomings of this trial:** one run, one input, one model, in one product only. It shows the template can be followed to the published result. It does not show how it behaves on a real export, on messy descriptions or when the proof does not agree.
