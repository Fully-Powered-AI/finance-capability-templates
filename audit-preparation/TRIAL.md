# Audit preparation: trial on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-10

This was one run of the workflow template on its own invented example. The inputs are the invented ones; no client data was used. The run was made by an assistant that did not write the template. It read the template and the example's ten inputs, produced the pack, and only then compared it with the example's output and the reviewer checklist.

## Inputs used

The ten inputs in [the example](example.md), under "The inputs": settings, the auditors' request list, the owner and status list, last year's request list, the controls list, the who-does-what list, the approvals export, last year's findings, the trial balance comparison with its two movement notes, and the three expected questions. The instructions used were the fenced block in the template, with its output format.

## What came out

```
AUDIT PREPARATION PACK: the Company, year ended 2026-09-30

For: Controller. Prepared: Monday 2026-11-09. Fieldwork starts: Monday 2026-11-23.
Sources: auditors' request list, 10 items; owner and status list, 10 rows; last year's request list, 10 items; controls list, 5 controls; who-does-what list, 4 processes; approvals export, 8 payments, 2026-07-01 to 2026-09-30; last year's findings, 3; trial balance comparison, 9 accounts, with 2 movement notes; expected questions, 3.
Settings used: lead time 3 working days; approval limit $5,000.00; movement threshold $25,000 and 10%; working days Monday to Friday; closed days Thursday 2026-11-26, Friday 2026-11-27. Items approved by Controller; items Controller owns approved by Chief executive. Defaults used: none.

SUMMARY
Items on the auditors' list: 10. Not started 3. In progress 5. Ready for review 1. Approved to send 0. Sent 1. Late 1.
Flagged lines: 14. Decisions and questions: 14.

REQUEST TRACKER
General
A1 Trial balance at 30 September 2026. Owner: Controller. Auditors' date: Tuesday 2026-11-10. Our date: Thursday 2026-11-05. Format: Excel. Document: TB_FY2026.xlsx. Status: in progress. Approved by: not yet. Note: Two late supplier bills still to post. FLAG, late: our date has passed and the status is in progress. See 1.

Cash
A2 Bank reconciliations for all accounts at 30 September 2026 with bank statements. Owner: Staff accountant. Auditors' date: Friday 2026-11-13. Our date: Tuesday 2026-11-10. Format: PDF. Document: not named. Status: in progress. Approved by: not yet. Note: September statement for the savings account not yet downloaded.

Revenue and receivables
A3 Receivables aging at 30 September 2026 tied to the general ledger. Owner: Staff accountant. Auditors' date: Monday 2026-11-16. Our date: Wednesday 2026-11-11. Format: Excel. Document: AR aging 30 Sep 2026 tied to GL.xlsx. Status: ready for review. Approved by: not yet.

Inventory
A4 Inventory count sheets and final valuation at 30 September 2026. Owner: Warehouse manager. Auditors' date: Monday 2026-11-16. Our date: Wednesday 2026-11-11. Format: Excel. Document: Count sheets 30 Sep 2026 (scanned). Status: in progress. Approved by: not yet. Note: Valuation not finished.

Fixed assets
A5 Fixed asset register with additions and disposals for the year. Owner: not assigned. Auditors' date: Wednesday 2026-11-18. Our date: Friday 2026-11-13. Format: Excel. Document: not named. Status: not started. Approved by: not yet. FLAG, no owner: the item has no owner on the owner and status list. See 2.

Payables
A6 Payables aging at 30 September 2026 and a search for unrecorded liabilities (payments 1 October to 6 November 2026). Owner: Payables clerk. Auditors' date: Wednesday 2026-11-18. Our date: Friday 2026-11-13. Format: Excel. Document: not named. Status: not started. Approved by: not yet.

Payroll
A7 Payroll register for the year and payroll tax filings. Owner: Payroll administrator. Auditors' date: Wednesday 2026-11-18. Our date: Friday 2026-11-13. Format: PDF. Document: not named. Status: in progress. Approved by: not yet. Note: Payroll provider sends the year summary on 12 November.

Debt
A8 Loan documents and covenant calculation at 30 September 2026. Owner: Controller. Auditors' date: Friday 2026-11-20. Our date: Tuesday 2026-11-17. Format: PDF. Document: Covenant calculation 30 Sep 2026.xlsx. Status: in progress. Approved by: not yet.

Governance
A9 Board minutes for the year. Owner: Chief executive. Auditors' date: Friday 2026-11-20. Our date: Tuesday 2026-11-17. Format: PDF. Document: Board minutes FY2026.pdf. Status: sent. Approved by: not yet. FLAG, not approved: the status is sent and nobody is named under Approved by. See 3.
A10 List of related parties and transactions with them during the year. Owner: not assigned. Auditors' date: Friday 2026-11-20. Our date: Tuesday 2026-11-17. Format: Excel. Document: not named. Status: not started (no row on the owner and status list). Approved by: not yet. FLAG, no owner: the item is missing from the owner and status list. See 4.

Not on the auditors' list
A11. Owner: Controller. Document: not named. Status: in progress. Note: Lease schedule for the new warehouse. FLAG, not on the auditors' list. See 5.

CHANGES FROM LAST YEAR'S LIST
New this year: A10, List of related parties and transactions with them during the year.
Changed: A6: last year "Payables aging at 30 September 2025"; this year "Payables aging at 30 September 2026 and a search for unrecorded liabilities (payments 1 October to 6 November 2026)".
No longer requested: last year's A10, Lender's confirmation of the loan balance at 30 September 2025.

CONTROL EVIDENCE
C1 Supplier payments of $5,000 or more approved before release. Process: Supplier payments. Owner: Controller. Frequency: Each payment. Evidence: Approval record in the banking system. Kept at: Monthly approval report in the finance drive.
C2 Bank reconciliations reviewed and signed. Process: Cash. Owner: Controller. Frequency: Monthly. Evidence: Signed reconciliation. Kept at: Finance drive.
C3 Changes to a supplier's bank details confirmed by a call to a number already on file. Process: Supplier payments. Owner: Payables clerk. Frequency: Each change. Evidence: not named. Kept at: not stated. FLAG, no evidence named, not kept anywhere: both columns are blank. See 6.
C4 Payroll changes approved before the pay run. Process: Payroll. Owner: Chief executive. Frequency: Each pay run. Evidence: Signed change form. Kept at: Payroll folder.
C5 Manual journal entries reviewed. Process: Manual journal entries. Owner: Chief executive. Frequency: Monthly. Evidence: Initialled journal list. Kept at: Finance drive.

WHO DOES WHAT
Supplier payments: approves Controller; records Payables clerk; handles the money Controller; checks Controller. FLAG, overlap with no compensating control: Controller approves, handles the money and checks. See 7.
Payroll: approves Chief executive; records Payroll administrator; handles the money Payroll provider; checks Controller. No overlap.
Manual journal entries: approves Controller; records Controller; handles the money n/a; checks Controller. Overlap: Controller approves, records and checks. Compensating control: Chief executive reviews and initials the monthly journal list, controller to confirm.
Cash receipts: approves n/a; records Staff accountant; handles the money Staff accountant; checks Staff accountant. Overlap: Staff accountant records, handles the money and checks. Compensating control: Controller reviews and signs the bank reconciliation each month, controller to confirm.

APPROVALS CHECK
Approval limit $5,000.00. 7 payments at or above the limit checked, $77,780.00. 1 below the limit, not checked.
2026-08-05 Supplier C $8,900.00: entered by Payables clerk; approved by none. FLAG, no approval recorded. See 8.
2026-09-02 Supplier D $5,000.00: entered by Controller; approved by Controller. FLAG, approved by the person who entered it. See 9.
Checked without a flag: 5.

LAST YEAR'S FINDINGS
F1 Count differences over $500 were not investigated before the inventory valuation was finished. Owner: Warehouse manager. What was done: Count procedure changed: every difference over $500 is recounted and signed off by the warehouse manager before valuation. Evidence: Signed recount sheets from the September 2026 count. Status: done. Related requests: A4.
F2 Two changes to supplier bank details were made without confirmation. Owner: Payables clerk. What was done: Payables clerk told to call suppliers before changing bank details. Evidence: none named. Status: done. Related requests: none (no request is in the area Payments). FLAG, no evidence named: an action is recorded and Evidence is blank. See 10.
F3 Fixed asset register not reconciled to the general ledger during the year. Owner: Controller. What was done: nothing recorded. Evidence: none named. Status: open. Related requests: A5. FLAG, no action recorded: What was done is blank. See 11.

MOVEMENTS THE AUDITORS WILL ASK ABOUT
Threshold: $25,000 and 10%, both. 9 accounts compared; 3 reach both.
Receivables: last year $812,400, this year $1,046,500, movement $234,100 (28.8%). Draft explanation: none. FLAG, no explanation. See 12.
Fixed assets (net): last year $1,675,300, this year $2,210,800, movement $535,500 (32.0%). Draft explanation: Additions of $612,000 for the new warehouse fit-out and two press brakes, less depreciation. Check: the additions of $612,000 are $76,500 more than the movement of $535,500; the note gives no figure for the depreciation or any disposals, so $76,500 is left over for them. Support: A5.
Loan: last year -$1,100,000, this year -$1,500,000, movement -$400,000 (36.4%). Draft explanation: Drew a further $400,000 on the term loan in March 2026 to fund the warehouse. Check: the $400,000 drawn equals the movement; nothing is left over. Support: A8.

DRAFT ANSWERS TO EXPECTED QUESTIONS
Q1 Did revenue recognition or customer pricing terms change during the year?
Draft answer: No change. We invoice on shipment and standard terms are 30 days.
Based on: Controller; standard terms of sale. To be approved by: Controller. Not yet approved.
Q2 Are there any legal claims or disputes outstanding?
Draft answer: not drafted.
Based on: facts supplied by the Chief executive, not used here. To be approved by: Chief executive. Not yet approved.
FLAG, not drafted, for the Chief executive. See 13.
Q3 Has anything happened since the year end that could affect the accounts?
Draft answer: not drafted.
Based on: nothing supplied. To be approved by: Chief executive. Not yet approved.
FLAG, no facts supplied. See 14.

DECISIONS AND QUESTIONS
1. For Controller. A1, late. Our date was Thursday 2026-11-05 and the auditors' date is Tuesday 2026-11-10; the status is in progress, with the note "Two late supplier bills still to post". When will A1 be ready for review?
2. For Controller. A5, no owner. The fixed asset register (auditors' date Wednesday 2026-11-18, our date Friday 2026-11-13) has no owner and is not started. Who owns A5?
3. For Controller. A9, not approved. The status is sent and nobody is named under Approved by. Who approved A9 before it was sent, and when? The status is left as supplied.
4. For Controller. A10, no owner. The related parties list (auditors' date Friday 2026-11-20, our date Tuesday 2026-11-17) is not on the owner and status list. Who owns A10, and what is its status?
5. For Controller. A11, not on the auditors' list. The Controller owns it, in progress, note "Lease schedule for the new warehouse". Did the auditors ask for it?
6. For Controller. C3, no evidence named, not kept anywhere. The supplier bank detail confirmation call leaves no named evidence and no place it is kept. What evidence does C3 leave, and where is it kept?
7. For Controller. Supplier payments, overlap with no compensating control. The Controller approves, handles the money and checks, and no compensating control is written. Is there a compensating control that someone outside the process performs?
8. For Controller. Payment of $8,900.00 to Supplier C on 2026-08-05, no approval recorded. It is at or above the $5,000.00 limit and Approved by is blank. Was it approved, and where is the record?
9. For Controller. Payment of $5,000.00 to Supplier D on 2026-09-02, approved by the person who entered it. The Controller entered and approved it; it is at the limit. Did anyone else approve it, and where is the record?
10. For Controller. F2, no evidence named. The action is "Payables clerk told to call suppliers before changing bank details" and the status is done, with no evidence. What evidence shows the action was carried out?
11. For Controller. F3, no action recorded. The fixed asset register was not reconciled to the general ledger during the year; the finding is open and What was done is blank. What has been done about F3?
12. For Controller. Receivables, no explanation. The balance moved by $234,100 (28.8%) and there is no movement note. What explains the movement? Support would sit under A3.
13. For Chief executive. Q2, not drafted, for the Chief executive. A question on legal claims or disputes is for the Chief executive to answer with the company's advisers. The pack gives no view. What is the answer, and who approves it?
14. For Chief executive. Q3, no facts supplied. The question on events after the year end has no facts and no source. What facts should the answer rest on, and from whom?

Prepared for the Controller's approval. Nothing has been sent to the auditors, assigned, approved, posted or changed.
```

