---
name: "job-cost-review-at-completion"
description: "When a job is complete, prepare one review of what it really cost against what it was estimated to cost. For every cost code and cost type (labour, material, subcontract, overhead) it sets the recorded cost beside the revised estimate (the original estimate plus approved change orders), shows the difference in money and as a percentage, splits labour into hours and rate, and quotes what the job-cost records themselves say about each difference over the limits. Cost recorded with no estimate line, cost with no code, estimate lines with nothing recorded, commitments not yet invoiced and pending change orders are each listed on their own. Every difference over the limits, and every gap in the records, becomes a question for the estimator, the job lead or the bookkeeper. The assistant adds up, compares and asks."
license: "MIT"
metadata:
  version: "0.1.0"
  publisher: "Fully Powered AI"
  template: "Job cost review at completion"
---

# Job cost review at completion

This is the technical file for a Fully Powered workflow template. It carries the instructions an AI product follows. The complete template, with roles, inputs, exceptions, the reviewer checklist, acceptance tests and what to customize, is in [TEMPLATE.md](TEMPLATE.md). A worked example with invented data is in [EXAMPLE.md](EXAMPLE.md).

## Instructions

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

## Before relying on it

Decide every item under "What to customize" in TEMPLATE.md and set the limits the instructions in this file leave open, written in square brackets such as [N], to your own. Then run the acceptance tests in TEMPLATE.md on past work. A person starts this work, supplies the inputs and decides what happens with the result.
