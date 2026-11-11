# Trial: Payroll preparation and timesheet review, run on its example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-09

The inputs for this trial are the invented example in `public/example.md` (Tolland Row Bakery, pay period 2 to 8 November 2026). No client data was used. The model that ran it did not write the template.

On 9 November 2026, after this run and after an independent review, the template and the example's sheet were edited and the run was not repeated. The example's inputs were not changed. In the template: flags and settled lines now print as "FLAG 1," and "SETTLED, question 1,"; the dollar effect of each kind of flag is defined (for above usual hours, the overtime hours at the overtime rate; for no hours and a name not on the roster, "Dollar effect unknown."); the above-usual check compares hours counted, after anything kept out; hours worked for the last run are its hourly rows' regular plus overtime hours; a name not on the roster is stated to be a flag with its own question; missing inputs are listed under "Not supplied" in both the procedure and the instructions; bracketed format lines are printed only when they apply; questions are addressed to the owner, name a supervisor only where the settings give the person's crew, and assume no cause. Each of these settles a point listed below under "Where the template left room to guess" in the way this run already chose, so on these inputs they change nothing in the sheet below. In the example's sheet: question 3 no longer names the head baker, question 6 asks whether $18.50 is the correct rate rather than whether it was a raise, question 7 says only that nothing changes on this sheet, and no one is given a pronoun. The record below is as returned on the day, and its comparison is with the example's sheet as it stood then.

On 10 November 2026, in an editorial review, the template and the example's sheet were edited again and the run was not repeated. The example's inputs were not changed. In the instruction block: its closing line had lost a word in the edits of 9 November and now reads "Status: prepared for approval. Nothing keyed in, submitted, paid, sent or changed.", exactly as the output format and this run have it; the short-shift default is written as 5 minutes, like the other defaults; long lines were rewrapped without changing their words. In the example's sheet: Noor's line under "Kept out of the totals" gives the dates, 2 and 3 November, and Tom's rate flag and question 6 give the period, 2 to 8 November, as the format asks of every flag and question. No figure changed.

## Inputs used

The settings, timesheet export, roster, approved leave, leave balances, prior runs and schedule, exactly as given under "The inputs" in `public/example.md`. Only the instruction block and the output format of `member/template.md` were followed. The example's own sheet was not read until after this one was finished.

## What came out

The full sheet, as produced before the comparison:

