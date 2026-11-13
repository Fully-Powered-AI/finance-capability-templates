# Collections call brief: an invented example

*Illustrative example with invented data.* The company, the customer, the people, the phone numbers, the invoices, the payments, the notes and every date below are invented. The company is an invented 40-person wholesale distributor of garden supplies. Its customer appears as Customer A, a business that runs three garden centres, and the customer's staff appear as Contact 1 and Contact 2. The company's own staff appear by role only. Phone numbers use the 555-01 range kept for fiction.

On the morning of Monday 9 November 2026 the credit controller exported Customer A's account and ran the brief before phoning. After the call, the credit controller ran it again with the call notes. The inputs come first, in full, so the workflow template can be run on them. The brief and the call record it returned follow.

## The inputs

### 1. Settings (typed by the credit controller)

```
Company: invented wholesale distributor of garden supplies, about 40 people
Customer: Customer A, account A-1042
Customer type: business
Today: Monday 9 November 2026
Caller: Credit controller
Approver: Finance manager
Applies payments and enters the contact log: Credit controller
Currency: USD
Ledger balance on the account today: 12070.40
Payment terms on the account: 30 days from invoice date
Account status: open
Promise grace days: 3
Contact log and payments period: 90 days
```

### 2. Open items export: open_items.csv

```
doc_no,doc_type,doc_date,due_date,amount,open_amount,reference
INV-5521,invoice,2026-08-14,2026-09-13,4860.00,4860.00,PO 7731
INV-5588,invoice,2026-09-02,2026-10-02,2315.40,2315.40,PO 7790
INV-5604,invoice,2026-09-11,2026-10-11,3120.00,1120.00,PO 7802
INV-5650,invoice,2026-09-29,2026-10-29,1985.00,1985.00,PO 7844
INV-5702,invoice,2026-10-20,2026-11-19,2740.00,2740.00,PO 7901
CN-0218,credit note,2026-10-05,,-350.00,-350.00,"Return of 10 bags of compost, INV-5588"
PAY-1105,unapplied payment,2026-11-05,,-600.00,-600.00,"Remittance: on account"
```

### 3. Payments export: payments.csv

```
payment_id,date,amount,applied_to
PAY-0925,2026-09-25,3410.00,INV-5480
PAY-1016,2026-10-16,2000.00,INV-5604
PAY-1105,2026-11-05,600.00,unapplied
```

### 4. Contact log: contact_log.csv

```
date,method,direction,contact,logged_by,summary,promise_amount,promise_date,promise_invoices
2026-09-21,email,out,Contact 1,Credit controller,"Statement sent. Noted INV-5521 overdue.",,,
2026-10-07,phone,out,Contact 1,Credit controller,"Contact 1 said INV-5521 is approved and will be in the payment run on 16 October.",4860.00,2026-10-16,INV-5521
2026-10-22,phone,out,Contact 1,Credit controller,"INV-5521 not paid. Contact 1 said Contact 2 is holding it over a query on PO 7731 and would call back.",,,
2026-10-28,email,in,Contact 2,,"Contact 2 reports 12 cases of plant pots on INV-5650 broken on delivery and asks for a credit.",,,
2026-11-02,phone,in,Contact 2,Credit controller,"Contact 2 promised 600.00 on account this week. INV-5521 to follow once the PO 7731 query is answered; the query is about the delivery address.",600.00,2026-11-06,
```

### 5. Contacts: contacts.csv

```
contact,role,phone,email,preferred_for_payments,notes
Contact 1,Accounts payable clerk,555-0142,ap@customer-a.example,yes,In the office Monday to Thursday.
Contact 2,Finance director,555-0157,,no,Approves the weekly payment runs.
```

### 6. Disputes file: disputes.csv

```
dispute_ref,doc_no,raised_date,amount,reason,status,owner,last_update
D-27,INV-5480,2026-09-08,120.00,Short delivery of one pallet,resolved,Warehouse manager,Credit note CN-0201 issued 15 September.
D-31,INV-5650,2026-10-28,410.00,12 cases of plant pots reported broken on delivery,open,Warehouse manager,Photos requested from Contact 2 on 29 October; none received yet.
```

