# Bank reconciliation preparation

Before the month is signed off, your bookkeeper holds one bank reconciliation for one account: every statement line matched to the books or explained, every open item aged, a proof that the two balances agree, and the entries still to make. Nothing is posted until a person approves.

*Workflow template · Finance and accounting · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/bank-reconciliation-preparation/)*

## The outcome

A bank reconciliation is where the books meet an outside record they cannot argue with. Your bookkeeper starts the review with the matching already done: each statement line paired with its entry in the books, or set apart with the reason it has no partner.

What is left is short and specific. Checks written and not yet cashed, deposits not yet on the statement, fees and interest the books do not show yet, an amount keyed wrongly, a supplier who seems to have been paid twice. Each one carries its age, so the deposit that should have reached the bank a week ago stands out from the one made yesterday.

The sheet ends with a proof: the statement balance and the ledger balance, each adjusted for the open items, side by side. Either they agree to the cent or the gap is shown in plain figures. Nothing is ever added to make it come out at zero.

The workflow template prepares and checks. Your bookkeeper decides how each entry is coded, a reviewer signs, and a person posts the entries in the accounting system.

## Who starts the work, and when

The bookkeeper or staff accountant starts it each month, as soon as the bank statement for the month is available and the books are up to date for the period. Many businesses run it again mid-month for a busy account. One run covers one bank account for one statement period.

The controller, the owner or the outside accountant reviews the result and signs it off. Whoever knows the answer to each open question, such as the person who banks the shop's cash, gets that question by name.

## What they supply

- **The bank statement export** for the account and the month, with the opening and closing balances from the statement.
- **The ledger export:** the same account's register from the accounting system for the same dates, with its opening and closing balances.
- **Last month's open items:** the checks, deposits and other items the previous reconciliation left outstanding.
- **A few settings:** who runs it, who reviews it, the bank's working days, and how wide a date gap still counts as a match.

Two files and a short list are enough. It needs no connection to your bank or your accounting system, and it never asks for a password or a login code.

## What comes out

One reconciliation sheet, in a fixed order:

1. **The result.** Whether the proof agrees, how many items are open and how many need attention.
2. **The balances.** Each export added up and checked against its own opening and closing figures, so nothing is matched from a file that is missing rows.
3. **The proof.** Both adjusted balances and the difference between them.
4. **What matched,** pair by pair, with each side's own wording and how many days apart they were.
5. **What is open,** by kind: checks not yet cashed, deposits in transit, items on the statement that are not in the books, amounts that differ, and lines that could belong to more than one partner.
6. **Last month's items,** each one cleared with its date or still open and older.
7. **Ageing and flags,** then **the entries to prepare** for approval, **the questions** for each person, and a sign-off line for the reviewer.

A good sheet lets the reviewer trace every figure to a row in one of the two exports and see every open item with its reason.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which owns the reconciliation and the close it feeds.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where client payments arrive by every route and each one has to land against the right deposit.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where card settlements, fees and refunds fill the statement every week.
- [Hospitality](https://fullypowered.ai/industries/hospitality/), where cash takings, card batches and supplier debits all run through one account.
- [Construction](https://fullypowered.ai/industries/construction/), where large supplier payments and progress receipts make a single keying error expensive.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the reconciliation has always lived with one careful person and should be repeatable by anyone.

## What has to change for your company

- **Your exports.** The column names your bank and your accounting system produce, so the template reads them as they come. If a heading does not match, it stops and asks rather than guessing.
- **Your matching window.** How many business days apart two dates may be and still count as the same transaction.
- **Your limits.** How many business days a deposit may take to reach the statement before it is flagged, and how old an uncashed check may get before someone decides what to do with it.
- **Your roles.** Who prepares, who reviews and signs, who codes and posts entries, and who answers questions about cash, cards and suppliers.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply. Decide which exports the assistant may read and where signed reconciliations are kept.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 9 November 2026. It was tried on its invented example on 9 November 2026 in one run; the record is published with it, and lists the small edits made afterward that have not been run again. That run did not reach the stop conditions or the path where the proof does not agree. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three past months your bookkeeper has already reconciled by hand, plus hard cases written in advance, each with the expected result: an export with a missing row, a check entered at the wrong amount, a supplier debited twice, a deposit that never reached the bank, a heading the template does not recognize. The reviewer compares every figure with the signed reconciliation before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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
- [Supplier bill review and payment-run preparation](../supplier-bill-review-and-payment-run-preparation/)
- [Receivables exception review](../receivables-exception-review/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