```
PAYROLL PREPARATION SHEET: pay period 2 November 2026 to 8 November 2026, pay date 13 November 2026

For: owner. Prepared by: office manager on 9 November 2026.
Sources: timesheet export 2 to 8 November 2026, 25 rows; roster as of 9 November 2026; approved leave for 2 to 8 November 2026; leave balances as of 1 November 2026; prior runs ending 11 October, 18 October, 25 October and 1 November 2026; schedule week starting 2 November 2026.
Rules used: overtime as set up with the payroll provider: hours worked over 40 in a workweek at 1.5 times the hourly rate; leave toward overtime no; breaks unpaid, the Break minutes column is subtracted from In to Out; rounding none (hours kept exact to two decimals); workweek Monday to Sunday.
Not supplied: Nothing. Defaults used: hours difference 0.10 hours; short shift 5 minutes; long shift 12 hours; long day 16 hours; days in a row 7.
Personal fields found: None.

THE PICTURE
People on the roster in this run: 7 (6 hourly, 1 salaried). Flags open: 8, on 6 people on the roster and 1 name not on it.
Hours worked by hourly staff: regular 128.00, overtime 8.00. Leave: 20.00 (Sick 12.00, Vacation 8.00).
Estimated gross before deductions: $4,520.00. Employer taxes, contributions and deductions: not estimated; the payroll provider calculates them.
Kept out of the totals: Priya (E03), 5 Nov 2026, hours unknown, start time with no finish; Lena (E05), 3 Nov 2026, 4.00 hours, before her start date of 4 Nov 2026; Noor (E07), sick leave 4.00 hours, above the balance of 12.00; Jo (no ID), 7 and 8 Nov 2026, 12.00 hours, name not on the roster.

PEOPLE
E03 Priya, hourly at $18.50
  Regular 32.00. Overtime 0.00. Leave none. Estimated gross $592.00.
  Gross leaves out: the shift on 5 Nov 2026 (in 07:00, no finish), hours unknown.
  FLAG [question 1], broken punch: 5 Nov 2026. Start 07:00 with no finish; the hours for this shift are unknown. The other four shifts (3 on 2 to 4 Nov, 1 on 6 Nov) total 32.00 hours. Dollar effect unknown.

E06 Sam, hourly at $19.00
  Regular 0.00. Overtime 0.00. Leave none. Estimated gross $0.00.
  Gross leaves out: nothing.
  FLAG [question 2], no hours: this period. No timesheet rows and no approved leave; the last run (week ending 1 Nov 2026) shows 24.00 hours and $456.00 gross, and the schedule shows 24.00 hours for the week of 2 Nov. Dollar effect unknown.

E02 Marco, hourly at $24.00
  Regular 40.00. Overtime 8.00 (over 40 in the workweek, at $36.00). Leave none. Estimated gross $1,248.00.
  Gross leaves out: nothing.
  FLAG [question 3], above usual hours: week of 2 Nov 2026. Worked 48.00 hours against 40.00 scheduled (8.00 more, 20.0%, margin 10%); overtime 8.00 hours against an average of 1.00 over the last four runs (0.00, 2.00, 1.00, 1.00; 125% of the average is 1.25). Dollar effect: the 8.00 overtime hours are $288.00 of the gross.

E07 Noor, hourly at $21.00
  Regular 24.00. Overtime 0.00. Leave Sick 12.00. Estimated gross $756.00 ($504.00 for 24.00 worked hours, $252.00 for 12.00 leave hours).
  Gross leaves out: 4.00 hours of sick leave above the balance.
  FLAG [question 4], leave beyond the balance: sick leave 2 and 3 Nov 2026. Approved 16.00 hours against a balance of 12.00 as of 1 Nov 2026. 12.00 hours counted, 4.00 kept out. Dollar effect: $84.00 (4.00 hours at $21.00) left out.

E05 Lena, hourly at $17.00
  Regular 12.00. Overtime 0.00. Leave none. Estimated gross $204.00.
  Gross leaves out: 4.00 hours on 3 Nov 2026, before the start date.
  FLAG [question 5], hours before the start date: 3 Nov 2026, 08:00 to 12:00, 4.00 hours; the roster start date is 4 Nov 2026. Kept out of the totals. Dollar effect: $68.00 (4.00 hours at $17.00) left out.

E04 Tom, hourly at $18.50
  Regular 20.00. Overtime 0.00. Leave none. Estimated gross $370.00.
  Gross leaves out: nothing.
  Note on the timesheet, 6 Nov 2026: "New bank account from next week, please update".
  FLAG [question 6], rate changed: the roster rate is $18.50; the last run paid $17.50. Difference $1.00 an hour. Dollar effect: $20.00 (20.00 hours at $1.00) more than the old rate.
  FLAG [question 7], pay-detail request: 6 Nov 2026, note "New bank account from next week, please update". Nothing is changed. No dollar effect.

E01 Asha, salaried at $1,350.00 per period
  Regular salaried. Overtime not applicable. Leave Vacation 8.00. Estimated gross $1,350.00.
  Gross leaves out: nothing.
  No flags.

NAMES NOT ON THE ROSTER
Jo, no ID: 7 Nov 2026 6.00 hours and 8 Nov 2026 6.00 hours, 12.00 hours. Not in the totals. See question 8.
On the last run, not on the roster: None.

CHANGE FROM THE LAST RUN
Last run, period ending 1 Nov 2026: 165.00 hours worked, gross $4,732.00 as exported. This run: 136.00 hours worked, estimated gross $4,520.00.
Change: hours -29.00, -17.6%; gross -$212.00, -4.5%.
Hours moved more than 10%: Sam 24.00 to 0.00 (-24.00); Noor 40.00 to 24.00 (-16.00; 12.00 of the gap is counted as sick leave); Priya 40.00 to 32.00 (-8.00; one shift unknown); Marco 41.00 to 48.00 (+7.00); Lena new, +12.00; Tom unchanged at 20.00. Gross within 10%.

CASH
$16,800.00 stated by the owner on 9 Nov 2026 - supplier payment run 12 Nov 2026 $6,250.00 - estimated gross $4,520.00 = $6,030.00, against a floor of $5,000.00, before employer taxes and contributions.

QUESTIONS FOR THE OWNER, ONE AT A TIME
1. Priya (E03), 5 Nov 2026: start 07:00, no finish, hours unknown. If left as it is: the shift is not paid; Priya's gross is $592.00. What time did the shift end, and were there breaks?
2. Sam (E06), this period: no hours and no leave, against 24.00 hours on the last run. If left as it is: nothing is paid to Sam; gross $0.00. Did Sam work or take approved leave this period, and if so which days and hours?
3. Marco (E02), week of 2 Nov 2026: 48.00 hours against 40.00 scheduled, 8.00 overtime against about 1.00 usual. If left as it is: 40.00 regular and 8.00 overtime are paid, $1,248.00. Are the 48.00 hours right?
4. Noor (E07), sick leave 2 and 3 Nov 2026: 16.00 hours approved, balance 12.00. If left as it is: 12.00 hours are paid, 4.00 are not ($84.00). How should the extra 4.00 hours be treated?
5. Lena (E05), 3 Nov 2026: 4.00 hours before the start date of 4 Nov 2026. If left as it is: the 4.00 hours are not paid ($68.00). Is the start date on the roster right, or should the 4.00 hours be paid?
6. Tom (E04), rate: roster $18.50, last run $17.50. If left as it is: the sheet pays $18.50, $370.00, $20.00 more than at the old rate. Is $18.50 the correct rate from this period?
7. Tom (E04), 6 Nov 2026: note "New bank account from next week, please update". If left as it is: nothing is changed on this sheet. Will you confirm the new account with Tom directly, in person or on a phone number already held, so the person authorized can make any change in the payroll provider?
8. Jo (no ID), 7 and 8 Nov 2026: 12.00 hours, name not on the roster. If left as it is: the 12.00 hours are not paid. Who is Jo, and should the hours be paid under an existing employee or a new roster entry?

FOR APPROVAL
7 people on the roster, 136.00 hours worked and 20.00 hours of leave, estimated gross $4,520.00 before deductions, pay date 13 November 2026, 8 questions open.

Status: prepared for approval. Nothing keyed in, submitted, paid, sent or changed.
```

