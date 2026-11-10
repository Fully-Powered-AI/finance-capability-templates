# Budget-versus-actual variance commentary: a trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-09

The inputs for this run are the invented example's inputs (the Fernhollow Print October 2026 settings, export, budget owners' notes and driver figures in `public/example.md`). No client data was used. The run was made by a model that did not write the template. It read the template and only the inputs of the example, followed the instruction block and the output format, and compared its result with the published example afterwards.

## What came out

All eleven parts of the format were produced, and nothing in the procedure told the assistant to stop. The output was:

```
BUDGET-VERSUS-ACTUAL COMMENTARY: October 2026

For: managing director, management meeting on Tuesday 10 November 2026. Prepared by the finance lead on Thursday 5 November 2026, for the finance lead's approval.
Sources: budget-versus-actual export for October 2026, as of 5 November 2026; notes from the sales director (4 November), the production manager (4 November), the operations manager (5 November) and the finance lead (5 November); driver figures for print sales, from the order system.
Settings used: comment at $10,000 or 10% of the line's budget; floor $1,000; revenue favourable above budget, costs favourable below budget. Defaults used: the sign rule.

THE PICTURE
Revenue: budget $450,000, actual $469,680, $19,680 (4.4%) favourable.
Costs: budget $313,000, actual $342,690, $29,690 (9.5%) unfavourable.
Result: budget $137,000, actual $126,990, $10,010 (7.3%) unfavourable.
Lines: 11. Commented: 6. Explanations confirmed: 4. To be confirmed: 2. Lines with no budget: 1. Other lines: 5.

TIE-OUT
Revenue lines add to Total revenue: budget $450,000, actual $469,680. Cost lines add to Total costs: budget $313,000, actual $342,690.

COMMENTARY BY LINE
Print sales (sales director). Favourable $26,480 (6.4%). Budget $412,000; actual $438,480.
Explanation: more short-run orders from two retail clients ahead of the holiday season; a volume discount was given to both, which is why the average order value is down. CONFIRMED by the sales director, note of 4 November 2026.
Arithmetic: from the order system, not the ledger. Volume part: (1,080 - 1,000) x $412.00 = +$32,960. Rate part: ($406.00 - $412.00) x 1,080 = -$6,480. Together +$26,480, which equals the line's variance. This shows how the figure moved, not why.
Rest of year: not stated.

Paper and materials (production manager). Unfavourable $18,900 (12.8%). Budget $148,000; actual $166,900.
Explanation: the mill's price rise took effect on 1 October; more paper went through the presses because of the extra retail orders. CONFIRMED by the production manager, note of 4 November 2026.
Arithmetic: not supplied.
Rest of year: not stated.

Production wages (production manager). Unfavourable $11,500 (12.0%). Budget $96,000; actual $107,500.
Explanation: overtime on the Saturday shifts of 10 and 17 October to clear the retail orders. CONFIRMED by the production manager, note of 4 November 2026.
Arithmetic: not supplied.
Rest of year: the production manager expects the same in November.

Marketing (sales director). Favourable $8,500 (70.8%). Budget $12,000; actual $3,500.
Explanation: the trade show deposit was budgeted for October, but the organiser invoiced it in September. CONFIRMED by the sales director, note of 4 November 2026.
Arithmetic: not supplied.
Rest of year: the sales director says nothing more is to come on it this year.

Design services (studio manager). Unfavourable $6,800 (17.9%). Budget $38,000; actual $31,200.
Explanation: suggested by the finance lead: "I think the studio had less capacity in October", not checked with the studio manager. TO BE CONFIRMED by the studio manager.
Arithmetic: not supplied.
Rest of year: not stated.

Press repairs (production manager). Unfavourable $6,200 (no budget). Budget $0; actual $6,200.
Explanation: none supplied. TO BE CONFIRMED by the production manager.
Arithmetic: not supplied.
Rest of year: not stated.

OTHER LINES
5 lines, net effect on the result $1,590 unfavourable: delivery and freight, $1,100 over budget, 7.9%; utilities, $640 over, 7.1%; office and administration, $600 under, 8.0%; software subscriptions, $450 over, 10.0%; rent, no variance.

BRIDGE: BUDGET TO ACTUAL RESULT
Budget result $137,000
Print sales +$26,480
Paper and materials -$18,900
Production wages -$11,500
Marketing +$8,500
Design services -$6,800
Press repairs -$6,200
Other lines (5) -$1,590
Actual result $126,990

QUESTIONS FOR BUDGET OWNERS
For the sales director: print sales: the line was $26,480 over budget, on 1,080 orders at an average of $406.00 against 1,000 at $412.00. Do you expect the extra retail orders and the discount to continue in the coming months?
For the production manager: paper and materials: the line was $18,900 over budget ($166,900 against $148,000). Your note gives two causes, the mill's price rise and more paper used, without figures. Can you give the quantity used and the price paid, budget and actual, so the $18,900 can be split between them? Do you expect the higher cost to continue in the coming months?
For the studio manager: design services: $31,200 against a budget of $38,000, $6,800 under. What caused it, and will it continue? The finance lead suggests the studio had less capacity in October; is that right?
For the production manager: press repairs: $6,200 against no budget. What caused the spend, and will it continue? What is expected for the rest of the year?
For the operations manager: delivery and freight: your note of 5 November says freight came in under budget, but the export shows $15,100 against a budget of $14,000, $1,100 over. Which is right?

CHECKS FOR THE FINANCE LEAD
Notes that disagree with the figures: delivery and freight, operations manager, 5 November 2026: the note says under budget; the export shows $1,100 (7.9%) over.
Lines with no budget: press repairs, $6,200 actual.
Explanations not from the line's owner: design services, suggested by the finance lead.
Lines with no owner named: none.

Draft for the finance lead's approval. Explanations marked TO BE CONFIRMED are not yet established. No figure, budget or record has been changed, and nothing has been sent.
```

