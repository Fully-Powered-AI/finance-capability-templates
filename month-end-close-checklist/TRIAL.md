# Month-end close checklist: one trial run on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Fable 5.2
- **Date:** 2026-11-09
- **Template version:** 0.1.0

This is a record of one run of the capability template on its own invented example. The firm, the people, the tasks, the dates and the amounts are invented, and no client data was used. It shows what the template produced once, on one set of inputs. It is not a test in any company's environment.

This is the second run on the same example. An earlier run the same day showed where the instructions left room to guess; the instructions and the example were revised, and the run recorded here was made on the revised instructions. What the earlier run found, and what was changed, is at the end.

## The inputs used

The inputs are exactly those in [the worked example](example.md), under "The inputs": the close settings for October 2026 (period end Saturday 31 October, today Wednesday 28 October, Monday-to-Friday working days, the office closed on Tuesday 3 November, the counting rule, the Day 5 target, the entry rule and the review rule), the firm's standing close task list of sixteen tasks (T01 to T16), and the controller's four notes for the month. No statuses were supplied, so this was a run before the close, not during it.

The run was a fresh session started from Claude Code with no tools and no access to any file. The template's instructions for an AI assistant and its output format were given as the session's instructions, and the inputs were sent as one message. The session did not see the example's own checklist or the earlier run.

## What came out

The complete output, as returned:

