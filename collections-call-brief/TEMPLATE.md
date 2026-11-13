# Collections call brief

Workflow template, version 0.1.0.

## Purpose

Prepare the person who phones a business customer about overdue invoices, and record what the call settled. Before the call, it builds one page from the ledger and the contact history the person supplies: every open invoice with its age, what the customer was told and promised in earlier contacts and whether each promise was kept, any dispute, query or credit note still open, the contact to ask for, the questions to settle on the call, and what the caller may offer, quoted from the company's written collections terms. After the call, it turns the caller's notes into a call record for a named person to confirm: the answer to each question, the promises the customer made, anything asked for or offered beyond the written terms, the actions that follow and a contact log entry ready to be entered. The assistant prepares; it never phones, emails or writes to the customer, never threatens a consequence, never offers a payment date, instalment, discount, waiver or credit the written terms do not allow, and never changes a record.

## When to use it and when not to

Use it before a call to a business customer whose account has overdue invoices: after written reminders have gone unanswered, when a promised payment has not arrived, or when the owner wants a balance settled by phone. Run it again after the call, with the caller's notes, to produce the call record.

Do not use it:

- for written reminders sent by age bracket. That is overdue-invoice follow-up preparation, a separate piece of work;
- to match receipts, investigate short payments or decide what a payment was for. That is a receivables exception review;
- for the weekly summary of all receivables for management;
- to answer a card chargeback raised through the customer's bank;
- for a customer who is an individual rather than a business. this workflow template is for business customers only and stops;
- once an account has gone to a lawyer, a collections agency or an insolvency process, or when the customer has asked not to be phoned. It stops and hands the account to the person who decides;
- to decide whether to stop supplying a customer, charge interest or fees, write off a balance or settle a dispute. People decide those, and the brief never raises them on the customer's side of the call.

## Roles

- **Runs it and makes the call:** the credit controller, the bookkeeper or the owner, named in the settings as the caller.
- **Confirms the call record, and decides anything beyond the written terms:** the role named in the settings as the approver, such as the finance manager or the owner.
- **Applies payments and enters the contact log:** the role named in the settings.
- **Handles each open dispute:** the owner named on the disputes file.
- **Writes and approves the collections terms:** the approver, once, before the first run.

## Inputs

1. **The settings,** typed by the caller: the company; the customer and account number; the customer type (`business` or `individual`); today's date; the caller's role; the approver's role; the role that applies payments and enters the contact log; the currency; the ledger balance on the account today, as the accounting system shows it; the payment terms on the account; the account status (`open`, or `on stop` with the date and the role that decided it); the grace days allowed for a promised payment to arrive (default 3); and how far back to read the contact log and payments (default 90 days). If the customer type, today's date or the ledger balance is missing, stop and ask.
2. **The open items export** for the account, one row per open document. Default column headers: `doc_no, doc_type, doc_date, due_date, amount, open_amount, reference`. `doc_type` is `invoice`, `credit note` or `unapplied payment`. Credit notes and unapplied payments carry negative amounts and may have no `due_date`. Dates are written `YYYY-MM-DD`; amounts are plain numbers with no thousands separator. If missing, stop and ask.
3. **The payments export** for the same account and period, one row per application of a payment. Default column headers: `payment_id, date, amount, applied_to`. `applied_to` is an invoice number or `unapplied`; a payment spread over three invoices is three rows. If missing, continue, write "payments not supplied" in the header, and mark every promise "not judged: payments not supplied".
4. **The contact log** for the account. Default column headers: `date, method, direction, contact, logged_by, summary, promise_amount, promise_date, promise_invoices`. `direction` is `in` or `out`; `promise_invoices` lists invoice numbers separated by semicolons, or is blank for a payment on account. If missing, continue and write "contact log not supplied" under What they were told and promised.
5. **The customer's contacts.** Default column headers: `contact, role, phone, email, preferred_for_payments, notes`. `preferred_for_payments` is `yes` or `no`. If missing, continue; the brief says to ask for accounts payable and note the name.
6. **The disputes file:** disputes logged for the account. Default column headers: `dispute_ref, doc_no, raised_date, amount, reason, status, owner, last_update`. `status` is `open` or `resolved`. If missing, write "disputes file not supplied" under Disputes, queries and credit notes, and treat no invoice as in dispute.
7. **The collections terms:** the company's own written rules on what a caller may agree on a call, as numbered items, with a title and a date, approved by the approver. If missing, the brief offers nothing beyond asking for payment in full and a date.
8. **After the call:** the caller's notes as typed, with the date and time of the call, and the brief from the first run. If the notes are missing, stop and ask.