## What was observed

Checked against the inputs: both the revenue lines and the cost lines add to their totals, for budget and actual. Six lines reach the threshold. Print sales, paper and materials, and production wages pass the $10,000 amount. Marketing (70.8%) and design services (17.9%) pass 10% and are above the $1,000 floor. Press repairs has no budget and an actual above the floor. Software subscriptions is exactly 10.0% but only $450, so the floor keeps it under Other lines. The bridge ends at the actual result of $126,990. The arithmetic split adds back to the line's variance, and the driver figures happen to agree with the ledger figures for the line (1,000 x $412.00 and 1,080 x $406.00).

The comparison with the published example found no difference in any figure, label, status or count. The differences were in wording and layout only:

- The example puts the Other lines in the order delivery and freight, utilities, software, office, rent. This run put them by size, ignoring sign, with the rent line last. The template does not say how to order them.
- The example adds "under the $1,000 floor" beside software subscriptions. This run did not, because the template does not ask for it.
- The example writes each Other line as "$1,100 unfavourable (7.9%)". This run wrote "over budget" or "under budget" for each, because the format shows only "variance, n%" and does not say whether to add a label.
- The finance lead's note on design services says "I think the studio had less capacity". The example paraphrases it as "may have had less capacity"; this run quoted the owner's words and added that it was not checked.
- The questions differ in wording. The example asks the sales director about "November and December"; this run said "the coming months". The example's paper question asks about the quantity and the price; this run also said the note gave two causes without figures. This run also asked the production manager what is expected for the rest of the year on press repairs.
- The example formats headings and lists in Markdown. This run kept the plain-text format from the template.

No fact appears in either output that is not in the inputs or derived from them by the template's rules. The "November and December" in one of the example's questions is a question, not a statement of fact, but December is not in the inputs.

## Where the template was unclear

- The settings list in the inputs section does not include the sign rule, and the output format asks for "Defaults used". This run listed the sign rule as a default, as the example does, but the template could say plainly that it is a setting that is normally defaulted.
- The header reads "Prepared by the [role] ... for the [approver role]'s approval". In the example both are the finance lead. The settings never name an approver; this run took it from the Roles section. The assistant itself prepares the draft, so "Prepared by the finance lead" means the person who ran it, which the template does not say.
- The order of the Other lines and whether each carries "favourable" or "unfavourable" are not stated.
- The format shows an unsigned amount with a label for each line ("Unfavourable $6,800"), while the procedure defines variance as a signed figure (actual less budget). The reader can work out the mapping, but a short note would help.
- The questions rule says to ask for figures that would split a variance where an owner names more than one cause. It does not say which figures to ask for. This run proposed quantity and price; that is a suggestion of what to supply, not a cause.
- Whether the counts "Explanations confirmed" and "To be confirmed" include lines under Other lines is not said. This run counted only commented lines, as the example does.
- A confirmed explanation with the rest of the year not stated gets a question about the coming months. This is in the procedure, but it is easy to miss in the instruction block, where it is tucked inside rule 10.

Nothing in the run was a defect that changed a figure. The template was followed to the end without stopping, and the output came out in the format asked for.

This was one run by one model on an invented example. It shows the template can be followed on that example; it is not a test in a client's environment.

## Changed after this run, and not run again

Changed on 9 November 2026 after an independent review of the published template, and not run again. The output and the observations above are as recorded and describe the template and the example as they stood at the run. No change alters a figure, a label, a status or a count in either output.

- **The settings** now list the sign rule, and say it is normally left to the default.
- **The header** now says "Prepared by" names the person who ran it, and that the approver is the finance lead unless the settings name another.
- **The picture** now says the confirmed and to-be-confirmed counts cover commented lines only, as this run and the example both counted. The procedure and the pasted instructions now say how the Result line gets its label and percentage: the actual result less the budgeted result, divided by the budgeted result, which is what both outputs did.
- **Each entry and Other lines** now show the variance without its sign, labelled favourable or unfavourable. Other lines are ordered by the size of the variance, ignoring sign, largest first, with lines that have no variance last. That is the order this run used, and the labels the example used.
- **The pasted instructions** now carry two checks from the procedure's first step: that the export covers one period, and the count of lines without the total rows.
- **The example** now quotes the finance lead's note on design services, as this run did. Its question to the sales director now asks about "the coming months", as this run did, in place of "November and December". Its Other lines now follow the new order, and it no longer adds "under the $1,000 floor" beside software subscriptions or a note under Checks that the freight line is below the threshold, since the format asks for neither.

The other places listed above where the template was unclear (which figures to ask for when an owner names two causes, and the question about the coming months sitting inside rule 10) are unchanged.
