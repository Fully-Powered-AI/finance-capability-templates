# Collections call brief: one trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID `claude-sonnet-5-5`)
- **Date:** 2026-11-12

The inputs were the invented example in [example.md](example.md): the settings, the open items, the payments, the contact log, the contacts, the disputes file, the collections terms and the caller's notes. No client data was used. The run was a single pass, done once, by a model that did not write the template. The model read the template and the example's inputs first, produced both parts of the output, and only then read the example's published output to compare.

## What came out

### Part A, before the call

The checks passed. The open items add to 12,070.40 USD, which ties to the ledger balance. The customer is a business, and no record mentions a lawyer, insolvency or a request not to be phoned. The account check held: 10,280.40 + 2,740.00 - 950.00 = 12,070.40.

- Ask for Contact 1, Accounts payable clerk, because of the broken promise of 7 October 2026. Also on file: Contact 2, Finance director, who approves the weekly payment runs.
- Overdue 10,280.40 on 4 invoices. In dispute 410.00 (D-31 on INV-5650). Overdue and not in dispute 9,870.40, of which 4,860.00 (INV-5521) is held by a query not logged. Not yet due 2,740.00 on 1 invoice. Credits not yet used 950.00 (CN-0218 350.00; PAY-1105 600.00).
- Open invoices, oldest first: INV-5521, 57 days overdue; INV-5588, 38 days; INV-5604, 29 days (1,120.00 open of 3,120.00); INV-5650, 11 days (410.00 in dispute); INV-5702, due in 10 days.
- Promises: 7 October, Contact 1, 4,860.00 for INV-5521 by 16 October: BROKEN, nothing applied to INV-5521 by 19 October; PAY-1016, 2,000.00 on 16 October, was applied to INV-5604. 2 November, Contact 2, 600.00 on account by 6 November: KEPT by PAY-1105, 600.00 on 5 November.
- Query not logged: INV-5521 (PO 7731), delivery address, from the log entries of 22 October and 2 November. The finance manager decides whether to log it.
- Questions:
  1. The broken promise on INV-5521 and the 2,000.00 applied to INV-5604: what held it up, on what date it will be paid, and whether the 2,000.00 was meant for INV-5604.
  2. The PO 7731 query: what exactly is wrong, what the customer needs from us to clear it, and on what date INV-5521 will be paid once it is cleared.
  3. INV-5588 2,315.40, INV-5604 1,120.00 and INV-5650 1,575.00 (the part not in dispute), total 5,010.40: on what date they will be paid.
  4. PAY-1105, 600.00, unapplied: which invoices it should go against.
  5. CN-0218, 350.00: whether the customer has it and which invoice they will take it against.
  6. D-31, status only, owner Warehouse manager: whether the photos asked for on 29 October have been sent.
- What the caller may offer, quoted from the collections terms of 1 March 2026. Standard terms: item 1. May agree without approval: item 2 (a promised date up to 14 days after the call) and item 5 (copies may be sent on request). Needs the finance manager's approval first: item 3 (a later date or instalments). Never offered on a call: item 4. Anything else: "I'll take that to the finance manager and come back to you."

### Part B, after the call

Call on 9 November 2026, 10:20. Spoke to Contact 1, Accounts payable clerk.

- Answers: INV-5521 is held because PO 7731 carries the old delivery address (Store 2, should be Store 3); the customer wants it reissued showing Store 3, after which it goes into a run, and no date was given for that. The 2,000.00 of 16 October was meant for INV-5604. The 600.00 of 5 November is for INV-5604. INV-5588 and the rest of INV-5604 (520.00) go in the 19 November run, as does the 1,575.00 of INV-5650. Contact 1 has not seen CN-0218; which invoice it goes against is not covered in the notes. Contact 2 is sending the D-31 photos this week.
- Promises made: 19 November 2026, 4,410.40, from Contact 1: INV-5588 2,315.40 (open balance; amount not stated in the notes); INV-5604 520.00; INV-5650 1,575.00. Within the collections terms, item 2 (10 days after the call). Also listed, with no date given: INV-5521 4,860.00 (open balance; amount not stated in the notes), to go into a run after it is reissued.
- Requests beyond the written terms, not agreed: INV-5521 paid in two halves on 19 November and 3 December (item 3 applies; the notes say the caller would check with the finance manager); INV-5521 reissued showing Store 3 (the terms do not cover it). The attention line was left out because the notes do not say anything was agreed on the call.
- What the credit controller said they would do: email a copy of CN-0218 today (9 November 2026), allowed by item 5; check the instalment request with the finance manager, no date given.
- Actions for a person: the finance manager decides the instalment request; the finance manager decides the reissue of INV-5521 and whether the PO 7731 query is logged as a dispute; the credit controller emails CN-0218; the credit controller applies PAY-1105 to INV-5604; the credit controller enters the promise in the contact log; the warehouse manager records the photos on D-31; the credit controller checks that the 4,410.40 arrived, by Monday 23 November 2026 (19 November plus 3 grace days is Sunday 22 November).
- Still open: the payment date for INV-5521; which invoice CN-0218 goes against. If it goes against INV-5588, the 19 November payment on that invoice would be 2,315.40 - 350.00 = 1,965.40 and the total 4,410.40 - 350.00 = 4,060.40. If the two halves of INV-5521 are equal they are 2,430.00 each; the notes do not say.
- Contact log entry: `2026-11-09,phone,out,Contact 1,Credit controller,"<short summary>",4410.40,2026-11-19,INV-5588;INV-5604;INV-5650`. Points the record could not place: None.