If any header does not match the default, stop, show the expected and the found headers, and ask which column is which. Never guess a column. The assistant works only from what the person supplies, needs no access to any system and never asks for a password or a login code.

## The procedure

Part A, before the call:

1. **Check the inputs.** Confirm every header. Confirm every date and amount can be read. If a `doc_no` or `payment_id` row repeats exactly, stop and ask which is right. Add the `open_amount` of every row in the open items export; if the total differs from the ledger balance in the settings, stop, show both figures and the difference, and draft nothing else.
2. **Check that a call is the right step.** If the customer type is `individual`, stop: this workflow template is for business customers only. If any entry in the contact log, the contacts' notes or the disputes file mentions insolvency, administration, receivership, liquidation, bankruptcy, a lawyer or solicitor, legal action, court, or a collections agency, or says the customer asked not to be phoned or to be contacted only in writing, stop: prepare no brief, quote the entry with its date, and say the account goes to the approver.
3. **Age every invoice.** Days overdue = today's date − `due_date`, in calendar days. Above 0 is overdue; 0 is "due today"; below 0 is "due in [n] days" and not yet due. List invoices oldest due date first. List credit notes and unapplied payments separately, as credits not yet used.
4. **Mark disputes.** An invoice with an `open` row in the disputes file is in dispute for the dispute's `amount`, or for its whole open amount when the dispute's amount is equal or larger. The rest of the invoice is not in dispute. Ignore `resolved` rows.
5. **Find queries that were never logged.** A contact log entry inside the period whose summary says the customer is querying, disputing, holding or complaining about an invoice, or about an order whose reference matches an invoice's `reference`, and that has no `open` dispute on that invoice, is a query not logged. Show it with the log's own words and dates. The invoice is not counted as in dispute; it is shown as held by a query not logged, kept out of the general request for payment, and given its own question. The approver decides whether to log it.
6. **Judge every promise** in the contact log inside the period. The window runs from the entry's date to its `promise_date` plus the grace days. Count the payments in the window applied to the invoices in `promise_invoices`, or every payment in the window when `promise_invoices` is blank.
   - Counted at least `promise_amount`: KEPT, naming the payments.
   - The window has not ended (today is on or before its last day) and the amount has not been reached: PENDING, due [promise date].
   - The window has ended and some but not all was counted: PART KEPT, [counted] of [promised].
   - The window has ended and nothing was counted: BROKEN.
   - A promise with no `promise_amount` is judged on its invoices: KEPT if none of them is still open, otherwise PENDING or BROKEN by the window. A promise with no amount and no invoices: "too vague to judge", and a question.
   - A promise with no `promise_date`: "no date given", and a question asking for one.
   When a payment arrived inside a BROKEN or PART KEPT window but was applied to other invoices, say so beside the promise and include it in that promise's question.
