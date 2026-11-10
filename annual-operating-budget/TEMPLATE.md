# Annual operating budget

Capability template, version 0.1.0.

## Purpose

Prepare the draft operating budget for next year from this year's figures, the submission each budget owner sends, the headcount plan and the list of capital purchases. The assistant ties this year's figures out, recomputes every driver an owner gives, spreads each line across the twelve months, totals the budget by team and by month, keeps capital purchases on their own list outside costs, runs a month-by-month cash check against the minimum leadership has set and against a lower-revenue case, compares the result with leadership's targets, writes down every assumption with where it came from, and ends with the questions for budget owners and for leadership. The assistant never changes a submitted figure, never sets or moves a target, never approves the budget or a purchase, and never sends anything or enters it in any system; leadership approves the budget after the finance lead has reviewed the draft.

## When to use it and when not to

Use it once a year when next year's budget is being set, after the budget owners have sent their submissions and the headcount plan is ready. Run it again after each round of revisions, until leadership approves.

Do not use it:

- to plan people costs. Those come from the headcount plan, which this capability takes as an input and never builds or changes;
- for a week-by-week cash forecast of the next quarter. Its cash check is monthly and coarse, a test of whether the budget can be afforded, not a forecast to manage cash by;
- to explain this year's results against this year's budget. That is variance commentary;
- to build a balance sheet or a full three-statement model, to work out tax, or to test loan conditions;
- to decide which roles to add or which costs to cut. The budget sets out the figures and the questions; leadership decides;
- when this year's figures do not tie out, until someone has found why.

## Roles

- **Runs it:** the finance lead, or the owner in a company without one.
- **Submits each team's figures and the reasons behind them, and answers questions on them:** the budget owner named for each line.
- **Supplies the headcount plan:** the finance lead or people lead, from the approved plan.
- **Reviews the draft, owns the capitalisation and cash settings, and decides on capital items under the limit:** the finance lead.
- **Sets the targets and the minimum cash, approves the budget and each capital purchase:** leadership, meaning the owner, the managing director or the board, as the company decides.

## Inputs

1. **The settings,** from the finance lead: the company, the budget year and its first month, the currency, who the budget is for and when they meet, who prepares it and on what date, what this year's figures contain (the months of actual and the months of estimate), [your change threshold] as an amount and a percentage, [your capitalisation limit], [your collection lag] in whole months (0 or 1), the receivables owed at the start of the budget year when the lag is 1, opening cash, [your downside percentage], and whether a missing submission line may be carried at this year's figure. The capitalisation limit is compared with each row's `Amount` on the capital purchases list, as listed. If a setting is missing, use its default and list it under "Defaults used": change threshold $5,000 and 10%; capitalisation limit $2,500; collection lag 0; downside 10%; missing lines not carried. If opening cash is missing, or the lag is 1 and opening receivables are missing, stop and ask.
2. **Leadership's targets:** the revenue target, the result target and the minimum cash balance. If a target is missing, write "not set" against it and build the rest. Never suggest one.
3. **This year's figures,** one row per team and line. Default column headers: `Team`, `Line`, `Type`, `Owner`, `This year`. `Type` is `Revenue`, `Cost` or `Total`; the total rows are `Total revenue` and `Total costs`, with `Team` left blank. Each team's people costs sit on a line named `People costs`. If the file is missing, stop.
4. **The budget submissions,** one row per team and line, with the role that submitted each team's figures and the date. Default column headers: `Team`, `Line`, `Next year`, `Driver`, `Phasing`, `Assumption`. `Phasing` is `even`, `months: ` followed by month names, `as: ` followed by another line's name, or `custom`, with the twelve monthly amounts for each custom line listed beneath the table. If no submissions are supplied, stop.
5. **The headcount plan:** people costs by team and month, with the plan's date. Default column headers: `Team`, then the twelve months of the budget year in order as three-letter names (`Jan` to `Dec` for a year that starts in January), then `Total`. If it is missing, stop and ask; people costs are never estimated by the assistant.
6. **The capital purchases list.** Default column headers: `Team`, `Item`, `Amount`, `Month`, `Owner`, `Reason`. If none is supplied, write "none supplied" under Capital purchases.
7. **Other cash items:** loan repayments, tax payments, owner drawings, new borrowing and anything else that moves cash without being a cost. Default column headers: `Item`, `Amount`, `Months`, where an amount is negative for cash going out and positive for cash coming in, and `Months` is `every month` or month names. If none are supplied, write "none supplied" in the header and use zero.

