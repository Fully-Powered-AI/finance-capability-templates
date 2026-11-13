# Job cost review at completion

When a job closes, the controller gets one review that sets recorded labour, material, subcontract and overhead beside the estimate by cost code, shows each difference and what the job-cost records say about it, and lists the questions for the estimator and the job lead. Nothing is changed.

*Workflow template · Finance and accounting · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/job-cost-review-at-completion/)*

## The outcome

Every finished job gets an honest answer to one question: what did it really cost, against what we said it would? The review lines up the estimate, including the change orders that were approved, with every cost the job recorded, cost code by cost code and type by type. Each line shows the difference in money and as a percentage, and labour is split into extra or saved hours and a higher or lower rate, so the conversation starts from the right place.

Where a difference is big enough to matter, the review shows what the records themselves say: a pending change order on the line, and the notes written on the timesheets and invoices, quoted exactly. It never turns a note into a reason. The job lead says what happened on the job, and the estimator says what the estimate assumed.

The review is just as clear about what the records cannot show yet. A line with nothing recorded is never counted as a saving. A commitment not yet invoiced means the cost is not final, and the review shows what the job comes to if it is invoiced in full. Cost on a code the estimate never had, and cost with no code at all, are listed on their own rather than lost in a total. Everything ties back to the job-cost report.

The controller verifies the figures and approves the final cost. Nothing in the estimate, the rates or the cost records is changed, and the job is not closed by the review.

## Who starts the work, and when

The controller of a job shop, contractor or project business starts it, or the operations lead or bookkeeper working for the controller, once a job's work is finished and its costs are posted. It runs before the controller signs off the job's final cost and before the estimator prices similar work again. It runs again, as a new version, when a late invoice arrives. The job lead, the estimator and the bookkeeper answer its questions.

## What they supply

- **The estimate,** as an export by cost code and cost type, with estimated hours on labour lines.
- **The job-cost export:** every posted cost on the job, with its code, type, source, reference, hours on labour rows, amount and memo.
- **The change orders,** each marked approved, pending or rejected.
- **The open commitments:** purchase orders and subcontracts for the job, with the amount committed and the amount invoiced so far.
- **A short settings note:** the job, its completion date, the currency, the control total from the job-cost report, the limits that decide which differences become questions, and who the job lead, the estimator and the records owner are.

Every export is read under stated default column headers. If one does not match, the work stops and asks which column is which.

## What comes out

One review in a fixed order: the whole job by cost type, every compared line by cost code with labour split into hours and rate, the lines that could not be compared, the record flags (commitments not invoiced, late rows, pending and rejected change orders), numbered questions each addressed to a named role, and a tie-out that proves the figures add up. Empty sections say "None." The worked example uses an invented fabrication shop and shows the full inputs as well as the result.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Construction](https://fullypowered.ai/industries/construction/), where contractors close out each job against its estimate and change orders.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), for job shops that build to order and estimate every quote.
- [Engineering firms](https://fullypowered.ai/industries/engineering-firms/), for design-and-build and project work costed by code.
- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which owns the job-cost records and signs off the final cost.
- [Project and delivery](https://fullypowered.ai/functions/project-and-delivery/), where the job lead answers for what happened on the job.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where estimates are priced from experience that should be checked against real jobs.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when more jobs run at once than anyone can review from memory.

It sits beside three related workflow templates and does not replace them. [Production cost variance sheet](https://fullypowered.ai/workflows/production-cost-variance-sheet/) measures repeat production against standard costs at a plant; this one compares one finished job with its own estimate. [Engagement margin review](https://fullypowered.ai/workflows/engagement-margin-review/) looks at fees, billing and margin on a services engagement; this one works on cost alone. [Estimate basis pack](https://fullypowered.ai/workflows/estimate-basis-pack/) records where an estimate's figures came from before the bid; this review is what the estimator reads after the job is done.

## What has to change for your company

Map your own estimate, job-cost, change order and commitment exports to the default headers. Set the percentage and amount a difference must reach before it becomes a question. Name your job lead, estimator and records owner. Add equipment or any other cost type your job-cost system keeps. Confirm how overhead reaches your jobs: the review uses the overhead your records apply and never allocates any itself. Decide whether costs dated after completion count in this review or wait for the next version. It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply; it needs no connection to your accounting system.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 12 November 2026. It was tried on its invented example in Claude on 12 November 2026, and the record is published with it. It has not been tested in a client environment or as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three finished jobs your controller already knows well, with cases written in advance: an approved change order, a pending one, a line with nothing recorded, an uncoded row and a header that does not match. The controller recomputes the differences by hand before anyone relies on the review. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that test set, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) shows the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 12 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 12 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the workflow template drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related workflow templates

- [Production cost variance sheet](https://fullypowered.ai/workflows/production-cost-variance-sheet/)
- [Estimate basis pack](https://fullypowered.ai/workflows/estimate-basis-pack/)
- [Project lessons review](https://fullypowered.ai/workflows/project-lessons-review/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
