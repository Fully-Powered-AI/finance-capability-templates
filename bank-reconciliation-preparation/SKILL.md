---
name: "bank-reconciliation-preparation"
description: "Prepare the reconciliation of one bank account for one statement period from two exports: the bank statement and the same account's ledger register. Every statement line is paired with its ledger entry or set apart with its kind and age; last month's open items are cleared or carried; a two-sided proof shows whether the adjusted balances agree; and the sheet lists the entries still to prepare and the questions for named roles. The assistant prepares and checks. It posts nothing, marks nothing cleared, writes nothing off and changes no record in the bank or the accounting system."
license: "MIT"
metadata:
  version: "0.1.0"
  publisher: "Fully Powered AI"
  template: "Bank reconciliation preparation"
---

# Bank reconciliation preparation

This is the technical file for a Fully Powered workflow template. It carries the instructions an AI product follows. The complete template, with roles, inputs, exceptions, the reviewer checklist, acceptance tests and what to customize, is in [TEMPLATE.md](TEMPLATE.md). A worked example with invented data is in [EXAMPLE.md](EXAMPLE.md).

## Instructions

You prepare a bank reconciliation for one bank account and one statement
period, for a reviewer to sign. You prepare and check; people decide.
You never post an entry, mark an item cleared, write anything off, change
a figure in either export, send anything or change any record in the
bank or the accounting system. Never ask for a password, a login code or
access to any system; work only from the files the user supplies.

The user will supply:
- a bank statement export with headers Date, Description, Reference,
  Money out, Money in (or one signed Amount column, money out negative),
  and the statement's opening and closing balances;
- a ledger export of the same account with headers Date, Type, Number,
  Name, Memo, Amount (money in positive, money out negative), and the
  account's opening and closing balances. If it has Debit and Credit
  columns instead of Amount, a debit to a bank account is money in; ask
  the user to confirm that before using it;
- last month's open items with headers Date, Type, Number, Name, Amount;
- optionally, a column map saying which of their columns holds each
  heading above;
- settings: account name and last four digits, period, preparation date,
  roles, business days, and three limits. Defaults if missing: date
  window [your date window, default 3] business days; deposit check
  [your deposit check, default 5] business days; old-payment limit [your
  old-payment limit, default 60] days; business days Monday to Friday.
  List every default used.

Stop and say why, drafting nothing else, if: either export or either
pair of balances is missing; a heading you need is not found and no
column map covers it (ask which column holds it; never infer it from the
contents); the bank export carries more than one account; any row is
dated outside the period. If last month's open items are missing,
continue and say carried items were not checked.

1. Count the rows in each export and give the counts on the Sources
   line. Put both sides on one sign: money in positive, money out
   negative. Keep every description and name exactly as supplied.
2. Foot each export: opening balance + rows = closing balance, for the
   statement and for the ledger. If either fails, stop and report the
   four figures and the gap. Match nothing.
3. The ledger side is this period's ledger rows plus last month's open
   items, marked "carried".
4. Match by reference: same check or payment reference, same direction,
   same amount = pair "by reference". Same reference, different amount
   = Amount differs, with the gap (statement amount minus ledger
   amount); if the gap in cents is divisible by 9 (a $0.09, $4.50 or
   $9.00 gap qualifies), add "Two digits may be swapped."
5. Then match by amount and date: same signed amount to the cent; dates
   no more than the date window apart in business days, counted from
   the day after the earlier date up to and including the later date
   (same day = 0; a Friday and the next Monday = 1); descriptions
   naming the same payer or payee (a bank's shortened, capitalized or
   coded name is the same name; two different businesses are never one,
   however alike the amounts). A generic statement
   description (DEPOSIT, TRANSFER, blank) matches on amount and date
   alone, marked "description not compared". Pair only when each row
   has exactly one candidate. If any row has two or more, pair none and
   list every row involved under Needs a person to pair.
6. Sort what is left: unpaired ledger payments are outstanding payments;
   unpaired ledger receipts are deposits in transit; unpaired statement
   rows go under On the statement only, with one kind from this list,
   chosen from the statement description: fee, interest, returned
   item, direct debit, or "kind not clear" when none fits. A carried item that paired is
   "cleared on [statement date]"; otherwise it stays open, marked
   "carried".
7. Age each open item in calendar days from its date to the last day of
   the period (an Amount differs pair uses the earlier date). The open
   items are every outstanding payment, every deposit in transit and
   every row On the statement only (carried items included), plus each
   Amount differs pair once and each row under Needs a person to pair
   once; this is the count on the RESULT line and in the brackets.
   Count them within 30 days, 31 to 60 days, over 60 days. Flag an
   outstanding payment older than the old-payment limit "old payment".
   Flag a deposit in transit dated more than the deposit check before
   the last business day of the period, counting business days from
   the day after the deposit date up to and including that last
   business day, "not on the statement after [n] business days", [n]
   being the business days counted.
8. Prove: statement closing balance + ledger receipts the bank has not
   shown yet - ledger payments the bank has not shown yet = adjusted
   statement balance. Ledger closing balance + bank receipts the ledger
   does not show - bank payments the ledger does not show + Amount
   differs gaps = adjusted ledger balance. Rows under Needs a person to
   pair go in on their own side, so an unresolved pair shows on both
   sides until a person decides; that is expected. Difference = adjusted statement minus
   adjusted ledger. Report it as it is; add no rounding item, write-off
   or unnamed amount to close it.
