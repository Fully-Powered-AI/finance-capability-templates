# Year-end tax packet for the accountant

Workflow template, version 0.1.0.

## Purpose

Prepare one year-end tax packet for a small business's outside accountant once the year's books are closed: the year's headline figures restated from the closed books with two arithmetic checks; the documents the accountant asked for, each marked have, partly, missing or nothing to send; every contractor paid for services in the tax year, totalled by payee, with those at or above the reporting threshold the person supplies and every missing tax details form flagged; the estimated or advance tax payments made for the year, exactly as recorded; the questions to ask the accountant; and the actions the person must finish before the packet goes. Every assumption is printed on the packet. The assistant organizes and checks. It works out no tax, says nothing about how any item should be treated, and gives no tax position. People request the missing forms, approve the packet and send it to the accountant. The assistant sends, files and pays nothing and changes no record.

## When to use it and when not to

Use it after the books for the tax year are closed and the year-end bank and card accounts are reconciled, usually in the first weeks after the year end, and when the accountant's request letter or organizer arrives. Run it again as missing documents and forms come in, until the packet is complete.

Do not use it:

- while a notice, letter, audit or inquiry from a tax authority is open. That goes to the accountant at once, and this packet waits;
- to close the books or reconcile an account. Those come first and are their own workflow templates;
- to prepare for a financial statement audit. That is a different pack for a different reader;
- to work out tax owed, an estimated payment, a deduction, a penalty or a safe-harbour figure, or to decide a business structure or an election. Those belong to the accountant. The packet lists them as questions;
- to decide which states or countries the business must collect sales tax, VAT or GST in. Ask the accountant;
- to prepare, issue or file a tax form for a contractor or a tax return. The packet tells the person and the accountant what is ready and what is missing.

## Roles

- **Runs it:** the owner or the bookkeeper.
- **Approves the packet and sends it to the accountant:** the owner, or whoever the settings name.
- **Requests each missing tax details form from the contractor:** the owner or the bookkeeper. The assistant contacts nobody.
- **Answers the questions, prepares and files the returns and forms:** the accountant.

## Inputs

1. **Settings.** Business name; country, and the state, province or region where it taxes the business separately; the tax year's first and last day; the currency; the business structure and accounting basis as the person states them; who prepares the packet, who approves it and who requests missing tax details forms; the date the books were closed, by whom, and whether the year-end bank and card accounts are reconciled; today's date; the expense accounts that hold payments to contractors for services; the reporting threshold for contractors, the name of the form that reports them and the name of the form that records a contractor's tax details, with where each came from. If the country, the tax year or the closing date is missing, stop and ask. If the reporting threshold is missing, never supply one: list every contractor and write "reporting rule not supplied". If the service accounts are missing, ask which accounts hold payments to contractors.
2. **The accountant's request letter or organizer,** if one arrived: each item asked for, and the date the accountant wants the packet. If none, use the default document list in step 5 and say so.
3. **The closed year's reports:** the profit and loss for the tax year, and the balance sheet, or its cash, card and loan lines, at the last day of the tax year. If missing, stop: the packet is built from the closed books.
4. **The vendor payments export,** every payment in the service accounts for the tax year and to the same payees in other accounts. Default headers: `Date,Payee,Account,Amount,Method,Reference`. Method is one of bank transfer, cheque, cash, card or payment platform. A payment made after the year end may be included; it is shown and not counted.
5. **The contractor details list.** Default headers: `Payee,Legal name,Entity type,Tax details form on file,Tax ID on file`. Entity type is as the person states it. The last two columns say yes or no; they never hold the numbers themselves.
6. **Estimated or advance tax payments.** Default headers: `Date paid,Authority,Period,Amount,Confirmation held`. Period is the tax period the payment was made for, as the person records it.
7. **Documents on hand:** each document gathered, its status (have or missing) and a note, such as a statement's closing balance or the date a missing document is expected.
8. **Notes on the year:** events the accountant should know about, such as a large purchase, a new loan, a change of premises or a home office, any letter from a tax authority, and the person's own questions.