```
MONTH-END CLOSE CHECKLIST: October 2026

For: Controller. Period end Saturday 31 October 2026. Target: October locked by Monday 9 November 2026 (Day 5). Statements needed by Monday 9 November 2026.
Prepared: Wednesday 28 October 2026, from the close task list (16 tasks), the close settings, and the notes for this month.
Working days: Day -2 Thursday 29 October 2026 · Day -1 Friday 30 October 2026 · Day 1 Monday 2 November 2026 · Day 2 Wednesday 4 November 2026 · Day 3 Thursday 5 November 2026 · Day 4 Friday 6 November 2026 · Day 5 Monday 9 November 2026
Days skipped: Saturday 31 October 2026, Sunday 1 November 2026, Tuesday 3 November 2026 (office closed), Saturday 7 November 2026, Sunday 8 November 2026
Tasks: 17 (16 from the list, 1 new this month). Tasks flagged: 4.

**Thursday 29 October 2026 (Day -2)**
T01 Send the cut-off reminder: supplier bills and timesheets in by the end of Friday 30 October 2026. Owner: Controller. Waits on: nothing. Reviewer: none.

**Friday 30 October 2026 (Day -1)**
T02 Confirm all October time is entered and approved. Owner: Billing coordinator. Waits on: T01. Reviewer: Controller.

**Monday 2 November 2026 (Day 1)**
T03 Close payables for October; list goods and services received but not invoiced. Owner: Payables and payroll clerk. Waits on: T01. Reviewer: Controller.
T04 Issue the final October invoices and close billing. Owner: Billing coordinator. Waits on: T02. Reviewer: Controller.
T05 Prepare the payroll accrual entry, for approval. Owner: Payables and payroll clerk. Waits on: nothing. Reviewer: Controller.

**Wednesday 4 November 2026 (Day 2)**
T06 Reconcile the operating and payroll bank accounts. Owner: Staff accountant. Waits on: nothing. Reviewer: Controller.
T07 Prepare the depreciation, prepaid release and supplier accrual entries, for approval. Owner: Staff accountant. Waits on: T03. Reviewer: Controller.
T11 Reconcile the receivables ledger to the general ledger. Owner: Staff accountant. Waits on: T04; T10. Reviewer: Controller. FLAG, order: due Wednesday 4 November 2026 (Day 2), but it waits on T10, which is due Thursday 5 November 2026 (Day 3). See decision 1.

**Thursday 5 November 2026 (Day 3)**
T08 Prepare the unbilled revenue entry, for approval. Owner: Billing coordinator. Waits on: T04. Reviewer: Controller.
T09 Approve the prepared entries (T05, T07, T08). Owner: Controller. Waits on: T05; T07; T08. Reviewer: none.
T10 Post the approved entries. Owner: Staff accountant. Waits on: T09. Reviewer: Controller. FLAG, owner away: the staff accountant is out on Thursday 5 November 2026, the day this task is due. See decision 2.

**Friday 6 November 2026 (Day 4)**
T12 Reconcile the payables ledger and the remaining balance sheet accounts. Owner: Staff accountant. Waits on: T10. Reviewer: Controller. Carried item: $640 difference on the company credit card reconciliation, open since Saturday 12 September 2026, controller to confirm.
T13 Run the trial balance; compare with September and with budget; explain movements over the threshold. Owner: Controller. Waits on: T11; T12. Reviewer: Controller. FLAG, owner and reviewer the same person: the Controller is listed as both, and the review rule says nobody reviews their own work. See decision 3.

**Monday 9 November 2026 (Day 5)**
T14 Draft the October statements pack. Owner: Controller. Waits on: T13. Reviewer: Managing partner.
T15 Review the pack and sign off. Owner: Managing partner. Waits on: T14. Reviewer: none.
T16 Lock October in the accounting system. Owner: Controller. Waits on: T15. Reviewer: none.

**Day not set**
N01 (new this month) Prepare the accrual entry for the office fit-out, for approval. The work finished on Friday 23 October 2026; the contractor's final invoice has not arrived; the controller's estimate is $18,400. Owner: not assigned. Waits on: not stated. Reviewer: not stated. FLAG, no owner, no day, no approval step: the note assigns nobody and gives no day, and T09 names only T05, T07 and T08. See decision 4.

**Decisions for the Controller before the close starts: 4, one per flagged task**

1. T11, order. T11 is due Wednesday 4 November 2026 (Day 2) and waits on T04 (Monday 2 November 2026) and T10 (Thursday 5 November 2026, Day 3).
   - The earliest day the order allows is Thursday 5 November 2026 (Day 3), the same day as T10. The staff accountant is away that day.
   - T10 is itself flagged (decision 2).
   - T13 waits on T11.
   - Question: does T11 stay on Day 2 with the wait on T10 as listed, or do you change its day or its waits-on list?

2. T10, owner away. T10 is due Thursday 5 November 2026 (Day 3) and its owner, the staff accountant, is out that day.
   - The entry rule says entries are posted by the staff accountant.
   - T10 waits on T09, due the same day. T11 and T12 wait on T10.
   - T10 is on the chain that sets the close date, and there is no spare day.
   - Question: who posts the approved entries on Thursday 5 November 2026, or do you set another day for T10?

3. T13, owner and reviewer the same person. The Controller is listed as both owner and reviewer of T13, due Friday 6 November 2026 (Day 4).
   - The review rule says nobody reviews their own work.
   - T14 waits on T13, and T13 is on the chain.
   - Question: who reviews T13?

4. N01, no owner, no day, no approval step. The office fit-out accrual has nobody assigned and no day.
   - T09 approves only T05, T07 and T08, so no approval task names this entry. T10 posts only approved entries.
   - Nothing on the list waits on N01.
   - Questions: who prepares the entry? Which day is it due? Which task approves it?

**The chain that sets the close date**
T01 → T02 → T04 → T08 → T09 → T10 → T12 → T13 → T14 → T15 → T16. Last task due Monday 9 November 2026; target Monday 9 November 2026: no spare day. Flagged tasks on the chain: T10, T13.

**Entries this month**
T05, payroll accrual entry: prepared by Payables and payroll clerk.
T07, depreciation, prepaid release and supplier accrual entries: prepared by Staff accountant.
T08, unbilled revenue entry: prepared by Billing coordinator.
N01, office fit-out accrual entry: prepared by not assigned.
Approved by Controller in T09 (T05, T07, T08). Posted by Staff accountant in T10, after approval.
Entries with no approval step: N01. Entries with no posting step: none.

**Carried from last month**
$640 difference on the company credit card reconciliation, open since Saturday 12 September 2026. Picked up under T12 by its general heading, controller to confirm.

**Also noted**
- The partners' meeting is Wednesday 11 November 2026. The managing partner wants the pack by the end of Monday 9 November 2026, the same day T14 (draft) and T15 (sign-off) are due.
- No task statuses were supplied, so this is the before-the-close checklist as of the "Today" date in the settings.

Draft for the Controller's approval. Nothing has been assigned, posted, sent or locked.
```

## What was observed

**What held.** Every part of the output format was produced. The calendar skipped the weekend and the closed Tuesday, and every one of the sixteen listed tasks appeared once on the right date with its number, owner, waits-on list and reviewer unchanged. The day number inside T01's wording was replaced by its date. The three problems planted in the example were found: T11 listed a day before the posting it waits on, the staff accountant away on the day posting is due, and the controller reviewing the controller's own task. The fit-out accrual became one new task with no owner and no day chosen for it, and the estimate was repeated only as the controller's own figure. Nothing in these inputs called for a stop, and nothing was assigned, moved, calculated or posted.

**Agreement with the published example.** On every point that is counted or decided, the run and the example agree:

- Four tasks flagged and four decisions, on the same four tasks (T11, T10, T13, N01).
- N01 carries one flag naming all three problems (no owner, no day, no approval step), and its one decision asks who prepares it, by which day and who approves it.
- The same chain, no spare day, and the same two flagged tasks on it. No extra line about T11 was added under the chain.
- "Entries with no approval step: N01", and none with no posting step.
- The $640 credit card difference attached to T12 by its general heading, marked for the controller to confirm.
- "none" for a reviewer the list leaves empty, "nothing" for an empty waits-on, and "not stated" for the two fields the note on N01 does not give.
- The date the statements are needed on the Target line.