9. Result: "Proof agrees: difference $0.00." or "Proof does not agree:
   unexplained difference of [amount]." Then the counts of open items,
   flagged items and entries to prepare.
10. Entries to prepare: one for each row under On the statement only.
    The bookkeeper chooses the coding. Amount differs and
    Needs a person to pair items are "waiting on an answer". Post
    nothing.
11. Questions: one sentence each, to a role from the settings, naming
    the row, date and figures, for every Amount differs pair, every
    group needing a person, every flag, every statement row whose kind
    is not clear and every returned item. A statement payment to an
    unfamiliar payee with no explaining description goes first, to the
    owner. Say what the statement shows; do not speculate.
12. If the proof does not agree, list where to look, in order: an older
    open item missing from last month's list; a ledger row that belongs
    to another account; a gap whose amount in cents is divisible by 9;
   a row counted twice in an
    export; an item dated in the wrong period. Otherwise "Not needed."

Use the output format exactly. Every section appears, in order; write
"None." under any section with nothing in it. Show no account number
beyond its last four digits. If a file shows a full account number, a
password or a login code, repeat no password or code and tell the user
to remove it from the file. End with: "Prepared for review. Nothing has
been posted, cleared, written off or sent."

If asked to post, mark cleared, write off, change a figure or make the
proof agree, decline and name the role that does it.

## Output format

```
BANK RECONCILIATION: [account name], ending [last four digits], [statement period]

For: [reviewer role]. Prepared by: [role that ran it] on [preparation date].
Sources: bank statement export, [n] rows, [period]; ledger export, [n] rows; last month's open items, [n], from [period] / not supplied, carried items not checked.
Settings used: date window [n] business days; deposit check [n] business days; old-payment limit [n] days; business days [days]. Defaults used: [list / none].

RESULT
[Proof agrees: difference $0.00. / Proof does not agree: unexplained difference of [amount]. / Stopped at [step]: [reason].]
Open items: [n]. Flagged: [n]. Entries to prepare: [n].

BALANCES
Statement: opening [amount] + money in [amount] - money out [amount] = [amount]. Closing balance on the statement [amount]: [agrees / differs by amount].
Ledger: opening [amount] + money in [amount] - money out [amount] = [amount]. Closing balance in the ledger [amount]: [agrees / differs by amount].

PROOF
Statement closing balance                          [amount]
  Add: ledger receipts the bank has not shown yet   [amount]
  Less: ledger payments the bank has not shown yet  ([amount])
Adjusted statement balance                         [amount]
Ledger closing balance                             [amount]
  Add: bank receipts the ledger does not show       [amount]
  Less: bank payments the ledger does not show      ([amount])
  Amount differences                                [amount]
Adjusted ledger balance                            [amount]
Difference                                         [amount]

MATCHED: [n] pairs. Money in [amount]. Money out [amount].
By reference: statement [date] "[description]" [amount in/out] = ledger [date] [number] "[name]"[, carried].
By amount and date: statement [date] "[description]" = ledger [date] [number] "[name]"[, carried], [amount in/out], [n] business days apart[, description not compared].

OUTSTANDING PAYMENTS
[Date] [number] "[name]" [amount] out, [n] days[, carried]. [FLAG: old payment.]

DEPOSITS IN TRANSIT
[Date] [number] "[name]" [amount] in, [n] days[, carried]. [FLAG: not on the statement after [n] business days.]

ON THE STATEMENT ONLY
[Date] "[description]" [reference, if any] [amount in/out], [n] days. Kind: [fee / interest / returned item / direct debit / kind not clear].

AMOUNT DIFFERS
Reference [ref]: statement [date] [amount in/out]; ledger [date] [number] "[name]" [amount in/out]. Gap [amount]. [n] days.[ Two digits may be swapped.]

NEEDS A PERSON TO PAIR
[Statement / Ledger] [date] [number] "[description or name]" [amount in/out], [n] days. Candidates: [rows].

CARRIED FROM LAST MONTH
[Date] [number] "[name]" [amount]: cleared on [date] / still open, now [n] days.

AGEING
Within 30 days: [n]. 31 to 60 days: [n]. Over 60 days: [n].
Flags: [item: flag / none].

ENTRIES TO PREPARE FOR APPROVAL
[n]. [Statement date] "[description]" [amount in/out]. Kind: [kind].
Coding: chosen by [role]. Posted by [role] after [reviewer role] approves.
Waiting on an answer: [items / none].

QUESTIONS
For [role]: [one sentence naming the row, the date and the figures].

IF THE PROOF DOES NOT AGREE: WHERE TO LOOK
[The checks in order / Not needed.]

SIGN-OFF
Prepared by: [role], [date].
Reviewed by: ____________________  Date: ____________

Prepared for review. Nothing has been posted, cleared, written off or sent.
```

## Before relying on it

Decide every item under "What to customize" in TEMPLATE.md and set the limits the instructions in this file leave open, written in square brackets such as [N], to your own. Then run the acceptance tests in TEMPLATE.md on past work. A person starts this work, supplies the inputs and decides what happens with the result.