Where an export's headers do not match the defaults or the column map in the settings, stop and ask: show the headers found and the headers expected, and continue only when the person says which column is which. The assistant works from files and notes the person supplies, needs no connection to the accounting system, the bank or any tax authority's site, and never asks for a password or a login code.

## The procedure

1. **Look for a stop first.** Read the notes and the documents list for any notice, letter, audit, examination or inquiry from a tax authority. If one is open, or its state is not said, stop and return only the stopped block from the output format. A letter the person says is closed and already with the accountant is listed under the documents instead. A note saying there are none, such as "no letters from the tax authority this year", and an item on the accountant's request list asking for any such letters are not a stop.
2. **Check the books are closed.** The settings must give the closing date and say the year-end bank and card accounts are reconciled. If either is missing, stop and say the packet waits for the closed books.
3. **Check the inputs.** Confirm one business, one tax year and one jurisdiction. Check every export's headers; on a mismatch, stop and ask. Where the business structure or the accounting basis is not stated, write "not stated" and add an action for the person; never assume one.
4. **The year in figures.** Restate, with the report each comes from: total income, total expenses and net profit from the profit and loss; each service account's line; each cash, card and loan balance at the last day of the tax year. Then two checks. First, total income less total expenses against the net profit the report prints. Second, each year-end balance against the closing balance in the documents on hand: agrees, differs by the amount, or statement not supplied. A difference becomes an action for the bookkeeper; it is not corrected.
5. **Documents for the accountant.** Use the accountant's request list, item by item in its order and wording. Without one, use this default list: the profit and loss for the tax year; the balance sheet at its last day; the general ledger or trial balance; year-end statements for every bank, card and loan account; the payroll provider's year-end reports, where the business has employees; the contractor list in this packet, with the forms on file; records of estimated or advance tax payments; invoices for equipment, vehicles and other large purchases, and records of anything sold or scrapped; annual summaries from card processors and payment platforms; sales tax, VAT or GST returns filed for the year, where the business files them; last year's return; and records the owner keeps outside the books that the accountant has asked for before, such as a vehicle log. Match each item to the documents on hand and mark it: have, partly (say what is missing), missing (with the expected date where given), in this packet, nothing to send (as the person states), or not stated. Flag any document expected after the date the accountant wants the packet.
6. **Contractors.** Count a payment when its date falls inside the tax year and its account is a service account. Show, and do not count, payments dated outside the tax year and payments to the same payees in other accounts. Total the counted payments by payee, matching the payee name exactly. Join each payee to the contractor details list. Then:
   - With a threshold supplied, list payees at or above it, then every payee below it with their totals. With none, list every payee in one list.
   - Flag, on the payee's line: no tax details form on file; not on the contractor details list; any payment by card or payment platform, since the accountant rules on how such payments are reported; an entity type the person states as a corporation; an entity type stated as an LLC, a partnership or another entity with no tax treatment stated beside it (a stated LLC with no tax treatment is flagged; one stated as taxed as a corporation is flagged as a corporation); entity type not stated. Never leave a payee out because of its entity type or payment method.
   - Possible duplicates: names that share their distinctive words, or two payees with the same legal name. Show both, with the combined total, and say if the combined total reaches the threshold. Never merge them; the person confirms.
   - Missing forms: every payee at or above the threshold with no tax details form on file, and every possible-duplicate pair whose combined total reaches the threshold with no form for either. With no threshold supplied, every payee with no form on file. A person requests each form; the assistant drafts and sends nothing.
   - Cross-check: the counted total for each service account against that account's line in the profit and loss. If they differ, say by how much, and add an action for the bookkeeper. On an accrual basis a difference can be timing; say so and do not explain it further.
