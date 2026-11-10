# Month-end close checklist: an invented example

*Illustrative example with invented data.* The firm, the people, the tasks, the dates and the amounts below are all invented. The firm is an invented 45-person engineering consultancy whose finance team is a controller, a staff accountant, a billing coordinator and a payables and payroll clerk, reporting to a managing partner. First come the inputs the controller supplied, in full, then the checklist the capability returned.

## The inputs

### 1. Close settings

```
Month being closed: October 2026
Period end: Saturday 31 October 2026
Today: Wednesday 28 October 2026
Working days: Monday to Friday
Office closed: Tuesday 3 November 2026
How we count: Day -1 is the last working day of the month. Day 1 is the
  first working day after the period end. Day -2 is the working day
  before Day -1.
Target: October locked by the end of Day 5
Entries: prepared by the task's owner, approved by the controller, posted
  by the staff accountant. The assistant posts nothing.
Review rule: nobody reviews their own work.
```

### 2. Close task list (the firm's standing list, exported)

```
id,task,day,owner,waits_on,reviewer
T01,Send the cut-off reminder: supplier bills and timesheets in by the end of Day -1,Day -2,Controller,-,-
T02,Confirm all October time is entered and approved,Day -1,Billing coordinator,T01,Controller
T03,Close payables for October; list goods and services received but not invoiced,Day 1,Payables and payroll clerk,T01,Controller
T04,Issue the final October invoices and close billing,Day 1,Billing coordinator,T02,Controller
T05,Prepare the payroll accrual entry,Day 1,Payables and payroll clerk,-,Controller
T06,Reconcile the operating and payroll bank accounts,Day 2,Staff accountant,-,Controller
T07,"Prepare the depreciation, prepaid release and supplier accrual entries",Day 2,Staff accountant,T03,Controller
T08,Prepare the unbilled revenue entry,Day 3,Billing coordinator,T04,Controller
T09,"Approve the prepared entries (T05, T07, T08)",Day 3,Controller,T05; T07; T08,-
T10,Post the approved entries,Day 3,Staff accountant,T09,Controller
T11,Reconcile the receivables ledger to the general ledger,Day 2,Staff accountant,T04; T10,Controller
T12,Reconcile the payables ledger and the remaining balance sheet accounts,Day 4,Staff accountant,T10,Controller
T13,Run the trial balance; compare with September and with budget; explain movements over the threshold,Day 4,Controller,T11; T12,Controller
T14,Draft the October statements pack,Day 5,Controller,T13,Managing partner
T15,Review the pack and sign off,Day 5,Managing partner,T14,-
T16,Lock October in the accounting system,Day 5,Controller,T15,-
```

### 3. Notes for this month (typed by the controller)

```
- The staff accountant is out on Thursday 5 November.
- Office fit-out: the work finished on 23 October. The contractor's final
  invoice has not arrived. My estimate is $18,400. It needs an accrual.
  Nobody is assigned yet.
- Carried from September: a $640 difference on the company credit card
  reconciliation, open since 12 September.
- Partners' meeting is Wednesday 11 November. The managing partner wants
  the pack by the end of Monday 9 November.
```

## The output

**MONTH-END CLOSE CHECKLIST: October 2026**

- **For:** Controller. Period end Saturday 31 October 2026. Target: October locked by Monday 9 November (Day 5). Statements needed by Monday 9 November.
- **Prepared:** Wednesday 28 October 2026, from the close task list (16 tasks), the close settings and the notes for October.
- **Working days:** Day −2 Thursday 29 October · Day −1 Friday 30 October · Day 1 Monday 2 November · Day 2 Wednesday 4 November · Day 3 Thursday 5 November · Day 4 Friday 6 November · Day 5 Monday 9 November.
- **Days skipped:** Saturday 31 October, Sunday 1 November, Tuesday 3 November (office closed), Saturday 7 and Sunday 8 November.
- **Tasks:** 17 (16 from the list, 1 new this month). **Tasks flagged:** 4.

**Thursday 29 October (Day −2)**

- **T01** Send the cut-off reminder: supplier bills and timesheets in by the end of Friday 30 October. Owner: Controller. Waits on: nothing. Reviewer: none.

**Friday 30 October (Day −1)**

- **T02** Confirm all October time is entered and approved. Owner: Billing coordinator. Waits on: T01. Reviewer: Controller.

**Monday 2 November (Day 1)**

- **T03** Close payables for October; list goods and services received but not invoiced. Owner: Payables and payroll clerk. Waits on: T01. Reviewer: Controller.
- **T04** Issue the final October invoices and close billing. Owner: Billing coordinator. Waits on: T02. Reviewer: Controller.
- **T05** Prepare the payroll accrual entry, for approval. Owner: Payables and payroll clerk. Waits on: nothing. Reviewer: Controller.

