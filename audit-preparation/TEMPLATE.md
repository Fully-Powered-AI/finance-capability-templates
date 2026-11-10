# Audit preparation

Capability template, version 0.1.0.

## Purpose

Prepare one audit preparation pack for a controller or bookkeeper before the external auditors arrive: every item on the auditors' request list turned into a tracker line with its owner, the auditors' date, an earlier date of our own, the document that answers it, its status and who approved it; the controls the auditors will test, with the evidence each one leaves; a check of who approves, records, handles the money and checks in each process; a check of the payments that needed approval; last year's findings and what was done about each; the balances that moved enough to draw a question; and draft answers to the questions the auditors are expected to ask. Every gap becomes a numbered decision or question for a named role. The assistant prepares and checks. People supply every document, approve every item and every answer before it goes to the auditors, and send it themselves. The assistant sends nothing, assigns nothing, approves nothing and changes no record.

## When to use it and when not to

Use it when the auditors' request list arrives, usually three to six weeks before fieldwork. Run it again each week with updated statuses until fieldwork starts, and whenever the auditors add requests or questions.

Do not use it:

- to run the month-end close or to reconcile a bank account. Those are their own capabilities, and their finished work becomes documents on this tracker;
- to decide how something should be accounted for, or to agree or dispute an adjustment the auditors propose. Those are the controller's decisions, with the auditors;
- to answer questions about legal claims or disputes, tax positions, suspected fraud, or whether the business can keep operating. The pack lists those questions for the role named in the settings to answer with the company's advisers. It gives no legal or tax advice;
- to write the management representation letter. The auditors supply it and management signs it; the pack tracks it as an item like any other;
- to read the contents of payroll records, personnel files, contracts or legal correspondence. The tracker names those documents; it does not open them.

## Roles

- **Runs it:** the controller, the bookkeeper or the finance manager.
- **Approves the pack and settles every decision:** the controller, or whoever leads the audit for the company.
- **Prepares each item:** the owner named on the owner and status list.
- **Approves each item before it goes to the auditors:** the role named in the settings, never the item's own owner. The settings name a second approver, such as the chief executive or finance director, only for the items that role owns; every other item, whoever owns it, goes to the role named first.
- **Approves each draft answer:** the role named in the settings for that kind of question.
- **Sends items and answers to the auditors:** a person, after approval. Always a person.
- **Answers questions on legal claims, tax positions, suspected fraud and the business's ability to keep operating:** the role named in the settings, with the company's advisers.

## Inputs

The assistant works from files and notes the person supplies. It needs no connection to the accounting system, the bank or the auditors' portal and never asks for a password or a login code. Dates are written YYYY-MM-DD.

1. **The auditors' request list.** Default column headers: `Ref`, `Request`, `Area`, `Due`, `Format`. `Ref`, `Request` and `Due` are required; if `Area` or `Format` is absent, write "not stated" and group the items under "Area not stated". If the list is missing, stop.
2. **The owner and status list,** the company's own working list. Default column headers: `Ref`, `Owner`, `Status`, `Document`, `Approved by`, `Note`. Statuses: not started, in progress, ready for review, approved to send, sent. If the list is missing, build the tracker with every owner "not assigned" and every status "not started", and make one decision asking for the list instead of flagging every line.
3. **Last year's request list** (optional). Default column headers: `Ref`, `Request`, `Area`.
4. **The controls list** (optional): the controls the company expects the auditors to test. Default column headers: `ID`, `Control`, `Process`, `Owner`, `Frequency`, `Evidence`, `Kept at`.
5. **The who-does-what list** (optional): for each process, who approves, who records, who handles the money and who checks the result. Default column headers: `Process`, `Approves`, `Records`, `Handles the money`, `Checks`, `Compensating control`. "n/a" means the duty does not arise.
6. **The approvals export** (optional): payments from the accounting system or the bank for a period the controller chooses. Default column headers: `Date`, `Supplier`, `Amount`, `Entered by`, `Approved by`.
7. **Last year's findings** (optional), from the auditors' letter to management. Default column headers: `ID`, `Finding`, `Area`, `What was done`, `Evidence`, `Owner`, `Status`.
8. **The trial balance comparison** (optional). Default column headers: `Account`, `This year`, `Last year`, with debits positive and credits negative. With it, the controller's **movement notes**, default column headers `Account`, `Explanation`.
9. **Expected questions** (optional): last year's questions, the auditors' planning questions or the controller's own list. Default column headers: `ID`, `Question`, `Facts`, `Source`, where `Facts` is what the company knows and `Source` is the document or person it comes from.
10. **Settings:** the company, the year end, today's date, the date fieldwork starts, the role that runs the pack, the role that approves items and the second approver for items that role owns, who approves answers of each kind, the working days and closed days, and three limits. If a limit is missing, use its default and list it under "Defaults used":
    - **lead time:** how many working days before the auditors' date our own date falls. Default 3 working days;
    - **approval limit:** the payment amount at or above which an approval by someone other than the person who entered the payment is required. No default: if it is missing, write "approval limit not supplied" and check no payments;
    - **movement threshold:** an amount and a percentage; a balance is listed when its movement reaches both. No default: if it is missing, write "threshold not supplied" and list no movements. Take it from the controller, who may take it from the auditors' planning.
    If the working days are missing, use Monday to Friday and list that too.
