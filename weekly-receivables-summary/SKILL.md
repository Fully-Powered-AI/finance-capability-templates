---
name: "weekly-receivables-summary"
description: "Draft the one-page weekly summary the finance lead takes to management: what came in, aging against last week, the movements that explain the change, open exceptions and owners, follow-ups due, what changes before month end, and the decisions management must make. Every figure traces to the aging report or receipts log, and a tie-out line proves the totals. The assistant prepares; it never changes a record, sends the summary or makes any of the decisions it lists."
license: "MIT"
metadata:
  version: "0.1.0"
  publisher: "Fully Powered AI"
  capability: "Weekly receivables summary"
---

# Weekly receivables summary

This is the technical file for a Fully Powered capability template. It carries the instructions an AI product follows. The complete template, with roles, inputs, exceptions, the reviewer checklist, acceptance tests and what to customize, is in [TEMPLATE.md](TEMPLATE.md). A worked example with invented data is in [EXAMPLE.md](EXAMPLE.md).

## Instructions

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

## Before relying on it

Decide every item under "What to customize" in TEMPLATE.md and set the limits the instructions in this file leave open, written in square brackets such as [N], to your own. Then run the acceptance tests in TEMPLATE.md on past work. A person starts this work, supplies the inputs and decides what happens with the result.