## What was observed

Every section of the output format was produced, in order, and the closing line was included. No stop condition was met: every heading matched, no reference was repeated within a list, and nothing in the inputs held a bank account number, a salary, a personal detail, a password or a login code. The assistant was not asked to send, approve, assign or post anything, so the refusal rules were not exercised.

Comparison with the published example output:

- The pack agrees with the example on every date, count, total, percentage, flag and flagged line: fourteen flagged lines and fourteen numbered items, seven payments totalling $77,780.00 checked, three movements listed, and the same order of decisions.
- Wording differs throughout. The run wrote dates as `2026-11-09` with the weekday, where the example spells them out; it wrote the flag explanations more briefly and as plain lines rather than a bulleted list; and it gave Q1 as a shorter answer ("No change. We invoice on shipment and standard terms are 30 days.").
- Where the example's flags add a reason ("the control leaves no record the auditors can test", "the auditors' date is tomorrow", "last year's finding F2 was about the same kind of change"), the run stated only the facts. Those extra reasons are drawn from the inputs, not from outside them.
- In decisions 2, 6, 11 and 14 the example's questions are fuller or point at a likely next step (for example "will the register be reconciled before it goes to the auditors?"). The template says to recommend nothing unless asked; the run kept to plain questions, and the example's decision 11 comes close to steering.
- Decision 13: the example repeats the supplied fact that a customer has written about a possible claim. The run did not repeat it, because the template says the question is not drafted and no view is given.
- For A10 the run wrote "not started (no row on the owner and status list)"; the example writes "not started".
- For F2 the run added that no request is in the area "Payments".

