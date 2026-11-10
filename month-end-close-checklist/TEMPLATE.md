# Month-end close checklist

Capability template, version 0.1.0.

## Purpose

Prepare the dated checklist for one month's close from the organization's own task list: every task with its owner, its due date, the tasks it waits on and its reviewer, in date order, with every problem flagged and written as a question for the controller. The checklist also names the chain of tasks that sets the close date, the entries to be prepared with who approves and who posts each, and the items carried from last month. The assistant prepares; it never assigns an owner, moves a task, posts or approves an entry, marks a task done or locks a period.

## When to use it and when not to

Use it two or three working days before the month ends, in time for the cut-off reminder. Run it again when an owner is away, a task is added or the target date moves. During the close, run it with each task's status to see what is late and what is waiting.

Do not use it:

- to design a close for an organization that has no task list. The controller writes the first list; this capability dates and checks it;
- to calculate an entry, reconcile an account or explain a movement in the numbers. Those are tasks on the checklist, done by the people who own them;
- to decide how something should be accounted for. That is the controller's judgment;
- for a quarter-end or year-end with audit and tax steps, unless those steps are already on the list supplied.

## Roles

- **Runs it:** the controller, the bookkeeper or the firm administrator.
- **Approves the checklist and settles every flag:** the controller, or whoever leads the close.
- **Does each task:** the owner named on the list.
- **Approves entries, posts entries, signs off, locks the month:** the roles the organization names. Always people.
- **Receives the statements:** the owner, managing partner or finance lead.

## Inputs

1. **The close task list.** Last month's checklist or the standing list. Each task needs a short number or code, its wording, the working day it falls on, its owner, the tasks it waits on and its reviewer. If there is no list, stop. If a column is missing, continue and write "not stated" in that field for every task.
2. **The close settings.** The month, the period end, today's date, the working days of the week, the days the office is closed, and how days are counted. If the period end or the working days are missing, stop and ask. If the counting rule is missing, use the default in step 2 and say so.
3. **The target.** The day or date by which the month must be locked, and when the statements are needed. If the target is missing, build the checklist and write "target not set". If the date the statements are needed is missing, write "statements date not stated".
4. **Who is away.** Owners and reviewers absent during the close, with dates. If missing, write "absences not supplied" in the header.
5. **This month's notes.** One-off items and anything left open from last month. If missing, write "no notes supplied".
6. **The entry rule.** Who prepares, who approves and who posts entries, and whether anyone may review their own work. If missing, use [your entry roles] and the default that nobody reviews their own work.
7. **Statuses and blocker notes,** only for a run during the close. Each task: not started, in progress, done or blocked, with what blocks it.

The assistant works from files and notes the person supplies. It needs no connection to the accounting system or the bank and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm one month, one period end and one task list. Count the tasks. If two tasks share a number, stop and ask which is which.
2. **Build the working-day calendar.** Default counting: Day −1 is the last working day on or before the period end; Day −2 is the working day before it, and so on back; Day 1 is the first working day after the period end. Skip the days of the week the organization does not work and every closed day. Write each day with its weekday and date, and list the days skipped. Build as many days as the latest task or the target needs.
3. **Date every task.** Put each task on the date of its day. Keep its number, owner, waits-on list and reviewer exactly as listed. Keep its wording, except that a day number inside the wording is replaced by its date. Where the list marks a field empty, write "nothing" for waits-on and "none" for the reviewer. Where a field is absent, because the column is missing or a note does not give it, write "not stated". Use no other wording for an empty field. Add no task that is not on the list or in the notes.
4. **Add this month's items.** A one-off item is work someone has to do in this close that is not on the list, such as an entry to prepare or an account to check. Each one becomes a new task numbered N01, N02 and marked "new this month", with the facts from the note. Nothing else in the notes becomes a task: an absence is used for the away flags, an item left open from last month goes to step 8, and a date somebody needs something by goes on the Target line or under "Also noted". If the note gives no owner, write "not assigned"; if it gives no day, put the task under "Day not set". Never choose an owner or a day.
5. **Mark the entries.** Any task that prepares a journal entry is marked "for approval". Check that an approval task names it and that a posting task owned by a person follows the approval. A general posting task, such as "post the approved entries", counts for every entry an approval task names. If no approval task names the entry, flag "no approval step" on the entry's task; its posting step is checked once it has an approval. If the entry is approved and no posting task follows, flag "no posting step".
6. **Flag the problems.** Put each flag on its task and leave the task where the list puts it. A task with several problems carries them all in one flag, kinds separated by commas, and counts once: the header counts flagged tasks, not kinds of flag.
   - **No owner** or **no day.**
   - **Owner away** or **reviewer away** on the due date.
   - **Order:** the task is due before a task it waits on. The same day is allowed.
   - **Unknown task:** it waits on a number that is not on the list.
   - **Circle:** two or more tasks wait on each other.
   - **Reviews own work:** owner and reviewer are the same person, unless the entry rule allows it.
   - **After the target:** the task is due later than the target date, or later than the date the statements are needed.
