# Job cost review at completion

Workflow template, version 0.1.0.

## Purpose

When a job is complete, prepare one review of what it really cost against what it was estimated to cost. For every cost code and cost type (labour, material, subcontract, overhead) it sets the recorded cost beside the revised estimate (the original estimate plus approved change orders), shows the difference in money and as a percentage, splits labour into hours and rate, and quotes what the job-cost records themselves say about each difference over the limits. Cost recorded with no estimate line, cost with no code, estimate lines with nothing recorded, commitments not yet invoiced and pending change orders are each listed on their own. Every difference over the limits, and every gap in the records, becomes a question for the estimator, the job lead or the bookkeeper. The assistant adds up, compares and asks. It never states a cause, never changes an estimate, a rate or a cost record, never recodes a row and never closes the job.

## When to use it and when not to

Use it when the work on the job is done and every cost has been posted, before the controller signs off the job's final cost and before the estimator prices similar work again. Run it again, as a new version, when a late invoice or a correction arrives.

Do not use it:

- for a job still in progress that needs a cost-to-complete forecast. This review compares what is recorded with what was estimated; it forecasts nothing beyond adding open commitments to the recorded cost;
- for a plant that costs production orders against standard cost cards. That is the production cost variance sheet;
- for fees, billing and margin on a services engagement. That is the engagement margin review. This review works on cost only and needs no contract value, billing or revenue figure;
- for the landed cost of imported products. That is the product landed cost worksheet;
- to set new estimating rates, update the estimate, recode a cost row, post a correction or close the job in the accounting system. People do those, from the approved review;
- to decide whether to bill the customer for extra work or charge a subcontractor back. The review lists pending change orders; the controller and the job lead decide what follows;
- to judge or rank people. A difference is never attributed to a crew, an employee, a supplier or a subcontractor by the review.

## Roles

- **Runs it:** the controller, or the operations lead or bookkeeper working for the controller.
- **Verifies the figures and approves the review:** the controller.
- **Answers questions about what happened on the job:** [your job lead], default the project manager or foreman who ran the job.
- **Answers questions about what the estimate assumed:** [your estimator].
- **Answers questions about the records (codes, missing postings, commitments):** [your records owner], default the bookkeeper.
- **Decides the job's final cost for the books, and any action that follows:** the controller. Any change to future estimating rates is the estimator's call, with the controller.

## Inputs

The assistant works only from the files and notes the person supplies. It needs no connection to the accounting or job-cost system and never asks for a password or a login code. All amounts are in one currency and are plain numbers.

1. **The estimate,** as an export with one row per cost code and cost type. Default column headers: `cost_code`, `description`, `cost_type`, `est_hours`, `est_cost`. `cost_type` is one of `labour`, `material`, `subcontract`, `overhead`. `est_hours` is filled for labour rows and blank for the others. Required.
2. **The job-cost export,** one row per posted cost. Default column headers: `job`, `date`, `cost_code`, `cost_type`, `source`, `reference`, `vendor_or_employee`, `hours`, `amount`, `memo`. `hours` is filled on labour rows. A negative `amount` is a credit. Applied overhead appears as rows with `cost_type` `overhead`; the assistant never allocates overhead itself. Required.
3. **The change orders,** as an export. Default column headers: `change_order`, `cost_code`, `cost_type`, `hours`, `cost`, `status`. `status` is `approved`, `pending` or `rejected`. If not supplied, the review says "change orders not supplied" in its header and uses the original estimate as the revised estimate.
4. **The open commitments,** as an export of purchase orders and subcontracts for the job. Default column headers: `commitment`, `vendor`, `cost_code`, `cost_type`, `committed`, `invoiced_to_date`. If not supplied, the header says "open commitments not supplied; the recorded cost may not be final".
5. **The settings,** typed: the job number and name; the date the job was completed; the currency; the file name of each export supplied, if the person wants them printed (any not given print as "as supplied"); the control total of the job-cost report, if the person has it; [your percentage limit], default 10; [your amount limit], default 500; who the job lead, the estimator and the records owner are.

If a header in any export does not match the defaults, or a column is missing, stop and ask which column holds what. Never guess a mapping and never rename a column silently. If the estimate or the job-cost export is missing, stop and say so. If the settings are partly missing, use the defaults and say which were used.

## The procedure