**Differences from the published example.**

- **The name of one flag.** The run called the flag on T13 "owner and reviewer the same person"; the example and the template's procedure call it "reviews own work". The instructions the run was given described that flag without naming it.
- **A hint copied into the output.** The decisions heading reads "4, one per flagged task". The output format carried that phrase as a note beside the count, and the run copied it.
- **Weekdays and years on every date.** The run wrote the year on each date and added a weekday to the two dates in the notes (Friday 23 October, Saturday 12 September). Both weekdays are correct. The example gives the year once and leaves the notes' dates as written.
- **The first decision.** The run says the earliest day the order allows is Thursday 5 November and that the staff accountant is away that day. The example goes one step further and names Friday 6 November as the first day that owner could do it. The instructions ask only for the earliest day and whether the owner is available.
- **Layout.** The run set its decisions out as short bullet lists and put headings in bold; it kept the semicolons of the task list in "Waits on", where the example uses commas. The carried item on T12's line repeats the whole note; the example shortens it.
- **One extra note.** Under "Also noted" the run added that no statuses were supplied. It is true and harmless, and the format does not ask for it.

**Where the instructions still leave room to guess.**

1. How much of a note to repeat on a task's line for a carried item.
2. Whether dates quoted from the notes take a weekday and a year.
3. Whether a decision on an order flag should name the next day the owner is available when the earliest day is one the owner is away.

**Shortcomings to know about.**

- A task with no reviewer at all (T01, T09, T15, T16) is not one of the flags, so the approval of entries and the locking of the month pass without comment on who checks them. The template now says so under "What to customize".
- The staff accountant both prepares the entries in T07 and posts them in T10. The entry rule allows it and there is no flag for it. The template now says so under "What to customize".
- This was one run, before the close. The part of the template used during the close (statuses, late and blocked tasks, "raise today", the list of tasks not reported done before the lock) was not exercised, and neither were the stop conditions, a circle or a late close, since the inputs were complete and had none of these.

## The earlier run, and what was changed

The first run, on 9 November 2026 in Claude Code, used the template as first written and the same inputs. It found the same three planted problems and the same chain, and differed from the example then published in these ways:

- It counted six flags and wrote six decisions where the example counted four, because the instructions asked for one decision per flag and N01 had three flags (no owner, no day, no approval step). The example joined the first two and did not flag the missing approval at all, which the template's own reviewer checklist requires.
- It wrote "no task picks this up" for the $640 credit card difference; the example attached it to T12.
- It wrote "none listed" and "nothing stated" where the example wrote "not stated".
- It added a line under the chain about what would happen if T11 moved, as the example did; the format asked for neither.
- It put the date the statements are needed under "Also noted", because the header had no place for it.

Changed after the first run, before the run recorded above:

- **Counting.** One decision per flagged task. Several flags on one task are written as one flag and share one decision, and the header counts flagged tasks.
- **The example's N01.** It now carries the "no approval step" flag, its decision asks who approves it as well as who prepares it and by when, and the entries section lists it under "Entries with no approval step".
- **Carried items.** An item goes to the task that names its account; if a task covers it only by a general heading it is attached there and marked "controller to confirm"; otherwise "no task picks this up".
- **Empty fields.** One wording: "nothing" and "none" where the list marks the field empty, "not stated" where the field is absent.
- **One-off items.** The instructions now say what becomes a task and what does not.
- **The chain.** Traced on listed dates; no line about what would happen if a flagged task moved.
- **The header.** The Target line now carries the date the statements are needed, and LATE when the close runs past it.
- **The pasted instructions** now carry rules that were only in the procedure: "chain not found" for a circle, statuses that contradict the order, referring to a client or an employee in a dispute or a pay matter by task number only, and the late close. They also list, before the lock, every task not reported done.

Changed after the run recorded above, and not run again:

- The pasted instructions now name the flag "reviews own work", so the label matches the procedure and the example.
- The note "one per flagged task" was taken out of the decisions heading in the output format, so it is no longer copied into a checklist.

Changed on 9 November 2026 after an independent review of the published template, and not run again. The output and the observations above are as recorded and describe the template and the example as they stood at the run:

- **The pasted instructions, step 5.** A broken line was rewrapped, and two flags that were described without their names now carry the procedure's labels, "unknown task" and "circle".
- **The output format, during the close.** The single line for a run during the close ("Raise today", "Late", "Blocked", "Not reported done before the lock") was set out as one line for each, with the fields the procedure already asks for. This part of the template has still not been tried.
- **The example's first decision.** It no longer names Friday 6 November as the first workable day for the owner. It now gives what the instructions ask for, the earliest day the order allows and that the owner is away that day, as the run did.
- **The example's "Waits on" lists.** They now keep the semicolons of the task list, as the run did.

The first two places where the instructions leave room to guess are unchanged. On the third, the example now follows the instructions as written.