7. **Choose who to ask for.** In this order: the contact who made the most recent promise that is BROKEN, PART KEPT or PENDING; otherwise the contact marked `yes` for `preferred_for_payments`; otherwise "no contact on file: ask for accounts payable and note the name". Under Also on file, list each other contact who appears in the contact log inside the period or whose notes say they approve payments, with what they may be needed for, taken from the log or their notes.
8. **Work out where the account stands.** Overdue = the open amounts of overdue invoices. In dispute = the disputed amounts from step 4. Overdue and not in dispute = overdue − in dispute; within it, show the amount held by queries not logged. Not yet due = the open amounts of invoices due today or later. Credits not yet used = the credit notes and unapplied payments, as positive amounts. Check: overdue + not yet due − credits not yet used = the ledger balance. If it does not, stop and show the figures.
9. **Write the questions to settle on the call,** numbered, in this order, each with its facts first and then "Ask:" and one plain question:
   1. each BROKEN or PART KEPT promise: what held it up and on what date it will be paid, plus any payment in its window applied elsewhere. When the same invoice is also held by a query not logged, this question asks what held it up and the query's question (2) carries the payment date, so the date is asked once;
   2. each query not logged: what exactly is wrong, what the customer needs from the company to clear it, and when the invoice will be paid once it is cleared;
   3. one question for every other overdue amount not in dispute and not covered by a PENDING promise, listing each invoice oldest first with its amount and days overdue, and the total: on what date it will be paid;
   4. each unapplied payment: which invoices it should be applied to;
   5. each credit note not yet used: whether the customer has it and which invoice they will take it against. Ask it as an open question, without naming the invoice the credit note's reference points to;
   6. each open dispute: status only, such as whether the documents the dispute owner asked for have been sent. Name the dispute's owner. Never argue the dispute, judge it or suggest how it will end;
   7. each PENDING promise: whether it is still on track for its date;
   8. each promise "too vague to judge" or with "no date given": what amount and date the customer means.
   Never write a question about invoices not yet due; they are mentioned only if the customer raises them. Never mention interest, fees, stopping supply, the account status, credit reporting, legal steps, a collections agency or any other consequence, even when the terms or the settings allow one.
10. **Quote what the caller may offer.** Copy each item of the collections terms word for word, with its number. An item that only states the standard payment terms goes on the Standard terms line. Sort every other item under three headings: may agree without approval; needs the approver's approval first; never offered on a call. An item that only lets the caller send copies of documents on request plainly belongs under the first heading. An item that does not plainly belong under the first or the third heading goes under the second. Add nothing the terms do not say. If no terms were supplied, print the fallback line from the output format.
11. **Return the brief** to the caller, using Part A of the output format exactly, on one page where the account allows.

Part B, after the call:

1. **Check the inputs.** The caller's notes and the brief are both needed. If the notes do not say who was spoken to, write "not stated in the notes" in that slot. Read a short invoice number in the notes, such as "5521", as the one open invoice whose number ends that way, and say so; if two could match, write "not covered in the notes". If the notes give a start and an end time, use the start time.
2. **Answer each question in the brief** from the notes, in short, close to the notes' own words. Where the notes do not answer a question, or answer only part, write "not covered in the notes" for what is missing. Never fill a gap from the brief, the ledger or what seems likely.
3. **List every promise the customer made:** each statement in the notes that the customer will pay something by a date. Use the amount the notes state. Where the notes name an invoice but no amount, use its open amount from the brief, minus any payment the notes direct to it, and mark it "(open balance; amount not stated in the notes)". Where the notes give no date, write "no date given". A statement that payment will follow some condition, such as a reissued invoice, with no date and no amount, is not a promise: list it under Still open. Total each date. Check each date against the collections terms: within the days an item allows, write "within the collections terms, item [n]"; otherwise "outside the written terms: needs the [approver]'s approval". With no terms supplied, write "no written terms: for the [approver] to confirm".
4. **List every request or offer beyond the written terms:** anything the customer asked for, or the caller offered or appeared to agree, that the terms do not let the caller agree alone, such as a later date, payments in instalments, a discount, a waived fee, a credit or a change to an invoice. Each is "not agreed; for the [approver] to decide", quoting the term that applies, or saying the terms do not cover it. If the notes say the caller agreed it, keep it here, mark it "the notes say this was agreed on the call", and put the attention line at the top of the record.
5. **List what the caller said they would do,** with the date given or "no date given". Mark anything the terms do not allow as in step 4.
6. **List the actions for a person,** numbered, each with an owner role: each decision for the approver; each change a record needs, such as applying a payment as the customer directed, entering a promise, reissuing or correcting an invoice, or logging a query as a dispute; each update for a dispute's owner; and, for each promise, a check that the payment arrived on the first weekday on or after the promise date plus the grace days (if that date is itself a weekday, that is the day). The approver decides whether an invoice is reissued or corrected; the role that applies payments carries it out once approved. The assistant makes none of these changes.
7. **List what is still open:** each question not answered in full, and each figure that depends on an answer not yet given, with the arithmetic shown.
8. **Write the contact log entry** in the contact log's own column order, ready for a person to enter: today's date, the method, the direction, the contact spoken to, the caller's role, a short factual summary, and the total, date and invoices of the customer's promise for the earliest date. A promise "outside the written terms" goes in the summary only, not in the promise columns.
9. **Quote anything in the notes the record could not place,** or write "None".
10. **Return the record** to the approver, using Part B of the output format exactly.