1. **Check the files before any arithmetic.** Confirm every header. Confirm that every row of the job-cost export carries the job number in the settings; if any row carries another job, stop and ask. Confirm that every `cost_type` in every file is one of the four; if one is blank or different, stop and ask. Confirm that no cost code and cost type pair appears twice in the estimate; if one does, stop and ask which row is right. Confirm every change order `status` is approved, pending or rejected; stop on anything else. Confirm every amount, cost and hours figure is a plain number: a currency symbol or code in a figure, or a second currency named by the person, means more than one currency, so stop and ask.
2. **Check the record total.** Add every `amount` in the job-cost export. If the settings give a control total and the sum differs from it, stop and report both figures. If no control total was given, print the sum and say it was not checked against the report.
3. **Build the revised estimate.** A line is one cost code and cost type pair. For each line, revised estimate = `est_cost` plus the `cost` of every approved change order on that pair; revised hours = `est_hours` plus the `hours` of every approved change order on that pair. An approved change order on a pair that is not in the estimate creates a line whose original estimate is 0.00. Pending change orders are never added: list them against their line. Rejected change orders are not used: count them in the header and list them under Record flags.
4. **Total the records by line.** For each line, add the `amount` of every row on that pair, credits included, and, for labour, the `hours`. A row with a blank `cost_code` is uncoded: keep it out of every line, and list it with its date, source, reference, vendor or employee, amount and memo.
5. **Sort every line into one of three groups.**
   - **Compared:** the revised estimate is above 0.00 and at least one row is recorded on it.
   - **Estimated, nothing recorded:** the revised estimate is above 0.00 and no row is recorded on it. No difference is printed; nothing recorded is never read as a saving.
   - **Recorded, not in the estimate:** rows are recorded on a pair whose revised estimate is 0.00 or that the estimate does not have.
   - A line whose revised estimate is below 0.00 (an approved deductive change order larger than the estimate): stop and ask; never net it silently. A line whose revised estimate is 0.00 and has no rows has no cost on either side: leave it out of all three groups and of the line count.
6. **Work out each compared line's difference.** Difference = recorded cost − revised estimate. Positive is "over", negative is "under", exactly zero prints as 0.00. Percentage = the difference ÷ the revised estimate, to one decimal place. Compute at full precision and round only when printing: amounts to the cent, hours to two decimals.
7. **Split labour into hours and rate.** For a compared labour line whose revised hours are above 0 and whose rows all carry hours: estimate rate = revised estimate ÷ revised hours; hours part = (recorded hours − revised hours) × estimate rate; rate part = recorded cost − (recorded hours × estimate rate). Print the average recorded rate (recorded cost ÷ recorded hours) beside the rate part. The two parts must add to the line's difference; if they do not, stop and report the line and the figures. If any labour row on the line has blank hours, print "Hours split not given" with the rows named, and list them under Record flags. If the revised hours are 0 (cost estimated, no hours), print "Hours split not given: the estimate has no hours."
8. **Test each compared line against the limits.** A line is over the limits when the absolute difference is at least [your percentage limit] percent of its revised estimate and at least [your amount limit]. Both must be met. Under-runs are tested the same way as over-runs. Lines below the limits are printed with their figures and get no question.
9. **Show what the records say about each line over the limits.** Under the line, print "In the records:" and then, in this order:
   - every pending change order on the same pair, with its number and cost, and the difference that would remain if it were approved as stated;
   - every row on the line with a memo that is not blank, largest absolute amount first, at most five, each with its date, source, reference and amount, and the memo quoted word for word in quotation marks. If more than five rows have a memo, say how many more there are;
   - if there is neither, "Nothing in the supplied records bears on this line."
   A memo is what the record says. Never present it as the reason for the difference, never add words to it, and never infer a cause from it.
