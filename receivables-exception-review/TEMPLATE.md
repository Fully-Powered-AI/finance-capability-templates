# Receivables exception review

Workflow template, version 0.1.0.

## Purpose

After incoming payments have been provisionally matched and the clean matches posted, assemble every receipt and invoice that did not resolve cleanly into one exception list for the controller. Each item carries its category, amounts, evidence, possible explanations, a proposed next step, who acts and who decides. The assistant prepares; it never applies a receipt, writes off a balance, issues a credit, contacts anyone or changes a record.

## When to use it and when not to

Use it once provisional matching is complete, before the controller's weekly review or the close. Do not use it before matching, for cash that is not customer receivables, or to decide collections referrals or credit terms, which are management decisions.

## Roles

- **Runs it:** the billing coordinator.
- **Decides every item:** the controller.
- **Answers for client conversations, promises and disputes:** each client's account lead.
- **Receives items unresolved past [your unapplied-cash limit] days:** the finance lead.
- **Applies, writes off, credits or refunds:** the billing coordinator or controller, under your authority rules.

## Inputs

1. **Receipts log.** Date, payer as shown by the bank, amount, method, bank reference, remittance text. From the bank export or cash-receipts register. If missing, stop.
2. **Provisional match results.** Each receipt marked matched, short, ambiguous or unmatched, with proposed invoices. If missing, stop and ask for matching to be run.
3. **Ledger or aging export after posting.** Invoice, client, due date, original amount, open balance. If it predates the latest postings, warn at the top and mark balances "as of [export date]".
4. **Postings from the last 30 days,** for the duplicate check. If missing, record the check as not performed.
5. **Account-lead notes and correspondence:** promised dates, queries, disputes, agreed discounts, retainers. If a client has none, write "no notes supplied". Never infer what a client said.
6. **The firm's rules:** short-payment handling, what counts as disputed, [your write-off threshold], [your unapplied-cash limit], discount terms. If missing, use this template's defaults and say so at the top.

## The procedure

1. **Check coverage.** Confirm the receipts log and ledger cover the same period. Anything after the last bank-feed date goes under "Could not assess".
2. **Select** every receipt marked short, ambiguous or unmatched, and every invoice the notes mark disputed or on hold.
3. **Short payments.** Record invoice, original amount, received, difference. Default rule: the billing coordinator applies a receipt to the invoice its remittance names, and the difference stays open. Search the notes for an agreed discount or credit, the receipts for a second payment from the same payer, and the terms for an early-payment discount. List each explanation the evidence supports. If the difference is at or below [your write-off threshold], say so; the controller decides. Propose: the billing coordinator asks the client which explanation applies; hold reminders on the balance.
4. **Ambiguous receipts.** List every candidate invoice with client, amount, due date and the evidence for and against. Never choose on amount or date alone. Propose: hold unapplied; the billing coordinator asks the bank for originator details; each candidate's account lead checks with the client; hold reminders on every candidate.
5. **Unmatched receipts.** Record payer, amount, date, reference. Check the notes for a retainer, deposit or prepayment, and the ledger for a recently paid invoice of the same amount. Propose: the payer's account lead confirms what it is for, or the billing coordinator asks the bank if no client is identified. The controller decides whether it is held, applied or returned.
6. **Possible duplicates.** Flag any two receipts, or a receipt and a posting in the last 30 days, with the same payer and amount within [your duplicate window] days, or the same bank reference. Otherwise record "none found".
7. **Disputed items.** Record amount, days past due, the note and its date. Propose: not chased; the account lead reports on progress. Any credit is the controller's decision.
8. **Assign.** Name who acts and who decides (the controller unless your rules say otherwise). Flag anything older than [your unapplied-cash limit] days for the finance lead.
9. **Write the list** in the output format, in category order: short payments, ambiguous, unmatched, possible duplicates, disputed. Then "Checked, nothing found", then "Could not assess". Return it to the controller.

## Exceptions and stop conditions

- **Receipts log or match results missing:** stop; tell the billing coordinator.
- **Ledger and receipts log disagree on whether a receipt was posted:** stop on that item; ask the billing coordinator.
- **A note suggests financial difficulty or legal action:** list that item first; flag it to the controller and finance lead the same day.
- **A receipt exceeds the payer's open balances by more than [your overpayment threshold]:** list as unmatched; flag a possible overpayment.
- **Asked to apply, write off, credit, refund or contact anyone:** decline; name the controller.

## Output format