7. **Estimated tax payments.** List every row as recorded, in date order. A payment belongs to the period in its Period column; if that is blank, write "period not stated". Group: payments for the tax year (including any made after the year end), and payments made during the tax year for an earlier period. Total the payments for the tax year by authority. Any row with no confirmation held becomes an action. Never say whether the payments are enough, what is still owed, or what to pay next.
8. **Questions for the accountant.** One question per contractor flag that needs the accountant's judgment (card or platform, a stated entity type) on a payee at or above the threshold, or on every payee when no threshold is supplied; one per possible duplicate whose combined total reaches the threshold; one per event in the notes; one per figure check that differs; one asking for the reporting rule when none was supplied; one per negative payment; and each of the person's own questions as written, tidied only for grammar. Where the person's question is about an event in the notes, ask it once, in their words, with the event's facts. Each question gives the facts from the inputs and names its source. Answer none of them and suggest no answer.
9. **Actions before the packet goes.** One numbered action per gap the person can close: a missing or partly missing document, a missing tax details form, a possible duplicate to confirm, a payee missing from the contractor details list, a payee whose entity type is not stated, a missing estimated payment confirmation, a figure that differs, a structure or basis not stated, a document due after the accountant's date. Each names the role that does it: documents and figures go to the preparer; form requests go to the role the settings name for them; confirming payees (a possible duplicate, a payee missing from the list, an entity type not stated) and finding a missing estimated payment confirmation go to the approver.
10. **Assumptions.** Print every assumption the packet relies on: how contractor payments were counted and by which date, which accounts were treated as services, how payees were matched, which period each estimated payment was put in, every default used, that counted payments are shown as totals by payee, without each payment's date, which stays in the vendor payments export, and that the structure and basis are as the person states them. Write "none" only if there are none.
11. **Return the draft** to the person who ran it, for the approver. The approver settles the actions, and a person sends the approved packet to the accountant.

## Exceptions and stop conditions

- **A notice, letter, audit, examination or inquiry from a tax authority that is open, or whose state is not said:** stop. Return only the stopped block, which tells the person to take it to the accountant now. Prepare no packet and draft no reply to the authority. A note saying there are none, or a request-list item asking for any, is not a stop.
- **The books are not stated as closed, or the year-end bank and card accounts are not reconciled:** stop and say the packet waits for the closed books.
- **No country or region, no tax year, or no profit and loss:** stop and ask.
- **An export's headers do not match:** stop and ask, showing the headers found and expected.
- **No reporting threshold supplied:** do not supply one from memory. List every contractor, write "reporting rule not supplied", and add a question asking the accountant for the rule.
- **Asked what tax is owed, what to pay, whether the payments are enough, what can be deducted, how an item should be treated, or whether to change structure or make an election:** decline in one line, and add the question to the questions for the accountant.
- **Asked to file a return, issue or file a contractor form, send a form request, pay a tax, contact the accountant, a contractor or a tax authority, or change a record:** decline, and name the person who does it.
- **An input holds a tax ID number, a personal identity number, a complete bank account number or a complete card number:** do not repeat it anywhere in the packet. Show only "on file", and tell the person to remove it from the source before the packet is shared.
- **A payee appears in the export with a negative amount, such as a refund from a contractor:** show it on the payee's line, count it in the net total, and add a question for the accountant.

## Output format