**Wednesday 4 November (Day 2)**

- **T06** Reconcile the operating and payroll bank accounts. Owner: Staff accountant. Waits on: nothing. Reviewer: Controller.
- **T07** Prepare the depreciation, prepaid release and supplier accrual entries, for approval. Owner: Staff accountant. Waits on: T03. Reviewer: Controller.
- **T11** Reconcile the receivables ledger to the general ledger. Owner: Staff accountant. Waits on: T04; T10. Reviewer: Controller. **FLAG, order:** listed for Day 2, but it waits on T10, which is due on Day 3 (Thursday 5 November). Left where the list puts it; see decision 1.

**Thursday 5 November (Day 3)**

- **T08** Prepare the unbilled revenue entry, for approval. Owner: Billing coordinator. Waits on: T04. Reviewer: Controller.
- **T09** Approve the prepared entries (T05, T07, T08). Owner: Controller. Waits on: T05; T07; T08. Reviewer: none.
- **T10** Post the approved entries. Owner: Staff accountant. Waits on: T09. Reviewer: Controller. **FLAG, owner away:** the staff accountant is out on Thursday 5 November. See decision 2.

**Friday 6 November (Day 4)**

- **T12** Reconcile the payables ledger and the remaining balance sheet accounts. Owner: Staff accountant. Waits on: T10. Reviewer: Controller. Carried item: the \$640 credit card difference, controller to confirm.
- **T13** Run the trial balance; compare with September and with budget; explain movements over the threshold. Owner: Controller. Waits on: T11; T12. Reviewer: Controller. **FLAG, reviews own work:** the owner and the reviewer are the same person. See decision 3.

**Monday 9 November (Day 5)**

- **T14** Draft the October statements pack. Owner: Controller. Waits on: T13. Reviewer: Managing partner.
- **T15** Review the pack and sign off. Owner: Managing partner. Waits on: T14. Reviewer: none.
- **T16** Lock October in the accounting system. Owner: Controller. Waits on: T15. Reviewer: none.

**Day not set**

- **N01** (new this month) Prepare the accrual entry for the office fit-out, for approval. The work finished on 23 October; the contractor's final invoice has not arrived; the controller's estimate is \$18,400. Owner: not assigned. Waits on: not stated. Reviewer: not stated. **FLAG, no owner, no day, no approval step:** the note assigns nobody and gives no day, and the approval task, T09, names T05, T07 and T08 only. See decision 4.

**Decisions for the controller before the close starts: 4**

1. **T11, order.** The receivables reconciliation is listed for Wednesday 4 November but waits on the entries posted in T10 on Thursday 5 November. The earliest day the order allows is Thursday 5 November, and the staff accountant is out that day. T13, due on Friday 6 November, waits on T11. Does T11 move, or does someone else do it?
2. **T10, owner away.** The staff accountant posts the approved entries and is out on the day they are due. T10 is on the chain that sets the close date, and T11, T12 and T13 wait on it. Who posts on Thursday 5 November, or does posting move to Friday 6 November?
3. **T13, reviews own work.** The controller both prepares and reviews the trial balance comparison, and the settings say nobody reviews their own work. Who reviews T13?
4. **N01, no owner, no day, no approval step.** The fit-out accrual is new this month and nothing on the list waits on it. The note assigns nobody and gives no day. The approval task, T09, names T05, T07 and T08 only, so nobody is yet listed to approve this entry; the other entries are approved and posted on Thursday 5 November. Who prepares it, by which day, and who approves it: under T09 or in a separate step?

**The chain that sets the close date**

T01 → T02 → T04 → T08 → T09 → T10 → T12 → T13 → T14 → T15 → T16. The last task is due on Monday 9 November and the target is Monday 9 November: no spare day. Flagged tasks on the chain: T10 and T13.

**Entries this month**

- T05, payroll accrual: prepared by the payables and payroll clerk.
- T07, depreciation, prepaid release and supplier accrual: prepared by the staff accountant.
- T08, unbilled revenue: prepared by the billing coordinator.
- N01, office fit-out accrual: preparer not assigned.
- Approved by the controller in T09 (T05, T07, T08). Posted by the staff accountant in T10, after approval.
- Entries with no approval step: N01. Entries with no posting step: none.

**Carried from last month**

- \$640 difference on the company credit card reconciliation, open since 12 September. Picked up under T12 by its general heading, "the remaining balance sheet accounts"; no task names the credit card. Controller to confirm.

**Also noted**

- The partners' meeting is on Wednesday 11 November. T14, T15 and T16 are all due on Monday 9 November, the day the managing partner wants the pack, so the pack is drafted, reviewed and signed off within one day.

Draft for the controller's approval. Nothing has been assigned, posted, sent or locked.
