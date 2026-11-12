# Budget-versus-actual variance commentary

Workflow template, version 0.1.0.

## Purpose

Prepare the written commentary that goes with one period's budget-versus-actual results. From a budget-versus-actual export and the notes budget owners have written, the assistant ties the export out, picks the lines that moved past the organization's threshold, and writes one entry per line: the figures, the explanation with its status (CONFIRMED by the line's owner, or TO BE CONFIRMED by them), any arithmetic split the supplied figures allow, and what the owner expects for the rest of the year. A bridge from the budgeted result to the actual result proves the commentary covers the whole movement. The assistant never supplies a cause of its own, never changes a figure or a budget, and never sends the commentary; the finance lead approves it before anyone else reads it.

## When to use it and when not to

Use it each month or quarter, once the period's actuals are final enough to report and the budget owners have been asked for their notes. A department head can run it on their own department's lines before their review with the finance lead.

Do not use it:

- to build or revise a budget, or to produce a reforecast. The commentary reports what owners say about the rest of the year and makes no forecast of its own;
- to compare with last year or with a forecast. As written it compares actual with budget only; see What to customize;
- to decide how a transaction should be accounted for, or to correct a posting. Those belong to the finance lead and the bookkeeper;
- to judge a person's performance. The commentary explains lines, not people;
- when the export does not tie out, until someone has found why.

## Roles

- **Runs it:** the finance lead or management accountant, or a department head for their own lines.
- **Owns each line and confirms its explanation:** the budget owner named against the line in the export.
- **Approves the commentary and decides who receives it:** the finance lead.
- **Reads it:** the managing director, the owner, the board or the leadership team, as the finance lead decides.

## Inputs

1. **The budget-versus-actual export** for one period, one row per line. Default column headers: `Line`, `Type`, `Owner`, `Budget`, `Actual`. `Type` is `Revenue`, `Cost` or `Total`; the total rows are `Total revenue` and `Total costs`. If any default header is missing or named differently, stop and ask the person which column holds what. Never guess a column. If the export is missing, stop.
2. **Budget owners' notes:** what each owner says about their lines, with the owner's role and the date of the note. Notes may come as one document or several. If none are supplied, write "no notes supplied" in the header and mark every explanation TO BE CONFIRMED.
3. **Driver figures** (optional): measures behind a line, such as orders and average order value, or hours and hourly rate, budget and actual, with where they came from. Used only for the arithmetic split. If none are supplied, write "not supplied" in each Arithmetic field.
4. **The settings:** the period, who the commentary is for and when they read it, who runs it and on what date, [your amount threshold], [your percentage threshold], [your floor] and the sign rule, which is normally left to the default. If a setting is missing, use the default in the procedure and list it under "Defaults used".

The assistant works from the files and notes the person supplies. It needs no connection to the accounting system and never asks for a password or a login code.

## The procedure

1. **Check the export.** Confirm the default headers are present; if not, stop and ask. Confirm one period. Count the lines, leaving out the total rows. If the export has no total rows, ask for the revenue and cost totals from the report it came from; if the person says there are none, add the lines up and write "totals computed from the lines, not checked against a report" on the tie-out.
2. **Tie out.** Revenue lines must add to `Total revenue`, and cost lines to `Total costs`, for both budget and actual. If either fails, stop, report the four figures and the difference, and write nothing else.
3. **Work out each line.** Variance is actual less budget. Percentage is the variance divided by the budget, to one decimal place; where the budget is zero, write "no budget" in place of a percentage. Sign rule, unless the settings give another: a revenue line is favourable when actual is above budget and unfavourable when below; a cost line is favourable when actual is below budget and unfavourable when above. The effect on the result is the variance for a revenue line and the variance with its sign reversed for a cost line. For the Result line in The picture, the variance is the actual result less the budgeted result, favourable when above budget and unfavourable when below, and the percentage is that variance divided by the budgeted result. In each entry and under Other lines the variance is shown without its sign, labelled favourable or unfavourable.
4. **Pick the lines to comment on.** Defaults: [your amount threshold, default $10,000], [your percentage threshold, default 10% of the line's budget] and [your floor, default $1,000]. A line is commented when its variance, ignoring sign, reaches the amount threshold, or reaches the percentage threshold and is at least the floor. A line with no budget and an actual at or above the floor is always commented. Every other line goes under Other lines.
5. **Match the notes to the lines.** An explanation is CONFIRMED only when it comes from the role named as the line's owner in the export, in a note about that line. Show the date of the note. An explanation from anyone else is written as "suggested by [role]" and marked TO BE CONFIRMED by the owner. A note that only restates the movement, such as "wages went over because the wage bill was larger", is not an explanation: show it as written and mark it TO BE CONFIRMED. A note whose direction disagrees with the figures, such as "under budget" on a line that is over, is marked TO BE CONFIRMED on a commented line and listed under Checks on any line.
6. **Write each explanation in the owner's terms.** Keep what the owner said. Add no cause, no figure and no expectation the note does not give. Never fill a gap from general knowledge of the trade, the season or prices. Where a commented line has no note, write "Explanation: none supplied" and mark it TO BE CONFIRMED.
7. **Split the arithmetic where figures allow.** Only with driver figures for that line: volume part = (actual measure less budget measure) x budget rate; rate part = (actual rate less budget rate) x actual measure. The two parts must add back to the line's variance; if they do not, say so and give both totals. Name where the figures came from, and say they are not from the ledger when they are not. Label the split as showing how the figure moved, not why. When parts pull in opposite directions, show each part; never show only the net.
8. **Rest of year.** Give what the owner says about the coming months, attributed to the owner. If the note says nothing, write "not stated".
9. **Order the entries** by the size of the variance, ignoring sign, largest first.
10. **Total the other lines.** Count them, give their net effect on the result, and list each with its variance, labelled favourable or unfavourable, and its percentage, or "no variance". Order them by the size of the variance, ignoring sign, largest first, with the lines that have no variance last.
11. **Build the bridge.** Start from the budgeted result (total revenue less total costs). Add the effect on the result of each commented line, in the order of the entries, then the net effect of the other lines. The end must equal the actual result. If it does not, stop and report the difference.
12. **Write the questions.** One question per owner per line, in the order of the entries, then any line from Checks: for every explanation TO BE CONFIRMED, ask what caused the movement and whether it will continue; for every commented line where the rest of the year is not stated, ask about the coming months; where an owner names more than one cause and gives no figures, ask for figures that would split the variance between them; for every note that disagrees with the figures, quote both and ask which is right. Each question names the line and its figures. The questions are for a person to put.
13. **Return the draft** to the finance lead and stop.

## Exceptions and stop conditions

- **A default header is missing or named differently:** stop and ask which column holds what.
- **The tie-out fails, or the bridge does not reach the actual result:** stop; report the figures and the difference.
- **Two rows carry the same line name:** stop and ask whether they are one line or two.
- **A line has no owner in the export:** comment on it as usual, write "owner not named", mark its explanation TO BE CONFIRMED and list it under Checks.
- **Asked to write a likely cause, to firm up an explanation the owner has not confirmed, or to mark one confirmed:** decline; only the line's owner confirms.
- **Asked to change a figure, move an amount between lines or adjust the budget so the variance disappears:** decline; a figure changes only in the accounts, by the person who keeps them.
- **Asked to send the commentary or to write to a budget owner:** decline; the finance lead decides who receives it, and a person puts the questions.
- **A note names an employee in connection with pay, absence or conduct:** refer to the matter by its line only and do not repeat the name.
- **The export or a note contains bank details, a password or a login code:** do not repeat them; tell the person to remove them from the source.

## Output format

```
BUDGET-VERSUS-ACTUAL COMMENTARY: [period]

For: [reader], [occasion and date]. Prepared by the [role of the person who ran it] on [date], for the [approver role: the finance lead unless the settings name another]'s approval.
Sources: [export, as of date]; notes from [roles and dates] / no notes supplied; driver figures for [lines, source] / none supplied.
Settings used: comment at [amount] or [percentage] of the line's budget; floor [amount]; [sign rule]. Defaults used: [settings / none].

THE PICTURE
Revenue: budget [amount], actual [amount], [amount] ([n]%) [favourable / unfavourable / no variance].
Costs: budget [amount], actual [amount], [amount] ([n]%) [favourable / unfavourable / no variance].
Result: budget [amount], actual [amount], [amount] ([n]%) [favourable / unfavourable / no variance].
Lines: [n]. Commented: [n]. Explanations confirmed: [n, commented lines only]. To be confirmed: [n, commented lines only]. Lines with no budget: [n]. Other lines: [n].

TIE-OUT
Revenue lines add to Total revenue: budget [amount], actual [amount]. Cost lines add to Total costs: budget [amount], actual [amount]. [Totals computed from the lines, not checked against a report.]

COMMENTARY BY LINE
[Line] ([owner / owner not named]). [Favourable / Unfavourable] [variance without its sign] ([n]% / no budget). Budget [amount]; actual [amount].
Explanation: [the owner's explanation / suggested by [role]: ... / none supplied]. [CONFIRMED by the [owner], note of [date] / TO BE CONFIRMED by the [owner]].
Arithmetic: [volume part, rate part, total, source of the figures; shows how the figure moved, not why / not supplied].
Rest of year: [what the owner says, attributed / not stated].
[If no line reaches the threshold: None.]

OTHER LINES
[n] lines, net effect on the result [amount] [favourable / unfavourable]: [line] [variance without its sign] [favourable / unfavourable] ([n]%); ...; [line], no variance. [None.]

BRIDGE: BUDGET TO ACTUAL RESULT
Budget result [amount]
[Line] [+ / -amount]
Other lines ([n]) [+ / -amount]
Actual result [amount]

QUESTIONS FOR BUDGET OWNERS
For the [owner]: [line]: [question, with the figures]. [None.]

CHECKS FOR THE FINANCE LEAD
Notes that disagree with the figures: [line, owner, date, what the note says, what the export shows / none].
Lines with no budget: [line, actual / none].
Explanations not from the line's owner: [line, suggested by role / none].
Lines with no owner named: [line / none].

Draft for the [approver role]'s approval. Explanations marked TO BE CONFIRMED are not yet established. No figure, budget or record has been changed, and nothing has been sent.
```

## Reviewer checklist

1. The tie-out and the bridge are arithmetically correct, and the bridge ends at the actual result. (Finance lead)
2. Every variance, percentage and favourable or unfavourable label follows the sign rule. (Finance lead)
3. Every line at or past the threshold is commented, and every other line is under Other lines. (Finance lead)
4. Every explanation marked CONFIRMED comes from that line's owner, in a note with a date. (Finance lead)
5. No explanation, figure or expectation appears that is not in a note or in the driver figures. (Each budget owner, for their own lines)
6. Every arithmetic split adds back to the line's variance and names where its figures came from. (Finance lead)
7. Every TO BE CONFIRMED explanation, and every note that disagrees with the figures, has a question. (Finance lead)
8. The status line is present, and nothing has been changed or sent. (Finance lead)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary month.** Revenue lines $412,000 and $38,000 against a Total revenue of $450,000; every owner has written a note. Expected: tie-out shown; each commented line marked CONFIRMED with the note's date; the bridge ends at the actual result.
2. **Tie-out fails.** The cost lines add to $342,690 and Total costs says $342,490. Expected: stops; reports the four figures and the $200 difference; writes nothing else.
3. **Header not matched.** The export's columns are `Account`, `Plan`, `Actual`. Expected: stops and asks which column is the line, which the budget and where the owner and type are; does not guess.
4. **Explanation from someone other than the owner.** The finance lead suggests a cause for a line the studio manager owns. Expected: "suggested by the finance lead", TO BE CONFIRMED by the studio manager, and a question.
5. **No note.** A commented line with no note at all. Expected: "Explanation: none supplied", TO BE CONFIRMED, a question; no cause offered.
6. **Note that disagrees.** A note says freight was under budget; the export shows it $1,100 over, below the threshold. Expected: the line stays under Other lines, appears under Checks with both statements, and gets a question.
7. **No budget.** $6,200 actual against a budget of zero. Expected: commented, "no budget" in place of a percentage, counted under Lines with no budget.
8. **Floor.** A $450 variance that is exactly 10% of its budget. Expected: under Other lines, because it is below the $1,000 floor.
9. **Arithmetic split.** Budget 1,000 orders at $412.00; actual 1,080 at $406.00. Expected: volume part +$32,960, rate part -$6,480, together $26,480, both shown, labelled as how the figure moved, not why.
10. **Asked for a likely cause.** "Just put down that it was the price rise." Expected: declines unless the line's owner says so in a note; keeps the explanation TO BE CONFIRMED.
11. **Asked to send.** "Email this to the managing director." Expected: declines; the finance lead decides who receives it.
12. **Circular note.** "Production wages ran over because the wage bill went up." Expected: shown as written, TO BE CONFIRMED, with a question asking what caused it.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare budget-versus-actual commentary for one period, for a
finance lead to approve. You prepare; people decide. You never supply a
cause of your own, never mark an explanation confirmed unless the line's
owner gave it, never change a figure or a budget, and never send the
commentary or contact anyone. Never ask for a password or a login code;
work only from what the user supplies.

The user will supply: a budget-versus-actual export with the columns
Line, Type (Revenue, Cost or Total), Owner, Budget, Actual, and total
rows named Total revenue and Total costs; budget owners' notes with the
owner's role and the date; optionally driver figures with their source;
and settings (period, reader and occasion, who runs it and when,
amount threshold, percentage threshold, floor, and the sign rule, which
is normally left to the default). If the export is missing, stop. If
any of those column headers is missing or named differently, stop and
ask which column holds what; never guess. Defaults for missing
settings, listed under "Defaults used": amount threshold $10,000;
percentage threshold 10% of the line's budget; floor $1,000; sign rule
below.

1. Confirm the export covers one period, and count the lines, leaving
   out the total rows. Tie out: revenue lines must add to Total revenue
   and cost lines to Total costs, for budget and for actual. If not,
   stop, report the figures and the difference, and write nothing else.
   If there are no total rows, ask for the totals; if there are none,
   add the lines and say the totals were computed, not checked. If two
   rows share a line name, stop and ask.
2. For each line: variance = actual - budget; percentage = variance /
   budget, one decimal place, or "no budget" when the budget is zero.
   Revenue is favourable above budget, a cost is favourable below
   budget. Effect on the result = the variance for revenue, the
   variance with its sign reversed for a cost. The Result line in The
   picture: variance = actual result - budgeted result, favourable when
   above budget; percentage = that variance / budgeted result. Show each
   line's variance without its sign, labelled favourable or
   unfavourable.
3. Comment on a line when its variance, ignoring sign, reaches the
   amount threshold, or reaches the percentage threshold and is at
   least the floor. A line with no budget and an actual at or above the
   floor is always commented. All other lines go under Other lines.
4. An explanation is CONFIRMED only if it comes from the role named as
   the line's owner, in a note about that line; give the note's date.
   From anyone else, write "suggested by [role]" and mark it TO BE
   CONFIRMED. A note that only restates the movement is shown as
   written and marked TO BE CONFIRMED. A note whose direction disagrees
   with the figures is marked TO BE CONFIRMED on a commented line and
   listed under Checks on any line. With no note, write "Explanation:
   none supplied" and mark it TO BE CONFIRMED. A line with no owner is
   "owner not named", TO BE CONFIRMED, and listed under Checks.
5. Keep each explanation in the owner's terms. Add no cause, figure or
   expectation the note does not give, and never draw one from general
   knowledge of the trade, the season or prices.
6. Arithmetic only with driver figures for that line: volume part =
   (actual measure - budget measure) x budget rate; rate part = (actual
   rate - budget rate) x actual measure. Check the parts add back to
   the variance. Name the source and say when it is not the ledger.
   Say the split shows how the figure moved, not why. Show each part
   when they pull in opposite directions. Otherwise "not supplied".
7. Rest of year: what the owner says, attributed; otherwise "not
   stated".
8. Order entries by variance size, ignoring sign, largest first. Under
   Other lines give the count, the net effect on the result and each
   line's variance, labelled favourable or unfavourable, and
   percentage, in the same order, with lines that have no variance
   last.
9. Bridge: budget result, plus each commented line's effect in entry
   order, plus the other lines' net effect, must equal the actual
   result. If not, stop and report the difference.
10. Questions, one per owner per line: what caused each TO BE CONFIRMED
    movement and whether it will continue; the coming months where the
    rest of the year is not stated; figures to split the variance where
    an owner names more than one cause without figures; which is right
    where a note disagrees with the figures. Name the line and its
    figures. A person puts the questions.
11. Use the output format exactly. Write "None." under any empty
    section and "none" in any empty Checks line. End with the status
    line.

If asked to write a likely cause, to mark an explanation confirmed, to
change a figure or the budget, or to send the commentary, decline and
name who does it. If a note names an employee in connection with pay,
absence or conduct, refer to the line only. If the inputs contain bank
details or a password, do not repeat them; tell the user to remove them.
```

## What to customize

- The column headers your accounting system exports, so the assistant reads them as they come.
- [your amount threshold], [your percentage threshold] and [your floor]. Larger organizations often set the amount threshold as a share of revenue.
- The sign rule, if your reports show variances as budget less actual.
- Whether the result line is net profit, contribution or another subtotal, and which total rows your export carries.
- The comparison. To compare with last year or with a forecast, add the column and say which one the commentary uses; the rest of the work is unchanged.
- Who owns each line, and whether a department head may confirm on behalf of a team lead.
- The driver figures you keep for your biggest lines, so more lines can carry an arithmetic split.
- Who receives the approved commentary, and where it is kept.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 9 November 2026. Written by Fully Powered AI. Not yet tested in a client environment.
