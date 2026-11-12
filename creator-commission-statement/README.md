# Creator commission statement

Each month, the finance lead gets a draft statement of what every creator has earned, worked from the store's orders export: commission under the programme's rules, flat fees, amounts carried under the minimum, and a payout list. A person approves it; finance pays.

*Workflow template · Finance and accounting · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/creator-commission-statement/)*

## The outcome

Creator payouts stop being a spreadsheet argument. Every order in the month lands in exactly one place: credited to a creator, set aside by a named rule, or listed as a code nobody owns. Every creator's figure can be traced back to order numbers in the export, and the order count at the bottom proves nothing slipped through.

The questions that usually surface after money has moved are on the page before it does: a code that belongs to a creator who has left, an order that carries two creators' codes, a refund inside the holdback, a creator buying with their own code, a platform figure that does not match. Each one is written as an item for a named person, with the facts beside it.

The workflow template prepares the statement. The approver approves it, and finance makes the payments.

## Who starts the work, and when

The finance lead, the bookkeeper or the programme lead starts it once a month for each creator programme, after the month has ended. An early run gives a preview while refunds can still come in; the run that finance pays from comes on or after the day the holdback closes.

The programme owner, usually the business owner or the head of marketing, approves the statement before anything is paid.

## What they supply

- **The programme rules.** The default commission rate, what the commission is calculated on, how partial refunds are treated, the holdback in days, the minimum payout, and the store's own promotion codes.
- **The creator list.** Each creator's status, deal, rate, flat fee, codes, start date and whether they are paid by you or by a creator platform.
- **The orders export** for every day of the month, straight from the store.
- **Where needed:** the orders credited to tracked links, the deliverables accepted for flat-fee deals, last month's carried amounts, and the platform's own commission figures.

No connection to the store, the platform or the bank is needed, and none is asked for.

## What comes out

One draft statement in a fixed order:

1. **The outcome:** final, preview or partial, and the rules that were applied.
2. **Per creator:** orders, exclusions, the basis, the rate, commission, flat fees, carried amounts and the total due.
3. **The payout list,** with only the creators who are fully assessed and over the minimum.
4. **Exclusions by rule,** pending orders, and everything that needs a person.
5. **Codes nobody owns,** for the programme lead.
6. **The platform check,** for creators a platform pays directly.
7. **The order check and coverage:** every order accounted for, and exactly what the inputs did not allow it to check.

Good looks like this: finance can recompute any creator's figure from the order numbers on the page, and nobody is paid on a guess.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which pays creators and needs a statement it can check.
- [Marketing and content](https://fullypowered.ai/functions/marketing-and-content/), which runs the creator programme and owns its codes and links.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where creator codes and affiliate links drive a share of online orders.
- [Consumer brands](https://fullypowered.ai/industries/consumer-brands/), where creator programmes grow faster than the process for paying them.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when a handful of creators becomes dozens and payouts can no longer be worked out by hand.

## What has to change for your company

- **Your rules.** Your commission rate, what it is calculated on, how refunds are treated, how long orders wait before they count, and the minimum payout.
- **Your creator list.** The deals you offer, and which creators you pay yourselves and which a platform pays.
- **Your exports.** The column names your store produces, if they differ from the defaults.
- **Your roles.** Who approves the statement, who pays, and who answers for codes and links.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini. Decide which exports the assistant may read.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 9 November 2026. It was tried on its invented example in Claude on 9 November 2026, and the record of that run is published with the template; it lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three past months your finance lead has already paid, with hard cases written in advance: a partial refund, an order before a creator's start date, a code belonging to a creator who has left, an order with two creators' codes, a month where a creator falls below the minimum. Finance checks every figure against the export before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Supplier bill review and payment-run preparation](../supplier-bill-review-and-payment-run-preparation/)
- [Weekly receivables summary](../weekly-receivables-summary/)
- [Month-end close checklist](../month-end-close-checklist/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
