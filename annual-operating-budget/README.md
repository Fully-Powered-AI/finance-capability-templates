# Annual operating budget

For an owner or finance lead preparing next year: revenue and costs by month and by team, built from this year's figures and each budget owner's drivers, every assumption written down, capital purchases listed apart, the whole checked against cash, and the questions leadership has to settle.

*Workflow template · Finance and accounting · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/annual-operating-budget/)*

## The outcome

Next year's budget arrives as one coherent draft instead of a stack of spreadsheets from every team. Each line shows this year's figure, next year's, the change, and how the owner got there: the orders and prices behind sales, the share of sales behind materials, the monthly charge behind rent. Where the arithmetic an owner gives does not produce the figure they sent, the draft says so and keeps their figure until they answer.

The budget is laid out month by month and team by team, with people costs taken straight from your headcount plan. Equipment, vehicles and other capital purchases sit on their own list, outside running costs, so the result is not distorted and the cash is still counted.

Then the test that matters: can the company afford it? A month-by-month cash check shows the lowest point of the year and every month that falls below the minimum leadership has set, and runs again with revenue lower than budgeted. Every gap to a target, every month short of cash and every capital purchase arrives as a question for leadership, with the facts beside it. Leadership sets the targets and approves the budget; the draft changes no one's figures to make them fit.

## Who starts the work, and when

The finance lead starts it a few months before the budget year begins, once the budget owners have sent their figures and the headcount plan is ready; in a smaller company, the owner does. It runs again after each round of revisions, as owners answer their questions and resubmit, until leadership approves the budget. The finance lead reviews every draft before it reaches leadership.

## What they supply

- **Settings.** The budget year, who the budget is for and when they meet, the size of change worth questioning, the capitalisation limit, how long customers take to pay, opening cash, and whether a missing line may be carried at this year's figure.
- **Leadership's targets.** Revenue, result and the minimum cash balance.
- **This year's figures,** by team and line, as a simple table with stated column headers.
- **Each budget owner's submission:** next year's figure for every line, the driver behind it, how it falls across the months and the reason for any big change.
- **The headcount plan,** people costs by team and month. [Headcount plan](https://fullypowered.ai/workflows/headcount-plan/) prepares it.
- **The capital purchases list,** and any loan repayments, tax payments or other cash movements that are not running costs.

It works from files you supply. No connection to your accounting system or bank is needed, and none is asked for.

## What comes out

One draft budget in a fixed order:

1. **The picture.** Revenue, costs and the result against this year and against target, capital purchases, and cash at its lowest point, in the budget and in the lower-revenue case.
2. **The tie-out.** Proof that this year's figures and the headcount plan add up before anything is built, and that every view of the budget agrees.
3. **The budget by team,** line by line, with each driver recomputed and each flag in place.
4. **The budget by month,** and costs by team by month.
5. **The largest changes from this year,** with the reason each owner gave.
6. **Capital purchases,** month by month, outside costs.
7. **The cash check,** month by month, with the months below the minimum marked.
8. **Every assumption,** with who made it.
9. **Questions for budget owners,** and **open questions for leadership.**
10. **Checks for the finance lead:** missing submissions, drivers that do not match, changes with no reason, flagged capital items.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which runs the budget and owns the figures it is built from.
- [Leadership](https://fullypowered.ai/functions/leadership/), where the targets are set, the gaps are settled and the budget is approved.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where fees depend on people and a hire in March changes the whole year.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where materials follow sales and one machine purchase can take cash below the line.
- [Ecommerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where sales are seasonal and the months matter as much as the total.
- [Nonprofits](https://fullypowered.ai/industries/nonprofits/), where the board approves a budget every year and expects every figure to have its reason.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the budget is rebuilt every year from last year's spreadsheet and the reasons live in a few heads.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when new people, new equipment and slower-paying customers make cash the question before profit is.

## What has to change for your company

- **Your form.** The teams, lines and column headers your budget form and accounting system use.
- **Your limits.** The size of change worth questioning, the capitalisation limit, and how far below budget the lower-revenue case should go.
- **Your cash rules.** How long customers take to pay, and which loan, tax and owner payments belong in the cash check.
- **Your owners.** Who owns each line, and whether a missing line may be carried at this year's figure or must be submitted.
- **Your result.** Whether you report before depreciation, as written, or after it.
- **Your approvals.** Who sets the targets, who approves the budget and who approves each capital purchase.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini. Decide which files the assistant may read and where the approved budget is kept.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example in Claude on 10 November 2026; the record of that run is published with it, lists the ambiguities it met, and lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on last year's budget round, which your finance lead remembers well, with hard cases written in advance: figures that do not add up, a driver that does not produce the owner's figure, a missing submission, a big change with no reason, a purchase that takes cash below the minimum. The finance lead checks every figure against the submissions before anyone relies on the draft. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 10 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 10 November 2026. The record is in [TRIAL.md](TRIAL.md).
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

- [Headcount plan](https://fullypowered.ai/workflow templates/headcount-plan/)
- [Thirteen-week cash flow forecast](../thirteen-week-cash-flow-forecast/)
- [Budget-versus-actual variance commentary](../budget-versus-actual-variance-commentary/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
