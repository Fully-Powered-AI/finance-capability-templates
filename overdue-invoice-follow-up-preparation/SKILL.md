---
name: "overdue-invoice-follow-up-preparation"
description: "Each week, from the refreshed aging report, account notes, past correspondence and the current exception list, prepare a follow-up plan for every overdue invoice and a draft for each one that should be followed up, in the firm's tone for its age bracket and from the sender the firm's rules name. Every invoice that should not be chased is held with its reason and the person who can release it. The assistant prepares; it never sends a message, offers terms, issues a credit or changes a record."
license: "MIT"
metadata:
  version: "0.1.0"
  publisher: "Fully Powered AI"
  capability: "Overdue-invoice follow-up preparation"
---

# Overdue-invoice follow-up preparation

This is the technical file for a Fully Powered capability template. It carries the instructions an AI product follows. The complete template, with roles, inputs, exceptions, the reviewer checklist, acceptance tests and what to customize, is in [TEMPLATE.md](TEMPLATE.md). A worked example with invented data is in [EXAMPLE.md](EXAMPLE.md).

## Instructions

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

## Before relying on it

Decide every item under "What to customize" in TEMPLATE.md and set the limits the instructions in this file leave open, written in square brackets such as [N], to your own. Then run the acceptance tests in TEMPLATE.md on past work. A person starts this work, supplies the inputs and decides what happens with the result.