## What was observed

Every part of the output format was produced, in order, and every section was filled. Nothing in the inputs triggered a stop condition: the headers matched, the break convention and overtime rule were stated, the period is exactly one workweek, and no roster ID repeats. The sheet ended with the required status line and nothing was keyed in, submitted, paid, sent or changed. The reviewer checklist was met: every hour traces to a row or is listed as kept out, eight flags and eight questions, no tax or personal field, gross recomputed to $4,520.00.

Compared with the example's sheet, the substance is the same: the same eight flags, the same question order, the same totals ($4,520.00 gross, 128.00 regular, 8.00 overtime, 20.00 leave), the same change from the last run (hours -29.00, -17.6%; gross -$212.00, -4.5%), and the same cash line ($6,030.00 against a floor of $5,000.00). Differences were in wording and a few choices:

- The example writes weekday names with dates (Thursday 5 November); this run used dates only. The example's pay date line includes "Friday"; this run left the weekday off.
- The example prints flags as "FLAG 1, kind:"; the template format says "FLAG [question n], kind:". This run followed the template; the example does not.
- This run's first draft put Sam, who has no rows, into "Kept out of the totals"; on checking the template that was removed, as nothing of his is in the exports to keep out. The example does not list him there.
- Question wording differs. This run asked each question in a neutral form; the example's questions suggest causes.
- This run gave the history figures for Marco's flag with the 125% threshold (1.25) stated; the example does not.

Facts in the example's output that are not in the inputs: Sam, Noor, Priya and Lena are given "he" or "her" (the inputs give no gender); question 3 asks whether the Saturday was agreed with "the head baker", which assumes Marco is in the bakery crew (the roster has no crew column); question 6 asks "Is this a raise you gave", which assumes a cause; question 7 says Tom's pay "goes to the account already held by the payroll provider", which the inputs do not state. This run's output carried no fact outside the inputs that it could find; all figures were derived from them.

Where the template left room to guess, this run chose as follows:

- Dollar effect of an "above usual hours" flag is not defined. This run (like the example) used the cost of the overtime hours, $288.00. A reader could as fairly use only the premium, $96.00. The ordering of people depends on this choice only weakly, because $288.00 or $96.00 is still the largest effect.
- Dollar effect of "no hours" (Sam) is not defined. The template says unknown-hours flags carry no figure, but Sam's hours are absent rather than unknown. This run wrote "Dollar effect unknown" and quoted last run's $456.00 as context.
- Whether a name not on the roster (Jo) is a flag is not stated. This run counted it, so flags and questions both come to eight, which the checklist item "questions equal flags" needs. The "Flags open" line then reads "6 people ... and 1 name".
- For the above-usual check against the schedule, it is not said whether "worked hours" means hours counted or hours recorded. Lena has 16.00 recorded and 12.00 counted against 12.00 scheduled. This run used counted hours, so there was no flag.
- Prior-run "hours worked" is not defined. This run used regular plus overtime, giving 165.00 for the last run.
- The roster has no crew or department column, so the template cannot say whether the owner or the supervisor answers a given question. This run addressed all questions to the owner.
- The format shows optional lines in brackets, such as the by-workweek line and "Timesheet hours, not used for pay", without saying when a line is dropped. This run printed only the lines that applied.
- The procedure says to write "Leave not supplied" and similar; the instruction block says to list inputs under "Not supplied". They agree in effect but not in wording.
- Rounding "none" is read as exact to two decimals, as the template says.

Shortcomings of the trial: one run, one model, an example the template was written alongside, and no person reviewed the sheet. It shows the instructions can be followed on the example and yield the same result as the published sheet. It does not show how the template behaves on a real export, with real headers, or on the stop conditions and acceptance tests that were not exercised here.