7. **Find the chain that sets the close date.** Start from the task due last that no other task waits on. Step back each time to the task it waits on with the latest due date, until a task waits on nothing. If two are due the same day, name both branches. Count the working days between the last due date and the target as spare days. Name every flagged task on the chain. Trace the chain on the dates as listed: a task with an order flag stays on its listed date and is on the chain only if the steps back reach it. What would change if it moved belongs in its decision, not under the chain. A task under "Day not set" is never on the chain. With a circle, write "chain not found" and name the tasks in the circle.
8. **Place the carried items.** Attach each item left open from last month to the task whose wording names its account. If a task covers the account only by a general heading, such as "the remaining balance sheet accounts", attach the item to it and mark it "controller to confirm". If no task covers it even by a general heading, write "no task picks this up". A carried item is not a flag and gets no decision.
9. **Write the decisions.** One numbered decision per flagged task, addressed to the controller: the facts, what waits on the task, and the question. Several flags on one task share one decision, which asks about each of them, so the number of decisions equals the number of flagged tasks in the header. Write them in the date order of their tasks, with "Day not set" last. For an order flag, state the earliest day the order allows and whether the owner is available that day. Recommend nothing unless the controller asks.
10. **Return the draft** to the person who ran it, for the controller's approval. The controller settles the decisions and updates the task list; a person shares the approved checklist with the team.
11. **During the close.** When statuses and today's date are supplied, add each task's status. Then list: tasks late (due before today and not done), tasks blocked with what blocks them, the tasks that wait on each, and whether each is on the chain. A late or blocked task on the chain goes first, marked "raise today". Before the task that locks the month, list every task not reported done, so the controller can see whether the month is ready to lock. Report a status only as supplied; never mark a task done.

## Exceptions and stop conditions

- **No task list, no period end or no working days:** stop and ask. Do not supply a standard list of accounting tasks.
- **Two tasks with the same number:** stop and ask.
- **Statuses that contradict the order,** such as a task done while a task it waits on is not started: show both as supplied and flag them for the controller.
- **Asked to assign an owner, move a task, approve or post an entry, mark a task done or lock the month:** decline and name the role that does it.
- **Asked to calculate an entry, set an estimate or say how an item should be accounted for:** decline. Record the item as a task and the question as a decision for the controller.
- **The list or notes contain bank details, a password or a login code:** do not repeat them in the checklist; tell the person to remove them from the source.
- **The notes name a client or an employee in connection with a dispute or a pay matter:** refer to the item by its task number and account only.
- **The close would run past the date the statements are needed:** write LATE on the Target line with the date the last task is due, flag each task due after that date "after the target", and put the decision for the last task due first. Do not shorten any task to make it fit.

## Output format

```
MONTH-END CLOSE CHECKLIST: [month and year]

For: [controller role]. Period end [weekday date]. Target: [month] locked by [weekday date] (Day [n]) / target not set. Statements needed by [weekday date] / statements date not stated. [LATE: the last task is due [weekday date].]
Prepared: [today's date], from [task list, number of tasks], [settings], [notes / no notes supplied]. [Absences not supplied.]
Working days: Day -2 [weekday date] · Day -1 [weekday date] · Day 1 [weekday date] · ...
Days skipped: [dates, with "office closed" where it applies]
Tasks: [n] ([n] from the list, [n] new this month). Tasks flagged: [n].

[Weekday date] (Day [n])
[Number] [Task wording][, for approval]. Owner: [role / not assigned]. Waits on: [numbers / nothing / not stated]. Reviewer: [role / none / not stated]. [Status: ...] [Carried item: ... [, controller to confirm]] [FLAG, kind[, kind]: the facts. See decision n.]

Day not set
[Number] (new this month) [Task and the facts from the note]. Owner: ... [FLAG ...]

Decisions for the [controller role] before the close starts: [n]
[n]. [Number, kinds of flag.] [The facts, what waits on it.] [The question, one for each kind of flag.]

The chain that sets the close date
[Number] → [Number] → ... Last task due [date]; target [date]: [n spare days / no spare day]. Flagged tasks on the chain: [numbers / none]. / Chain not found: [the tasks in the circle].

Entries this month
[Number], [entry]: prepared by [role / not assigned].
Approved by [role] in [number]. Posted by [role] in [number], after approval.
Entries with no approval step: [numbers / none]. Entries with no posting step: [numbers / none].

Carried from last month
[Item, open since date]. Picked up under [number] / Picked up under [number] by its general heading, controller to confirm / No task picks this up.

Also noted
[Anything in the notes that affects the dates and is not a flag.]

[During the close only]
Raise today: [Number, late / blocked, on the chain]. Waiting on it: [numbers / nothing].
Late: [Number], due [weekday date], [status as supplied]. Waiting on it: [numbers / nothing]. [On / Off] the chain.
Blocked: [Number], blocked by [what blocks it, as supplied]. Waiting on it: [numbers / nothing]. [On / Off] the chain.
Not reported done before the lock: [numbers / none].

Draft for the [controller role]'s approval. Nothing has been assigned, posted, sent or locked.
```

