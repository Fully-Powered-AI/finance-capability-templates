# Receivables exception review

The controller gets every short payment, unmatched or ambiguous receipt, possible duplicate and disputed invoice on one list, each with its evidence and a proposed next step, before anything is applied on a guess.

*Workflow template · Finance and accounting · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/receivables-exception-review/)*

## The outcome

Most receipts match themselves. The few that do not are where the controller’s week goes: the check that is \$200 short, the wire with no reference, the payment from a client with nothing open. This workflow template puts all of them on one list after matching, with the evidence gathered and a proposed next step for each.

The controller spends the review deciding. The billing coordinator leaves with the exact questions to send. Unapplied cash stops drifting into month end. The list never applies a receipt, writes off a difference or issues a credit; people the firm names take those actions.

## Who starts the work, and when

The billing coordinator runs it once provisional matching is done and the clean matches are posted, each week and again before close. The controller reviews the list and decides each item. Account leads join on items that depend on what a client said.

## What they supply

- The receipts log, with remittance details and bank references.
- The provisional match results: matched, short, ambiguous or unmatched.
- The ledger or aging export after posting, plus 30 days of postings for the duplicate check.
- Each account lead’s notes and client correspondence: promises, queries, disputes and agreed discounts.
- The firm’s rules for short payments, disputes and write-offs.

## What comes out

An exception list for the controller. Each item gives the amounts, the evidence, the possible explanations, a proposed next step and who decides. It closes with the checks that found nothing and what could not be assessed.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Professional services](https://fullypowered.ai/industries/professional-services/), where retainers and partial payments are routine and the account lead often holds the explanation.
- [Law firms](https://fullypowered.ai/industries/law-firms/), where one payment can cover several matters and billing needs the responsible attorney’s notes.
- [Engineering firms](https://fullypowered.ai/industries/engineering-firms/), where retainage produces expected short payments that must stay apart from unexpected ones.
- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which owns cash application and the close.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the same awkward items return every month.
- [Acquisitions & integration](https://fullypowered.ai/situations/acquisitions-and-integration/), where two ledgers send more receipts that match neither cleanly.

## What has to change for your company

Your controller sets the rules: how a short payment is applied when the remittance names the invoice, the write-off amount the controller may approve, and how long unapplied cash may sit before it goes to the finance lead. Account leads record promises and disputes in one place the assistant can read. The assistant gets read-only exports and no access to post.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 9 November 2026. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on a past month whose answers your controller already knows, with cases written in advance: a short payment, a receipt that fits two invoices, a disputed invoice, a duplicate and a missing account note. The controller compares each list with what was actually decided before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 9 November 2026.
- Package format checked by script on every release.
- Not yet tried on its example in a named AI product.
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the workflow template drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related workflow templates

- [Overdue-invoice follow-up preparation](../overdue-invoice-follow-up-preparation/)
- [Weekly receivables summary](../weekly-receivables-summary/)
- [SOP exception capture](https://fullypowered.ai/workflows/sop-exception-capture/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