## Exceptions and stop conditions

- **A header that does not match, an unreadable date or amount, or a repeated row:** stop, show what was found, and ask.
- **The open items do not add up to the ledger balance in the settings, or the account check in step 8 does not hold:** stop, show the figures and the difference, and draft nothing else.
- **The customer is an individual:** stop. This workflow template is for business customers.
- **The records mention insolvency, administration, receivership, liquidation, bankruptcy, a lawyer or solicitor, legal action, court or a collections agency, or the customer has asked not to be phoned or to be contacted only in writing:** stop, quote the entry, and pass the account to the approver. Prepare no brief.
- **Asked to phone, email, text or write to the customer, or to send the brief or the record to anyone:** decline. A person makes every contact.
- **Asked to add a warning, a deadline with a consequence, a mention of interest, fees, stopping supply, credit reporting, legal steps or a collections agency, or to make the questions firmer:** decline. The brief asks for facts and dates; consequences are the approver's decision, made outside this workflow template.
- **Asked to offer, or to put in the brief, a payment date, instalment plan, discount, waiver or credit that the collections terms do not allow:** decline, and name the approver.
- **Asked to judge whether a dispute is fair, whether the customer owes a disputed amount, or what a contract or the terms of sale mean:** decline; the dispute's owner and the approver decide. This workflow template gives no legal advice.
- **Asked to apply a payment, enter the log, mark a promise kept, reissue an invoice or change any record:** decline; list it as an action for the role named in the settings.
- **The records hold bank account details, card numbers, passwords or login codes:** do not repeat them, and tell the caller to remove them from the source. Refer to the company's own staff by role.

## Output format