## What was observed

- Every part the template requires was produced, in the order the output format sets, and no stop condition was met. Nothing was sent, entered or changed.
- Compared with the published example, the facts and figures agree: every amount, every day count, both promise judgments, the question set, the offer lines and the 4,410.40 promise. The wording of the questions differs. The published example's question 5 asks "will you take it against INV-5588?", which names an invoice the template only supports by the credit note's reference; this run asked which invoice. The published example's question 1 leaves out the payment date that the template's step 9 asks for, because question 2 asks it.
- Differences in content: this run also listed INV-5521 as an undated promise ("then it goes in a run"); the published example does not. The published example's first action covers the instalment request and its second covers both the reissue and logging the query as a dispute; this run folded the same decisions into three actions.
- Three statements in the published example are not in the inputs: that the warehouse manager is the one who asked Contact 2 for photos (the disputes file says photos were requested, not by whom); that Contact 2 "raised" D-31 (the file does not say who raised it); and that the halves of INV-5521 are equal (the notes say "two halves"). This run made the third assumption only as a labelled "if equal".
- Where the template was ambiguous, or the model had to decide:
  1. INV-5521 is both a broken promise and a query not logged, so questions 1 and 2 both ask when it will be paid. The template does not say which question carries the date.
  2. Item 5 of the terms ("copies ... may be sent on request") does not say whether it needs approval. The template says an item that is not plainly in the first or third group goes in the second. This run judged it plainly allowed and put it with the items that need no approval, as the published example does. A stricter reader would put it under approval.
  3. The notes say INV-5521 "goes in a run" after reissue but give no date and no amount. The template does not say whether that is a promise. It was listed as one, with "no date given".
  4. The template names no role that reissues an invoice, and the settings do not either, so the owner of that action is the finance manager only as the decider.
  5. "The first weekday after the promise date plus the grace days" does not say whether that date itself counts if it is a weekday. Here it fell on a Sunday, so the question did not arise.
  6. The settings name a role that enters the log and applies payments but the template does not say who emails a copy of a credit note; the notes settle it here.
  7. The notes use short invoice numbers ("5521"); they were read as INV-5521. The template does not mention this.
  8. For the time of the call, the notes give a start and an end; the start was used.
- The acceptance tests in the template are still proposed. This trial ran the template once on one account with a broken promise, a query not logged, a dispute, a credit note and an instalment request. The stop cases (a balance that does not tie, a renamed column, an individual, a lawyer, a request to threaten) were not run.
- One run by one model is not a test for a client, and the template is not tested in a client environment.

## Changed after the run recorded above, and not run again

Changed on 12 November 2026 after an independent review of the published template, and not run again. The output and the observations above are as recorded and describe the template and the example as they stood at the run:

- **The example's question 5 and its answer.** Question 5 now asks which invoice the credit note will be taken against, as this run did, and the answer reads "Which invoice it will be taken against: not covered in the notes". The "Still open" line keeps the labelled "if" arithmetic.
- **The example's D-31 lines.** The warehouse manager is no longer named as the one who asked for the photos, and Contact 2 no longer "raised" D-31; the Also on file line says "see D-31".
- **The example's instalment request.** It now reads "two halves (2,430.00 each if equal; amounts not stated in the notes)", the same labelled assumption this run made.
- **The pasted instructions.** They now say that the payment date is asked once when an invoice is both a broken promise and a query not logged (the ambiguity in observation 1), that the approver decides whether an invoice is reissued (observation 4), that the contact log and payments are read for the period in the settings (default 90 days), and that a repeated row stops the run. The over-long line was rewrapped.
- **The template's "When to use it" list.** The line about individuals now says only that the workflow template is for business customers.
