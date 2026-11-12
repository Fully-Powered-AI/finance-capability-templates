# Spreadsheet check before sharing

Before a model or schedule goes to a client, a lender or a board, the sender gets one report on it: every error value, short total, buried assumption and hidden row pinned to its cell, each with a fix or a question, and a plain list of what was not checked. Nothing in the workbook is changed.

*Workflow template · Finance and accounting · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/spreadsheet-check-before-sharing/)*

## The outcome

The file leaves without the mistake everyone notices except its author. The total that skips a row, the `#REF!` on the summary page, the title that names last year, the note to a colleague still sitting in a comment: each is found before the recipient finds it, with the cell, the formula and what it does to the figures they will read.

Not everything odd is wrong, and the report knows the difference. A totals row is supposed to look unlike the rows it adds; an opening figure is supposed to be typed. Those land in a short "flagged but fine" list. The cells only the model's owner can explain arrive as questions, each with the figures it turns on, so a single conversation settles them.

The sender also sees what the recipient can see: hidden sheets and rows, comments, placeholder text, links to other files. Hidden is not private once a file leaves the building.

The workflow template checks and reports. The model's owner makes the fixes, and the sender decides whether the file goes.

## Who starts the work, and when

The person about to send the file runs it: a finance manager sending a projection to the bank, an analyst sending a pricing schedule to a client, an owner sending the board pack, an adviser sending a model to an investor. The usual moment is the day before it goes, with time to fix what turns up. It is equally useful on a workbook inherited from someone who has left.

The sender reads the report and decides what to fix and whether to send. The model's owner, often the same person, answers the questions.

## What they supply

- **The workbook,** as a file the assistant can open, or as ranges pasted twice: once showing formulas and once showing values, each labelled with its sheet and cells.
- **A sending note:** who receives it and when, who built it, and the headline figures the recipient will read, by cell.
- **Known design choices,** where there are any: overrides, opening figures and hidden helper rows that are meant.
- **The sheet list and comments,** when working from pasted ranges, so hidden sheets and notes are not missed.

No connection to any system is needed and none is asked for. No linked file is opened and no macro is run.

## What comes out

One report in a fixed order:

1. **The header:** what was read, the headline figures, and the count of findings in each section.
2. **Coverage:** what was read in full, what was not, and what no check of this kind can see.
3. **Fix before sending:** the mistakes, each with the cell, the evidence, the effect on headline figures and the exact correction.
4. **Confirm before sending:** what may be meant, each with one question for the model's owner.
5. **Tidy if time:** fragile habits that are not yet wrong.
6. **Flagged but fine:** what looked odd and why it is right.
7. **What the recipient can see:** hidden sheets, rows and columns, comments and internal text.
8. **The checklist run:** a result for each of twelve items, so nothing is skipped silently.

Good looks like this: every finding names a real cell, every recomputed figure is right, and nobody is told a correct total is wrong.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which sends the projections, budgets and schedules that outsiders rely on.
- [Quality management](https://fullypowered.ai/functions/quality-management/), for any team that wants a repeatable check before work leaves the building.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where a schedule sent to a client carries the firm's name.
- [Finance and investment](https://fullypowered.ai/industries/finance-and-investment/), where models travel to investment committees and counterparties.
- [Real estate](https://fullypowered.ai/industries/real-estate/), where development appraisals and rent rolls go to lenders and partners.
- [Nonprofits](https://fullypowered.ai/industries/nonprofits/), where budgets go to boards and funders who read every line.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the models were built years ago by someone else and are still sent out every quarter.

## What has to change for your company

- **Your headline figures.** The cells your lenders, clients or board actually read, so the findings that touch them come first.
- **Your checklist.** Add the checks your own reviewers always make, such as cash flow tying to the balance sheet, and drop the ones that never apply.
- **Your design choices.** The overrides and helper sheets your models use on purpose.
- **Your internal words.** The placeholder text, codes and other client names that should never reach a recipient.
- **Your second pair of eyes.** Whether someone besides the model's owner looks at the fixes before the file goes.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini, from an attached workbook or from pasted ranges. Decide which files the assistant may read.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 9 November 2026. It was tried on its invented example in Claude on 9 November 2026 in one run, by a model that had not written it, on the template as it now stands; the record is published with it. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three workbooks your team has already sent, with known mistakes planted in copies and written down in advance: a total one row short, a typed figure among formulas, a hidden row feeding a summary, a title with the wrong year. The model's owner confirms each finding against the workbook before anyone relies on the report. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 9 November 2026.
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

- [Budget-versus-actual variance commentary](../budget-versus-actual-variance-commentary/)
- [Thirteen-week cash flow forecast](../thirteen-week-cash-flow-forecast/)
- [Month-end close checklist](../month-end-close-checklist/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
