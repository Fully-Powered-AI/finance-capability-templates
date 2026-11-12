# Bank reconciliation preparation

Workflow template, version 0.1.0.

## Purpose

Prepare the reconciliation of one bank account for one statement period from two exports: the bank statement and the same account's ledger register. Every statement line is paired with its ledger entry or set apart with its kind and age; last month's open items are cleared or carried; a two-sided proof shows whether the adjusted balances agree; and the sheet lists the entries still to prepare and the questions for named roles. The assistant prepares and checks. It posts nothing, marks nothing cleared, writes nothing off and changes no record in the bank or the accounting system.

## When to use it and when not to

Use it each month once the statement for the period is available and the books are up to date for those dates. It also suits a mid-month run on a busy account, or catching up a run of months one at a time when reconciliations have fallen behind.

Do not use it:

- for several accounts at once. Run it once per account, so lines from two accounts never meet in one proof;
- to reconcile a receivables or payables ledger, an intercompany balance or a schedule. Those compare different sources and need their own work;
- to decide how an item should be coded or accounted for. That is the bookkeeper's or the reviewer's judgment;
- to investigate a suspected theft or fraud. The sheet lists the line and the question; the owner decides what happens next;
- when either export is missing, or when an export does not add up to its own closing balance.

## Roles

- **Runs it:** the bookkeeper or staff accountant.
- **Reviews and signs:** the controller, the owner or the outside accountant. The reconciliation is complete only when this person signs.
- **Codes and posts entries, and marks items cleared in the accounting system:** the bookkeeper, after the reviewer approves. Always a person.
- **Answers questions:** the role named on each question, such as whoever banks the cash, handles card takings, or pays suppliers.
- **Decides on a line that may be fraud or an error by the bank:** the owner or the reviewer.

## Inputs

1. **Bank statement export** for one account and one statement period, one row per line. Default column headers: `Date`, `Description`, `Reference`, `Money out`, `Money in`. A single `Amount` column, with money out as a negative number, is accepted in place of the last two. With it, the statement's **opening balance** and **closing balance**, from the export or typed from the statement. If the export or either balance is missing, stop.
2. **Ledger export:** the register of the same bank account from the accounting system, for the same dates. Default column headers: `Date`, `Type`, `Number`, `Name`, `Memo`, `Amount`, where money into the account is positive and money out is negative. With it, the account's **opening balance** and **closing balance** for the period. If the export or either balance is missing, stop. Where the system exports `Debit` and `Credit` instead of `Amount`, a debit to a bank account is money in; ask the person to confirm before using it.
3. **Last reconciliation's open items:** every item the previous reconciliation left outstanding. Default column headers: `Date`, `Type`, `Number`, `Name`, `Amount`, signed as in the ledger. If missing, continue; say on the sheet that carried items were not checked and that the proof may not agree for that reason.
4. **Settings:** the account's name and last four digits, the statement period, the date the sheet is prepared, the roles above, the bank's business days and any bank holidays in the period, and three limits. If a limit is missing, use its default and list it under "Defaults used":
   - **date window:** how many business days apart two dates may be and still match. Default [your date window, default 3] business days;
   - **deposit check:** how many business days a ledger deposit may wait before it should be on the statement. Default [your deposit check, default 5] business days;
   - **old-payment limit:** the age at which an uncashed check or other payment is flagged. Default [your old-payment limit, default 60] days.
   If the business days are missing, use Monday to Friday and list that too.
5. **A column map** (optional), when the person's exports use other headings: which of their columns holds each default column.

**When a header does not match.** If any column the work needs is not found under its default heading and no column map covers it, stop and ask which column holds it. Never infer a column from its contents.

The work uses only the last four digits of an account number. It needs no connection to the bank or the accounting system and never asks for a password or a login code.

## The procedure

