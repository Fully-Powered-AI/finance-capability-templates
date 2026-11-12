# Investor update

Workflow template, version 0.1.0.

## Purpose

Draft one period's update from a founder to the company's investors, monthly or quarterly: the headline, the standing figures against plan and against the last period, cash and runway worked out from the cash report, wins, problems stated plainly with their cause and what is being done, what became of the problems and asks in the last update, this period's asks, and team changes. Every figure comes from a report the person supplies; a figure that does not is labelled as the founder's. Gaps are listed first, as questions for the founder or the finance lead. The assistant prepares; it never sends the update, never contacts an investor, never changes a figure or a record, and never supplies a headline, cause, win or ask of its own.

## When to use it and when not to

Use it on the same day each month or quarter, once the period's billing, sales and cash reports are final and the founder has written their notes. Run it again after the questions are settled. Run it every period, including the difficult ones.

Between regular updates, when news should not wait for the next one (a large customer lost, a key person leaving, a change in funding), run it with the type set to "off-cycle". The draft then carries the headline, the news under Problems, cash and runway, and any asks, and leaves the other sections out.

Do not use it:

- for board papers, or for anything the board must decide. That is the board meeting pack workflow template;
- for a report a lender requires under a loan agreement, whose content and timing the agreement sets;
- for a company whose shares trade on a public market. Its communications with investors follow the market's disclosure rules and its advisers;
- to raise money. The update describes the company; it is not an offer of shares. Terms of a round, a valuation and the wording of any offer go to the company's advisers;
- to build the figures. The finance lead prepares the reports; this workflow template reads them;
- to forecast. Runway is worked out from the last three months as they happened, and nothing else is projected.

## Roles

- **Runs it:** the founder or CEO, or the finance lead, chief of staff or operations lead who assembles the update for them.
- **Decides and sends:** the founder. They write the headline, the wins, the cause of each problem and what is being done about it, and the asks; settle every question for the founder; approve the final text; and send it.
- **Owns the figures:** the finance lead, bookkeeper or outside accountant. They confirm each figure against its report and settle any figure that differs from the last update.
- **Reads it:** the company's investors, on the founder's list. The assistant never sees the list and never writes to anyone on it.

## Inputs

Everything is pasted or attached by a person. No accounting system, bank, billing system or mailbox is connected, and the assistant never asks for a password or a login code.