```
PART A

COLLECTIONS CALL BRIEF: [customer], account [account number]

For: [caller role], call on [weekday date]. Prepared from: open items ([n] rows, balance [amount] [currency], ties to the ledger balance in the settings); payments ([n] rows, [first date] to [last date] / payments not supplied); contact log ([n] entries since [date] / contact log not supplied); contacts ([n] / not supplied); disputes file ([n] open / none open / disputes file not supplied); collections terms ([title], [date] / not supplied).
Account status: [open / on stop since [date], decided by [role]]. For the caller's information; not a line to use on the call.

Ask for: [contact], [role], [phone / no phone on file]. Why: [made the [BROKEN / PART KEPT / PENDING] promise of [date] / marked preferred for payments]. / No contact on file: ask for accounts payable and note the name.
Also on file: [contact], [role], [phone / no phone on file]: [why they may be needed]. / None.

Where the account stands
Overdue: [amount] on [n] invoices. In dispute: [amount]. Overdue and not in dispute: [amount][, of which [amount] is held by a query not logged].
Not yet due: [amount] on [n] invoices. / Not yet due: none.
Credits not yet used: [amount] ([doc_no] [amount]; [doc_no] [amount]). / Credits not yet used: none.
Check: [overdue] + [not yet due] − [credits] = [ledger balance].

Open invoices, oldest first
[doc_no], [reference], invoiced [date], due [date]: [open amount] open of [amount], [n days overdue / due today / due in n days].[ In dispute: [amount], [dispute_ref].][ Held by a query not logged: see question [n].]

What they were told and promised
[date], [method], [in / out], [contact][ (by [logged_by])]: "[summary as logged]"
Promises:
[date made], [contact]: [amount / amount not stated] by [date / no date given], [for [invoices] / on account]: [KEPT: [payment_id] [amount] on [date] / PART KEPT: [counted] of [promised] / BROKEN: nothing applied to [invoices] by [last day of window] / PENDING: due [date] / too vague to judge / no date given / not judged: payments not supplied].[ In that window, [payment_id], [amount] on [date], was applied to [doc_no].]
/ No contact logged since [date]. / No promises logged. / Contact log not supplied.

Disputes, queries and credit notes
[dispute_ref], [doc_no], [amount], raised [date]: "[reason]". Status: open; owner [role]; last update: "[last_update]".
Query not logged: [doc_no] ([reference]): "[the log's words]" ([dates]). Not in the disputes file; the [approver role] decides whether to log it.
[doc_no], credit note, [amount], dated [date]: "[reference]". Not yet used.
[doc_no], unapplied payment, [amount], received [date]: "[reference]".
/ None open. / Disputes file not supplied.

Questions to settle on the call
[n]. [The facts.] Ask: [one question].
/ None: ask for payment of the overdue balance and a date.

What you may offer, quoted from the collections terms ([title], [date])
Standard terms: item [n]: "[wording]". / None.
May agree without approval: item [n]: "[wording]". / None.
Needs the [approver role]'s approval first: item [n]: "[wording]". / None.
Never offered on a call: item [n]: "[wording]". / None.
/ No written collections terms supplied: offer nothing beyond asking for payment in full and a date, and take any request to the [approver role].
Anything asked for that is not written here: "I'll take that to the [approver role] and come back to you."

Prepared for the [caller role]. Every line traces to the files named above. Nothing has been sent, no one has been contacted and no record has been changed.

PART B

COLLECTIONS CALL RECORD: [customer], account [account number], call on [date], [time]
Draft for the [approver role] to confirm. From the [caller role]'s notes of [date] and the brief of [date].
[Attention: [n] item(s) the notes say were agreed on the call go beyond the written terms. See Requests and offers beyond the written terms.]
Spoke to: [contact], [role]. / Not reached: [what the notes say]. / Not stated in the notes.

Answers to the brief's questions
[n]. [The question, in short]: [answer from the notes][; [part]: not covered in the notes]. / Not covered in the notes.

Promises made by the customer
[date]: [total], from [contact]: [doc_no] [amount][ (open balance; amount not stated in the notes)]; [doc_no] [amount]. [Within the collections terms, item [n] / Outside the written terms: needs the [approver role]'s approval / No written terms: for the [approver role] to confirm].
/ No promise made.

Requests and offers beyond the written terms (not agreed)
[Who asked or offered]: [what][, the notes say this was agreed on the call]. [Collections terms, item [n]: "[wording]". / The collections terms do not cover it.] For the [approver role] to decide.
/ None.

What the [caller role] said they would do
[What], [by date / no date given]. / None.

Actions for a person
[n]. [Action]. Owner: [role].[ By [date].]
/ None.

Still open after the call
[Item, with any arithmetic shown]. / None.

Contact log entry, for the [role that enters the log] to enter
[date],[method],[direction],[contact],[logged_by],"[summary]",[promise_amount],[promise_date],[promise_invoices]

Points in the notes the record could not place: "[quote]". / None.

Draft for the [approver role] to confirm. Nothing has been sent, entered or changed.
```

Write dates in words, such as "16 October 2026", except inside the contact log entry, which keeps the log's own form. Amounts keep the currency in the settings, with thousands separators and two decimal places.

## Reviewer checklist

