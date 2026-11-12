# Budget-versus-actual variance commentary

Before the month's results go to management, the finance lead gets written commentary on every line that moved past the threshold: the figures, the budget owner's explanation marked confirmed or to be confirmed, a bridge from budget to actual, and the questions still open. No cause is invented.

*Workflow template · Finance and accounting · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/budget-versus-actual-variance-commentary/)*

## The outcome

The results arrive with their story, and the story is honest about what is known. Every line that moved enough to matter has its figures, its explanation in the budget owner's own terms, and a plain label: confirmed by the person who owns the line, or still to be confirmed by them. A line nobody has explained says so, instead of carrying a plausible guess.

The finance lead walks into the meeting with a bridge that runs from the budgeted result to the actual one, line by line, so nothing is left unaccounted for. The questions that remain are already written, each addressed to the owner who can answer it. Where the order figures or hours allow, a line's movement is split into how much came from volume and how much from price, labelled as arithmetic, not as a reason.

The workflow template prepares. The budget owners explain, the finance lead approves, and nothing is sent until they do.

## Who starts the work, and when

The finance lead or management accountant runs it each month or quarter, once the period's actuals are ready to report and the budget owners have sent their notes. A department head can run it on their own department's lines before sitting down with the finance lead.

The finance lead approves the commentary and decides who receives it: the managing director, the owner, the board or the leadership team.

## What they supply

- **The budget-versus-actual export** for the period: each line with its type, its owner, the budget and the actual, plus the revenue and cost totals.
- **The budget owners' notes:** what each owner says about their lines, with the date.
- **Figures behind a line,** where you keep them: orders and average order value, hours and rate, budget and actual. Optional.
- **Your settings:** who reads it and when, and the size of movement worth explaining.

It works from files you supply. No connection to your accounting system is needed, and none is asked for.

## What comes out

One commentary in a fixed order:

1. **The picture.** Revenue, costs and the result against budget, and how many lines are explained, confirmed and still open.
2. **The tie-out.** Proof that the lines add to the export's totals before a word is written.
3. **Commentary by line,** largest movement first: the figures, the explanation and its label, any arithmetic split, and what the owner expects for the rest of the year.
4. **Other lines.** Everything under the threshold, counted and listed with its figures.
5. **The bridge** from the budgeted result to the actual one.
6. **Questions for budget owners,** one per line that still needs an answer.
7. **Checks for the finance lead:** notes that disagree with the figures, lines with no budget, explanations offered by someone other than the owner.

Good looks like this: every figure traces to the export, every explanation traces to a dated note, and the bridge lands exactly on the actual result.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which owns the budget and reports against it.
- [Analytics and reporting](https://fullypowered.ai/functions/analytics-and-reporting/), where the monthly management pack is assembled.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where partners want to know why fees and staff costs moved before the next month starts.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where materials, overtime and repairs move every month and each has an owner on the shop floor.
- [Nonprofits](https://fullypowered.ai/industries/nonprofits/), where boards and funders expect spending against budget to be explained line by line.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the budget is set every year and the explanations still live in a few people's heads.

## What has to change for your company

- **Your export.** The column names your accounting system produces, so the template reads them as they come.
- **Your threshold.** The amount and the percentage that make a line worth explaining, and the floor below which small lines are left alone.
- **Your owners.** Who owns each line, and who may confirm an explanation on behalf of a team.
- **Your comparison.** It compares with budget as written; add last year or a forecast if that is how you report.
- **Your figures.** The order counts, hours or volumes you keep for your biggest lines, so more of them can be split.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini. Decide which files the assistant may read and where the approved commentary is kept.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 9 November 2026. It was tried on its invented example on 9 November 2026; the record is published with it, and lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three past months your finance lead remembers well, with hard cases written in advance: an export that does not tie, a line with no note, an explanation offered by someone other than the owner, a note that says under budget on a line that is over. The finance lead checks every figure against the export before anyone relies on the commentary. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Month-end close checklist](../month-end-close-checklist/)
- [Weekly receivables summary](../weekly-receivables-summary/)
- [Supplier bill review and payment-run preparation](../supplier-bill-review-and-payment-run-preparation/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