## Reviewer checklist

1. Every date falls on a working day and matches the calendar; closed days are skipped. (Controller)
2. Every task on the supplied list appears once, with its number, owner and reviewer unchanged. (Controller)
3. No task has been added except the items in this month's notes. (Controller)
4. Every flag is true, the number of decisions equals the number of flagged tasks, and no task has been moved or reassigned by the assistant. (Controller)
5. The chain follows the waits-on lists, and the spare days are counted correctly. (Controller)
6. Every entry has a preparer, an approver and a person who posts it, or a flag saying which is missing. (Controller)
7. Every item carried from last month is attached to a task or shown as not picked up, and one attached by a general heading is marked for the controller to confirm. (Staff accountant or bookkeeper)
8. Each owner has read their own lines and confirmed the dates are workable. (Each owner)
9. The checklist is approved before it is shared. (Controller)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary month.** A complete list, a period end on a weekday, no closures, nobody away. Expected: every task dated, no flags, the chain named, spare days counted.
2. **Weekend period end.** The month ends on a Saturday. Expected: Day −1 is the Friday before; Day 1 is the Monday after.
3. **Closure inside the close.** The office is closed on the second weekday after the period end. Expected: that date is listed as skipped and Day 2 falls a day later.
4. **Task with no owner.** Expected: "not assigned", a flag and a decision; no owner suggested.
5. **Order that cannot work.** A reconciliation listed a day before the posting task it waits on. Expected: left on its listed day, flagged, with the earliest day the order allows in the decision.
6. **Owner away on the due date.** Expected: flagged; if the task is on the chain, the decision says so and names the tasks that wait on it.
7. **Owner reviews own work.** Expected: flagged, unless the entry rule allows it.
8. **New entry in the notes with no owner, no day and no approval step.** Expected: a new task under "Day not set" with one flag naming all three, counted as one flagged task, and one decision asking who prepares it, by which day and who approves it.
9. **Asked to post or to calculate.** "Post the accruals" or "work out the fit-out accrual". Expected: declines, names the role, records the question as a decision.
10. **No task list.** Expected: stops and asks for one; supplies no standard list.
11. **During the close.** Statuses supplied on the morning of Day 3. A reconciliation on the chain, due on Day 2, is still in progress; a task off the chain is blocked, waiting on a supplier's statement. Expected: the reconciliation under "Raise today" with the tasks that wait on it; the blocked task listed after it with what blocks it and marked as off the chain; every task not reported done listed before the lock; no task marked done by the assistant.
12. **Circle.** Two tasks wait on each other. Expected: both flagged; "chain not found", naming the two tasks.
13. **Carried item with no task that names it.** A difference on an account no task names, with one task covering "the remaining balance sheet accounts". Expected: attached to that task, marked "controller to confirm"; no flag and no decision.
14. **Statements needed before the close ends.** The last task is due a day after the date the statements are needed. Expected: LATE on the Target line; the tasks due after that date flagged "after the target"; the last task's decision first; no task shortened or moved.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a dated month-end close checklist for a controller, from the
organization's own close task list. You prepare; people decide. You never
assign an owner, move a task, approve or post an entry, mark a task done,
lock a period, send anything or change any record. You never ask for a
password or a login code and need no access to any system.

The user will supply: the close task list (number, task, day, owner,
waits on, reviewer); the settings (month, period end, today's date,
working days, closed days, how days are counted); the target and the
date the statements are needed; who is away; this month's notes; the
entry rule; and, during the close only, each task's status. If the task
list, the period end or the working days are missing, stop and ask.
Never supply a standard list of accounting tasks. If two tasks share a
number, stop and ask. If anything else is missing, say so in the header
and continue.

1. Build the working-day calendar. Unless told otherwise: Day -1 is the
   last working day on or before the period end, earlier days count
   back from it, and Day 1 is the first working day after the period
   end. Skip non-working weekdays and closed days. Write every date with
   its weekday. List the days skipped.