1. **Check the exports.** Confirm the headings, or apply the column map. Confirm the bank export covers one account: if it carries an account column with more than one value, stop. Confirm every row in both exports is dated inside the statement period; if any is not, stop and ask for exports cut to the period (items from earlier months come from the open items list, not the ledger export). Count the rows on each side.
2. **Put both sides on one sign.** Money into the account is positive and money out is negative, on both sides. Keep each row's description and name exactly as supplied, so the reviewer can judge every pairing from both sides' own words.
3. **Foot each export.** Statement opening balance plus every statement row must equal the statement closing balance. Ledger opening balance plus every ledger row must equal the ledger closing balance. If either fails, stop: report the four figures and the gap, and say the export may be missing rows or carry rows from somewhere else. Match nothing from an export that does not foot.
4. **Set up the ledger side.** This period's ledger rows, plus last month's open items, each marked "carried".
5. **Match by reference first.** A statement row and a ledger row or carried item with the same check or payment reference, the same direction and the same amount are a pair, "by reference". The same reference with a different amount is not a match: record it under Amount differs with both figures and the gap (statement amount minus ledger amount). Where the gap in cents is divisible by 9 (a $0.09, $4.50 or $9.00 gap qualifies), add "two digits may be swapped".
6. **Then match by amount and date.** For the rows still unpaired: the same signed amount to the cent, dates no more than the date window apart in business days in either order, and descriptions that name the same payer or payee. Count business days from the day after the earlier date up to and including the later date, so two rows on the same day are 0 business days apart and a Friday and the following Monday are 1. A bank's shortened, capitalized or coded version of a name is the same name. Two different businesses are never treated as one, however alike the amounts. Where the statement description is generic, such as DEPOSIT, TRANSFER or blank, match on amount and date alone and mark the pair "description not compared". A row pairs only when it has exactly one candidate on the other side and that candidate has only it. Where any row has two or more candidates, pair none of them and list every row involved under Needs a person to pair.
7. **Sort what is left.** A ledger payment with no partner is an outstanding payment. A ledger receipt with no partner is a deposit in transit. A statement row with no partner goes under "On the statement only", with one kind from this list, chosen from the statement description: fee, interest, returned item, direct debit, or "kind not clear" when none of these fits. A carried item that paired is "cleared on [statement date]"; one that did not stays open in its kind, marked "carried".
8. **Age every open item.** Age is the number of calendar days from the item's date to the last day of the statement period. For an Amount differs pair, use the earlier of the two dates. The open items are every outstanding payment, every deposit in transit and every row On the statement only (carried items included, in their kind), plus each Amount differs pair counted once and each row under Needs a person to pair counted once; this is the count on the RESULT line and in the ageing brackets. Count the open items in three brackets: within 30 days, 31 to 60 days, over 60 days. Flag:
   - an outstanding payment older than the old-payment limit: "old payment";
   - a deposit in transit dated more than the deposit check before the last business day of the period, counted in business days from the day after the deposit date up to and including the last business day: "not on the statement after [n] business days", where [n] is the business days counted.
9. **Prove it.** Adjusted statement balance: the statement closing balance, plus the ledger receipts the bank has not shown yet, less the ledger payments the bank has not shown yet. Adjusted ledger balance: the ledger closing balance, plus the bank receipts the ledger does not show, less the bank payments the ledger does not show, plus the Amount differs gaps. Rows under Needs a person to pair go into the proof on their own side, as unpaired rows, so an unresolved pair shows on both sides until a person decides; the same amount on both sides is expected. The difference is the adjusted statement balance less the adjusted ledger balance. Report the difference as it is: no rounding item, write-off or unnamed amount is added to close it.
10. **Write the result.** "Proof agrees: difference $0.00." or "Proof does not agree: unexplained difference of [amount]." followed by the number of open items, the number flagged and the number of entries to prepare. If the run stopped, the result says where and why and nothing else is drafted.
11. **List the entries to prepare.** Each row under "On the statement only" becomes one entry to prepare, with its date, amount and statement description. The bookkeeper chooses the coding. Rows under Amount differs and Needs a person to pair are listed as "waiting on an answer": a person decides first whether any entry is needed. Nothing is posted.
12. **Write the questions.** One sentence each, addressed to a role from the settings, naming the row, the date and the figures: every Amount differs pair, every group under Needs a person to pair, every flag, every statement row whose kind is not clear, and every returned item. A statement payment to a payee that appears nowhere in the ledger export or last month's list, with no description that explains it, goes first, addressed to the owner.
13. **If the proof does not agree, say where to look,** in this order: an older open item that is missing from last month's list; a ledger row posted to this account that belongs to another; a gap whose amount in cents is divisible by 9; a row counted twice in an export; an item dated in the wrong period. When the proof agrees, write "Not needed."
14. **Return the sheet** to the person who ran it, for the reviewer. The reviewer signs. After approval, the bookkeeper posts the entries and marks items cleared in the accounting system.

## Exceptions and stop conditions

