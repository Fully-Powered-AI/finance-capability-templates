# Journal entry preparation

At month end, your bookkeeper hands the controller every proposed journal entry ready to review: balanced lines on accounts from your own chart, the arithmetic and the document behind each amount, whether it reverses, and who approves it. Nothing is posted until a person approves.

*Capability template · Finance and accounting · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/journal-entry-preparation/)*

## The outcome

The manual entries of the close arrive at the controller's desk as a package instead of a pile. Each one has its lines, a memo that will still make sense to an auditor next year, the calculation that produced the amount, and the document that proves it. Accruals, prepaid releases, depreciation, deferred revenue and corrections all come out in the same shape, so review becomes reading, not reconstructing.

The package also catches the mistakes that cost a second close. An accrual for a bill that has already been posted. An account that is not in the chart, or has been retired. A correction booked as a net difference instead of a clean reversal. An accrual left standing into next month, where the real bill will land on top of it. A round number with nothing behind it. Each arrives as a hold or a flag, with a question for the person who can answer it.

Your team still decides. The capability prepares and checks; the controller reviews, the right person approves, and someone on your team posts the entries.

## Who starts the work, and when

The bookkeeper or staff accountant starts it at month end, once the requests for manual entries are gathered from the schedules, the open purchase orders, the contracts and the notes from project leads. It runs again for a request that arrives late, or when a hold is cleared.

The controller reviews every entry. The person your approval limits name for its amount and kind approves it, such as a finance director for larger entries or for any correction of a closed month.

## What they supply

- **The list of entries wanted:** for each, what it records, its kind, the accounts, where the amount comes from, the documents behind it, and whether it reverses.
- **The chart of accounts,** exported as it stands, so every account can be checked.
- **What is already posted this month** in the revenue and expense accounts the requests use, so nothing is booked twice.
- **The supporting documents:** prepaid and deferred revenue schedules, the asset register, contract or order extracts, bills, and for a correction the original entry.
- **A few settings:** the period, who prepares, reviews, approves and posts, your approval limits and when depreciation starts on a new asset.

Files and a short list are enough. It needs no connection to your accounting system, and it never asks for a password or a login code.

## What comes out

One package for the period, in a fixed order:

1. **A summary:** how many entries are ready for review, how many are held and why, how many need no entry, and the totals of what is ready.
2. **One block per entry:** its status, its lines with totals, its memo, the calculation with the source of each figure, what was already booked, its support, the checks it passed, any flags, and who approves it.
3. **The questions,** each addressed to a named role with the figures it is about.
4. **A sign-off line** for the reviewer and the approver of every entry.

A good package lets the controller follow any amount from a line back to the document it came from, without asking anyone.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which owns the close and every entry in it.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where retainers billed in advance and contractor work not yet invoiced make deferred revenue and accruals a monthly routine.
- [Software and technology](https://fullypowered.ai/industries/software-technology/), where subscriptions are billed ahead and released month by month, and the equipment register keeps growing.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where depreciation on plant and accruals for goods received but not billed are large enough that an error moves the month.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the entries have been made the same way for years by one person and should be checkable by anyone.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when the number of manual entries outgrows the time one reviewer has at month end.

## What has to change for your company

- **Your exports.** The column names your accounting system produces. If a heading does not match, it stops and asks rather than guessing.
- **Your kinds of entry.** The capability knows accruals, prepaid releases, depreciation, deferred revenue, reclassifications and corrections. Add your own, such as payroll accruals, with the accounts each should use.
- **Your approval limits.** Who approves which amounts, and who approves a correction of a closed month.
- **Your rules.** When depreciation starts on a new asset, the dates entries and reversals carry, and the round figure that should make a reviewer ask how an estimate was reached.
- **Your roles.** Who prepares, reviews, approves and posts, and who answers questions about suppliers, customers and accounting treatment.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply. Decide which exports the assistant may read and where approved packages are kept.

## What has been checked

Fully Powered AI wrote this capability template. It was editorially reviewed on 10 November 2026. It was tried on its invented example on 9 November 2026 in two runs: the instructions were revised after the first, and the record of the second is published with it. Neither run reached the stop conditions. It has not yet been tested in a client environment, and it has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three past months whose entries your controller already approved, plus hard cases written in advance, each with the expected result: an accrual for a bill already posted, an account retired from the chart, a correction of a closed month, an asset placed in service mid-month, a heading the template does not recognize. The controller compares every line with the approved entries before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 9 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete capability template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the capability drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related capabilities

- [Month-end close checklist](../month-end-close-checklist/)
- [Bank reconciliation preparation](../bank-reconciliation-preparation/)
- [Budget-versus-actual variance commentary](../budget-versus-actual-variance-commentary/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
