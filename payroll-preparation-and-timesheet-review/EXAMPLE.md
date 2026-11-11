# Payroll preparation and timesheet review: an invented example

*Illustrative example with invented data.* The company, the people, the hours and every figure below are invented. Tolland Row Bakery is an invented bakery and café with seven people on its roster, paid weekly. Its office manager prepares the payroll for the week of Monday 2 to Sunday 8 November 2026 for the owner to approve. Staff are invented and referred to by first name and employee ID.

The inputs come first, in full, so the template can be run on them. The payroll preparation sheet follows, in the template's output format.

## The inputs

### Settings

```
Pay period: Monday 2 November 2026 to Sunday 8 November 2026. Paid weekly.
Pay date: Friday 13 November 2026. Sheet prepared: Monday 9 November 2026.
Workweek: Monday to Sunday.
Runs it: office manager. Approves and answers the questions: owner.
Answers for the bakery crew's hours: head baker. For the counter: owner.
Keys the approved hours into the payroll provider: office manager.
Submits the payroll: owner.
Overtime rule, as set up with the payroll provider: hours worked over 40
  in a workweek are paid at 1.5 times the hourly rate. Leave hours do not
  count toward the 40.
Breaks: unpaid. The Break minutes column is subtracted from In to Out.
Rounding: none.
Prior runs: the last 4.
Above usual hours: more than 10% above the schedule, or overtime above
  125% of the person's average over the prior runs.
Change from the last run: explain a move of more than 10%.
Cash: operating account $16,800.00, stated by the owner on the morning of
  9 November 2026. A supplier payment run of $6,250.00 leaves on Thursday
  12 November. The owner wants at least $5,000.00 left in the account.
```

### Timesheet export, 2 to 8 November 2026

```
Employee ID | Name | Date | In | Out | Break minutes | Hours | Note
E02 | Marco | 2 Nov 2026 | 05:00 | 13:30 | 30 | 8.00 |
E02 | Marco | 3 Nov 2026 | 05:00 | 13:30 | 30 | 8.00 |
E02 | Marco | 4 Nov 2026 | 05:00 | 13:30 | 30 | 8.00 |
E02 | Marco | 5 Nov 2026 | 05:00 | 13:30 | 30 | 8.00 |
E02 | Marco | 6 Nov 2026 | 05:00 | 13:30 | 30 | 8.00 |
E02 | Marco | 7 Nov 2026 | 05:00 | 13:30 | 30 | 8.00 |
E03 | Priya | 2 Nov 2026 | 07:00 | 15:30 | 30 | 8.00 |
E03 | Priya | 3 Nov 2026 | 07:00 | 15:30 | 30 | 8.00 |
E03 | Priya | 4 Nov 2026 | 07:00 | 15:30 | 30 | 8.00 |
E03 | Priya | 5 Nov 2026 | 07:00 |  |  |  |
E03 | Priya | 6 Nov 2026 | 07:00 | 15:30 | 30 | 8.00 |
E04 | Tom | 2 Nov 2026 | 10:00 | 14:00 | 0 | 4.00 |
E04 | Tom | 3 Nov 2026 | 10:00 | 14:00 | 0 | 4.00 |
E04 | Tom | 4 Nov 2026 | 10:00 | 14:00 | 0 | 4.00 |
E04 | Tom | 5 Nov 2026 | 10:00 | 14:00 | 0 | 4.00 |
E04 | Tom | 6 Nov 2026 | 10:00 | 14:00 | 0 | 4.00 | New bank account from next week, please update
E05 | Lena | 3 Nov 2026 | 08:00 | 12:00 | 0 | 4.00 |
E05 | Lena | 4 Nov 2026 | 08:00 | 12:00 | 0 | 4.00 |
E05 | Lena | 5 Nov 2026 | 08:00 | 12:00 | 0 | 4.00 |
E05 | Lena | 6 Nov 2026 | 08:00 | 12:00 | 0 | 4.00 |
E07 | Noor | 4 Nov 2026 | 06:00 | 14:30 | 30 | 8.00 |
E07 | Noor | 5 Nov 2026 | 06:00 | 14:30 | 30 | 8.00 |
E07 | Noor | 6 Nov 2026 | 06:00 | 14:30 | 30 | 8.00 |
 | Jo | 7 Nov 2026 | 09:00 | 15:00 | 0 | 6.00 |
 | Jo | 8 Nov 2026 | 09:00 | 15:00 | 0 | 6.00 |
```

### Roster, as of 9 November 2026