11. **A column map** (optional), when an export uses other headings: which of its columns holds each default column.

**When a header does not match.** If a required column is not found under its default heading and no column map covers it, stop and ask which column holds it. Never infer a column from its contents.

## The procedure

1. **Check the inputs.** Confirm the headings, or apply the column map. Count the rows of each input. If two items on the auditors' list share a `Ref`, stop and ask which is which.
2. **Build the tracker.** One line per item on the auditors' list, joined to the owner and status list by `Ref`. Keep the request wording, the owner, the document, the note and the format as supplied. An item with no row on the owner and status list is shown with owner "not assigned" and status "not started", and is counted as not started in the summary. Our date is the auditors' date counted back by the lead time in working days, skipping non-working weekdays and closed days. Group the lines by area in the order each area first appears on the auditors' list, and within an area keep the list's order. A row on the owner and status list whose `Ref` is not on the auditors' list goes under "Not on the auditors' list".
3. **Flag the tracker.** Put each flag on its line; a line with several problems carries them in one flag, kinds separated by commas, and counts once.
   - **No owner:** the owner is blank, or the item is missing from the owner and status list (shown as "not started").
   - **Late:** our date is before today and the status is not started or in progress.
   - **Not approved:** the status is approved to send or sent and nobody is named under `Approved by`.
   - **Approved by its owner:** the approver is the item's owner.
   - **Document not named:** the status is ready for review or later and no document is named.
   - **Status not recognised:** a status outside the five.
   - **Not on the auditors' list.**
4. **Compare with last year's list.** Pair each item with last year's item that asks for the same document in the same area, ignoring references, dates and years. List items new this year, items whose wording changed beyond a date or a year (both wordings), and last year's items no longer requested. Where a pairing is uncertain, list it under Changed so the controller can confirm it.
5. **Check the control evidence.** One line per control, as supplied. Flag **no evidence named** where `Evidence` is blank or "none", and **not kept anywhere** where `Kept at` is blank.
6. **Check who does what.** For each process, find any person named under two or more of Approves, Records, Handles the money and Checks; "n/a" is ignored. Where there is an overlap and a compensating control is written, list it as a documented overlap for the controller to confirm. Where there is an overlap and no compensating control, flag **overlap with no compensating control**.
7. **Check the approvals.** Count the payments at or above the approval limit, with their total, and the payments below it, which are not checked. For each payment at or above the limit, flag **no approval recorded** where `Approved by` is blank, and **approved by the person who entered it** where the two are the same. Count the payments checked without a flag.
8. **Review last year's findings.** One line per finding, as supplied, with the request items whose area has exactly the same name named as related; a similar name, such as Payments against Payables, does not count. Flag **no action recorded** where `What was done` is blank, and **no evidence named** where an action is recorded and `Evidence` is blank.
9. **List the movements.** For each account, the movement is this year less last year, and the percentage is the movement divided by last year's balance, to one decimal place. Both are tested by size, ignoring signs, so a fall or a larger credit balance counts the same as a rise. Where last year is zero, write "new balance" and test the amount only. List each account whose movement reaches both parts of the threshold, in the order of the comparison. Where the controller has a note, give it as the draft explanation; where the note states figures, compare them with the movement and show what is left over, naming the request item that holds the support; a leftover amount is shown for the controller to read, not flagged. Where there is no note, flag **no explanation**.
10. **Draft the answers.** For each expected question, write a draft answer using only its facts, and name its source. Add nothing the facts do not say. A question about legal claims or disputes, tax positions, suspected fraud or the business's ability to keep operating is not drafted: flag **not drafted, for the role named in the settings** and say it is for that role to answer with the company's advisers. A question with no facts is not drafted: flag **no facts supplied**. Name the role who approves each answer; every answer is "not yet approved".
11. **Write the decisions and questions.** One numbered item per flagged line, in the order of the sections, each addressed to a role: the reference, the kind of flag, the facts, and the question. Expected-question items go to the role who answers them; the rest go to the controller. For a question left undrafted, the item may restate the facts as supplied, adding no view on them. Recommend nothing unless the controller asks, and ask plain questions that do not suggest an answer. The number of items equals the flagged lines counted in the summary.
12. **Write the summary.** Items on the auditors' list, the count at each status, the count late, the flagged lines and the decisions and questions.
13. **Return the draft** to the person who ran it, for the controller's approval. The controller settles the decisions; owners finish their items; the named approver approves each item and answer; a person sends them to the auditors.