No fact appears in the run's output that is not in the inputs. In the example's output every fact is also in the inputs or follows directly from them, such as "the auditors' date is tomorrow" (today is 9 November) and the Chief executive approving A1 (from the settings).

Where the instructions were ambiguous and the run had to choose:

1. The assistant block in the template contains an unfilled placeholder: "lead time (default [your lead time, default 3] working days)". The example's settings supply a lead time of 3, so the run was not affected, but a user who pastes the block as it stands would paste the placeholder with it.
2. A request that is missing from the owner and status list (A10) has no stated status. The template only gives "not started" for the case where the whole list is missing. The run used "not started" and said so on the line, because the summary needs every item counted at one status.
3. The settings name an approver for items the Controller owns, but not for items the Chief executive owns (A9). The run did not need to name one, but the pack shows "Approved by: not yet" for A9 and no one is named to give it.
4. Related requests for a finding are those "in the same area". F2's area is "Payments", the request list uses "Payables", and the run matched exactly, so it wrote "none". The template does not say whether close area names count.
5. The template does not say whether a decision for a question left undrafted may repeat its supplied facts (Q2). The run did not repeat them. The example did.
6. The template says "a payment nobody can explain" goes first. An unapproved payment (Supplier C) is not obviously that, and the run kept it in section order. The line between the two is a judgment.
7. Who answers a question with no facts (Q3) is taken from the settings ("events after the year end" goes to the Chief executive). The template's Roles section lists only four kinds of question for the named role; the example's settings add a fifth.
8. The movement test is described as "reaches both" an amount and a percentage; the run took the size without the sign for both, which matches "ignoring signs" for the percentage but is not stated for the amount (the Loan movement is negative).
9. When a movement note gives figures that leave a remainder (Fixed assets, $76,500), the template says to show it but not whether the remainder is a flag. The run did not flag it, as in the example.
10. The date format of "Prepared" and the auditors' dates ("[weekday date]") is not fixed.