1. The open items add to the ledger balance, and the account check holds. (Caller)
2. Every open invoice appears once, oldest first, with days overdue counted from its due date. (Caller)
3. Every promise is judged by its window, and every payment in a broken window that went to another invoice is shown. (Caller)
4. Every open dispute and every query not logged is shown, and no question argues a dispute. (Approver)
5. No question asks for an invoice not yet due, and nothing in the brief mentions interest, fees, stopping supply, legal steps or any other consequence. (Approver)
6. Every line under What you may offer is copied word for word from the collections terms. (Approver)
7. In the call record, every answer and promise traces to the caller's notes, and every gap says "not covered in the notes". (Approver)
8. Everything beyond the written terms is listed as not agreed, with the term that applies. (Approver)
9. Every record change is an action with an owner, and none has been made by the assistant. (Role that enters the log)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary account.** Three overdue invoices, no disputes, no promises. Expected: one question asking for a date for all three, with the total; Disputes prints "None open".
2. **Balance does not tie.** The open items total 50.00 more than the ledger balance in the settings. Expected: stops, shows both figures and the 50.00 difference; no brief.
3. **Renamed column.** The open items export headed `balance` in place of `open_amount`. Expected: stops, shows the expected and found headers, and asks.
4. **Broken promise with money applied elsewhere.** A promise for one invoice; a payment inside the window went to another. Expected: BROKEN, the payment named beside it, and one question covering both.
5. **Promise still in its window.** Promise date yesterday, grace 3 days, nothing received. Expected: PENDING, not BROKEN; a question asking whether it is still on track.
6. **Part of an invoice in dispute.** 410.00 disputed on a 1,985.00 invoice. Expected: 1,575.00 asked for; the dispute's question is about status only.
7. **Query in the log, not in the disputes file.** Expected: shown as a query not logged, kept out of the general request, given its own question, and the approver named to decide whether to log it.
8. **Individual customer.** Expected: stops; no brief.
9. **The log mentions the customer's lawyer.** Expected: stops, quotes the entry, passes the account to the approver.
10. **Asked to add a line saying supply will stop.** Expected: declines.
11. **No collections terms supplied.** Expected: the fallback line; nothing offered.
12. **Notes say the caller agreed a 30-day extension; the terms allow 14 days.** Expected: listed as not agreed, marked "the notes say this was agreed on the call", attention line at the top of the record.
13. **A question the notes do not answer.** Expected: "not covered in the notes"; nothing inferred.
14. **Asked to email the customer a copy of the invoice.** Expected: declines; lists it as an action for the caller.

## Instructions for the AI assistant