10. **Check the commitments.** For each open commitment, remaining = `committed` − `invoiced_to_date`. A remaining amount above 0.00 means the job's cost is not final: list the commitment under Record flags and mark its line "not final" wherever the line is printed, whether under By cost code or under Not compared. A remaining amount below 0.00 means more has been invoiced than committed: list it under Record flags. A commitment on a pair that is in no line is listed all the same, with "no estimate line".
11. **Flag the rest of the records.** Under Record flags also list: rows dated after the completion date (they are counted; the flag only names them); labour rows with blank hours; pending change orders; rejected change orders. Print "None." under any heading with nothing in it.
12. **Write the questions.** One question for each line over the limits, and one for each flag that needs an answer, in this order: lines over the limits in ascending cost code (labour, material, subcontract, overhead within a code); then flag-only questions in ascending cost code, with uncoded rows last. Each question states the figures, then asks named roles, one sentence per role. A role is printed as its role name (Controller, Estimator, Job lead, Records owner), never as the person's job title or name.
    - A line over the limits: the job lead is asked what they know about the cost on the line; the estimator is asked what quantity, hours or price the estimate used for it. On an overhead line, the controller is asked instead what basis applied the overhead and whether the estimate used the same basis. A flag on the same line (pending change order, commitment not invoiced) joins the same question.
    - Estimated, nothing recorded: the records owner is asked whether cost for the line is posted elsewhere or still to come; if a commitment on the line is not invoiced, the job lead is asked whether it will be invoiced or closed.
    - Recorded, not in the estimate: the estimator is asked whether the work was in the estimate under another code; the job lead is asked what the cost was for, beyond any memo quoted.
    - A commitment not invoiced, or invoiced above its commitment, on a line not already asked about: the job lead is asked whether more will be invoiced or the commitment closed.
    - A pending change order on a line not already asked about: the job lead is asked for its status.
    - An uncoded row, or a labour row with blank hours: the records owner is asked which code or hours the row should carry. The review never recodes it.
    - Rows dated after the completion date and rejected change orders get no question.
    A question never contains a reason, a guess or "possibly", and never names an employee or a crew as the cause of anything.
13. **Total by cost type and for the whole job.** For each cost type: original estimate, approved change orders, revised estimate, recorded cost (every row of that type, coded or not), difference and percentage. Labour also shows revised and recorded hours. Then the whole job. Then the open commitments not invoiced, and the recorded cost plus those commitments with its difference against the revised estimate. Then pending change orders, not included in any estimate figure.
14. **Tie out.** Show: original estimate lines + approved change orders = revised estimate; the rows' sum against the control total; compared-line differences + recorded not in the estimate + uncoded − estimated with nothing recorded = recorded cost − revised estimate; and the four cost-type differences adding to the whole-job difference. If any of these fails, stop and report it.
15. **Trace line and return.** Name the files behind every figure. Return the review to the controller only.

## Exceptions and stop conditions

- **A header does not match, a column is missing, or the estimate or the job-cost export is missing:** stop and ask.
- **A row carries another job number:** stop and ask.
- **A cost type is blank or not one of the four:** stop and ask; never assign one.
- **A cost code and cost type pair appears twice in the estimate, or a change order status is not approved, pending or rejected:** stop and ask which is right.
- **The rows do not add to the control total, or a tie-out line fails:** stop and report the figures. Never adjust a figure so the review ties.
- **A line's revised estimate is below 0.00:** stop and ask.
- **A labour line's hours part and rate part do not add to its difference:** stop and report the line.
- **A figure carries a currency symbol or code, or the person names a second currency:** stop and ask; never convert on a guess.
- **Asked what caused a difference, to blame a person, crew, supplier or subcontractor, to change the estimate or a rate, to recode or post a row, to close the job, or to decide whether to bill the customer or charge a subcontractor back:** decline. A difference is a question; the controller decides, and the job lead and the estimator answer.

## Output format

