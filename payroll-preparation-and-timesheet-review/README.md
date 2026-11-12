# Payroll preparation and timesheet review

Before each payroll run, the owner gets one sheet built from the timesheet and roster exports: hours by person and type, every missing punch and odd entry raised as a question, and an estimated total. Nothing is keyed in, submitted or paid until a person approves.

*Workflow template · Finance and accounting · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/payroll-preparation-and-timesheet-review/)*

## The outcome

The owner approves payroll knowing what is in it. Every person on the roster has a line: hours worked, overtime, leave and an estimated gross, worked out from your own exports and your own overtime rule. Anything that looks wrong sits on that person's line, with the date, both figures and what it would cost if left alone.

The usual payroll surprises surface before the money moves: the shift with a start and no finish, the regular who has no hours this week, a name on the timesheet nobody set up, a pay rate that moved, leave taken beyond the balance, hours logged before someone's first day. The sheet corrects none of them. Each becomes one plain question for the owner, asked one at a time.

The workflow template prepares and checks. It never fills in a missing time, never runs payroll and never touches the payroll provider. A person keys in the approved hours and the owner submits the run.

## Who starts the work, and when

The payroll clerk or office manager starts it once the pay period has closed and the timesheets are in, a day or two before the hours are due at the payroll provider. In a small company the owner runs it themselves.

The owner approves the sheet and answers its questions. Supervisors answer for their crews' hours, and the finish time of a shift is something the employee confirms. After the owner's answers, the same person can run it again to get a clean sheet before keying in.

## What they supply

- **The timesheet export** for the pay period: one row per person per shift, with start, finish and break.
- **The roster:** who is employed, hourly or salaried, the current rate, start dates and final days.
- **Approved leave** for the period and the **leave balances** from your payroll provider.
- **The last four payroll runs,** person by person, so the sheet can compare.
- **The schedule** for the period, if you keep one.
- **Your settings:** the pay period and pay date, your overtime rule as it is set up with your payroll provider, how breaks are recorded, and the cash position if you want it on the sheet.

No connection to your payroll provider, bank or time clock is needed, and none is asked for.

## What comes out

One payroll preparation sheet, in a fixed order:

1.  **The picture.** How many people, total hours by type, the estimated gross, the open flags, and everything kept out of the totals with the reason.
2.  **People.** One block per person: regular, overtime and leave hours, estimated gross, what the gross leaves out, and every flag for that person attached to their name. People with open questions come first.
3.  **Names not on the roster.** Anyone on the timesheet who is not set up, kept out of the totals.
4.  **Change from the last run.** Hours and estimated gross against the last run, with the people who account for any large move.
5.  **Cash.** The estimated gross against the balance you supply, or a plain statement that cash was not checked.
6.  **Questions for the owner.** One question per flag, each with what happens if it is left as it is.
7.  **For approval.** The headcount, hours, estimated gross, pay date and the number of questions still open.

Good looks like this: every hour on the sheet traces to a row in an export, and every row left out appears on the sheet with its reason. Employer taxes and deductions are left to your payroll provider; the sheet never guesses them.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which owns the payroll run and the cash it takes.
- [People and HR](https://fullypowered.ai/functions/people-and-hr/), which keeps the roster, the start dates and the leave records the sheet checks against.
- [Construction](https://fullypowered.ai/industries/construction/), where crews clock in at several sites and a missed clock-out is easy to overlook.
- [Hospitality](https://fullypowered.ai/industries/hospitality/), where shifts change daily, part-time staff come and go, and overtime builds up unnoticed.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where store and warehouse rotas stretch at busy times of year.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where shift work and overtime are a normal part of every payroll.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where payroll has always depended on one careful person reading every timecard.

## What has to change for your company

- **Your overtime rule.** Written exactly as it is set up with your payroll provider. The workflow template applies the rule you give it and never picks one, because the right rule depends on where your people work.
- **Your break and rounding conventions.** Whether the timesheet already takes breaks out, and whether you round.
- **Your limits.** What counts as a long shift, a long day, hours well above the schedule and overtime well above someone's usual.
- **Your roles.** Who prepares, who approves, who keys hours in and who submits.
- **Your exports.** The column names your time clock and payroll provider produce, so the template reads them as they come.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini. Decide which exports the assistant may read, and remove anything it does not need, such as tax numbers, dates of birth and bank details.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its own invented example in one AI product on 9 November 2026; the record of that run is published with the template, and lists the edits made afterward that have not been run again. That is a trial, not a test. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on past pay periods your payroll clerk already knows, with hard cases written in advance: a missing clock-out, a regular with no hours, a name not on the roster, a rate change, leave beyond the balance. The owner checks every line against the exports before anyone relies on the sheet. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 9 November 2026. The record is in [TRIAL.md](TRIAL.md).
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

- [Supplier bill review and payment-run preparation](../supplier-bill-review-and-payment-run-preparation/)
- [Thirteen-week cash flow forecast](../thirteen-week-cash-flow-forecast/)
- [Employee offboarding and handover checklist](https://fullypowered.ai/workflow templates/employee-offboarding-and-handover-checklist/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
