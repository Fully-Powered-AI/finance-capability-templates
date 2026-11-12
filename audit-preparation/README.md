# Audit preparation

Before the external auditors arrive, your controller holds one audit pack: every request with its owner, date, document and status, the control evidence they will test, last year's findings and what was done, and draft answers to the questions they will ask. People approve everything before it goes.

*Workflow template · Finance and accounting · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflow templates/audit-preparation/)*

## The outcome

Audit season stops being a scramble. The auditors' request list becomes a tracker the whole finance team can work from: each item has a named owner, the date the auditors want it, an earlier date of your own so there is time to check it, the document that answers it, and where it stands. Anything late, unowned or sent without an approval stands out on the first page.

The pack also looks where auditors look. It lists the controls they will test and the evidence each one leaves, shows where one person approves, records, handles the money and checks in the same process, and picks out payments at or above your approval limit that lack a proper approval. Last year's findings sit beside what was done about each, so a finding marked done with nothing to show for it is caught now, not in the closing meeting.

Then the questions. Balances that moved enough to draw a question are listed with your own explanation, or with a question for you where there is none. Expected questions get draft answers built only from the facts you supply, each naming its source. Questions on legal claims, tax positions, suspected fraud or whether the business can keep operating go to the person you name, to answer with your advisers.

The workflow template prepares and checks. Your team prepares the documents, a named person approves each item and each answer, and a person sends them to the auditors.

## Who starts the work, and when

The controller, the bookkeeper or the finance manager starts it the day the auditors' request list arrives, usually a few weeks before fieldwork. It runs again each week with updated statuses until the auditors are on site, and whenever they add a request or a question.

The controller approves the pack and settles every decision in it. Each item's owner sees their own lines; the named approver signs off each item and answer before it goes.

## What they supply

- **The auditors' request list,** as they sent it.
- **Your owner and status list:** who prepares each item, where it stands, the document and who approved it.
- **Last year's request list and findings,** to see what is new and what was promised.
- **Your controls and who does what** in each process, such as supplier payments, payroll and journals.
- **A payments export** for a period you choose, with who entered and who approved each payment.
- **The trial balance against last year,** with your notes on the big movements.
- **The questions you expect,** with the facts you already know.
- **A few settings:** your dates, who approves what, your approval limit and the movement size worth explaining.

Only the request list is required; each further file adds a section. It works from exports and notes you supply, needs no connection to your accounting system, bank or the auditors' portal, and never asks for a password or a login code.

## What comes out

One pack in a fixed order: a summary of where the requests stand; the tracker grouped by area; what changed from last year's list; the control evidence; who does what; the payments check; last year's findings; the movements the auditors will ask about; the draft answers; and a numbered list of decisions and questions, each for a named person.

A good pack lets the controller walk into the planning call knowing what is late, what is missing, and what the auditors are likely to raise, with every point traced to a line in one of your own files.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which owns the audit and every schedule handed over.
- [Compliance, risk and privacy](https://fullypowered.ai/functions/compliance-risk-and-privacy/), where the controls and their evidence are kept in order between audits.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where inventory counts, equipment and lender covenants make the audit request list long.
- [Construction](https://fullypowered.ai/industries/construction/), where sureties and lenders often ask for audited statements each year.
- [Nonprofits](https://fullypowered.ai/industries/nonprofits/), where funders and boards often expect an annual audit from a small finance team.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where unbilled work and receivables draw the auditors' first questions.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where audit preparation lives in one long-serving person's memory and should live in a pack.
- [Private equity & portfolios](https://fullypowered.ai/situations/private-equity-and-portfolios/), where a portfolio company faces its first full audit under new owners.

## What has to change for your company

- **Your exports.** The column headings your auditors and your systems use, so the template reads them as they come. If a heading does not match, it stops and asks rather than guessing.
- **Your dates.** How many working days ahead of the auditors' dates your own dates fall, and the days your office is closed.
- **Your limits.** Your payment approval limit, and the size of movement worth explaining, agreed with your auditors.
- **Your approvers.** Who approves each item before it goes, who approves the items the controller owns, and who answers questions on legal, tax and other sensitive matters with your advisers.
- **Your platform.** It runs in ChatGPT, Claude, Copilot or Gemini, from files you supply. Decide which exports the assistant may read and where approved items are kept.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 10 November 2026. It was tried on its invented example on 10 November 2026 in one run; the record of that run is published with it, and lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on last year's audit, which your controller remembers well, plus hard cases written in advance, each with the expected result: an item with no owner, an item marked sent with no approval, a payment approved by the person who entered it, a finding marked done with no evidence, a heading the template does not recognize. The controller checks every date and figure before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) sets those cases up, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Month-end close checklist](../month-end-close-checklist/)
- [Bank reconciliation preparation](../bank-reconciliation-preparation/)
- [Budget-versus-actual variance commentary](../budget-versus-actual-variance-commentary/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