```
JOB COST REVIEW AT COMPLETION: [job number], [job name]

For: [controller]. Completed [date]. Amounts in [currency], to the cent; hours to two decimals. "Over" means recorded cost above the revised estimate; "under" means below. A line is asked about when its difference reaches both [percentage] percent and [amount]. A difference is a question, not a cause.
Files: estimate [name]; job-cost export [name], [n] rows; change orders [name / not supplied]; open commitments [name / not supplied; the recorded cost may not be final].
Lines: [n] in the revised estimate. Compared: [n]. Estimated, nothing recorded: [n]. Recorded, not in the estimate: [n]. Uncoded rows: [n]. Lines over the limits: [n]. Questions: [n]. Rejected change orders not used: [n].

WHOLE JOB
Labour: estimate [amount] + approved change orders [amount] = [amount] ([hours] h). Recorded [amount] ([hours] h). [amount over/under], [percent]%.
Material: estimate [amount] + approved change orders [amount] = [amount]. Recorded [amount]. [amount over/under], [percent]%.
Subcontract: estimate [amount] + approved change orders [amount] = [amount]. Recorded [amount]. [amount over/under], [percent]%.
Overhead: estimate [amount] + approved change orders [amount] = [amount]. Recorded [amount]. [amount over/under], [percent]%.
Whole job: estimate [amount] + approved change orders [amount] = [amount]. Recorded [amount]. [amount over/under], [percent]%.
Open commitments not invoiced: [amount] in [n] commitments. Recorded plus those commitments: [amount], [amount over/under] the revised estimate, [percent]%. / None.
Pending change orders, not in any estimate figure above: [amount] in [n]. / None.

BY COST CODE
[code] [description], [type]: revised estimate [amount] ([original] + [approved change orders]); recorded [amount]. [amount over/under], [percent]%.[ Over the limits.][ Not final: [commitment], [amount] not invoiced.]
- Hours: revised [hours] h, recorded [hours] h. Hours part [amount over/under] ([hours] h [more/fewer] at the estimate's [rate]). Rate part [amount over/under] (average recorded rate [rate]). / Hours split not given: [rows] have no hours. / Hours split not given: the estimate has no hours.
- In the records: [CO number] pending, [amount]; if approved as stated, [amount over/under] would remain. [date], [source] [reference], [amount]: "[memo]". / Nothing in the supplied records bears on this line.
(Compared lines only, in ascending cost code; labour, material, subcontract, overhead within a code. The Hours line appears on labour lines only. The In the records line appears on lines over the limits only. / None.)

NOT COMPARED
Estimated, nothing recorded: [code] [description], [type]: revised estimate [amount].[ Not final: [commitment], [amount] not invoiced.] / None.
Recorded, not in the estimate: [code], [type]: [amount].[ Not final: [commitment], [amount] not invoiced.] Rows: [date], [source] [reference], [amount][: "[memo]"]. / None.
Uncoded rows: [date], [type], [source] [reference], [vendor or employee], [amount][: "[memo]"]. / None.

RECORD FLAGS
Open commitments not invoiced: [commitment] ([vendor], [code] [type]): [committed] committed, [invoiced] invoiced, [remaining] not invoiced. / None.
Invoiced above a commitment: [commitment]: [committed] committed, [invoiced] invoiced. / None.
Rows dated after completion: [date], [code] [type], [reference], [amount]. / None.
Labour rows with no hours: [date], [code], [reference], [amount]. / None.
Pending change orders: [CO number], [code] [type], [amount]. / None.
Rejected change orders, not used: [CO number], [code] [type], [amount]. / None.

QUESTIONS FOR THE CONTROLLER, THE ESTIMATOR, THE JOB LEAD AND THE RECORDS OWNER
1. [Code] [description], [type]: [recorded against revised estimate, the difference and its percentage; any pending change order or commitment on the line]. [Role]: [question]. [Role]: [question].
2. [Code or row, flag]: [what is flagged, with the figures]. [Role]: [question].
(Lines over the limits first, then flag-only questions, each in ascending cost code, uncoded rows last. / None.)

TIE-OUT
Estimate: lines [amount] + approved change orders [amount] = revised estimate [amount].
Records: [n] rows add to [amount]; control total [amount / not supplied]; [agree / not checked].
Difference: compared lines [signed amount] + recorded, not in the estimate [amount] + uncoded [amount] - estimated, nothing recorded [amount] = [signed amount]; recorded [amount] less revised estimate [amount] = [signed amount].
By type: labour [signed amount] + material [signed amount] + subcontract [signed amount] + overhead [signed amount] = [signed amount].
(Signed amounts: over is positive, under is negative.)

Every figure traces to [estimate file], [job-cost export] and [change order and commitment files]. The review changes no estimate, rate or record, and closes nothing.
```

## Reviewer checklist

1. The headers were matched as supplied, every row of the job-cost export belongs to this job, and the rows add to the job-cost report's total. (Controller)
2. Each approved change order is in the revised estimate once, on the right line, and no pending change order is in it. (Controller)
3. For two lines chosen by the controller, the recorded cost is recomputed by hand from the rows, and the difference and percentage are right. (Controller)
4. Each labour line's hours part and rate part add to its difference. (Controller)
5. No estimate line with nothing recorded is counted as a saving, and every uncoded row and every cost with no estimate line appears under Not compared. (Records owner)
6. The open commitments match the purchasing records, and the amounts invoiced match the rows in the export. (Records owner)
7. Every memo is quoted word for word, and no line says or implies a cause. (Controller)
8. Every line over the limits has a question, no line under them does, and every question names a role and gives figures only. (Controller)
9. The job lead and the estimator have answered, and their answers are kept as theirs, with their names, beside the review, not written into it as fact. (Controller)
10. Nothing in the estimate, the rates or the cost records has been changed because of the review, and the job's final cost is approved by the controller before it is shared. (Controller)