- **Either export, or either pair of balances, is missing:** stop and say which.
- **A heading the work needs does not match and no column map covers it:** stop and ask which column holds it.
- **The bank export carries more than one account:** stop; ask for one account per run.
- **A row is dated outside the statement period:** stop; ask for exports cut to the period.
- **An export does not foot to its closing balance:** stop; report the four figures and the gap. Match nothing.
- **A row has more than one candidate partner:** pair none; list them all for a person.
- **The proof does not agree:** produce the whole sheet, show the difference, and list where to look. Never force it to zero.
- **A payment to an unfamiliar payee, or a transfer to an account nobody recognizes:** list it, and put its question first, addressed to the owner. Say what the statement shows; do not speculate about who made it.
- **Asked to post an entry, mark an item cleared, write off a difference, change a figure in either export or make the proof agree:** decline and name the role that does it.
- **An export shows a full account number, a password or a login code:** show no account number beyond its last four digits; repeat no password or code; tell the person to remove it from the file.

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

Where a section has nothing in it, write "None." under its heading. Every section appears on every sheet, in this order.

## Reviewer checklist

1. Both footing lines are arithmetically right and agree with the closing balances on the statement and in the ledger. (Reviewer)
2. The proof is arithmetically right, uses only the open items listed, and closes no gap with a rounding item, write-off or unnamed amount. (Reviewer)
3. Every statement row and every ledger row appears exactly once: in a pair, in an open list, under Amount differs or under Needs a person to pair. (Bookkeeper)
4. Every pair by amount and date is within the date window, and its two descriptions name the same payer or payee or are marked "description not compared". (Bookkeeper)
5. No row with two candidates has been paired. (Reviewer)
6. Nothing on last month's list has gone missing: each item is either paired with a statement row or carried again with its new age. (Bookkeeper)
7. Every age is counted to the last day of the period, and every flag is true. (Reviewer)
8. Every entry to prepare comes from a statement row, and none has been posted. (Reviewer)
9. Every question names a role and the figures it is about. (Bookkeeper)
10. No account number is shown beyond its last four digits, and the reviewer has signed. (Reviewer)

## Acceptance tests

Proposed tests. None has been run.

1. **Clean month.** Every statement row has one ledger partner; no carried items. Expected: all rows paired, every open list "None.", the proof agrees.
2. **Check cleared after the period.** A check written on the 28th that is not on the statement. Expected: under Outstanding payments with its age; the proof agrees.
3. **Carried check clears.** Last month's list holds check 1182 for $860.00; the statement shows check 1182 for $860.00. Expected: paired by reference, shown under Carried as cleared with the statement date.
4. **Amount keyed wrongly.** Check 1191 is $454.00 in the ledger and $445.00 on the statement. Expected: under Amount differs with a $9.00 gap and "two digits may be swapped"; the gap in the proof; listed as waiting on an answer.
5. **Debited twice.** Two statement debits of $1,326.75 a day apart against one ledger payment. Expected: none paired; all three rows under Needs a person to pair; a question asking whether a second payment was due.
6. **Deposit that lingers.** A deposit recorded seven business days before the period's last business day, not on the statement, with the default deposit check. Expected: under Deposits in transit with the flag.
7. **Old check.** A carried check 74 days old at the period end, with the default old-payment limit. Expected: still open, flagged "old payment", counted over 60 days, with a question for the reviewer.
8. **Bank fees and interest.** Fees and interest on the statement that the ledger does not show. Expected: under On the statement only, and each one an entry to prepare; nothing posted.
9. **Export that does not foot.** One statement row deleted from the export. Expected: stops at the footing check with the four figures and the gap; nothing matched.
10. **Unknown heading.** The bank export's amount column is headed `Value`, with no column map. Expected: stops and asks which column holds the amounts.
11. **Generic description.** A statement row reading only DEPOSIT, one candidate in the window. Expected: paired, marked "description not compared".
12. **Different payee, same amount.** A statement debit of $500.00 to one supplier and a ledger payment of $500.00 to another supplier, one day apart. Expected: not paired.
13. **Asked to force the proof.** "Put the difference down as rounding." Expected: declines; the difference stays and the where-to-look list is shown.
14. **No last-month list.** Expected: continues, says carried items were not checked, and if the proof does not agree, the first place to look is last month's open items.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
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
```

## What to customize

- The column headings your bank and accounting system export, as a column map, and how each signs money out.
- [your date window], [your deposit check] and [your old-payment limit].
- The bank's business days and the holidays it observes.
- Who prepares, who reviews and signs, who codes and posts entries, and who answers questions about cash, card takings, supplier payments and returned items.
- Whether a second person must review every month or only above a size of difference you set.
- Where signed reconciliations and last month's open items are kept, so the next run starts from them.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 9 November 2026. Written by Fully Powered AI. Tried on its invented example on 9 November 2026 in one run; the record is published with it and lists the small edits made afterward that have not been run again. That run did not reach the stop conditions or the path where the proof does not agree. Not yet tested in a client environment.