## Exceptions and stop conditions

- **No auditors' request list:** stop and ask for it. Do not supply a standard list of audit requests.
- **A required heading does not match and no column map covers it:** stop and ask which column holds it.
- **Two items share a reference:** stop and ask.
- **An optional input is missing:** its section reads "Not prepared: [input] not supplied." and the run continues.
- **Asked to send an item or an answer to the auditors, upload to their portal, mark an item approved or sent, assign an owner, or post or change an entry:** decline and name the role that does it.
- **Asked to decide an accounting treatment, agree or dispute a proposed adjustment, set the movement threshold, or write the representation letter:** decline; record the question as a decision for the controller.
- **Asked to answer a question about legal claims, tax positions, suspected fraud or the business's ability to keep operating:** decline to draft it, give no view on it, and list it for the named role and the company's advisers.
- **An input contains bank account numbers, salaries, personal details of employees, a password or a login code:** do not repeat them in the pack; refer to the item by its reference; tell the person to remove them from the file.
- **An approvals row or a note suggests a payment nobody can explain:** list the facts as supplied and put the question first among the decisions, addressed to the controller. Do not speculate about who made it or why. A payment nobody can explain is one whose supplier is blank in the approvals export, or whose supplier or purpose a note, or the person running the pack, says nobody recognises. A missing approval, or an approval by the person who entered the payment, is not that on its own: it is flagged in the approvals check and keeps its place in section order.

## Output format

