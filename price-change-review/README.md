# Price change review

Before prices change, the owner or finance lead gets one review: the margin on each product or service from the sales and cost exports, how costs have moved, what each proposed price does to sales and gross profit across a stated range of customer responses, and dated competitor prices. It recommends no price.

*Workflow template · Finance and accounting · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/price-change-review/)*

## The outcome

The price decision is made with the numbers in front of you instead of a feeling that costs have gone up. Every product or service shows what it earns on each sale at today's cost, and how many points of margin the cost rises since the start of the period have taken away.

Each proposed price is worked through at the customer responses you choose to test, from no change in units to the fall you are worried about. For every item the review shows how far units could drop before the new price leaves you with less gross profit than today. Competitors' public prices sit beside the proposal, each with the date and place it was seen, so a price from last spring cannot pass for this week's.

The review recommends no price. You read it and decide. Nothing on the price list, the website or the till changes until a person changes it.

## Who starts the work, and when

The owner, the finance lead or the bookkeeper runs it when costs have moved and a price rise is on the table, ahead of an annual price review, or before a new price list goes to customers. It runs again whenever the owner wants to try a different proposal or a different range of customer responses.

The owner, or whoever sets prices, reads the review and makes the call.

## What they supply

- **A sales export** for a stated period, usually the last twelve months: units sold and net sales for each product or service, after discounts and refunds.
- **A cost export:** each item's unit cost on dated rows, ideally one from the start of the period and one from today. For a service, count the hours each unit takes at a rate you set, your own hours included.
- **The proposed changes:** each item's current list price and the price being considered.
- **The range to test:** the changes in units sold you want worked through, such as no change, 5% fewer and 10% fewer.
- **Competitors' public prices,** each with the date and place it was seen. Optional.
- **Earlier price changes,** with units sold before and after. Optional.
- **Prices agreed with customers** that hold until a set date. Optional.

It works from the files you supply. No connection to your accounting system, shop platform or till is needed, and it never asks for a password.

## What comes out

One review in a fixed order:

1. **The picture.** Today's sales and gross profit at today's costs, and the totals at each customer response you chose.
2. **Margin by item.** Units, net sales, the price customers actually paid against the list price, today's unit cost, the margin and the gross profit, with any item under your margin floor marked.
3. **How costs have moved.** Each item's cost at the start and today, and the points of margin lost at the price customers are paying.
4. **The proposed changes.** For each item, the new price and margin, then units, sales and gross profit at each response, and the fall in units at which gross profit drops back to today's.
5. **Competitors' public prices,** dated, with old ones set aside, and where each proposed price sits against the in-date ones.
6. **Earlier price changes,** shown as single observations.
7. **Price commitments, data notes and questions for the owner.**

Good looks like this: every figure traces to a row in an export, every competitor price carries a date, and nowhere does the review say what the price should be.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which owns the cost figures and the margin.
- [Sales](https://fullypowered.ai/functions/sales/), which keeps the price list and hears first how customers respond.
- [Ecommerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where supplier costs move several times a year and a shelf of products needs repricing at once.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where materials and energy costs feed straight into the price of every product.
- [Hospitality](https://fullypowered.ai/industries/hospitality/), where food, drink and wage costs rise ahead of the menu.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where hourly and fixed-fee rates lag behind the cost of the people delivering them.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where prices have stood for years and nobody remembers the margin they were set to earn.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), where a growing range makes it easy for a few items to slip below cost without anyone noticing.

## What has to change for your company

- **Your exports.** The column names your accounting system, shop platform or till produces, so the template reads them as they come.
- **Your period.** Twelve months is the default; use a shorter one if prices or the range changed recently.
- **Your range.** The customer responses worth testing for your trade, and whether some items deserve a run of their own.
- **Your cost.** What counts in a unit cost for you: materials, packaging, freight in, direct time.
- **Your limits.** Your margin floor, and how old a competitor's price can be before it is set aside.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini. Decide which files the assistant may read and where the review is kept.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example on 10 November 2026; the record is published with it, and lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past price change your owner remembers well, with hard cases written in advance: an export whose headers do not match, an item with a cost of zero, a competitor price with no date, a proposed price below today's cost. The person who keeps the books checks every figure against the exports before anyone relies on the review. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Discount request review](https://fullypowered.ai/workflows/discount-request-review/)
- [Competitor profile from public pages](https://fullypowered.ai/workflows/competitor-profile-from-public-pages/)
- [Slow-moving stock and markdown plan](https://fullypowered.ai/workflows/slow-moving-stock-and-markdown-plan/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