```
YEAR-END TAX PACKET: [business], tax year [year]

Draft packet for [the accountant] to review. It is not tax advice: it works out no tax and says nothing about how any item should be treated.
For: [the accountant]. Packet wanted by: [date / not stated]. Prepared by: [role], [today's date]. Approves: [role].
Jurisdiction: [country, state or region]. Tax year: [first day] to [last day]. Currency: [code].
Business structure: [as stated / not stated]. Accounting basis: [as stated / not stated].
Books closed: [date], by [role]. Year-end bank and card accounts reconciled: [yes, as stated].
Sources: [each input, with its count of items or rows / "not supplied"].

ASSUMPTIONS
[n]. [Assumption.] / None.

1. THE YEAR IN FIGURES
[Line]: [amount] ([report]).
Check: total income [amount] less total expenses [amount] = [amount]. The report prints net profit [amount]: [agrees / differs by amount].
Check: [account] at [last day]: balance sheet [amount], statement [amount]: [agrees / differs by amount / statement not supplied].

2. DOCUMENTS FOR THE ACCOUNTANT
List used: [the accountant's request list, n items / the default list, n items].
Have [n]. Partly [n]. Missing [n]. In this packet [n]. Nothing to send [n]. Not stated [n].
[n]. [Item, in the accountant's wording]: [have / partly: what is missing / missing[, expected date] / in this packet, section 3 / nothing to send, as [role] states / not stated]. [Detail from the documents on hand.] [FLAG, after the accountant's date: expected [date].]

3. CONTRACTORS
Reporting rule: [threshold, form that reports contractors, form that records tax details], from [source]. / Reporting rule not supplied: every contractor is listed.
Counted: [n] payments, [total], in [service accounts], dated [first day] to [last day].
Shown, not counted: [payee, date, account, amount, reason] / none.
At or above [threshold]: [n] payees, [total].
[Payee] ([legal name / not on the contractor details list]): [total] in [n] payments, [accounts]. Paid by: [methods]. Entity type: [as stated / not stated]. Tax details form: [on file / not on file / not stated]. [FLAG, kind[, kind]: the facts.]
Below [threshold]: [Payee] [total], paid by [methods], tax details form [on file / not on file / not stated][, FLAG ...] / none.
Possible duplicates: [Payee] ([total]) and [Payee] ([total]): combined [total][, which reaches the threshold]. For [role] to confirm; not merged. / None.
Missing tax details forms: [n]. [Payee, total] / none. [Role] requests each form; nothing has been sent.
Check: [service account] counted [amount]; profit and loss [amount]: [agrees / differs by amount].

4. ESTIMATED TAX PAYMENTS
For tax year [year]:
[Date paid]  [Authority]  [Period / period not stated]  [Amount]  Confirmation: [held / not held / not stated][  (paid after the year end)]
Total for [year]: [Authority] [total] in [n] payments.[ [Next authority] [total] in [n] payments.] / None recorded.
Paid during [year] for an earlier period:
[Date paid]  [Authority]  [Period]  [Amount]  Confirmation: [held / not held / not stated] / None.
These are the payments as recorded. Whether they are enough is for the accountant.

5. QUESTIONS FOR THE ACCOUNTANT
[n]. [Question, with the facts.] (From: [section, notes, or the person's own question].) / None.

6. BEFORE THE PACKET GOES
[n]. [Action.] ([Role].) / None.

Draft for the [approver]'s approval. Nothing has been sent, filed, paid or changed.

[If stopped, return only this:]
STOPPED: [business], tax year [year]
[The notice, letter, audit or inquiry], from [authority], as [source] describes it. Take it to [the accountant] now. No packet has been prepared and no reply has been drafted.
```

## Reviewer checklist

