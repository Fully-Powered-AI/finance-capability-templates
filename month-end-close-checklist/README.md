# Month-end close checklist

Before the month ends, your controller holds the whole close on one page: every task with its owner, its date and what it waits on, the chain that sets the close date, and each gap already written as a question. Entries are prepared for approval, never posted.

*Capability template · Finance and accounting · version 0.1.0 · [Capabilities Directory](https://fullypowered.ai/capabilities/month-end-close-checklist/)*

## The outcome

The close starts with a plan instead of a memory. Every task has a named owner and a real date, counted in your working days and skipping the days your office is closed. The page shows which tasks set the close date, so everyone knows where a late afternoon costs a whole day.

The problems that usually surface on day three are on the page before day one: a task nobody owns, an owner who is away on the due date, a reconciliation scheduled ahead of the entries it needs, a person reviewing their own work. Each arrives as a question for the controller, with the facts beside it.

Your accounting team still does the accounting. The checklist says who prepares each entry, who approves it and who posts it. The AI assistant posts nothing, assigns nothing and locks nothing.

## Who starts the work, and when

The controller, the bookkeeper or the firm administrator starts it two or three working days before the month ends, in time to send the cut-off reminder. It runs again when something changes: an owner is away, a task is added, the target date moves. During the close, the same person can run it with each task's status to see what is late and what is waiting.

The controller approves the checklist before it is shared with the team.

## What they supply

- **Your close task list.** Last month's checklist or the standing list: each task, the working day it falls on, its owner, what it waits on and who reviews it.
- **The calendar.** The period end, the date the books must be locked, and the days your office is closed.
- **Who is away.** Any owner or reviewer absent during the close.
- **This month's notes.** One-off items, such as an invoice that has not arrived, and anything left open from last month.
- **Statuses,** only when it is run during the close.

## What comes out

One checklist in date order. Each task carries its number, owner, due date, the tasks it waits on, its reviewer and a status. Tasks with a problem are flagged where they stand; none is silently moved or reassigned.

Under the tasks: the decisions the controller has to make before the close starts, the chain of tasks that sets the close date and how many spare days it has, the entries to be prepared with who approves and who posts each, and the items carried from last month with the task that picks each up.

A good checklist can be checked against a wall calendar in two minutes, and nobody on the team is surprised by their name.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Finance and accounting](https://fullypowered.ai/functions/finance-and-accounting/), which owns the close and the statements that follow it.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where the close waits on time entry and billing, and partners want the numbers on a fixed day.
- [Law firms](https://fullypowered.ai/industries/law-firms/), where the firm administrator runs the close around the partners' meeting.
- [Engineering firms](https://fullypowered.ai/industries/engineering-firms/), where unbilled work on projects has to be counted before the statements mean anything.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the close lives in one long-serving person's head and should live on a page.

## What has to change for your company

Start from your own task list; the capability adds no accounting tasks of its own. Decide how you count days: which day is day one, and which days the office is closed. Name who approves entries, who posts them and who locks the month, and decide whether anyone may review their own work. Set the target date and who must have the statements by when. Agree where the approved checklist lives and how the team marks a task done. It runs in ChatGPT, Claude, Copilot or Gemini, from files and notes you supply; it needs no connection to your accounting system.

## What has been checked

Fully Powered AI wrote this capability template. It was editorially reviewed on 9 November 2026. It was tried on its invented example on 9 November 2026 in two runs; the record of the second is published with it, and lists the small edits made afterward that have not been run again. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three past months your controller remembers well, plus hard cases written in advance, each with its expected behavior: a month that ends on a weekend, an office closure inside the close, a task with no owner, a reconciliation listed before the entries it needs. The controller checks every date against the calendar before anyone relies on it. [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/) builds that test set, and [What we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) shows the record.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 9 November 2026.
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

- [Weekly receivables summary](../weekly-receivables-summary/)
- [Receivables exception review](../receivables-exception-review/)
- [Pilot acceptance-test preparation](https://fullypowered.ai/capabilities/pilot-acceptance-test-preparation/)

## Make it yours

This is the starting version. Fully Powered AI adapts capabilities to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