### 7. Collections terms

```
Collections terms, approved by the finance manager, 1 March 2026
1. Our standard terms are payment within 30 days of the invoice date.
2. The caller may accept a promised payment date up to 14 days after the day of the call without approval.
3. A later date, or payment in instalments, needs the finance manager's approval before it is agreed.
4. No discount, fee waiver or credit is offered on a call. Credits are issued only through the dispute process.
5. Copies of invoices, credit notes, statements and proofs of delivery may be sent on request.
```

### 8. The credit controller's notes, typed after the call

```
Call Mon 9 Nov 2026, 10:20 to 10:34. Rang 555-0142, spoke to Contact 1.
- 5521 held because PO 7731 has our old delivery address for them (Store 2, should be Store 3). Wants 5521 reissued showing Store 3, then it goes in a run. Asked if they can pay 5521 in two halves, 19 Nov and 3 Dec. Told her I'd have to check with the finance manager.
- The 2,000 on 16 Oct was meant for 5604, not 5521.
- 600 on 5 Nov is for 5604.
- 5588 and the rest of 5604 (520.00) go in the 19 Nov run.
- 5650: paying the 1,575 not in dispute on 19 Nov. Contact 2 sending the photos this week.
- CN-0218: she hasn't seen it. Said I'd email a copy today.
```

## The output, before the call (Part A)

**COLLECTIONS CALL BRIEF: Customer A, account A-1042**

**For:** Credit controller, call on Monday 9 November 2026. Prepared from: open items (7 rows, balance 12,070.40 USD, ties to the ledger balance in the settings); payments (3 rows, 25 September 2026 to 5 November 2026); contact log (5 entries since 11 August 2026); contacts (2); disputes file (1 open); collections terms (Collections terms, 1 March 2026).

**Account status:** open. For the caller's information; not a line to use on the call.

**Ask for:** Contact 1, Accounts payable clerk, 555-0142. Why: made the BROKEN promise of 7 October 2026.

**Also on file:** Contact 2, Finance director, 555-0157: approves the weekly payment runs; on 28 October 2026 emailed about broken plant pots on INV-5650 (see D-31); on 2 November 2026 said INV-5521 waits on the PO 7731 query.

**Where the account stands**

- Overdue: 10,280.40 on 4 invoices. In dispute: 410.00. Overdue and not in dispute: 9,870.40, of which 4,860.00 is held by a query not logged.
- Not yet due: 2,740.00 on 1 invoice.
- Credits not yet used: 950.00 (CN-0218 350.00; PAY-1105 600.00).
- Check: 10,280.40 + 2,740.00 − 950.00 = 12,070.40.

**Open invoices, oldest first**

- INV-5521, PO 7731, invoiced 14 August 2026, due 13 September 2026: 4,860.00 open of 4,860.00, 57 days overdue. Held by a query not logged: see question 2.
- INV-5588, PO 7790, invoiced 2 September 2026, due 2 October 2026: 2,315.40 open of 2,315.40, 38 days overdue.
- INV-5604, PO 7802, invoiced 11 September 2026, due 11 October 2026: 1,120.00 open of 3,120.00, 29 days overdue.
- INV-5650, PO 7844, invoiced 29 September 2026, due 29 October 2026: 1,985.00 open of 1,985.00, 11 days overdue. In dispute: 410.00, D-31.
- INV-5702, PO 7901, invoiced 20 October 2026, due 19 November 2026: 2,740.00 open of 2,740.00, due in 10 days.

**What they were told and promised**

- 21 September 2026, email, out, Contact 1 (by Credit controller): "Statement sent. Noted INV-5521 overdue."
- 7 October 2026, phone, out, Contact 1 (by Credit controller): "Contact 1 said INV-5521 is approved and will be in the payment run on 16 October."
- 22 October 2026, phone, out, Contact 1 (by Credit controller): "INV-5521 not paid. Contact 1 said Contact 2 is holding it over a query on PO 7731 and would call back."
- 28 October 2026, email, in, Contact 2: "Contact 2 reports 12 cases of plant pots on INV-5650 broken on delivery and asks for a credit."
- 2 November 2026, phone, in, Contact 2 (by Credit controller): "Contact 2 promised 600.00 on account this week. INV-5521 to follow once the PO 7731 query is answered; the query is about the delivery address."

