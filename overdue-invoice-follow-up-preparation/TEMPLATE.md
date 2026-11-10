# Overdue-invoice follow-up preparation

Capability template, version 0.1.0.

## Purpose

Each week, from the refreshed aging report, account notes, past correspondence and the current exception list, prepare a follow-up plan for every overdue invoice and a draft for each one that should be followed up, in the firm's tone for its age bracket and from the sender the firm's rules name. Every invoice that should not be chased is held with its reason and the person who can release it. The assistant prepares; it never sends a message, offers terms, issues a credit or changes a record.

## When to use it and when not to

Use it each week once aging is refreshed and the exception list for the same period is assembled, and whenever a client misses a promised date.

Do not use it when:

- the exception list is not ready. Without it, the plan can chase a client whose payment sits unidentified;
- the invoice has gone to a collections agency or a lawyer;
- the client has asked for a payment plan. A person negotiates it.

## Roles

- **Runs it:** the billing coordinator.
- **Reviews and sends early-bracket reminders:** the billing coordinator.
- **Reviews and sends firmer notes for their clients:** the account lead.
- **Copied on the firmest notes:** the finance lead.
- **Releases a hold on a balance under review or an unidentified receipt:** the controller.
- **Releases a disputed invoice for follow-up:** the account lead, once the dispute is resolved.

## Inputs

1. **Refreshed aging report:** invoice, client, due date, open balance, days past due. From the accounting system. If missing or older than [your staleness limit] days, stop.
2. **Account notes:** promised dates, disputes, agreed holds, contacts. If a client has none, treat it as no promise and no dispute, and say so.
3. **Past correspondence** on each overdue invoice, with dates. From the shared mailbox or billing system. If missing, mark each draft "previous contact not checked".
4. **Current exception list,** from the receivables exception review. Supplies holds for short-payment balances and unidentified receipts. If missing, stop.
5. **Tone guide:** brackets, one approved example each, sender and copy rules. If missing, use the defaults below and say so.
6. **Payables contact** for each client. If missing, prepare the draft and flag "no contact on file".

## The procedure

1. **List every overdue invoice** from the aging report: days past due of 1 or more. Leave out current invoices.
2. **Apply the holds first,** in this order, and stop at the first that applies:
   - Disputed or on hold in the notes: **Not chased.** Reason: the note and its date. Released by the account lead.
   - The invoice is a candidate for an ambiguous receipt on the exception list: **Held.** Reason: may already be paid. Released by the controller once identified.
   - The open balance is a short-payment difference under review: **Held.** Reason: cause unconfirmed. Released by the controller.
   - A reminder was sent fewer than [your minimum gap] days ago and has had no reply: **Held.** Reason: date of last reminder.
   - A promised date in the notes has not yet arrived: **Held** until the day after the promised date.
3. **Set the bracket** for each remaining invoice. Defaults, unless the tone guide sets others:
   - 1 to 30 days: a short reminder from the billing coordinator.
   - 31 to 60 days: a request for a payment date from the billing coordinator, account lead copied.
   - Over 60 days, or any missed promise: a direct note from the account lead, finance lead copied.
4. **Read the history:** last reminder, last reply, any promise. A missed promise moves the invoice to the firmest bracket regardless of age.
5. **Draft the message** in the bracket's tone, modelled on the approved example. State the invoice number, amount and due date; refer to the last reply or promise; thank the client for any recent payment on another invoice; reference the invoice copy. Ask for one thing: a payment date, or what is holding it up.
6. **Never include** a payment plan, discount, credit, late fee, threat or statement about legal action. The sender adds any of these.
7. **Write the plan:** every overdue invoice, its action (draft, held, not chased), the reason and the sender or releaser. Then the drafts in the same order. Return it to the billing coordinator, who routes account-lead drafts.

## Exceptions and stop conditions

- **Aging report missing or stale:** stop; ask the billing coordinator.
- **Exception list missing:** stop; ask for the exception review to be run.
- **A client's reply disputes the invoice but the notes do not mark it disputed:** treat it as disputed; flag it to the account lead.
- **A note mentions the client's financial difficulty, a complaint about the work or legal action:** prepare no draft for that client; flag it to the account lead and finance lead.
- **Asked to send, or to offer terms:** decline; name the sender or the controller.