```
AUDIT PREPARATION PACK: [company], year ended [date]

For: [controller role]. Prepared: [weekday date]. Fieldwork starts: [weekday date].
Sources: auditors' request list, [n] items; owner and status list, [n] rows / not supplied; last year's request list, [n] items / not supplied; controls list, [n] controls / not supplied; who-does-what list, [n] processes / not supplied; approvals export, [n] payments, [period] / not supplied; last year's findings, [n] / not supplied; trial balance comparison, [n] accounts, with [n] movement notes / not supplied; expected questions, [n] / not supplied.
Settings used: lead time [n] working days; approval limit [amount] / approval limit not supplied; movement threshold [amount] and [percent] / threshold not supplied; working days [days]; closed days [dates / none]. Items approved by [role]; items [role] owns approved by [role]. Defaults used: [list / none].

SUMMARY
Items on the auditors' list: [n]. Not started [n]. In progress [n]. Ready for review [n]. Approved to send [n]. Sent [n]. Late [n].
Flagged lines: [n]. Decisions and questions: [n].

REQUEST TRACKER
[Area]
[Ref] [request]. Owner: [role / not assigned]. Auditors' date: [weekday date]. Our date: [weekday date]. Format: [as supplied / not stated]. Document: [as supplied / not named]. Status: [status]. Approved by: [role / not yet]. [Note: as supplied.] [FLAG, kind[, kind]: the facts. See [n].]

Not on the auditors' list
[Ref]. Owner: [role / not assigned]. Document: [as supplied / not named]. Status: [status]. Note: [as supplied / none]. FLAG, not on the auditors' list. See [n].

CHANGES FROM LAST YEAR'S LIST
New this year: [Ref, request / none].
Changed: [Ref]: last year "[wording]"; this year "[wording]". / none
No longer requested: [last year's Ref, request / none].

CONTROL EVIDENCE
[ID] [control]. Process: [process]. Owner: [role]. Frequency: [as supplied]. Evidence: [as supplied / not named]. Kept at: [as supplied / not stated]. [FLAG, kind: the facts. See [n].]

WHO DOES WHAT
[Process]: approves [role]; records [role]; handles the money [role]; checks [role]. [No overlap. / Overlap: [role] [duties]. Compensating control: [as written], controller to confirm. / FLAG, overlap with no compensating control: [role] [duties]. See [n].]

APPROVALS CHECK
Approval limit [amount]. [n] payments at or above the limit checked, [total]. [n] below the limit, not checked.
[Date] [supplier] [amount]: entered by [role]; approved by [role / none]. FLAG, [kind]. See [n].
Checked without a flag: [n].

LAST YEAR'S FINDINGS
[ID] [finding]. Owner: [role]. What was done: [as supplied / nothing recorded]. Evidence: [as supplied / none named]. Status: [as supplied]. Related requests: [Refs / none]. [FLAG, kind: the facts. See [n].]

MOVEMENTS THE AUDITORS WILL ASK ABOUT
Threshold: [amount] and [percent], both. [n] accounts compared; [n] reach both.
[Account]: last year [amount], this year [amount], movement [amount] ([percent] / new balance). Draft explanation: [the controller's note / none]. [Check: [the note's figures against the movement, what is left over, and the request item that holds the support].] [FLAG, no explanation. See [n].]

DRAFT ANSWERS TO EXPECTED QUESTIONS
[ID] [question]
Draft answer: [answer from the facts supplied / not drafted].
Based on: [source / nothing supplied]. To be approved by: [role]. Not yet approved.
[FLAG, kind. See [n].]

DECISIONS AND QUESTIONS
[n]. For [role]. [Reference], [kind of flag]. [The facts.] [The question.]

Prepared for the [controller role]'s approval. Nothing has been sent to the auditors, assigned, approved, posted or changed.
```

Every section appears on every pack, in this order. Where a section has nothing in it, write "None." under its heading. Where its input was not supplied, write "Not prepared: [input] not supplied." Write each [weekday date] in full, such as Monday 9 November 2026; the dates in the inputs stay YYYY-MM-DD.

## Reviewer checklist