Promises:

- 7 October 2026, Contact 1: 4,860.00 by 16 October 2026, for INV-5521: BROKEN: nothing applied to INV-5521 by 19 October 2026. In that window, PAY-1016, 2,000.00 on 16 October 2026, was applied to INV-5604.
- 2 November 2026, Contact 2: 600.00 by 6 November 2026, on account: KEPT: PAY-1105 600.00 on 5 November 2026.

**Disputes, queries and credit notes**

- D-31, INV-5650, 410.00, raised 28 October 2026: "12 cases of plant pots reported broken on delivery". Status: open; owner Warehouse manager; last update: "Photos requested from Contact 2 on 29 October; none received yet."
- Query not logged: INV-5521 (PO 7731): "Contact 1 said Contact 2 is holding it over a query on PO 7731" and "the query is about the delivery address" (22 October 2026 and 2 November 2026). Not in the disputes file; the finance manager decides whether to log it.
- CN-0218, credit note, 350.00, dated 5 October 2026: "Return of 10 bags of compost, INV-5588". Not yet used.
- PAY-1105, unapplied payment, 600.00, received 5 November 2026: "Remittance: on account".

**Questions to settle on the call**

1. Contact 1 promised 4,860.00 for INV-5521 by 16 October 2026; nothing was applied to INV-5521 by 19 October 2026. In that window PAY-1016, 2,000.00 on 16 October 2026, was applied to INV-5604. Ask: What held up INV-5521, and was the 2,000.00 paid on 16 October meant for INV-5604?
2. On 22 October and 2 November 2026 the log records INV-5521 held over a query on PO 7731 about the delivery address. The query is not in the disputes file. Ask: What exactly is wrong with the delivery address on PO 7731, what do you need from us to clear it, and on what date will INV-5521 be paid once it is cleared?
3. Overdue and not in dispute: INV-5588 2,315.40, 38 days overdue; INV-5604 1,120.00, 29 days overdue; INV-5650 1,575.00 of 1,985.00, 11 days overdue (410.00 is in dispute D-31). Total 5,010.40. Ask: On what date will these be paid?
4. PAY-1105, 600.00, received 5 November 2026 with the remittance "on account", has not been applied. Ask: Which invoice or invoices should the 600.00 go against?
5. CN-0218, 350.00, dated 5 October 2026, for the return of 10 bags of compost on INV-5588, has not been used. Ask: Have you received CN-0218, and which invoice will you take it against?
6. D-31 on INV-5650, 410.00, is open, with the warehouse manager as owner. Photos were requested from Contact 2 on 29 October 2026; none have arrived. Ask: Have the photos of the broken cases been sent, or when will they be?

**What you may offer, quoted from the collections terms (Collections terms, 1 March 2026)**

- Standard terms: item 1: "Our standard terms are payment within 30 days of the invoice date."
- May agree without approval: item 2: "The caller may accept a promised payment date up to 14 days after the day of the call without approval." Item 5: "Copies of invoices, credit notes, statements and proofs of delivery may be sent on request."
- Needs the finance manager's approval first: item 3: "A later date, or payment in instalments, needs the finance manager's approval before it is agreed."
- Never offered on a call: item 4: "No discount, fee waiver or credit is offered on a call. Credits are issued only through the dispute process."
- Anything asked for that is not written here: "I'll take that to the finance manager and come back to you."

Prepared for the credit controller. Every line traces to the files named above. Nothing has been sent, no one has been contacted and no record has been changed.

## The output, after the call (Part B)

**COLLECTIONS CALL RECORD: Customer A, account A-1042, call on 9 November 2026, 10:20**

Draft for the finance manager to confirm. From the credit controller's notes of 9 November 2026 and the brief of 9 November 2026.

**Spoke to:** Contact 1, Accounts payable clerk.