## Output format

```
FOLLOW-UP PLAN: aging as of [date]
Exception list of [date] applied. Rules: [tone guide, or "template defaults"]

[Invoice], [client], [amount], [days] days past due
Action: [Draft / Held / Not chased]. Reason: [reason, source and date].
From: [sender role], copy [role]. / Released by: [role].

DRAFTS

[Invoice], for [sender role] to review and send
To: [payables contact or "no contact on file"]   Cc: [role]
Subject: Invoice [number], [amount]: [payment date / payment reminder]

[Message]

[Sender role]

Status: Drafts for review. Nothing has been sent.
```

## Reviewer checklist

1. Every overdue invoice on the aging report is in the plan exactly once. (Billing coordinator)
2. No draft exists for a disputed, held or not-chased invoice. (Billing coordinator)
3. Every hold from the exception list is applied. (Billing coordinator)
4. Each draft's invoice number, amount, due date and promise match the sources. (Billing coordinator)
5. Each draft sounds like the firm and the sender. (Account lead, for theirs)
6. No draft offers terms, a credit or a fee. (Account lead or billing coordinator)
7. Every sender and copy follows the bracket rules. (Billing coordinator)

## Acceptance tests

Proposed tests. None has been run.

1. **Missed promise.** An invoice 58 days past due; notes record a promised date that passed two weeks ago. Expected: draft from the account lead, finance lead copied, citing the promise.
2. **Disputed invoice.** A note records a dispute over hours. Expected: not chased; no draft; released by the account lead.
3. **Possibly paid.** Two invoices are candidates for one unidentified wire. Expected: both held; no drafts.
4. **Balance under review.** A $200 short-payment difference is on the exception list. Expected: held; no draft.
5. **Recent payment on another invoice.** The client paid a newer invoice this week. Expected: the draft for the older one thanks them for it and asks for a date.
6. **Reply disputes, notes do not.** The client's last email questions the invoice. Expected: treated as disputed; flagged to the account lead.
7. **No contact on file.** Expected: draft prepared, "no contact on file" flagged.
8. **Asked to offer a payment plan.** Expected: declines; the plan notes the request for the account lead.

## Instructions for the AI assistant

```
You prepare overdue-invoice follow-ups for the firm's review. You never send
messages, offer payment plans, discounts, credits or fees, or change records.

The user will supply: the refreshed aging report; account notes; past
correspondence; the current exception list; the tone guide; contacts. If
the aging report or the exception list is missing, stop and say so. If the
tone guide is missing, use the defaults below and say so.

1. List every invoice 1 or more days past due.
2. Apply holds in this order, first match wins:
   disputed or on hold in notes -> Not chased, released by account lead;
   candidate for an ambiguous receipt -> Held, released by controller;
   short-payment balance under review -> Held, released by controller;
   reminder sent under [your minimum gap] days ago, no reply -> Held;
   promised date not yet reached -> Held until the day after it.
3. Default brackets: 1-30 days, short reminder from the billing
   coordinator; 31-60 days, request for a payment date from the billing
   coordinator, account lead copied; over 60 days or any missed promise,
   direct note from the account lead, finance lead copied.
4. Draft each message in the bracket's tone, modelled on the approved
   example. State invoice number, amount and due date. Refer to the last
   reply or promise. Thank the client for any recent payment on another
   invoice. Ask for one thing: a payment date or what is holding it up.
5. Never include terms, credits, fees, threats or legal statements.
6. If a reply disputes an invoice the notes do not mark disputed, treat it
   as disputed and flag it. If notes mention financial difficulty, a
   complaint or legal action, draft nothing for that client and flag it.
7. Output the plan for every overdue invoice, then the drafts, using the
   output format exactly. End with: "Status: Drafts for review. Nothing
   has been sent."

If asked to send or to offer terms, decline and name who does it.
```

## What to customize

- Your brackets, one approved example message each, and sender and copy rules.
- [your minimum gap] between reminders and [your staleness limit] for the aging report.
- Whether a missed promise jumps straight to the account lead.
- Hold categories beyond the defaults, such as clients on agreed extended terms.
- Where drafts land: a shared review document or each sender's drafts folder.
- Which notes and mailboxes the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 9 November 2026. Written by Fully Powered AI. Not yet tested in a client environment.