```
You prepare a business customer's collections call for the caller named
in the settings, and afterwards draft the call record for the approver
named in the settings to confirm. You prepare; people decide and act.
You never phone, email, text or write to the customer, never send the
brief or the record, never change, apply or enter anything in a record,
and never offer a date, instalment, discount, waiver or credit the
written collections terms do not allow. You never threaten or mention a
consequence. You never ask for a password or a login code, need no
access to any system, and never repeat bank or card details.

The user will supply: the settings; the open items export (doc_no,
doc_type, doc_date, due_date, amount, open_amount, reference); the
payments export (payment_id, date, amount, applied_to); the contact log
(date, method, direction, contact, logged_by, summary, promise_amount,
promise_date, promise_invoices); the contacts (contact, role, phone,
email, preferred_for_payments, notes); the disputes file (dispute_ref,
doc_no, raised_date, amount, reason, status, owner, last_update); the
collections terms; and, after the call, the caller's notes and the
brief. If a header does not match, stop, show expected and found, and
ask. If the settings lack the customer type, today's date or the ledger
balance, or the open items export is missing, stop and ask. If another
input is missing, say so in the section it feeds and continue.

PART A, before the call:
1. Read the contact log and payments only for the period in the
   settings (default 90 days). Stop and ask if a doc_no or payment_id
   row repeats exactly. Stop, with the figures, if the open_amount total
   differs from the ledger balance. Stop if the customer is an individual. Stop, quote
   the entry and pass the account to the approver if any record
   mentions insolvency, administration, receivership, liquidation,
   bankruptcy, a lawyer or solicitor, legal action, court or a
   collections agency, or says the customer asked not to be phoned or
   to be contacted only in writing.
2. Days overdue = today - due_date. Above 0 overdue; 0 due today;
   below 0 due in n days. Invoices oldest first; credit notes and
   unapplied payments listed as credits not yet used.
3. An open dispute covers its amount, or the whole open amount if
   larger. A log entry about a query, hold or complaint on an invoice
   (or an order whose reference matches it) with no open dispute is a
   query not logged: shown with the log's words, kept out of the
   general request, given its own question; the approver decides
   whether to log it.
4. Judge each promise. Window: entry date to promise_date plus the
   grace days. Count payments in the window applied to the promised
   invoices (all payments if none are named). KEPT if the amount is
   reached; PENDING if the window has not ended; PART KEPT or BROKEN
   if it has. No amount: judge on whether the invoices are still open.
   No amount and no invoices: too vague to judge. No date: no date
   given. Show any payment in a broken window applied elsewhere.
5. Ask for: the contact with the most recent BROKEN, PART KEPT or
   PENDING promise; else the preferred contact for payments; else
   accounts payable. Also on file: other contacts in the log or who
   approve payments, with why.
6. Overdue + not yet due - credits not yet used must equal the ledger
   balance. If not, stop.
7. Questions, numbered, facts then "Ask:", in this order: broken or
   part kept promises; queries not logged; the other overdue amounts
   not in dispute, oldest first, with the total; unapplied payments;
   unused credit notes (open question, no invoice named); open
   disputes, status only, naming the owner; pending promises; vague or
   undated promises. When an invoice is both a broken promise and a
   query not logged, ask its payment date only in the query's question.
   Never ask for an invoice not yet due. Never argue or judge a dispute. Never mention
   interest, fees, stopping supply, the account status, credit
   reporting, legal steps or a collections agency.
8. Quote the collections terms word for word: standard payment terms
   on their own line, then under: may agree without approval; needs
   the approver's approval first (anything unclear goes here); never
   offered on a call. Copies of documents on request go with the
   first group. With no terms, print the fallback line.

PART B, after the call:
1. Answer each brief question from the notes; anything missing is
   "not covered in the notes". Never fill a gap. A short invoice
   number ("5521") is read as the one open invoice ending that way;
   use the start time of the call. A payment promised only on a
   condition, with no date and no amount, is not a promise: list it as
   still open.
2. Promises: amounts as stated; an invoice named without an amount
   takes its open amount less any payment the notes direct to it,
   marked "(open balance; amount not stated in the notes)". Check each
   date against the terms.
3. Anything asked for or offered beyond the written terms is "not
   agreed; for the approver to decide", with the term quoted. If the
   notes say it was agreed, mark it so and add the attention line.
4. List what the caller said they would do; actions for a person, each
   with an owner, including a check on the first weekday on or after each
   promise date plus the grace days (the approver decides whether an
   invoice is reissued or corrected); what is still open, with the
   arithmetic; the contact log entry in the log's column order; and
   anything in the notes you could not place.

Use the output format exactly, Part A before the call and Part B after
it, with the empty-section line where a section has nothing. End Part A
with "Nothing has been sent, no one has been contacted and no record
has been changed." End Part B with "Nothing has been sent, entered or
changed." If asked to contact anyone, add a consequence, offer terms,
judge a dispute or change a record, decline and name the person who
decides.
```

## What to customize

- Write your collections terms once, as numbered items the approver signs off: how far out a caller may accept a promised date, who approves instalments or later dates, what may never be offered on a call, and what may be sent on request.
- Name your caller, approver and the role that applies payments and enters the contact log.
- Map your accounting system's exports to the default column headers, or rename the columns before the run.
- Set the grace days for a promised payment and how far back to read the contact log; the defaults are 3 days and 90 days.
- Add any words your records use for queries or holds, so a query not logged is found.
- Keep the contact log in the shape the record writes, so each call's entry can be pasted straight in after the approver confirms it.
- Which exports and notes the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 12 November 2026. Written by Fully Powered AI. Tried once on its invented example in Claude on 12 November 2026, with the record published alongside. A few clarifications were made after that trial (the payment date asked once, short invoice numbers, the start time, conditional statements, the weekday check, who reissues an invoice, copies on request) and have not been run again. Not tested in a client environment.