1. Every item on the auditors' list appears once in the tracker, with its reference, wording and auditors' date unchanged. (Controller)
2. Every "our date" is the auditors' date counted back by the lead time in working days, skipping closed days. (Controller)
3. Every flag is true, every flagged line has one numbered item, and the summary counts match the tracker. (Controller)
4. No item is shown as approved or sent unless the owner and status list says so, and no item is approved by its own owner without a flag. (Controller)
5. For every documented overlap in who does what, the controller has confirmed that the compensating control, as written in the who-does-what list, is actually carried out, and has named where its record is kept, from the controls list's `Evidence` and `Kept at` where the control appears there. (Controller)
6. The approvals check counts and totals are right, and every flagged payment has been looked up in the accounting system. (Staff accountant or bookkeeper)
7. Every movement is arithmetically right, every account that reaches both parts of the threshold is listed, and none below it is. (Controller)
8. Every draft answer says only what its facts say, and every question on legal, tax, fraud or the business's ability to keep operating has gone to the named role undrafted. (Controller and the role named)
9. No bank account number, salary, personal detail, password or login code appears in the pack. (Controller)
10. The pack is approved before items or answers go to the auditors, and each item and answer is approved by its named approver. (Controller)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary list.** Ten requests, all owned, none late, all inputs supplied with no gaps. Expected: every our date correct, no flags, every section present with "None." where empty.
2. **Our date across a weekend and a closed day.** An auditors' date of a Tuesday, a lead time of 3 working days and the Friday before closed. Expected: our date is the Wednesday of the week before.
3. **Item with no owner.** Expected: "not assigned", flagged, one decision; no owner suggested.
4. **Late item.** Our date yesterday, status in progress. Expected: flagged late, counted in the summary.
5. **Sent without approval.** Status sent, `Approved by` blank. Expected: flagged not approved; the status is left as supplied.
6. **Item on the company's list only.** Expected: under "Not on the auditors' list", flagged, with a question asking whether the auditors asked for it.
7. **Wording changed from last year.** Last year "Payables aging"; this year "Payables aging and a search for unrecorded liabilities". Expected: under Changed with both wordings; a change of year alone is not listed.
8. **Control with no evidence.** Expected: flagged no evidence named, with a decision.
9. **Overlap with and without a compensating control.** The controller approves, releases and checks payments with nothing written; the controller also posts and reviews journals with a monthly review by the chief executive written. Expected: the first flagged; the second listed as a documented overlap for the controller to confirm.
10. **Payments.** One at the limit entered and approved by the same person; one above it with no approver; one below it. Expected: two flags; the one below counted but not checked.
11. **Movement that reaches the amount but not the percentage.** Expected: not listed.
12. **Note with figures that do not match the movement.** Expected: the difference shown and the supporting request named; no figure changed.
13. **Legal question.** "Are there any claims against the company?" with facts supplied. Expected: not drafted, no view given, listed for the named role and the company's advisers.
14. **Unknown heading.** The request list's date column is headed `Deadline` with no column map. Expected: stops and asks which column holds the auditors' dates.
15. **Asked to send.** "Upload A3 to the auditors' portal." Expected: declines and names the role that sends it.
16. **Salaries in a note.** A note gives a named employee's salary. Expected: the salary and the name are not repeated; the person is told to remove them.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare an audit preparation pack for a controller before the
external auditors arrive. You prepare and check; people decide. You
never send anything to the auditors, upload to their portal, mark an
item approved or sent, assign an owner, post or change an entry, or
change any record. A person approves every item and every answer
before a person sends it. Never ask for a password, a login code or
access to any system; work only from what the user supplies.

The user will supply, with these default column headers:
- the auditors' request list: Ref, Request, Area, Due, Format
  (Ref, Request and Due required);
- the owner and status list: Ref, Owner, Status, Document, Approved by,
  Note. Statuses: not started, in progress, ready for review, approved
  to send, sent;
- optionally: last year's request list (Ref, Request, Area); the
  controls list (ID, Control, Process, Owner, Frequency, Evidence, Kept
  at); the who-does-what list (Process, Approves, Records, Handles the
  money, Checks, Compensating control); the approvals export (Date,
  Supplier, Amount, Entered by, Approved by); last year's findings (ID,
  Finding, Area, What was done, Evidence, Owner, Status); the trial
  balance comparison (Account, This year, Last year; debits positive,
  credits negative) with movement notes (Account, Explanation);
  expected questions (ID, Question, Facts, Source);
- a column map, if their headings differ;
- settings: company, year end, today's date, fieldwork start, who runs
  the pack, who approves items and who approves the items that person
  owns (every other item goes to the first approver), who approves
  answers of each kind, working days, closed days, lead time (default
  3 working days unless the settings say otherwise), approval limit and
  movement threshold (amount and percentage). Working days default to
  Monday to Friday. List every default used.

Stop and say why, drafting nothing else, if: the request list is
missing; a required heading is not found and no column map covers it
(ask which column holds it; never infer it from the contents); two
request items share a Ref. If the owner and status list is missing,
show every owner "not assigned" and status "not started" and make one
decision asking for it. If another input is missing, its section reads
"Not prepared: [input] not supplied." If the approval limit or the
movement threshold is missing, say so in its section and check nothing
there.

1. Tracker: one line per request, joined by Ref. Keep wording, owner,
   document, note and format as supplied. Our date = the auditors' date
   counted back by the lead time in working days, skipping non-working
   days and closed days. Group by area in order of first appearance.
   A request with no row on the owner list: owner "not assigned",
   status "not started". Rows on the owner list with no matching
   request go under "Not on the auditors' list".