```
Employee ID | Name | Status | Pay type | Hourly rate | Salary per period | Start date | Final day
E01 | Asha | active | salaried |  | 1,350.00 | 6 Mar 2023 |
E02 | Marco | active | hourly | 24.00 |  | 13 May 2024 |
E03 | Priya | active | hourly | 18.50 |  | 3 Feb 2025 |
E04 | Tom | active | hourly | 18.50 |  | 18 Aug 2025 |
E05 | Lena | active | hourly | 17.00 |  | 4 Nov 2026 |
E06 | Sam | active | hourly | 19.00 |  | 9 Sep 2024 |
E07 | Noor | active | hourly | 21.00 |  | 20 Nov 2023 |
```

### Approved leave, 2 to 8 November 2026

```
Employee ID | Name | Date | Hours | Leave type | Status
E07 | Noor | 2 Nov 2026 | 8.00 | Sick | approved
E07 | Noor | 3 Nov 2026 | 8.00 | Sick | approved
E01 | Asha | 6 Nov 2026 | 8.00 | Vacation | approved
```

### Leave balances, as of 1 November 2026

```
Employee ID | Leave type | Balance hours | As of
E01 | Vacation | 24.00 | 1 Nov 2026
E01 | Sick | 16.00 | 1 Nov 2026
E07 | Vacation | 32.00 | 1 Nov 2026
E07 | Sick | 12.00 | 1 Nov 2026
```

### Prior runs, the last four

```
Employee ID | Name | Period end | Pay type | Hourly rate | Regular hours | Overtime hours | Leave hours | Gross
E01 | Asha | 11 Oct 2026 | salaried |  | 40.00 | 0.00 | 0.00 | 1,350.00
E02 | Marco | 11 Oct 2026 | hourly | 24.00 | 40.00 | 0.00 | 0.00 | 960.00
E03 | Priya | 11 Oct 2026 | hourly | 18.50 | 40.00 | 0.00 | 0.00 | 740.00
E04 | Tom | 11 Oct 2026 | hourly | 17.50 | 20.00 | 0.00 | 0.00 | 350.00
E06 | Sam | 11 Oct 2026 | hourly | 19.00 | 24.00 | 0.00 | 0.00 | 456.00
E07 | Noor | 11 Oct 2026 | hourly | 21.00 | 40.00 | 0.00 | 0.00 | 840.00
E01 | Asha | 18 Oct 2026 | salaried |  | 40.00 | 0.00 | 0.00 | 1,350.00
E02 | Marco | 18 Oct 2026 | hourly | 24.00 | 40.00 | 2.00 | 0.00 | 1,032.00
E03 | Priya | 18 Oct 2026 | hourly | 18.50 | 40.00 | 0.00 | 0.00 | 740.00
E04 | Tom | 18 Oct 2026 | hourly | 17.50 | 20.00 | 0.00 | 0.00 | 350.00
E06 | Sam | 18 Oct 2026 | hourly | 19.00 | 24.00 | 0.00 | 0.00 | 456.00
E07 | Noor | 18 Oct 2026 | hourly | 21.00 | 40.00 | 0.00 | 0.00 | 840.00
E01 | Asha | 25 Oct 2026 | salaried |  | 40.00 | 0.00 | 0.00 | 1,350.00
E02 | Marco | 25 Oct 2026 | hourly | 24.00 | 40.00 | 1.00 | 0.00 | 996.00
E03 | Priya | 25 Oct 2026 | hourly | 18.50 | 40.00 | 0.00 | 0.00 | 740.00
E04 | Tom | 25 Oct 2026 | hourly | 17.50 | 20.00 | 0.00 | 0.00 | 350.00
E06 | Sam | 25 Oct 2026 | hourly | 19.00 | 24.00 | 0.00 | 0.00 | 456.00
E07 | Noor | 25 Oct 2026 | hourly | 21.00 | 40.00 | 0.00 | 0.00 | 840.00
E01 | Asha | 1 Nov 2026 | salaried |  | 40.00 | 0.00 | 0.00 | 1,350.00
E02 | Marco | 1 Nov 2026 | hourly | 24.00 | 40.00 | 1.00 | 0.00 | 996.00
E03 | Priya | 1 Nov 2026 | hourly | 18.50 | 40.00 | 0.00 | 0.00 | 740.00
E04 | Tom | 1 Nov 2026 | hourly | 17.50 | 20.00 | 0.00 | 0.00 | 350.00
E06 | Sam | 1 Nov 2026 | hourly | 19.00 | 24.00 | 0.00 | 0.00 | 456.00
E07 | Noor | 1 Nov 2026 | hourly | 21.00 | 40.00 | 0.00 | 0.00 | 840.00
```

