# Weekly receivables summary

Workflow template, version 0.1.0.

## Purpose

Draft the one-page weekly summary the finance lead takes to management: what came in, aging against last week, the movements that explain the change, open exceptions and owners, follow-ups due, what changes before month end, and the decisions management must make. Every figure traces to the aging report or receipts log, and a tie-out line proves the totals. The assistant prepares; it never changes a record, sends the summary or makes any of the decisions it lists.

## When to use it and when not to

Use it at the end of each weekly receivables cycle, once aging is refreshed, the exception list assembled and the follow-up plan done. It also serves a regular collections update to owners or lenders from the same source.

Do not use it for a cash forecast, which needs payables, payroll and timing assumptions, or when either week's aging is missing or the totals do not tie.

## Roles

- **Runs it:** the billing coordinator or the controller.
- **Reviews, approves, presents and records management's decisions:** the finance lead.
- **Owns each exception reported:** the role named on the exception list.
- **Makes the decisions listed:** management, at the meeting.

## Inputs

1. **This week's aging report,** by invoice and bracket, after the week's postings. If missing, stop.
2. **Last week's aging report.** If missing, stop: movements cannot be explained without it.
3. **Receipts log for the week:** each receipt and whether it was applied (to which invoices, for how much) or held. If missing, stop.
4. **Invoices issued during the week.** If missing, derive them from invoices in this week's aging absent from last week's, and say so.
5. **Exception list** with who acts and who decides. If missing, write "exception list not supplied" in that section; never reconstruct it.
6. **Follow-up plan:** drafts due, holds, not chased. If missing, write "follow-up plan not supplied".
7. **Last week's summary,** for open decisions. If missing, say carried-forward decisions were not checked.
8. **The firm's settings:** brackets, [your movement threshold], management decision categories, meeting day. If missing, use the defaults below.

## The procedure

1. **Tie out first:** last week's total open + invoices issued − cash applied (from the receipts log) must equal this week's aging total. Check each week's brackets add to its total. If anything fails, stop, report the figures and the difference to the billing coordinator, and draft nothing else.
2. **What came in.** Count and total the receipts. Split into applied (by invoice, naming partial applications and the role that posted them) and held. Check applied + held = total received.
3. **Aging by bracket.** Each bracket this week with last week's beside it. Defaults: current, 1 to 30 days, 31 to 60, 61 to 90, over 90. Add total overdue and how much is disputed.
4. **Movements.** Invoices paid in full, reduced (from and to), issued, and moved bracket, by number. Leave out changes below [your movement threshold] unless they reach 61 days or more. End with the tie-out line.
5. **Exceptions open.** One line each: item, amount, who acts. State who decides.
6. **Follow-ups due,** each with sender and copy; then invoices held and not chased.
7. **Before month end.** From the due dates, name every invoice that crosses into a higher bracket before the next month end, with the date. For each held receipt, state what the bracket becomes once a person decides it and applies it. No other forecast.
8. **Decisions for management.** Only the firm's management categories. Defaults: whether work continues for a client over 60 days or with a missed promise; any credit or write-off above [your management credit threshold]; any dispute open longer than [your dispute limit] days. Carry forward every unsettled decision from last week. Write each as a question with its facts. Recommend nothing unless the finance lead asks.
9. **Trace line and return.** Name the aging date and receipts period behind every figure. Return the draft to the finance lead only.

## Exceptions and stop conditions

- **Tie-out fails or brackets do not add up:** stop; report the figures.
- **An invoice appears in last week's aging and not in this week's, with no receipt, credit or write-off explaining it:** stop on that invoice; ask the controller.
- **A receipt is shown as applied in the log but the invoice balance did not fall:** stop; ask the billing coordinator.
- **An exception has no owner:** list it with "owner not assigned" and put it first under Exceptions open.
- **Asked to recommend a decision, change a figure to match expectations, or send the summary:** decline; the finance lead decides what goes to management.

## Output format