## Acceptance tests

Proposed tests. The invented example exercises tests 2, 3, 4, 6, 7, 8, 9 and 14 in one run (the record is public/trial.md); the others have not been run.

1. **Clean job.** Every line recorded, no change orders, no commitments open, all differences under the limits. Expected: no questions; every flag heading "None."; tie-out correct.
2. **Approved change order.** An approved change order adds 16 hours and 880.00 to a labour line. Expected: the revised estimate includes it; the line is compared against the revised figure, not the original.
3. **Pending change order on an over-run line.** Expected: not added to the estimate; shown under "In the records" with the difference that would remain; listed under Record flags; joined to the line's question.
4. **Both limits.** A line 10.0 percent under with a difference of 240.00, limits 10 percent and 500. Expected: printed, no question.
5. **Under-run over the limits.** A line 2,000.00 under, 25 percent. Expected: asked about, the same as an over-run.
6. **Nothing recorded.** An estimate line of 2,800.00 with no rows and an open commitment of 2,800.00. Expected: listed under Not compared marked "Not final", no difference printed, one question to the records owner and the job lead, and it appears in the tie-out.
7. **Code not in the estimate.** Rows on a code the estimate does not have. Expected: listed under Not compared; a question to the estimator and the job lead; counted in the tie-out.
8. **Uncoded row.** Expected: kept out of every line, counted in its cost type's whole-job figure, listed, and put to the records owner; never recoded.
9. **Labour split.** 262 hours and 14,000.00 against 220 hours and 11,000.00. Expected: hours part 2,100.00 over, rate part 900.00 over, average rate 53.44, adding to 3,000.00.
10. **Labour row with no hours.** Expected: hours split not given on its line, row named under Record flags, a question to the records owner.
11. **Control total differs.** The rows add to 100.00 less than the report. Expected: stops and reports both figures.
12. **Header mismatch.** `cost` where `amount` is expected. Expected: stops and asks; no mapping guessed.
13. **Another job's row.** Expected: stops and asks.
14. **Credit row.** A negative amount on a material line. Expected: counted in the line, quoted if it carries a memo and the line is over the limits.
15. **Asked for a cause.** "Was the extra labour rework?" Expected: declines, restates the figures and any memo as quoted, and puts the question to the job lead.
16. **Asked to update the estimate or recode a row.** Expected: declines and names who does it.
17. **Invoiced above a commitment.** Expected: listed under Record flags and put to the job lead.
18. **Pending change order on a line under the limits.** A compared line 4 percent over, 300.00, with a pending change order on the same pair. Expected: the line is printed with no "In the records" and no question from the limits; the change order appears under Record flags and in one question to the job lead asking for its status; it is not added to the estimate.
19. **Revised estimate below zero.** An approved deductive change order larger than the line's estimate. Expected: stops and asks; nothing is netted silently.
20. **Estimate with no hours.** A compared labour line whose revised hours are 0. Expected: difference printed, "Hours split not given: the estimate has no hours."; no rate part computed.

## Instructions for the AI assistant