1. The packet says on its first lines that it is a draft for the accountant to review and is not tax advice, and nowhere works out tax owed, an estimated payment or a deduction. (Owner)
2. Every figure in section 1 matches the closed profit and loss, balance sheet or statement it names, and both checks are arithmetically right. (Bookkeeper)
3. Every item on the accountant's list appears once, in the accountant's order and wording, with a status that matches the documents on hand. (Bookkeeper)
4. Every counted payment falls inside the tax year and in a service account; every payment shown and not counted gives its reason; the payee totals add up to the counted total. (Bookkeeper)
5. No payee was dropped for its entity type or payment method, and no possible duplicates were merged. (Owner)
6. Every missing tax details form at or above the threshold is on the missing list, with a person to request it. (Owner)
7. The estimated payments match the confirmations and are listed in the period recorded, with no judgment on whether they are enough. (Owner)
8. Every assumption the packet relies on is printed, and every question gives its facts without an answer. (Owner)
9. No tax ID, personal identity number or complete bank or card number appears anywhere. (Bookkeeper)
10. The packet is approved before a person sends it to the accountant. (Owner)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary year.** Closed books, the accountant's list, a full export, all forms on file. Expected: every section complete, both checks agree, no flags, questions only from the notes.
2. **Notice in the notes.** The notes mention a letter from a tax authority, with nothing said about whether it is closed. Expected: only the stopped block; no packet.
3. **Books not closed.** The settings give no closing date. Expected: stops and says the packet waits for the closed books.
4. **No threshold supplied.** Expected: every contractor in one list, "reporting rule not supplied", and a question asking the accountant for the rule; no threshold supplied from memory.
5. **Header mismatch.** The export's payee column is headed "Vendor". Expected: stops, shows the headers found and expected, asks which column is which.
6. **Payment after the year end.** A contractor paid on 6 January for December work. Expected: shown and not counted, with the reason; the assumption on counting by date paid is printed.
7. **Corporation and platform payee.** One payee stated as a corporation, one paid only through a payment platform. Expected: both listed and flagged, each with a question for the accountant; neither left out.
8. **Possible duplicate.** Two similar payee names, each below the threshold, combined above it, with no form on file. Expected: shown as a possible duplicate with the combined total, not merged, on the missing forms list, an action to confirm and a question.
9. **Payments in another account.** A contractor also paid for materials. Expected: the materials payment shown and not counted; the service total unchanged.
10. **Export differs from the profit and loss.** The counted contract labour total is $500 below the profit and loss line. Expected: the check says "differs by $500", an action for the bookkeeper, and a question; no figure changed.
11. **Asked what is owed.** "Tell me what to pay for the last quarter." Expected: declines in one line; the question appears under questions for the accountant.
12. **Tax ID in the input.** The contractor details list holds a full tax ID number. Expected: the number appears nowhere; "on file" only; the person told to remove it from the source.
13. **Default document list.** No request letter from the accountant. Expected: "the default list" with its items, each with a status.
14. **A note that there are no letters.** The notes say "No letters from the tax authority this year" and the request list asks for any letters. Expected: no stop; the request item is marked "nothing to send, as the owner states".

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a year-end tax packet for a small business's outside
accountant, after the year's books are closed. You organize and check.
You work out no tax, estimated payment, deduction or penalty, say
nothing about how any item should be treated, and give no tax position.
You never send, file or pay anything, request a form, contact anyone, or
change any record. You never ask for a password or a login code.

The user will supply: settings (business, country and region, tax year,
currency, structure and basis as stated, preparer, approver and who
requests missing forms, the date the books were closed and whether
year-end bank and card accounts are reconciled, today's date, the
service accounts, the reporting threshold and form names with their
source); the accountant's request list, if
any; the closed profit and loss and the balance sheet lines; the vendor
payments export (Date,Payee,Account,Amount,Method,Reference); the
contractor details list (Payee,Legal name,Entity type,Tax details form
on file,Tax ID on file); estimated tax payments (Date paid,Authority,
Period,Amount,Confirmation held); the documents on hand; notes on the
year.

1. If the notes or documents mention a notice, letter, audit or inquiry
   from a tax authority that is open or whose state is not said, return
   only the stopped block. A letter the person says is closed and
   already with the accountant is listed under the documents, not a
   stop. A note saying there are none, or a request list item asking
   for any, is not a stop. If the books are not stated as closed and
   reconciled, stop and say so. If the country or region,
   the tax year or the profit and loss is missing, stop and ask. If an export's
   headers do not match, stop: show the headers found and expected and
   ask which column is which. Never assume a structure or basis; write
   "not stated" and add an action.
2. The year in figures: restate total income, total expenses, net
   profit, each service account line, and each cash, card and loan
   balance at year end, naming the report. Check income less expenses
   against the printed net profit, and each balance against the
   statement's closing balance. A difference is an action, never a
   correction.
3. Documents: use the accountant's list in its order and wording. If
   there is none, use this default list and say so: profit and loss;
   year-end balance sheet; general ledger or trial balance; year-end
   statements for every bank, card and loan account; payroll year-end
   reports, if there are employees; the contractor list in this packet;
   estimated tax payment records; invoices for large purchases and
   records of anything sold or scrapped; card processor and payment
   platform annual summaries; sales tax, VAT or GST returns, if filed;
   last year's return; records the accountant has asked for before,
   such as a vehicle log. Mark each: have,
   partly (what is missing), missing (expected date), in this packet,
   nothing to send (as stated), or not stated. Flag any document
   expected after the date the accountant wants the packet.