**Answers to the brief's questions**

1. What held up INV-5521, and whether the 2,000.00 of 16 October was meant for INV-5604: INV-5521 is held because PO 7731 has the old delivery address (Store 2; it should be Store 3). The 2,000.00 of 16 October was meant for INV-5604, not INV-5521.
2. The PO 7731 query, what clears it, and when INV-5521 will be paid: the delivery address on PO 7731 is Store 2 and should be Store 3; Contact 1 wants INV-5521 reissued showing Store 3, after which it goes into a payment run. Payment date: not settled; Contact 1 asked to pay it in two halves, on 19 November and 3 December (see Requests and offers beyond the written terms).
3. Date for INV-5588, INV-5604 and the part of INV-5650 not in dispute: INV-5588 and the rest of INV-5604 (520.00) go in the 19 November run; the 1,575.00 of INV-5650 not in dispute is paid on 19 November.
4. Where the 600.00 of 5 November goes: INV-5604.
5. CN-0218: Contact 1 has not seen it; the credit controller said a copy would be emailed today. Which invoice it will be taken against: not covered in the notes.
6. D-31 photos: Contact 2 is sending them this week.

**Promises made by the customer**

- 19 November 2026: 4,410.40, from Contact 1: INV-5588 2,315.40 (open balance; amount not stated in the notes); INV-5604 520.00; INV-5650 1,575.00. Within the collections terms, item 2.

**Requests and offers beyond the written terms (not agreed)**

- Contact 1 asked: INV-5521 paid in two halves (2,430.00 each if equal; amounts not stated in the notes), on 19 November 2026 and 3 December 2026. Collections terms, item 3: "A later date, or payment in instalments, needs the finance manager's approval before it is agreed." For the finance manager to decide.
- Contact 1 asked: INV-5521 reissued showing the Store 3 delivery address. The collections terms do not cover it. For the finance manager to decide.

**What the credit controller said they would do**

- Email Contact 1 a copy of CN-0218, by 9 November 2026.
- Check the two-payment request for INV-5521 with the finance manager, no date given.

**Actions for a person**

1. Decide whether INV-5521 may be paid in two halves (2,430.00 each if equal; amounts not stated in the notes), on 19 November and 3 December 2026 (collections terms, item 3). Owner: Finance manager.
2. Decide whether INV-5521 is reissued showing the Store 3 delivery address, and whether the PO 7731 query is logged as a dispute. Owner: Finance manager.
3. Email Contact 1 a copy of CN-0218. Owner: Credit controller. By 9 November 2026.
4. Apply PAY-1105, 600.00, to INV-5604, as Contact 1 directed. Owner: Credit controller.
5. Enter the contact log entry below once this record is confirmed. Owner: Credit controller.
6. Record on D-31 that Contact 2 says the photos will be sent this week. Owner: Warehouse manager.
7. Check that the 4,410.40 promised for 19 November 2026 has arrived. Owner: Credit controller. By 23 November 2026.

**Still open after the call**

- The payment date for INV-5521, 4,860.00: waits on the finance manager's decisions in actions 1 and 2.
- Which invoice CN-0218 will be taken against: not covered in the notes. If it is taken against INV-5588, the 19 November payment on INV-5588 would be 2,315.40 − 350.00 = 1,965.40, and the total for 19 November 4,410.40 − 350.00 = 4,060.40.

**Contact log entry, for the credit controller to enter**

```
2026-11-09,phone,out,Contact 1,Credit controller,"INV-5521 held: PO 7731 has the old delivery address (Store 2, should be Store 3). Customer asks for INV-5521 reissued and paid in two halves on 19 Nov and 3 Dec; not agreed, with the finance manager. 2,000.00 of 16 Oct was for INV-5604. 600.00 of 5 Nov to go to INV-5604. CN-0218 not received; copy to be emailed. Contact 2 sending D-31 photos this week.",4410.40,2026-11-19,INV-5588;INV-5604;INV-5650
```

**Points in the notes the record could not place:** None.

Draft for the finance manager to confirm. Nothing has been sent, entered or changed.