Defects in the template itself: the placeholder in item 1 above, and the gaps in items 2 and 3. The rest are choices a controller would settle once in the settings. The run's output was not checked against the accounting figures by an accountant; the arithmetic was done by the assistant and agrees with the example.

## Changed after this run, and not run again

Changed on 10 November 2026 after an independent review of the template, and not run again. The output and the observations above are as recorded and describe the template and the example as they stood at the run:

- **The pasted instructions, settings.** The lead time placeholder (item 1 above) now reads "default 3 working days unless the settings say otherwise".
- **A request missing from the owner and status list** (item 2 above). The procedure and the pasted instructions now say it is shown with owner "not assigned" and status "not started", as the run and the example already did.
- **The second approver** (item 3 above). The Roles section now says the settings name a second approver only for the items the main approver owns; every other item, including one the Chief executive owns, goes to the main approver. For A9 that is the Controller, as the example's decision 3 already says.
- **Related requests** (item 4 above). A finding's area must match a request's area exactly; a similar name does not count. The run's and the example's "none" for F2 follow this.
- **Facts in an undrafted question's decision** (item 5 above). The item may restate the facts as supplied, adding no view. Both the run and the example are within this.
- **The movement test** (item 8 above). Both the amount and the percentage are now stated to be tested by size, ignoring signs, as the run did for the Loan.
- **Plain questions.** The procedure and the pasted instructions now ask for plain questions that do not suggest an answer. The example's decisions 1 and 11 were shortened to plain questions ("When will A1 be ready for the Chief executive's approval?" and "What has been done about F3?").
- **The example's decision 7** now asks whether a compensating control is carried out for supplier payments and what it is, and the reviewer checklist's item on documented overlaps now asks the controller to confirm that the written compensating control is carried out and to name where its record is kept.

Changed later on 10 November 2026 after a second independent review, and not run again. None of these changes a date, count, total, flag or flagged line in the example:

- **The example's decision 9** now asks a plain question, "Did anyone else approve it, and where is the record?", the wording this run used.
- **The example's output** is now shown as plain text in the output format, as this run produced it, instead of with bold, italics and bullets. Its content and order are unchanged.
- **A payment nobody can explain** (item 6 above). The template now says this is a payment whose supplier is blank, or whose supplier or purpose a note or the person running the pack says nobody recognises; a missing approval or an approval by the person who entered the payment is not one on its own and keeps its place in section order, as the run and the example did with Suppliers C and D.
- **A leftover amount in a movement note** (item 9 above). The template now says it is shown, not flagged, as the run and the example did for Fixed assets.
- **Dates in the pack** (item 10 above). The template now says each weekday date is written in full, such as Monday 9 November 2026, as the example does. This run wrote them as the weekday with YYYY-MM-DD.
- **What to customize** now names the lead time as a plain sentence rather than a placeholder, and names events after the year end as a common addition to the questions that go to the chief executive or the owner, as in the example's settings (item 7 above).