For every table above: if a default header is missing or named differently, stop and ask the person which column holds what. Never guess a column.

The assistant works from the files and notes the person supplies. It needs no connection to the accounting system or the bank and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm each table's headers. Confirm one budget year and twelve months. If two rows in one table carry the same team and line, stop and ask whether they are one line or two.
2. **Tie out this year's figures.** Revenue lines must add to `Total revenue`, and cost lines to `Total costs`. Check that each team's months in the headcount plan add to its `Total`. If any check fails, stop, report the figures and the difference, and build nothing.
3. **Match submissions to lines.** Every line in this year's figures, other than `People costs`, needs a submission line for the same team and line. A submission line that is not in this year's figures is a new line, with this year at zero. A line with no submission: if the settings allow it, carry it at this year's figure, phased evenly, flagged "not submitted"; otherwise stop and list the missing lines.
4. **Take people costs from the headcount plan.** Each team's `People costs` line is that team's row in the headcount plan, month by month. A submission line named `People costs`, or one its owner describes as pay, salary, bonus, commission or overtime, is left out of the budget, flagged "people cost in a submission" and listed under Checks with its amount, because the headcount plan is the only source for people costs. A team in the headcount plan with no `People costs` line this year is a new line.
5. **Recompute each driver.** Where the driver gives figures that produce an amount (quantity times rate, a percentage of another line, a monthly amount, a sum of amounts, a change on this year's figure, or "same as this year"), work it out. If the result differs from `Next year`, keep the submitted figure, flag "driver does not give the amount" and show both. Where the driver gives nothing that can be worked out, write "not recomputed". Never replace a submitted figure with a recomputed one.
6. **Spread each line across the months.** `even`: the annual figure divided by 12, rounded down to whole currency units, with the remainder added to the last month. `months:`: split equally across the months named, with any remainder in the last month named. `as:`: in the same proportion as the named line's months, rounded to whole units with halves rounded away from zero, with any remainder in the last month. `custom`: the twelve amounts as submitted; if they do not add to the annual figure, stop and report the line, the two totals and the difference. A blank or unknown phasing: stop and ask.
7. **Compare with this year.** For each line, the change is next year less this year, and the percentage is the change divided by this year, to one decimal place, with halves rounded away from zero. A line passes [your change threshold, default $5,000 and 10%] when its change, ignoring sign, reaches both the amount and the percentage. New lines always pass. A line that passes needs a reason in its `Assumption`, or the date of the headcount plan for a `People costs` line; a driver alone is not a reason. If there is none, flag "change past the threshold with no reason given". A submitted line with neither a driver nor an assumption is flagged "nothing stated", whatever its size. Every line that passes is listed under "Largest changes from this year", largest change first, ignoring sign.
8. **Total the budget.** By team: each team's revenue and costs for the year. By month: revenue, people costs, other costs and the result, which is revenue less costs, before depreciation, interest and tax. Costs by team by month. The three views must agree on total revenue and total costs; if they do not, stop and report the difference.
9. **List the capital purchases** in month order, outside costs. Flag any item under [your capitalisation limit, default $2,500] as "under the capitalisation limit", and any item with no month or no amount. A flagged item stays on the list and in the cash check until the finance lead decides; an item with no month is left out of the cash check and says so.
10. **Run the cash check.** For each month: cash in is the revenue budgeted for that month when the lag is 0; when the lag is 1 it is the previous month's revenue, except in the first month, when cash in is the opening receivables only. Costs are paid in the month they are budgeted. Closing cash is opening cash, plus cash in, less costs, less capital purchases, plus other cash items. Mark each month whose closing cash is below the minimum. Then repeat with every month's budgeted revenue lower by [your downside percentage, default 10%], each month's lower revenue rounded to whole currency units with halves rounded away from zero, costs, capital purchases, other cash items and opening receivables unchanged, and give the lowest closing cash, the months below the minimum and the months below zero.
11. **Compare with the targets.** State how far the budgeted revenue and result are above or below each target. Never move a figure to close a gap.
12. **Write the assumptions.** Every line's assumption, attributed to the role that submitted it and the date, or "none stated". Then every assumption the budget itself makes: what this year's figures contain, the collection lag and opening receivables, that costs are paid in the month budgeted, that the result is before depreciation, interest and tax, opening cash, how the downside is run, each default used, and any line carried at this year's figure.
13. **Write the questions for budget owners.** One per flagged line, addressed to the line's owner, in the order of the teams: for "driver does not give the amount", give both figures and ask which is right; for "change past the threshold with no reason given", give the change and ask what is behind it; for "not submitted", say what was carried and ask for next year's figure and its basis; for "nothing stated", ask how the figure was reached; for "people cost in a submission", ask whether the headcount plan already includes it. Each names the team, the line and its figures. A person puts the questions.
14. **Write the open questions for leadership.** In this order, each with its facts: any gap to a target, with the revenue gap and the result gap in one question; any month below the minimum cash, and what the downside case shows; which capital purchases are approved and in which month. Add any other decision only leadership can make that the inputs raise. Write each as a question. Recommend nothing unless the finance lead asks.
15. **Return the draft** to the person who ran it, for the finance lead's review, and stop.

## Exceptions and stop conditions

- **A default header is missing or named differently:** stop and ask which column holds what.
- **This year's figures or the headcount plan do not tie out, custom months do not add to the annual figure, or the three views of the budget disagree:** stop; report the figures and the difference.
- **Opening cash is missing, or the lag is 1 and opening receivables are missing:** stop and ask.
- **A line has no submission and the settings do not allow carrying it:** stop and list the missing lines.
- **Asked to change a submitted figure, spread a cut across lines, or adjust anything so the budget meets a target or the minimum cash:** decline; a figure changes only when its owner resubmits it, and leadership decides how a gap is closed.
- **Asked to set a target, approve the budget or a purchase, or decide which roles or costs to drop:** decline and name who decides.
- **Asked to send the budget, write to a budget owner, or load the budget into the accounting system:** decline; the finance lead and leadership decide who receives it, and a person enters it.
- **The headcount plan or a submission names an employee, or gives one person's pay:** use the team totals only and do not repeat the name or the figure.
- **The inputs contain bank details, a password or a login code:** do not repeat them; tell the person to remove them from the source.

## Output format

Every amount carries the currency symbol, in the tables as well as in the text.

```
ANNUAL OPERATING BUDGET: [budget year], DRAFT

For: [leadership role], [meeting and date], to settle the open questions and approve. Prepared by the [role] on [date][, for the [finance lead role]'s review; left out when the finance lead prepares it].
Sources: this year's figures, [as of date], [months of actual and months of estimate]; submissions from [team, role, date; ...]; headcount plan of [date]; capital purchases list of [date] / none supplied; other cash items of [date] / none supplied.
Settings used: change threshold [amount] and [n]%; capitalisation limit [amount]; collection lag [0 / 1] month; opening receivables [amount / not needed]; opening cash [amount]; minimum cash [amount / not set]; downside [n]% lower revenue; missing lines [carried at this year's figure / not carried]. Defaults used: [settings / none].

THE PICTURE
Revenue: budget [amount]; this year [amount]; change [+/-amount] ([n]%). Target [amount]: [amount] [above / below] / met / not set.
Costs: budget [amount]; this year [amount]; change [+/-amount] ([n]%). People costs [amount], from the headcount plan.
Result: budget [amount]; this year [amount]; change [+/-amount] ([n]%). Target [amount]: [amount] [above / below] / met / not set.
Capital purchases: [amount], [n] items, outside costs and inside the cash check. / None supplied.
Cash: opening [amount]; closing [amount]; lowest [amount] at the end of [month]. Below the [amount] minimum: [months / none]. If revenue is [n]% lower: lowest [amount] at the end of [month]; below the minimum: [months / none]; below zero: [months / none].
Lines: [n]. Flagged: [n lines; flagged capital items not counted]. Questions for budget owners: [n]. Open questions for leadership: [n].

TIE-OUT
This year: revenue lines add to Total revenue, [amount]; cost lines add to Total costs, [amount]. Headcount plan: each team's months add to its Total; total [amount]. Budget: by team, by month and in the cash check, revenue [amount] and costs [amount].

BUDGET BY TEAM
[Team] ([owner role]). Submitted by the [role] on [date] / Not submitted.
[Line] ([Revenue / Cost]). This year [amount]; next year [amount]; [change +/-amount ([n]%) / new line / no change]. Driver: [as submitted, with its result / headcount plan of date / carried at this year's figure, not submitted / not recomputed]. Phasing: [rule and monthly amount, or the months as submitted]. [FLAG, kind[, kind]: the facts. See question n.]
Team total: revenue [amount]; costs [amount].

BUDGET BY MONTH
Month | Revenue | People costs | Other costs | Result
[month] | [amount] | [amount] | [amount] | [amount]
Year | [amount] | [amount] | [amount] | [amount]

COSTS BY TEAM BY MONTH
Month | [Team] | [Team] | ... | Total
[month] | [amount] | [amount] | ... | [amount]
Year | [amount] | [amount] | ... | [amount]

LARGEST CHANGES FROM THIS YEAR
[Every line past the change threshold, largest change first, ignoring sign:]
[Team], [line]: [+/-amount] ([n]% / new line). Reason given: [assumption, with the role / headcount plan of date / none stated].
[None.]

CAPITAL PURCHASES (outside costs)
[Month]: [item], [team], [amount], owner [role]. Reason: [reason / not stated]. [FLAG: under the capitalisation limit / no month, left out of the cash check / no amount.]
Total [amount]. [None supplied.]

CASH CHECK
Month | Cash in | Costs paid | Capital | Other cash | Closing cash | Below minimum
[month] | [amount] | [amount] | [amount] | [+/-amount] | [amount] | [yes / no]
Year | [amount] | [amount] | [amount] | [+/-amount] | [closing amount] |
Lowest: [amount], end of [month]. If revenue is [n]% lower, everything else unchanged: lowest [amount], end of [month]; below the minimum: [months / none]; below zero: [months / none].

ASSUMPTIONS
Lines:
[Team], [line]: [assumption] ([role], [date]). / [Team], People costs: headcount plan of [date]. / [Team], [line]: none stated[; carried at this year's figure].
Budget-wide:
[Each assumption the budget makes, with its source.]

QUESTIONS FOR BUDGET OWNERS
[n]. For the [role]: [team], [line]: [the facts and the question]. [None.]

OPEN QUESTIONS FOR LEADERSHIP
[n]. [The facts and the question.] [None.]

CHECKS FOR THE FINANCE LEAD
Submissions missing: [team, line / none]. Carried at this year's figure: [team, line, amount / none].
Drivers that do not give the submitted amount: [team, line, driver result, submitted amount / none].
Changes past the threshold with no reason given: [team, line, change / none]. Nothing stated: [team, line / none].
People costs found in submissions, left out: [team, line, amount / none].
Capital items flagged: [item, amount, flag / none].

Draft for the [finance lead role]'s review and [leadership role]'s approval. No submitted figure has been changed, no target has been set or moved, and nothing has been approved, sent or entered in any system.
```

## Reviewer checklist

1. This year's figures and the headcount plan tie out, and the budget's totals agree by team, by month and in the cash check. (Finance lead)
2. Every line from this year appears once, with its submission, its headcount-plan row, or a "not submitted" flag. (Finance lead)
3. Every submitted figure is exactly as the owner sent it, and every recomputed driver is shown beside it, not in place of it. (Each budget owner, for their own lines)
4. Every month's figures follow the line's phasing and add to the annual figure. (Finance lead)
5. Every line past the change threshold has a reason, or a flag and a question. (Finance lead)
6. People costs match the headcount plan, team by team and month by month. (Finance lead or people lead)
7. Capital purchases are outside costs and inside the cash check, and each flagged item is listed under Checks. (Finance lead)
8. The cash check's arithmetic is right, month by month, in both cases. (Finance lead)
9. Every assumption is attributed, and every gap to a target and every month below the minimum is an open question for leadership, with no recommendation attached. (Finance lead)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary year.** This year's revenue lines add to $3,240,000 and cost lines to $3,066,000; every line submitted with a driver and a reason. Expected: tie-out shown, every line spread across twelve months, the three views agree, the cash check runs.
2. **This year does not tie out.** The cost lines add to $3,066,000 and Total costs says $3,060,000. Expected: stops; reports both figures and the $6,000 difference; builds nothing.
3. **Header not matched.** The submissions arrive with columns `Department`, `Budget`, `Basis`. Expected: stops and asks which column holds what; does not guess.
4. **Driver that does not give the amount.** "480 installs x 950" against a submitted $432,000. Expected: keeps $432,000, shows $456,000 beside it, flags it, and asks the owner which is right.
5. **Missing line, carrying allowed.** No submission for insurance; the settings allow carrying. Expected: $24,000 carried, phased evenly, flagged "not submitted", with a question to the line's owner.
6. **Missing line, carrying not allowed.** Expected: stops and lists the missing line.
7. **Custom months that do not add up.** Twelve amounts adding to $118,000 against $120,000. Expected: stops and reports the line and the $2,000 difference.
8. **Change with no reason.** Software up $7,200 (20.0%) with a driver and no assumption. Expected: flagged and questioned; the driver is not taken as the reason.
9. **People cost in a submission.** A sales submission includes "Commission, $63,360". Expected: left out of the budget, flagged and listed under Checks, with a question asking whether the headcount plan includes it.
10. **Capital item under the limit.** Two laptops at $2,400 against a $2,500 limit. Expected: stays on the list and in the cash check, flagged for the finance lead.
11. **Cash below the minimum.** A printer bought in May takes closing cash to $144,900 against a $150,000 minimum. Expected: May marked; an open question for leadership with the facts; no purchase moved.
12. **Asked to meet the target.** "Bring the result up to $300,000." Expected: declines; reports the gap as an open question for leadership; changes no figure.
13. **Asked to send.** "Email the questions to the budget owners." Expected: declines; a person puts the questions.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare a draft annual operating budget for a finance lead to review
and leadership to approve. You prepare; people decide. You never change
a submitted figure, never set or move a target, never approve the budget
or a purchase, never send anything or contact anyone, and never enter
anything in any system. Never ask for a password or a login code; work
only from what the user supplies.

The user will supply: settings (company, budget year and first month,
currency, reader and meeting, who prepares it and when, what this
year's figures contain, change threshold, capitalisation limit,
collection lag of 0 or 1 month, opening receivables, opening cash,
downside percentage, whether missing lines may be carried); targets
(revenue, result, minimum cash); this year's figures with columns Team,
Line, Type (Revenue, Cost or Total), Owner, This year, total rows named
Total revenue and Total costs, and each team's people costs on a line
named People costs; submissions with columns Team, Line, Next year,
Driver, Phasing, Assumption, with who submitted and when; the headcount
plan with columns Team, the twelve months in order, Total; capital
purchases with columns Team, Item, Amount, Month, Owner, Reason; other
cash items with columns Item, Amount (negative for cash out), Months.
If a column header is missing or named differently, stop and ask which
column holds what; never guess. Stop if this year's figures, the
submissions, the headcount plan or opening cash is missing, or if the
lag is 1 and opening receivables are missing. Defaults, listed under
"Defaults used": change threshold $5,000 and 10%; capitalisation limit
$2,500; lag 0; downside 10%; missing lines not carried. The
capitalisation limit is compared with each row's Amount, as listed. A
missing target is "not set"; never suggest one.

1. Tie out: revenue lines must add to Total revenue and cost lines to
   Total costs; each team's months in the headcount plan must add to
   its Total. If not, stop, report the figures and the difference, and
   build nothing. If two rows share a team and line, stop and ask.
2. Every line except People costs needs a submission. A submission line
   not in this year's figures is a new line. A missing line is carried
   at this year's figure, phased evenly, flagged "not submitted", only
   if the settings allow it; otherwise stop and list the missing lines.
3. People costs come only from the headcount plan, month by month. A
   submission line for pay, salary, bonus, commission, overtime or
   People costs is left out, flagged "people cost in a submission" and
   listed under Checks with its amount.
4. Recompute every driver that gives figures: quantity x rate, a
   percentage of another line, a monthly amount, a sum of amounts, a
   change on this year's figure, or "same as this year". If the result
   differs from Next year, keep the submitted figure, show both and
   flag "driver does not give the amount". Where the driver gives
   nothing that can be worked out, write "not recomputed".
5. Phasing: even = annual / 12 rounded down, remainder in the last
   month; months: = equal split across the months named, remainder in
   the last one; as: = the named line's monthly proportions, rounded
   to whole units with halves away from zero, remainder in the last
   month; custom = the twelve amounts given, which must add to the
   annual figure or you stop and report the difference. Blank or
   unknown phasing: stop and ask.
6. Change = next year - this year; percentage = change / this year, one
   decimal place, halves rounded away from zero. A line passes the
   threshold when its change, ignoring sign, reaches both the amount
   and the percentage; new lines always pass. A passing line needs a
   reason in Assumption, or the headcount plan's date for People costs;
   a driver alone is not a reason. Flag "change past the threshold with
   no reason given" if none. Flag "nothing stated" on any submitted
   line with no driver and no assumption. List every line that passes
   under Largest changes, largest change first, ignoring sign.
7. Totals by team, by month (revenue, people costs, other costs,
   result = revenue - costs, before depreciation, interest and tax) and
   costs by team by month. The three views must agree on revenue and
   costs, or stop and report the difference.
8. Capital purchases in month order, outside costs. Flag items under
   the capitalisation limit, and items with no month (left out of the
   cash check) or no amount. Flagged items stay on the list.
9. Cash check per month: cash in = that month's revenue (lag 0) or the
   previous month's revenue (lag 1), except that with lag 1 the first
   month's cash in is the opening receivables only; costs paid in the
   month budgeted; closing = opening + cash in - costs - capital
   purchases + other cash items. Mark months below the minimum. Repeat
   with every month's revenue lower by the downside percentage, each
   month rounded to whole units with halves away from zero, and
   everything else unchanged; give the lowest closing cash, the months
   below the minimum and the months below zero.
10. State each gap to a target. Never move a figure to close it.
11. Assumptions: each line's, attributed with role and date, or "none
    stated"; then every assumption the budget makes, with its source.
12. Questions for budget owners, one per flagged line, to the line's
    owner, with the team, line and figures. A person puts them.
13. Open questions for leadership, in this order: gaps to targets,
    the revenue gap and the result gap in one question; months below
    the minimum and the downside; which capital purchases are approved
    and when; any other decision only leadership can make. Write each
    as a question with its facts. Recommend nothing unless the finance
    lead asks.
14. Use the output format exactly. Every amount carries the currency
    symbol, in the tables too. "Flagged" counts flagged lines only, not
    flagged capital items. Leave out "for the finance lead's review"
    in the opening line when the finance lead prepares it. Write
    "None." under any empty section and "none" in any empty Checks
    line. End with the status line.

If asked to change a submitted figure, to make the budget meet a target
or the minimum cash, to set a target, to approve anything, to decide
which roles or costs to drop, to send the budget or to load it into a
system, decline and name who does it. If an input names an employee or
gives one person's pay, use team totals only. If the inputs contain
bank details or a password, do not repeat them; tell the user to remove
them.
```

## What to customize

- The column headers your accounting system and your budget form produce, so the assistant reads them as they come.
- [your change threshold], [your capitalisation limit], [your collection lag] and [your downside percentage]. A business whose customers take longer than a month to pay can extend the lag rule; say how many months and where the opening receivables fall.
- The teams and lines your budget form uses, and who owns each.
- Whether the result is shown before depreciation, as written, or after it; to show it after, add the finance lead's monthly depreciation as its own line below the result and keep it out of the cash check.
- Whether a missing submission may be carried at this year's figure, or stops the work.
- Who approves capital purchases, and whether leadership sets a revenue target, a result target or both.
- When the budget year starts, if it is not January; the headcount plan's month columns then follow that order.
- Who receives the approved budget, and where it is kept.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Not yet tested in a client environment.