```
RECEIVABLES EXCEPTIONS FOR THE CONTROLLER: [date]
Period: receipts [from] to [to]. Ledger as of [export date]. Bank feed to [date].
Rules applied: [firm rules, or "template defaults: firm rules not supplied"]

[n]. [CATEGORY]
Item: [invoice or receipt, client, amounts, dates]
Evidence: [facts, each with its source]
Possible explanations: [each one the evidence supports]
Proposed next step: [action]. Acts: [role]. Decides: [role].
[Hold: reminders on [invoices] until resolved.]

CHECKED, NOTHING FOUND
[Check]: [scope]

COULD NOT ASSESS
[What, and why]

Status: Prepared for the controller's review. Nothing has been applied, written off, credited or sent.
```

## Reviewer checklist

1. Every non-clean receipt from the match results appears once. (Controller)
2. No ambiguous receipt has been assigned to a candidate. (Controller)
3. Amounts and dates match the receipts log and ledger. (Billing coordinator)
4. Every explanation is supported by cited evidence. (Controller)
5. Every item names who acts and who decides. (Controller)
6. Every reminder hold is carried to the follow-up plan. (Billing coordinator)
7. "Could not assess" is filled in, or says nothing fell outside the files. (Controller)

## Acceptance tests

Proposed tests. None has been run.

1. **Short payment.** Invoice for $1,200; $1,000 check naming it; no discount in notes. Expected: $200 open, three possible explanations, reminder hold. Fail if the $200 is written off or chased.
2. **Ambiguous receipt.** A $5,600 wire with no reference; two clients each owe $5,600 with the same due date. Expected: both candidates listed, receipt held, holds on both. Fail if one is chosen.
3. **Unmatched with a hint.** $350 referenced "retainer top-up"; no open invoice, no retainer terms supplied. Expected: unmatched; account lead asked; no assumption that a retainer exists.
4. **Duplicate.** One client pays $2,300 twice in four days against one invoice. Expected: flagged with both receipts cited.
5. **Disputed invoice.** A note records a query about hours. Expected: disputed, not chased, account lead reports.
6. **Stale ledger.** The export predates Thursday's postings. Expected: warning at the top; balances marked "as of".
7. **Missing rules.** Expected: defaults applied and stated at the top.
8. **Asked to post.** The user asks to apply the wire to the first candidate. Expected: declines; names the controller.

## Instructions for the AI assistant

```
You prepare the receivables exception list for the controller after
provisional matching. You never apply receipts, write off balances, issue
credits or refunds, contact clients or the bank, or change any record.

Inputs: receipts log; provisional match results; ledger or aging export;
postings from the last 30 days; account-lead notes; the firm's rules. If
the receipts log or match results are missing, stop and say so. If the
rules are missing, use the defaults below and say so at the top.

Defaults: the billing coordinator applies a receipt to the invoice its
remittance names and the difference stays open; duplicate window [your
duplicate window] days.

1. Note the period, ledger export date and last bank-feed date.
2. Take every receipt marked short, ambiguous or unmatched, and every
   invoice the notes mark disputed or on hold.
3. SHORT PAYMENT: invoice, original, received, difference. Look for an
   agreed discount, a second payment and discount terms. List each
   explanation the evidence supports. Propose the billing coordinator asks
   the client. Hold reminders on the balance.
4. AMBIGUOUS RECEIPT: every candidate with evidence for and against. Never
   choose one. Propose: hold unapplied; billing coordinator asks the bank
   for originator details; each candidate's account lead checks with the
   client; hold reminders on every candidate.
5. UNMATCHED RECEIPT: payer, amount, date, reference. Check notes for a
   retainer or deposit and the ledger for a recent same-amount payment.
   Propose the account lead confirms. Never assume an arrangement exists.
6. POSSIBLE DUPLICATE: same payer and amount within the window, or same
   bank reference. Otherwise "none found".
7. DISPUTED: amount, days past due, note and date. Not chased.
8. Each item: who acts, who decides (controller by default).
9. Use the output format exactly, in the category order above, then
   CHECKED, NOTHING FOUND, then COULD NOT ASSESS. Cite a source for every
   fact. Never invent what a client said.
10. End with: "Status: Prepared for the controller's review. Nothing has
    been applied, written off, credited or sent."

If a note suggests financial difficulty or legal action, put that item
first and say it needs the controller and finance lead today. If asked to
apply, write off, credit, refund or send, decline and name the controller.
```

## What to customize

- How short payments are applied.
- [your write-off threshold], [your unapplied-cash limit], [your duplicate window], [your overpayment threshold].
- What counts as disputed, and where account leads record it.
- Who decides each category, if not the controller.
- Which exports and notes the assistant may read, read-only, in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 9 November 2026. Written by Fully Powered AI. Not yet tested in a client environment.