```
WEEKLY RECEIVABLES SUMMARY: week of [Monday date]

For: [Finance lead], for the management meeting on [day date]. Receipts [from] to [to]; aging as of [date].

What came in: [n] receipts, [total]. Applied by [role]: [amount], to [invoices, with partial amounts]. Held unapplied: [amount] in [n] receipts, [status].

Aging by bracket: Current [this] (last week [last]). 1 to 30 days [this] ([last]). 31 to 60 days [this] ([last]). 61 to 90 days [this] ([last]). Over 90 [this] ([last]). Total open [this] ([last]). Overdue [amount], of which [amount] is disputed.

Movements: Paid: [invoices]. Reduced: [invoice], from [amount] to [amount]. Issued: [invoice, client, amount]. Moved bracket: [invoice] into [bracket]. Tie-out: [last total] + [issued] − [applied] = [this total].

Exceptions open: [n]. [Item, amount]: [who acts]. The [role] decides each.

Follow-ups due: [invoice, client, amount]: from [role], [role] copied. Held: [invoices]. Not chased: [invoices].

Before month end: [invoice] enters [bracket] on [date]. [If held receipt resolved: bracket becomes amount.]

Decisions for management: [n]. [Question, with the facts.]

Every figure traces to the aging report as of [date] and the receipts log for [period]. The summary changes no records and sends nothing.
```

## Reviewer checklist

1. The tie-out line is arithmetically correct. (Finance lead)
2. Every bracket figure matches the aging report. (Finance lead)
3. Applied plus held equals total received. (Billing coordinator)
4. Every movement is explained by a receipt, invoice, credit or the passage of time. (Controller)
5. Every open exception has an owner. (Controller)
6. Every decision listed is management's to make, and none from last week has been dropped. (Finance lead)
7. The page fits on one page and keeps the fixed section order. (Finance lead)

## Acceptance tests

Proposed tests. None has been run.

1. **Normal week.** Last week $33,600; issued $8,900; applied $10,150; this week $32,350. Expected: tie-out line shown and correct; all sections complete.
2. **Tie-out fails.** Same, but this week's aging shows $32,550. Expected: stops; reports the $200 difference and the four figures; drafts nothing else.
3. **Partial application.** $1,000 applied to a $1,200 invoice. Expected: "Reduced: from $1,200 to $200" and $1,000 counted as applied.
4. **Held receipts.** $5,950 held across two receipts. Expected: shown as held, excluded from applied and from the tie-out.
5. **Crossing before month end.** An invoice at 58 days on the Friday, month end five days later. Expected: named under Before month end with the date it enters 61 to 90.
6. **Exception with no owner.** Expected: listed first with "owner not assigned".
7. **Carried decision.** Last week's summary listed a decision not recorded as settled. Expected: carried forward.
8. **Asked for a recommendation.** Expected: lists the decision with facts, recommends nothing unless the finance lead asks.

## Instructions for the AI assistant

```
You draft the weekly receivables summary for the finance lead. You never
change records, send the summary, or decide anything it lists.

The user will supply: this week's and last week's aging reports; the
week's receipts log; invoices issued; the exception list; the follow-up
plan; last week's summary; the firm's settings. If either aging report or
the receipts log is missing, stop and say so. If another input is missing,
say so in the section it feeds and continue.

1. Tie out: last week's total + issued this week - applied this week must
   equal this week's total. Check each week's brackets sum to its total.
   If anything fails, stop, report the figures and the difference, and
   draft nothing else.
2. What came in: count and total receipts; split applied (by invoice,
   naming partial amounts) and held. Applied + held must equal the total.
3. Aging by bracket: this week with last week in brackets. Add total
   overdue and how much is disputed.
4. Movements: paid, reduced (from and to), issued, moved bracket, by
   invoice number. Omit changes under [your movement threshold] unless
   they reach 61 days or more. End with the tie-out line.
5. Exceptions open: one line each with who acts; state who decides. Put
   any item with no owner first, marked "owner not assigned".
6. Follow-ups due with sender and copy; then held and not chased.
7. Before month end: invoices that cross into a higher bracket before the
   next month end, with the date; what a bracket becomes if a held receipt
   is resolved. No other forecast.
8. Decisions for management: only the firm's management categories, plus
   every unsettled decision from last week. Write each as a question with
   its facts. Recommend nothing unless asked.
9. Use the output format exactly, on one page. End with the trace line:
   "Every figure traces to the aging report as of [date] and the receipts
   log for [period]. The summary changes no records and sends nothing."

Never adjust a figure to make it tie. If asked to, decline.
```

## What to customize

- Your brackets and the meeting day.
- [your movement threshold], [your management credit threshold] and [your dispute limit].
- Which decisions go to management and which stay with the controller.
- Who receives the approved page, and in what form.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 9 November 2026. Written by Fully Powered AI. Not yet tested in a client environment.