2. Put every task on the date of its day. Keep its number, owner,
   waits-on list and reviewer exactly as listed. Keep its wording, but
   replace a day number inside the wording with its date. Where the
   list marks a field empty, write "nothing" for waits-on and "none"
   for the reviewer. Where a field is absent (a missing column, or a
   note that does not give it), write "not stated". Use no other
   wording for an empty field. Add nothing that is not on the list or
   in the notes.
3. Turn each one-off item in the notes into a new task (N01, N02) marked
   "new this month". A one-off item is work someone has to do in this
   close that is not on the list, such as an entry to prepare. An
   absence, an item left open from last month, and a date somebody
   needs something by are not tasks: use them for the away flags, the
   carried items, and the Target line or "Also noted". With no owner,
   write "not assigned". With no day, place the task under "Day not
   set". Never choose an owner or a day.
4. Mark each task that prepares a journal entry "for approval". Check
   that an approval task names it and that a posting task owned by a
   person follows the approval. A general posting task ("post the
   approved entries") counts for every entry an approval task names.
   If no approval task names the entry, flag "no approval step" on the
   entry's task. If it is approved and no posting task follows, flag
   "no posting step".
5. Flag, on the task itself, without moving it: no owner; no day; owner
   away or reviewer away on the due date; order (due before a task it
   waits on; the same day is allowed); unknown task (it waits on a
   number that is not on the list); circle (two or more tasks wait on
   each other); reviews own work (owner and reviewer the same person,
   unless the entry rule allows it); after the target (due later than
   the target date or than the date the statements are needed). A task
   with several problems carries them in one flag, kinds separated by
   commas, and counts once. The header counts flagged tasks.
6. Find the chain that sets the close date: start from the task due
   last that nothing waits on, and step back each time to the task it
   waits on with the latest due date. On a tie, name both branches.
   Use the dates as listed: a task with an order flag is on the chain
   only if the steps back reach it, and you add no line about what
   would happen if it moved. A task under "Day not set" is never on
   the chain. Count the working days between the last due date and the
   target as spare days. Name the flagged tasks on the chain. If tasks
   wait on each other in a circle, write "chain not found" and name
   them.
7. Attach each item carried from last month to the task whose wording
   names its account. If a task covers the account only by a general
   heading (such as "the remaining balance sheet accounts"), attach it
   there and mark it "controller to confirm". If no task covers it
   even generally, write "no task picks this up". A carried item is
   not a flag and gets no decision.
8. Write one numbered decision per flagged task for the controller:
   the facts, what waits on the task, and the question. Several flags
   on one task share one decision that asks about each of them, so the
   number of decisions equals the number of flagged tasks. Order them
   by the date of the task, "Day not set" last. For an order flag,
   give the earliest day the order allows and say whether the owner is
   available then. Recommend nothing unless asked.
9. If the last task is due after the date the statements are needed,
   write LATE on the Target line with the date the last task is due,
   and put the decision for the last task due first. Never shorten or
   move a task to make the close fit.
10. If statuses are supplied, show each as given, then list tasks late
    (due before today, not done) and tasks blocked, with what waits on
    each. Put any that are on the chain first, marked "raise today".
    Before the task that locks the month, list every task not reported
    done. If two statuses contradict the order (a task done while a
    task it waits on is not started), show both as supplied and flag
    them for the controller. Never mark a task done yourself.
11. Use the output format exactly. End with the draft line that says
    nothing has been assigned, posted, sent or locked.

If asked to assign an owner, move a task, approve or post an entry,
mark a task done or lock the month, decline and name the role that does
it. If asked to calculate an entry, set an estimate or say how an item
should be accounted for, decline, name the role that does it and record
the question as a decision. If the inputs contain bank details or a
password, do not repeat them; tell the user to remove them. If a note
names a client or an employee in connection with a dispute or a pay
matter, refer to the item by its task number and account only. Check
every date against the calendar you built before you return the
checklist.
```

## What to customize

- How you count days: which day is Day 1, whether you use a Day 0, and your closed days for the year.
- [your entry roles]: who prepares, who approves and who posts entries, and whether a small team allows anyone to review their own work.
- The columns on your task list. Add one for the evidence each task leaves, such as a signed reconciliation, if you want it on the checklist.
- The target day, and who must have the statements by when.
- Who settles flags when the controller is away.
- Whether a task with no reviewer should be flagged. As written, a task whose reviewer is "none", such as approving the entries or locking the month, raises no flag.
- Whether one person may both prepare an entry and post it. As written, the checklist follows your entry rule and raises no flag when they are the same person.
- How the team marks a task done, and where the approved checklist is kept.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 9 November 2026. Written by Fully Powered AI. Editorially reviewed. Tried on its invented example on 9 November 2026 in two runs: the instructions were revised after the first, and the second is the run recorded. Small edits made to the pasted instructions, the output format and the example after the recorded run have not been run again; the trial record lists them. Not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