```
You prepare the job cost review at completion for the controller. You
compare what a finished job recorded with what it was estimated to cost.
You never change an estimate, a rate or a cost record, never recode or
post a row, never close the job and never send the review. The controller
verifies and approves; the job lead and the estimator answer questions.

The user will supply: the estimate; the job-cost export; the change orders
and the open commitments if they have them; the settings (job number and
name, completion date, currency, file names, control total, limits, who the
job lead, estimator and records owner are). Print a file name as given, or
"as supplied" if none was given. If the estimate or the job-cost export is
missing, stop and say so. Never ask for a password or a login code.
Confirm every column header against these defaults; if one differs or is
missing, stop and ask which column holds what. Never guess a mapping.
Estimate: cost_code, description, cost_type, est_hours, est_cost.
Job-cost export: job, date, cost_code, cost_type, source, reference,
vendor_or_employee, hours, amount, memo (negative amount = credit).
Change orders: change_order, cost_code, cost_type, hours, cost, status
(approved, pending or rejected). Open commitments: commitment, vendor,
cost_code, cost_type, committed, invoiced_to_date. Cost types are labour,
material, subcontract, overhead. If the settings are partly missing, use
a 10 percent limit and a 500 amount limit and say so.

1. Check: every export row carries this job number; every cost type is one
   of the four; no code and type pair repeats in the estimate; every change
   order status is approved, pending or rejected; every figure is a plain
   number (a currency symbol or code, or a second currency named, means
   stop and ask). Stop on any failure.
2. Add every amount. If a control total is given and differs, stop and
   report both. If none is given, say the sum was not checked.
3. A line is one code and type pair. Revised estimate = est_cost + approved
   change orders on the pair; revised hours likewise. An approved change
   order on a pair the estimate does not have creates a line with original
   estimate 0.00. Never add pending or rejected change orders.
4. Total the rows by line, credits included. A row with a blank code is
   uncoded: keep it out of every line and list it.
5. Group each line: compared (revised estimate above 0, rows recorded);
   estimated, nothing recorded (no difference printed, never a saving);
   recorded, not in the estimate. A revised estimate below 0 (a deductive
   change order larger than the estimate): stop and ask. A revised estimate
   of 0 with no rows is left out of all three groups and the line count.
6. Difference = recorded - revised estimate; positive is over, negative
   is under; percentage of the revised estimate to one decimal. Full
   precision; round only when printing.
7. Labour lines with revised hours and hours on every row: estimate rate =
   revised estimate / revised hours; hours part = (recorded hours - revised
   hours) x estimate rate; rate part = recorded cost - recorded hours x
   estimate rate; print the average recorded rate. The parts must add to
   the difference or stop. Blank hours on any row: no split; flag the rows.
   Revised hours of 0: no split; print "Hours split not given: the
   estimate has no hours."
8. A compared line is over the limits when the absolute difference is at
   least the percentage of its revised estimate AND at least the amount.
   Under-runs are tested the same way.
9. Under each line over the limits print "In the records:": pending change
   orders on the pair with what would remain if approved as stated; then
   up to five rows with a memo, largest absolute amount first, memo quoted
   word for word, and how many more rows have a memo if there are more than
   five; or "Nothing in the supplied records bears on this line."
   A memo is what the record says, never the reason. Never infer a cause.
10. Commitments: remaining = committed - invoiced_to_date. Above 0: the
    line is not final; flag it and mark the line "Not final" wherever it
    is printed, in By cost code or in Not compared. Below 0: flag it as
    invoiced above the commitment. A commitment on a pair that is in no
    line is listed all the same, with "no estimate line".
11. Record flags also list rows dated after completion, labour rows with
    no hours, pending and rejected change orders. "None." when empty.
12. Questions, numbered: lines over the limits in code order (labour,
    material, subcontract, overhead within a code), then flag-only
    questions in code order, uncoded rows last. Give the figures, then
    one sentence per role, each role printed by its role name (Controller,
    Estimator, Job lead, Records owner), not a job title. Over the limits:
    job lead, what they know about the cost; estimator, what quantity,
    hours or price the estimate used; on overhead, the controller, what
    basis applied it. Nothing recorded:
    records owner, posted elsewhere or still to come; job lead too if a
    commitment is open. Not in the estimate: estimator and job lead.
    Commitment open or over-invoiced, or pending change order, on a line
    not asked about: job lead. Uncoded row or row with no hours: records
    owner. Late rows and rejected change orders: no question. Never a
    reason, a guess or "possibly"; never name a person or crew as a cause.
13. Totals by cost type and for the whole job (uncoded rows count in their
    type), labour hours, open commitments not invoiced and recorded plus
    those commitments, and pending change orders kept apart.
14. Tie out as the format shows. If any line fails, stop and report it.
15. Use the output format exactly, with "None." for an empty section, and
    end with the trace line, naming the files as given. Return the review
    to the controller only.

If asked for a cause, to blame anyone, to change the estimate or a rate,
to recode or post a row, to close the job, or to decide on billing the
customer or charging a subcontractor back, decline and say who decides.
```

## What to customize

- The default column headers, to your own estimate, job-cost, change order and commitment exports.
- [your percentage limit] and [your amount limit].
- The cost types. Add equipment, or any other type your job-cost system keeps, by naming it in the settings, the checks in step 1 and the Whole job section together.
- Who your job lead, estimator and records owner are for each kind of question.
- How overhead reaches your jobs. The review uses the overhead your records apply; if your shop applies none to jobs, drop the overhead type or leave it as "Estimated, nothing recorded" and say so in the settings.
- Whether rows dated after completion are counted (the default) or held for the next version of the review.
- The number of memos quoted per line (default five).
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 12 November 2026. Written by Fully Powered AI. Tried on its invented example in Claude on 12 November 2026 (the record is public/trial.md); not yet tested in a client environment.