4. Contractors: count a payment only if its date is inside the tax year
   and its account is a service account. Show the rest that concern the
   same payees, with the reason, and do not count them. Total by exact
   payee name; join to the contractor details list. List payees at or
   above the supplied threshold, then every payee below it. If no
   threshold is supplied, never supply one: list everyone and write
   "reporting rule not supplied". Flag: no form on file; not on the
   details list; any card or platform payment (the accountant rules on
   how it is reported); an entity type stated as a corporation; an LLC,
   partnership or other entity with no tax treatment stated (a stated
   LLC with no tax treatment is flagged); entity type not stated. State
   each flag as a fact. Never leave a payee out. Show a negative amount
   on its payee's line and count it in the net total. Show possible
   duplicates with the combined total, say if it reaches the threshold,
   and never merge them. List missing forms: every payee at or above the
   threshold with no form on file, and every possible-duplicate pair
   whose combined total reaches the threshold with no form for either;
   with no threshold, every payee with no form on file. Check each
   service account's counted total against the profit and loss; if they
   differ, say by how much and add an action for the bookkeeper. On an
   accrual basis, say a difference can be timing and explain no further.
5. Estimated payments: list each row as recorded, by the period in its
   Period column. Group those for the tax year, including any paid after
   the year end, and those paid during the year for an earlier period.
   Total for the tax year by authority. Never say whether the payments
   are enough, what is owed or what to pay next.
6. Questions for the accountant: one per card, platform or stated
   entity type flag on a payee at or above the threshold (every payee if no
   threshold), one per possible duplicate that reaches the threshold,
   one per event in the notes, one per check that differs, one asking
   for the reporting rule if none was supplied, one per negative
   payment, and each of the person's own questions as written; where a
   question is about an event, ask it once with the event's facts. Give
   the facts and the source. Answer none and suggest no answer.
7. Before the packet goes: one numbered action per gap the person can
   close, each with its role: documents and figures to the preparer;
   form requests to the role named for them; confirming payees (a
   possible duplicate, a payee missing from the details list, an entity
   type not stated) and finding a missing estimated payment
   confirmation to the approver.
8. Print every assumption: how payments were counted and by which date,
   which accounts were treated as services, how payees were matched,
   which period each estimated payment was put in, defaults used, that
   counted payments are shown as totals by payee, without each
   payment's date, which stays in the vendor payments export, and that
   the structure and basis are as stated.
9. Use the output format exactly. Write "none" in any empty section.
   Recompute every total before you return the packet. End with the
   line saying nothing has been sent, filed, paid or changed.

If asked what is owed, what to pay, whether payments are enough, what
can be deducted, how to treat an item, or whether to change structure
or make an election, decline in one line and add it as a question for
the accountant. If asked to file, issue a form, send a request, pay,
contact anyone or change a record, decline and name the person who does
it. If an input holds a tax ID, a personal identity number or a complete
bank or card number, never repeat it; write "on file" and tell the user
to remove it from the source.
```

## What to customize

- Your column map, if your accounting system's exports use other headings than the defaults.
- Your service accounts: the expense accounts that hold payments to contractors for services.
- Your reporting rule, from your accountant: the threshold, the form that reports contractors and the form that records a contractor's tax details. The template never supplies one for you.
- Your accountant's request list, saved each year, so the packet follows the accountant's order and wording.
- The default document list, with items your accountant always wants and items that never apply to you.
- Who prepares the packet, who approves it and who requests missing forms.
- Which events in the year always go to the accountant as questions, such as a change of premises or a new loan.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried once on its invented example in Claude on 10 November 2026; the record of that run is published with it, and lists the small edits made afterward that have not been run again. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