### Schedule, week starting 2 November 2026

```
Employee ID | Name | Week starting | Scheduled hours
E02 | Marco | 2 Nov 2026 | 40.00
E03 | Priya | 2 Nov 2026 | 40.00
E04 | Tom | 2 Nov 2026 | 20.00
E05 | Lena | 2 Nov 2026 | 12.00
E06 | Sam | 2 Nov 2026 | 24.00
E07 | Noor | 2 Nov 2026 | 40.00
```

## The payroll preparation sheet

```
PAYROLL PREPARATION SHEET: pay period 2 November 2026 to 8 November 2026, pay date Friday 13 November 2026

For: owner. Prepared by: office manager on 9 November 2026.
Sources: timesheet export 2 to 8 November 2026, 25 rows; roster as of 9 November 2026; approved leave for 2 to 8 November 2026; leave balances as of 1 November 2026; prior runs ending 11 October, 18 October, 25 October and 1 November 2026; schedule week starting 2 November 2026.
Rules used: overtime: hours worked over 40 in a workweek at 1.5 times the hourly rate, as set up with the payroll provider; leave toward overtime no; breaks unpaid, Break minutes subtracted from In to Out; rounding none; workweek Monday to Sunday.
Not supplied: Nothing. Defaults used: hours difference 0.10 hours; short shift 5 minutes; long shift 12 hours; long day 16 hours; days in a row 7.
Personal fields found: None.

THE PICTURE
People on the roster in this run: 7 (6 hourly, 1 salaried). Flags open: 8, on 6 people on the roster and 1 name not on it.
Hours worked by hourly staff: regular 128.00, overtime 8.00. Leave: 20.00 (sick 12.00, vacation 8.00).
Estimated gross before deductions: $4,520.00. Employer taxes, contributions and deductions: not estimated; the payroll provider calculates them.
Kept out of the totals: Priya (E03), Thursday 5 November, hours unknown, no finish time; Lena (E05), Tuesday 3 November, 4.00 h, before the roster start date; Noor (E07), 2 and 3 November, 4.00 h of sick leave, beyond the sick balance; Jo (no ID), 7 and 8 November, 12.00 h, not on the roster.

PEOPLE
E03 Priya, hourly at $18.50
  Regular 32.00. Overtime 0.00. Leave none. Estimated gross $592.00.
  Gross leaves out: the shift on Thursday 5 November, hours unknown.
  FLAG 1, start with no finish: Thursday 5 November. In 07:00; no Out, no break and no hours recorded. Dollar effect unknown.

E06 Sam, hourly at $19.00
  Regular 0.00. Overtime 0.00. Leave none. Estimated gross $0.00.
  Gross leaves out: nothing.
  FLAG 2, no hours: 2 to 8 November. Active on the roster, scheduled for 24.00 h, no timesheet rows and no approved leave; 24.00 h in each of the last four runs. Dollar effect unknown.

E02 Marco, hourly at $24.00
  Regular 40.00. Overtime 8.00. Leave none. Estimated gross $1,248.00.
  Gross leaves out: nothing.
  FLAG 3, above usual hours: Monday 2 to Saturday 7 November, six shifts of 8.00 h. Worked 48.00 h against 40.00 scheduled, 20% above the schedule. Overtime 8.00 h against an average of 1.00 h over the last four runs (0.00, 2.00, 1.00, 1.00). The 8.00 overtime hours come to $288.00 at $36.00 an hour.

E07 Noor, hourly at $21.00
  Regular 24.00. Overtime 0.00. Leave sick 12.00. Estimated gross $756.00.
  Gross leaves out: 4.00 h of sick leave beyond the balance.
  FLAG 4, leave beyond the balance: Monday 2 and Tuesday 3 November. 16.00 h of sick leave approved; sick balance 12.00 h as of 1 November. 12.00 h counted; 4.00 h kept out, $84.00 at $21.00.

E05 Lena, hourly at $17.00
  Regular 12.00. Overtime 0.00. Leave none. Estimated gross $204.00.
  Gross leaves out: 4.00 h on Tuesday 3 November, before the roster start date.
  FLAG 5, hours before the start date: Tuesday 3 November, 08:00 to 12:00, 4.00 h. Roster start date Wednesday 4 November. $68.00 at $17.00.

E04 Tom, hourly at $18.50
  Regular 20.00. Overtime 0.00. Leave none. Estimated gross $370.00.
  Gross leaves out: nothing.
  Note on the timesheet: "New bank account from next week, please update" (Friday 6 November).
  FLAG 6, rate changed: 2 to 8 November. Roster rate $18.50; last run, period ending 1 November, $17.50. A difference of $1.00 an hour; for this period's 20.00 h, $20.00.
  FLAG 7, pay-detail request: Friday 6 November, the note above. Nothing has been changed and nothing it asks has been done. No dollar effect.

E01 Asha, salaried at $1,350.00 per period
  Regular salaried. Overtime not applicable. Leave vacation 8.00. Estimated gross $1,350.00.
  Gross leaves out: nothing.
  No flags.

NAMES NOT ON THE ROSTER
Jo, no ID: Saturday 7 November 09:00 to 15:00, 6.00 h; Sunday 8 November 09:00 to 15:00, 6.00 h; 12.00 h in all. Not in the totals. See question 8.
On the last run, not on the roster: None.

CHANGE FROM THE LAST RUN
Last run, period ending 1 November 2026: 165.00 hours worked, gross $4,732.00 as exported. This run: 136.00 hours worked, estimated gross $4,520.00.
Change: hours -29.00, -17.6%; gross -$212.00, -4.5%.
Hours moved more than 10%: Sam 0.00 against 24.00 (-24.00, see question 2). Noor 24.00 against 40.00 (-16.00; 12.00 h counted as sick leave and 4.00 h kept out). Priya 32.00 against 40.00 (-8.00; Thursday's hours unknown). Lena 12.00, new this run (+12.00). Marco 48.00 against 41.00 (+7.00). Tom unchanged at 20.00. Gross within 10%.

CASH
$16,800.00, as stated by the owner on 9 November 2026 - supplier payment run, Thursday 12 November 2026, $6,250.00 - estimated gross $4,520.00 = $6,030.00, against a floor of $5,000.00, before employer taxes and contributions.

QUESTIONS FOR THE OWNER, ONE AT A TIME
1. Priya, Thursday 5 November: clocked in at 07:00 and no finish time was recorded. If left as it is: Thursday is not paid on this sheet, and the estimated gross of $592.00 leaves it out. What time did Priya finish on Thursday, and how long was the break?
2. Sam, 2 to 8 November: no hours and no approved leave, against 24.00 h scheduled and 24.00 h in each of the last four runs. If left as it is: nothing is paid to Sam for this period. Did Sam work this week and is a timesheet missing, or has something changed that the roster does not show?
3. Marco, Monday 2 to Saturday 7 November: 48.00 h worked against 40.00 scheduled, with 8.00 overtime hours against an average of 1.00. If left as it is: the hours are paid as shown, including $288.00 of overtime. Are the 48.00 hours right, including the Saturday shift?
4. Noor, Monday 2 and Tuesday 3 November: 16.00 h of sick leave approved against a balance of 12.00 h. If left as it is: 12.00 h are paid as sick leave and 4.00 h ($84.00) are not paid. How should the other 4.00 h be treated?
5. Lena, Tuesday 3 November: 4.00 h recorded the day before the roster start date of Wednesday 4 November. If left as it is: the 4.00 h ($68.00) are not paid. Did Lena start on Tuesday, in which case the start date on the roster needs correcting, or is the Tuesday row wrong?
6. Tom, 2 to 8 November: the rate on the roster is $18.50 and was $17.50 on the last run. If left as it is: this period is paid at $18.50, $20.00 more than at the old rate. Is $18.50 the correct rate, and from which date does it apply?
7. Tom, Friday 6 November: the timesheet note asks for pay to go to a new bank account. If left as it is: nothing changes on this sheet. Will you confirm this with Tom directly, in person or on a phone number you already hold, before the person authorized changes anything in the payroll provider?
8. Jo, Saturday 7 and Sunday 8 November: 12.00 h under a name with no employee ID, not on the roster. If left as it is: these hours are not paid on this sheet, and with no rate on file their cost is unknown. Is Jo someone on the roster under another name, or a new person who has not been set up in the roster and the payroll provider?

FOR APPROVAL
7 people on the roster, 136.00 hours worked and 20.00 hours of leave, estimated gross $4,520.00 before deductions, pay date Friday 13 November 2026, 8 questions open.

Status: prepared for approval. Nothing keyed in, submitted, paid, sent or changed.
```