1. **The settings:** the company name; the period (a month or a quarter) and the type (regular or off-cycle); the founder's name and title as they sign; the greeting; [your confidentiality line] (default: "Confidential: for [company] investors only. Please do not forward."); today's date and the planned send date; [your variance threshold] (default: 10% against plan); [your runway alert] (default: 12 months); [your word limit] (default: 600 words, counted from the headline to the sign-off). If the company or the period is missing, stop and ask. A missing threshold, alert or limit takes its default, listed under "Defaults used".
2. **The figures export** for the period, one row per standing metric, in the order the update shows them. Default column headers: `Metric`, `Unit`, `This period`, `Last period`, `Plan`, `Better when`, `Source`. `Unit` is `$` (or the company's currency), `count` or `%`. `Better when` is `higher` or `lower`. If any header is missing or named differently, stop, list the headers found and ask which column holds each; never guess. A blank `Plan` or `Last period` means there is no figure, not zero. If the export is missing, stop and ask.
3. **The cash report** for the last three months, one row per month, oldest first. Default column headers: `Month`, `Opening cash`, `Funding received`, `Other cash in`, `Cash out`, `Closing cash`. `Funding received` is money from investors or lenders: shares, notes, loans. `Other cash in` is everything else, mainly customer receipts. If a header does not match, stop and ask as above. If the report is missing or covers fewer than three months, stop and ask; runway is not worked out from less.
4. **The founder's notes** for the period, dated: the headline as the founder wants it; wins; problems, each with its cause and what is being done, by whom and by when; news on anything the last update raised; asks; team changes (joined, left, open roles, by role); any customer the founder has permission to name; any funding expected and not yet received; and anything that must not go in. If there are no notes, stop and ask: the headline, the causes and the asks are the founder's to write.
5. **The last update as sent,** with its date. If it is missing, write "Last update not supplied" under Since the last update, and say under Checks that last period's figures and dropped metrics were not checked.

## The procedure

1. **Check the inputs.** Confirm the company, the period and the type. Read both exports' headers against the defaults; on any mismatch, stop and ask. Count the metric rows. If two rows share a metric name, stop and ask which is which.
2. **Tie out the cash report.** For each month, opening cash + funding received + other cash in − cash out must equal closing cash, and each month's opening cash must equal the previous month's closing cash. If any check fails, stop, report the month, the figures and the difference for the finance lead, and draft nothing else.
3. **Work out cash and runway.** Net burn for a month = cash out − other cash in; funding received never reduces it. Average net burn = the three months' net burn added together and divided by three. Runway = the latest month's closing cash ÷ average net burn, in months, to one decimal place, rounded down, never up. If average net burn is zero or less, write "Cash grew over the three months before funding; no runway figure." in place of the runway. List the funding received in the three months by month, with the founder's description where the notes give one, or "none". Funding the founder expects and has not received, an expected loan or debt line included, goes on its own "Not counted" line, in the founder's words and with its amount where the notes give one, and is never added to cash or runway.
4. **Work out each metric.** Against plan: (this period − plan) ÷ plan, as a percentage to one decimal place, better or worse according to `Better when`. For a metric whose unit is `%`, give the difference in points first and that percentage in brackets. Status: "On or ahead of plan"; "Behind plan" (worse by less than [your variance threshold]); "Well behind plan" (worse by [your variance threshold] or more); "No plan" when the plan is blank. Against last period: (this period − last period) ÷ last period, to one decimal place, written as up, down or unchanged; in points for a `%` metric; "no last-period figure" when it is blank. Show every row in the export's order. Never leave a row out because it is behind.
5. **Check last period against the last update.** For each metric the last update reported, compare its figure with the export's `Last period`. Where they differ, mark the metric RESTATED with the figure the last update gave, and add a question for the finance lead: which is right? If the new figure stands, the update says the earlier one was revised. A metric the last update reported that is missing from the export goes under The numbers marked DROPPED, with its last figure, and becomes a question for the founder. If the founder decides to stop reporting it, the line reads "No longer reported" with the founder's reason. Never drop a metric silently.
6. **The headline.** Use the founder's headline as worded. If any metric is Well behind plan, or runway is under [your runway alert], and the headline mentions none of them, mark it HEADLINE CHECK with the reason and add a question. If the headline states a figure, or a comparison such as "record", that differs from the export or the cash report, or is in neither, mark it the same way; a rounded figure that matches its report once rounded is not a difference. Never rewrite the headline.
7. **Wins.** Each in the founder's words. A figure stated as fact in a win, or anywhere else the update carries the founder's words (an amount, a rate, a time, a count of anything, such as customers, locations or accounts, or a comparison such as "record", "largest" or "best"), that appears in a report or in the last update is checked against it; a date is not a figure for this rule. A figure or comparison in neither is kept, listed under Checks as a founder's figure, and covered by a question asking the founder to confirm it or supply the report behind it. Name a customer only where the notes say the founder has permission; otherwise use the founder's description of the customer, or "a customer". Add no win of your own.
8. **Problems.** List every problem in the founder's notes. Then make sure every metric that is Well behind plan, and a runway under [your runway alert], appears here; one problem may cover several metrics when the notes explain them together. A closely linked metric the notes do not name, such as revenue churn beside customers lost, may be grouped with that problem, with a question asking the founder to confirm the explanation covers it. For each: what happened, with the figures; the cause, in the founder's words; and what is being done, with the owner by role and the date. Where the notes give no cause, write CAUSE NEEDED; no response, RESPONSE NEEDED; a response with no owner or no date, OWNER AND DATE NEEDED. Each of these becomes a question. Never supply a cause or a response. Problems stay in their place, after Wins and before Asks, with their figures as reported.
9. **Since the last update.** For each problem and each ask in the last update, give the date of that update and what the notes say now. Where the notes say nothing, write STATUS NEEDED and add a question. A figure here follows the rule in step 7.
10. **Asks.** Each in the founder's words. An ask is specific when it says what help is wanted, from what kind of person or firm, and by when, as a day or at least a month ("by 30 November" or "before we sign in December" will do; "soon" will not). If any of the three is missing, keep the founder's wording, mark it MAKE SPECIFIC with what is missing, and add a question. If the notes give no asks, add a question; write "No asks this period." only once the founder confirms it.
11. **Team.** Joined, left and open roles, by role and month. Leave out the reason anyone left and anything about a person's pay, performance, health or circumstances, and list the kind of item left out under Checks.
12. **Off-cycle note.** When the type is off-cycle, write the headline; the news under Problems, with what happened, its effect on customers, revenue or cash as the reports or notes give it, and what is being done; Cash and runway; and Asks. Under The numbers, Wins, Since the last update and Team, write "Not included in an off-cycle note." If the news is a security incident, a regulator's inquiry or a legal claim, use only the facts the notes state, add nothing beyond them, and make the first question: the draft goes to the company's advisers before anyone sends it.
13. **Length.** Count the words of the update from the headline to the sign-off. If the count passes [your word limit], say by how much and name the two longest sections. Never shorten Problems or drop a metric to fit.
14. **Count the gaps** and list them first under To settle, one question each, with the section it affects and who answers it: the founder or the finance lead. Head the draft NOT READY TO SEND while any gap is open.
15. **Return the draft** to the person who ran it, for the founder. When a question is answered, update the draft, mark the question "settled by [role]" and recount. Before sending, the founder removes the To settle and Checks parts, approves the text and sends it.

## Exceptions and stop conditions

- **A header in either export does not match the defaults:** stop, list the headers found and ask which column holds each.
- **The cash report does not tie out, or covers fewer than three months:** stop; report the figures and the difference for the finance lead.
- **No figures export, or no founder's notes:** stop and ask.
- **Asked to improve a figure, round it in the company's favour, leave out a metric that is behind, or move a problem out of view:** decline. Every row appears; the founder may stop reporting a metric only openly, under "No longer reported" with a reason.
- **Asked to write the headline, a cause, a win or an ask:** decline and ask the founder for it; the update speaks in the founder's voice.
- **Asked to send the update, write to an investor or post it to an investor portal:** decline; return the text for the founder to send.
- **The notes include the terms of a new round, a valuation, an offer of shares, or a loan's interest rate and conditions:** leave them out of the update and add a question: these go to the company's advisers before any investor sees them. The amount of an expected loan or debt line, in the founder's words, may go on the Not counted line.
- **The notes name a customer without saying the founder has permission:** describe the customer instead, and say so under Checks.
- **The notes raise a dispute with a named person, or a person's pay, performance or health:** leave it out and list the kind of item under Checks.
- **The material contains bank account details, a password or a login code:** leave it out and tell the person to remove it from the source.

## Output format

```
INVESTOR UPDATE: [company], [period]
DRAFT for [founder]. [NOT READY TO SEND: [n] questions to settle. / Ready for [founder] to approve and send.]
Prepared [date] from: figures export ([n] rows, [source dates]); cash report ([first month] to [last month]); founder's notes ([date]); last update ([date] / not supplied).
Type: [regular / off-cycle]. Settings used: variance threshold [n]%; runway alert [n] months; word limit [n]. Defaults used: [settings / none].

TO SETTLE BEFORE SENDING, for [founder] only; remove before sending: [n / None]
[n]. [Section], for the [founder / finance lead]: [question]. [settled by (role)]

---------------- THE UPDATE ----------------
Subject: [company] investor update: [period]
[Confidentiality line]

[Greeting]

HEADLINE
[The founder's headline, as worded.] [HEADLINE CHECK: reason.]

THE NUMBERS: [period], against plan and [last period]
- [Metric]: [this period] (plan [plan]; [last period] [figure]). [On or ahead of plan / Behind plan / Well behind plan / No plan]: [n]% [better / worse] than plan, or [n] points [better / worse] ([n]%); [up / down] [n]% or [n] points on [last period] / unchanged / no last-period figure. [RESTATED: the last update gave [figure].]
- [Metric]: DROPPED. Last reported as [figure] in the update of [date]. / No longer reported: [founder's reason].
[Off-cycle: Not included in an off-cycle note.]

CASH AND RUNWAY
Cash at [end of latest month]: [amount].
Average net burn, [first month] to [last month]: [amount] a month ([month] [amount]; [month] [amount]; [month] [amount]).
Runway: [n] months at that rate. / Cash grew over the three months before funding; no runway figure.
Funding received in the three months: [amount, month, founder's description / none].
Not counted: [the founder's words on funding expected and not received / nothing].

WINS
- [Win, in the founder's words.]
[None this period. / Off-cycle: Not included in an off-cycle note.]

PROBLEMS
- [What happened, with the figures.] Cause: [founder's words / CAUSE NEEDED]. Response: [founder's words], [owner role], by [date] / RESPONSE NEEDED / OWNER AND DATE NEEDED.
[None this period.]

SINCE THE LAST UPDATE
- [Problem or ask], raised [date]: [what the notes say now / STATUS NEEDED].
[Nothing carried from the last update. / Last update not supplied. / Off-cycle: Not included in an off-cycle note.]

ASKS
[n]. [The founder's ask.] [MAKE SPECIFIC: what is missing.]
[No asks this period.]

TEAM
Joined: [role, month / none]. Left: [role, month / none]. Open roles: [roles / none].
[Off-cycle: Not included in an off-cycle note.]

[Sign-off: founder's name and title]
---------------- END OF THE UPDATE ----------------

CHECKS, for [founder] only; remove before sending
Words, headline to sign-off: [n] of [limit]. [Over by [n]: longest sections [section], [section].]
Cash tie-out: [first month] to [last month], each month ties and runs on from the last.
Figures traced: [metric(s)]: [source]; ... Cash: cash report, [months].
Founder's figures not in any report: [figure, section / none].
Metrics well behind plan: [metrics / none]. Each under Problems: [yes / no: which].
Left out of the update: [kind of item and why / nothing].
[Last period's figures and dropped metrics not checked: last update not supplied.]

Draft only. Nothing has been sent, and no figure or record has been changed.
```

## Reviewer checklist

1. The cash report ties out, and net burn, the average and the runway are arithmetically correct, with the runway rounded down. (Finance lead)
2. Every figure matches the report it came from, and every RESTATED figure is settled. (Finance lead)
3. Every metric the last update reported appears again, or is retired openly with a reason. (Finance lead)
4. Every metric well behind plan, and any runway under the alert, is under Problems with the founder's cause and what is being done, an owner and a date. (Founder)
5. The headline is the founder's, and it does not leave out the hardest news of the period. (Founder)
6. Every ask says what help is wanted, from whom and by when. (Founder)
7. No customer is named without permission; no reason for a departure, and nothing on a person's pay, performance or health, appears. (Founder)
8. Nothing about the terms of a round, a valuation or an offer of shares appears. (Founder)
9. To settle is at zero, and the To settle and Checks parts are removed before sending. (Founder)

## Acceptance tests

Proposed tests. None has been run.

1. **Ordinary month.** Six metrics, all on plan or within the threshold; cash report ties; the founder's notes cover every section. Expected: "To settle: None", Ready for the founder to approve and send, and every figure traced under Checks.
2. **Header not matched.** The figures export uses `Budget` in place of `Plan`. Expected: stops, lists the headers found and asks which column holds the plan; drafts nothing.
3. **Cash report does not tie.** October opens at $2,425,000, takes in $174,200, pays out $322,700 and closes at $2,286,500. Expected: stops and reports October's figures and the $10,000 difference; drafts nothing else.
4. **Runway arithmetic.** Net burn of $140,000, $145,000 and $148,500; closing cash $2,276,500. Expected: average $144,500 a month; runway 15.7 months (15.754 rounded down); September's $250,000 of funding listed but not counted against net burn.
5. **Expected funding.** The notes mention a loan "expected to close next month". Expected: shown on the Not counted line in the founder's words; cash and runway unchanged.
6. **Cash growing.** Other cash in exceeds cash out in all three months. Expected: "Cash grew over the three months before funding; no runway figure."
7. **Metric well behind plan with no note.** New customers 24 against a plan of 28. Expected: Well behind plan, 14.3% worse; listed under Problems with CAUSE NEEDED and RESPONSE NEEDED; a question for the founder.
8. **Headline leaves out bad news.** Three metrics are well behind plan and the headline speaks only of growth. Expected: headline kept as worded, marked HEADLINE CHECK with the three metrics named, and a question.
9. **Figure restated.** The export gives last period's pipeline as $590,000; the last update said $585,000. Expected: RESTATED with $585,000 shown, and a question for the finance lead.
10. **Metric dropped.** A metric in the last update is missing from this export. Expected: DROPPED with its last figure, and a question; never left out silently.
11. **Vague ask.** "Any help finding people." Expected: kept as worded, MAKE SPECIFIC naming what is missing (which role, from what kind of person, by when), and a question.
12. **Customer and departure.** The notes name a customer with no word on permission, and give the reason a support specialist left. Expected: the customer is described, not named; the departure is listed by role and month only; both listed under Checks.
13. **Round terms in the notes.** The notes give a valuation for a planned round. Expected: left out of the update; a question saying it goes to the company's advisers.
14. **Asked to send.** "Email this to the investor list." Expected: declines; returns the text for the founder to send.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You draft one period's investor update for a founder to approve and
send. You prepare; people decide. You never send the update, never
contact an investor, never change a figure or a record, and never write
a headline, cause, win or ask of your own. Never ask for a password or a
login code; work only from what the user supplies.

The user will supply: settings (company, period, type regular or
off-cycle, founder's name and title, greeting, confidentiality line,
today's date, send date, variance threshold, runway alert, word limit);
a figures export with the columns Metric, Unit, This period, Last
period, Plan, Better when, Source; a cash report for the last three
months with the columns Month, Opening cash, Funding received, Other
cash in, Cash out, Closing cash; the founder's dated notes; and the last
update as sent. If the company, period, figures export, cash report or
notes are missing, or the cash report covers fewer than three months,
stop and ask. If any column header is missing or named differently,
stop, list the headers found and ask which column holds each; never
guess. If two rows share a metric name, stop and ask which is which. If
the last update is missing, write "Last update not supplied." under
Since the last update, and say under Checks that last period's figures
and dropped metrics were not checked. Defaults, listed under "Defaults
used": variance threshold 10%; runway alert 12 months; word limit 600
words from headline to sign-off; confidentiality line "Confidential: for
[company] investors only. Please do not forward." A blank Plan or Last
period is no figure, not zero.

1. Tie out the cash report: for each month, opening + funding received +
   other cash in - cash out = closing, and each opening equals the
   previous closing. If not, stop, report the month, figures and
   difference, and draft nothing else.
2. Net burn per month = cash out - other cash in; funding never reduces
   it. Average = the three months added and divided by three. Runway =
   latest closing cash / average, one decimal place, rounded down. If
   the average is zero or less, write "Cash grew over the three months
   before funding; no runway figure." List funding received by month,
   with the founder's description where the notes give one. Put expected
   funding not received, an expected loan or debt line included, on the
   "Not counted" line in the founder's words, with its amount where the
   notes give one; never add it to cash or runway.
3. Each metric: against plan = (this - plan) / plan, one decimal place,
   better or worse by Better when; for a % metric give points first and
   the percentage in brackets. Status: On or ahead of plan; Behind plan
   (worse by less than the threshold); Well behind plan (worse by the
   threshold or more); No plan. Against last period: up, down or
   unchanged, in % or, for a % metric, points. Show every row in the
   export's order; never omit one because it is behind.
4. Compare each figure the last update reported with Last period. If
   they differ, mark RESTATED with the earlier figure and ask the
   finance lead which is right. A metric in the last update missing from
   the export is marked DROPPED with its last figure and becomes a
   question; it is retired only openly, as "No longer reported" with the
   founder's reason.
5. Headline: the founder's words. If a metric is Well behind plan or
   runway is under the alert and the headline mentions none of them, or
   it states a figure, or a comparison such as "record", the reports do
   not support, mark HEADLINE CHECK with the reason and ask. A rounded
   figure that matches its report once rounded is not a difference.
   Never rewrite it.
6. Wins: the founder's words. A figure stated as fact here or anywhere
   else in the founder's words (amount, rate, time, count of anything,
   or a comparison such as "record", "largest" or "best"; not a date) in
   no report and not in the last update is kept, listed under Checks as
   a founder's figure, and the founder is asked to confirm it or supply
   its report. Name a customer only with the founder's stated
   permission; otherwise describe it.
7. Problems: every problem in the notes, plus every metric Well behind
   plan and any runway under the alert. One problem may cover several
   metrics the notes explain together; a closely linked metric the notes
   do not name may be grouped with it, with a question asking the
   founder to confirm. Give what happened with the figures, the cause in
   the founder's words, and what is being done with owner and date.
   Otherwise write CAUSE NEEDED, RESPONSE NEEDED or OWNER AND DATE
   NEEDED and ask. Keep Problems after Wins and before Asks, figures as
   reported.
8. Since the last update: each problem and ask from it, with its date
   and what the notes say now, or STATUS NEEDED and a question. A figure
   here follows the rule in step 6.
9. Asks: the founder's words. Each must say what help, from what kind of
   person or firm, and by when, as a day or at least a month ("before we
   sign in December" will do; "soon" will not); otherwise mark MAKE
   SPECIFIC with what is missing and ask. With no asks, ask; write "No
   asks this period." only once the founder confirms.
10. Team: joined, left, open roles, by role and month. Leave out reasons
    for leaving and anything on pay, performance, health or personal
    circumstances; list the kind of item under Checks.
11. Off-cycle: headline, the news under Problems, Cash and runway, Asks;
    write "Not included in an off-cycle note." under The numbers, Wins,
    Since the last update and Team. For a security incident, regulator's
    inquiry or legal claim, use only the facts stated and make the first
    question that the draft goes to the company's advisers before
    sending.
12. Count words from headline to sign-off; if over the limit, say by how
    much and name the two longest sections. Never shorten Problems or
    drop a metric to fit.
13. List every gap first under To settle, one question each, with its
    section and who answers it. Head the draft NOT READY TO SEND while
    any is open.
14. Use the output format exactly. Print "None this period." or the
    stated empty wording in any empty section. End with: "Draft only.
    Nothing has been sent, and no figure or record has been changed."

Leave out terms of a round, valuations, offers of shares and a loan's
interest rate and conditions, and ask for them to go to the company's
advisers; an expected loan's amount may go on the Not counted line. If
asked to improve a figure, hide a metric or problem, write the founder's
words, or send the update, decline and say who does it. If the material
contains bank details, a password or a login code, leave it out and tell
the user to remove it from the source.
```

## What to customize

- The standing metrics and their order. Fix them once; the update shows the same rows every period.
- The column headers your billing, sales and cash reports export, so the assistant reads them as they come.
- [your variance threshold], [your runway alert] and [your word limit].
- Monthly or quarterly, and the day of the month or quarter the update goes out.
- How net burn is counted. As written it leaves out funding received and nothing else; if your finance lead counts it differently, change step 3 of the procedure and step 2 of the instructions together, so the same rule applies every period.
- [your confidentiality line], the greeting and the sign-off.
- Which customers may be named, and who gives that permission.
- Who sees the To settle and Checks parts, and where the approved update and the sent copy are kept, so the next period can use it as its last update.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 10 November 2026. Written by Fully Powered AI. Not yet tested in a client environment.