2. Flag tracker lines: no owner (blank, or no row on the owner list);
   late (our date before today, status not started or in progress); not
   approved (approved to send or sent, no approver); approved by its
   owner; document not named (ready for review or later, no document);
   status not recognised; not on the auditors' list. Several problems
   share one flag and count once.
3. Compare with last year's list by the document asked for and the
   area, ignoring refs, dates and years: new, changed (both wordings),
   no longer requested. Put uncertain pairings under changed.
4. Controls: flag "no evidence named" (blank or none) and "not kept
   anywhere" (Kept at blank).
5. Who does what: a person named in two or more of Approves, Records,
   Handles the money, Checks (ignore n/a) is an overlap. With a
   compensating control written, list it for the controller to
   confirm. Without one, flag "overlap with no compensating control".
6. Approvals: count and total payments at or above the limit; count
   those below, not checked. Flag "no approval recorded" (approver
   blank) and "approved by the person who entered it".
7. Last year's findings: name as related the request items whose area
   matches the finding's area exactly; a similar name does not count.
   Flag "no action recorded" (What was done blank) and "no evidence
   named" (action recorded, Evidence blank).
8. Movements: movement = this year - last year; percentage = movement
   / last year, one decimal. Test both the amount and the percentage
   by size, ignoring signs (last year zero: "new balance", test the
   amount only). List accounts reaching both parts of the threshold.
   Give the controller's note as the draft explanation; if it states
   figures, compare them with the movement, show what is left over (not
   a flag) and name the request item holding the support. No note: flag
   "no explanation".
9. Draft answers only from each question's facts, naming the source;
   add nothing. Do not draft, and give no view on, a question about
   legal claims or disputes, tax positions, suspected fraud or the
   business's ability to keep operating: flag "not drafted, for [the
   role in the settings]" with the company's advisers. No facts: flag
   "no facts supplied". Every answer is "Not yet approved".
10. Decisions and questions: one numbered item per flagged line, in
    section order, each for a role (expected questions to the role who
    answers; the rest to the controller): reference, kind, facts,
    question. For an undrafted question the item may restate its facts
    as supplied, with no view on them. Recommend nothing unless asked;
    ask plain questions that do not suggest an answer. A payment nobody
    can explain goes first; state the facts and do not speculate. That
    is a payment whose supplier is blank, or whose supplier or purpose
    a note or the user says nobody recognises; a missing approval or a
    self-approval alone is not one and keeps its place in section order.
11. Summary: items on the list, counts by status, late, flagged lines,
    decisions and questions. The counts must match the sections.

Use the output format exactly. Every section appears, in order; write
"None." under an empty section. Write each [weekday date] in full, such
as Monday 9 November 2026. Do not repeat bank account numbers,
salaries, employees' personal details, passwords or login codes; refer
to the item by its reference and tell the user to remove them. Do not
open or summarise payroll records, personnel files, contracts or legal
correspondence; the tracker names them only. End with: "Prepared for
the [controller role]'s approval. Nothing has been sent to the
auditors, assigned, approved, posted or changed."

If asked to send, upload, approve, mark sent, assign, post or change a
record, decline and name the role that does it. If asked to decide an
accounting treatment, agree or dispute an adjustment, set the
threshold or write the representation letter, decline and record it as
a decision for the controller.
```

## What to customize

- The column headings your auditors' list and your own exports use, as a column map.
- Your lead time: how many working days ahead of the auditors' date your own date falls.
- Your approval limit, and whether a second approval is needed above a higher amount.
- Your movement threshold, as an amount and a percentage, agreed with your auditors.
- Who approves items, who approves items the controller owns, and who approves answers of each kind.
- Which questions always go to the chief executive or the owner and your advisers, beyond legal claims, tax positions, suspected fraud and the business's ability to keep operating. Events after the year end is a common addition; in the example the chief executive approves those answers.
- Your statuses, if your team uses others, and what counts as ready for review.
- Whether auditors renumber their requests each year; if so, keep last year's list beside this year's so the comparison pairs by wording.
- Where approved items are kept before they go to the auditors, and who keeps the record of what was sent and when.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried on its invented example on 10 November 2026 in one run, the run recorded. Small edits made to the pasted instructions, the method and the example after the recorded run have not been run again; the trial record lists them. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
