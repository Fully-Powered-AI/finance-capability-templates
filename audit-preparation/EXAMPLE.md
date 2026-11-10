# Audit preparation: an invented example

*Illustrative example with invented data.* The company, the audit, the suppliers, every row and every figure below are invented. The company is an invented 60-person maker of commercial kitchen equipment, called "the Company" here, with a year end of 30 September. Its finance team is a controller, a staff accountant, a payables clerk and a part-time payroll administrator, reporting to the chief executive. Suppliers are referred to by letter and people by role. The external auditors sent their request list two weeks ago, and the controller runs the pack on Monday 9 November 2026.

The inputs come first, in full, so the template can be run on them. The pack follows.

## The inputs

### 1. Settings

```
Company: the Company. Year end: 30 September 2026.
Today: Monday 9 November 2026. Fieldwork starts: Monday 23 November 2026.
Runs the pack and approves it: Controller.
Approves items before they go to the auditors: Controller.
  Items the Controller owns: Chief executive.
Approves answers: Chief executive for legal claims, tax positions,
  suspected fraud, the business's ability to keep operating and events
  after the year end. Controller for everything else.
Working days: Monday to Friday.
Closed: Thursday 26 and Friday 27 November 2026.
Lead time: 3 working days.
Approval limit: $5,000.00. A payment at or above it must be approved by
  someone other than the person who entered it.
Movement threshold: $25,000 and 10%, both.
```

### 2. The auditors' request list

```
Ref,Request,Area,Due,Format
A1,Trial balance at 30 September 2026,General,2026-11-10,Excel
A2,Bank reconciliations for all accounts at 30 September 2026 with bank statements,Cash,2026-11-13,PDF
A3,Receivables aging at 30 September 2026 tied to the general ledger,Revenue and receivables,2026-11-16,Excel
A4,Inventory count sheets and final valuation at 30 September 2026,Inventory,2026-11-16,Excel
A5,Fixed asset register with additions and disposals for the year,Fixed assets,2026-11-18,Excel
A6,Payables aging at 30 September 2026 and a search for unrecorded liabilities (payments 1 October to 6 November 2026),Payables,2026-11-18,Excel
A7,Payroll register for the year and payroll tax filings,Payroll,2026-11-18,PDF
A8,Loan documents and covenant calculation at 30 September 2026,Debt,2026-11-20,PDF
A9,Board minutes for the year,Governance,2026-11-20,PDF
A10,List of related parties and transactions with them during the year,Governance,2026-11-20,Excel
```

### 3. The owner and status list

```
Ref,Owner,Status,Document,Approved by,Note
A1,Controller,in progress,TB_FY2026.xlsx,,Two late supplier bills still to post
A2,Staff accountant,in progress,,,September statement for the savings account not yet downloaded
A3,Staff accountant,ready for review,AR aging 30 Sep 2026 tied to GL.xlsx,,
A4,Warehouse manager,in progress,Count sheets 30 Sep 2026 (scanned),,Valuation not finished
A5,,not started,,,
A6,Payables clerk,not started,,,
A7,Payroll administrator,in progress,,,Payroll provider sends the year summary on 12 November
A8,Controller,in progress,Covenant calculation 30 Sep 2026.xlsx,,
A9,Chief executive,sent,Board minutes FY2026.pdf,,
A11,Controller,in progress,,,Lease schedule for the new warehouse
```

### 4. Last year's request list

```
Ref,Request,Area
A1,Trial balance at 30 September 2025,General
A2,Bank reconciliations for all accounts at 30 September 2025 with bank statements,Cash
A3,Receivables aging at 30 September 2025 tied to the general ledger,Revenue and receivables
A4,Inventory count sheets and final valuation at 30 September 2025,Inventory
A5,Fixed asset register with additions and disposals for the year,Fixed assets
A6,Payables aging at 30 September 2025,Payables
A7,Payroll register for the year and payroll tax filings,Payroll
A8,Loan documents and covenant calculation at 30 September 2025,Debt
A9,Board minutes for the year,Governance
A10,Lender's confirmation of the loan balance at 30 September 2025,Debt
```

### 5. The controls list

```
ID,Control,Process,Owner,Frequency,Evidence,Kept at
C1,"Supplier payments of $5,000 or more approved before release",Supplier payments,Controller,Each payment,Approval record in the banking system,Monthly approval report in the finance drive
C2,Bank reconciliations reviewed and signed,Cash,Controller,Monthly,Signed reconciliation,Finance drive
C3,Changes to a supplier's bank details confirmed by a call to a number already on file,Supplier payments,Payables clerk,Each change,,
C4,Payroll changes approved before the pay run,Payroll,Chief executive,Each pay run,Signed change form,Payroll folder
C5,Manual journal entries reviewed,Manual journal entries,Chief executive,Monthly,Initialled journal list,Finance drive
```

### 6. The who-does-what list

```
Process,Approves,Records,Handles the money,Checks,Compensating control
Supplier payments,Controller,Payables clerk,Controller,Controller,
Payroll,Chief executive,Payroll administrator,Payroll provider,Controller,
Manual journal entries,Controller,Controller,n/a,Controller,Chief executive reviews and initials the monthly journal list
Cash receipts,n/a,Staff accountant,Staff accountant,Staff accountant,Controller reviews and signs the bank reconciliation each month
```

### 7. The approvals export (supplier payments, 1 July to 30 September 2026)

```
Date,Supplier,Amount,Entered by,Approved by
2026-07-08,Supplier A,12400.00,Payables clerk,Controller
2026-07-22,Supplier B,6150.00,Payables clerk,Controller
2026-08-05,Supplier C,8900.00,Payables clerk,
2026-08-12,Supplier F,3200.00,Payables clerk,
2026-08-19,Supplier A,15200.00,Payables clerk,Controller
2026-09-02,Supplier D,5000.00,Controller,Controller
2026-09-16,Supplier B,7480.00,Payables clerk,Controller
2026-09-30,Supplier E,22650.00,Payables clerk,Controller
```

### 8. Last year's findings

```
ID,Finding,Area,What was done,Evidence,Owner,Status
F1,Count differences over $500 were not investigated before the inventory valuation was finished,Inventory,Count procedure changed: every difference over $500 is recounted and signed off by the warehouse manager before valuation,Signed recount sheets from the September 2026 count,Warehouse manager,done
F2,Two changes to supplier bank details were made without confirmation,Payments,Payables clerk told to call suppliers before changing bank details,,Payables clerk,done
F3,Fixed asset register not reconciled to the general ledger during the year,Fixed assets,,,Controller,open
```

### 9. The trial balance comparison and the movement notes

```
Account,This year,Last year
Cash,412300,388900
Receivables,1046500,812400
Inventory,1384200,1402600
Fixed assets (net),2210800,1675300
Payables,-598400,-561200
Loan,-1500000,-1100000
Revenue,-9420000,-8860000
Cost of sales,6310500,5845200
Payroll expense,2085000,1998400

Account,Explanation
Fixed assets (net),"Additions of $612,000 for the new warehouse fit-out and two press brakes, less depreciation"
Loan,"Drew a further $400,000 on the term loan in March 2026 to fund the warehouse"
```

### 10. Expected questions

```
ID,Question,Facts,Source
Q1,Did revenue recognition or customer pricing terms change during the year?,No change. We invoice on shipment and standard terms are 30 days.,Controller; standard terms of sale
Q2,Are there any legal claims or disputes outstanding?,A customer has written about a possible claim over a late delivery.,Chief executive
Q3,Has anything happened since the year end that could affect the accounts?,,
```

## The output

```
AUDIT PREPARATION PACK: the Company, year ended 30 September 2026

For: Controller. Prepared: Monday 9 November 2026. Fieldwork starts: Monday 23 November 2026.
Sources: auditors' request list, 10 items; owner and status list, 10 rows; last year's request list, 10 items; controls list, 5 controls; who-does-what list, 4 processes; approvals export, 8 payments, 1 July to 30 September 2026; last year's findings, 3; trial balance comparison, 9 accounts, with 2 movement notes; expected questions, 3.
Settings used: lead time 3 working days; approval limit $5,000.00; movement threshold $25,000 and 10%; working days Monday to Friday; closed days Thursday 26 and Friday 27 November 2026. Items approved by Controller; items Controller owns approved by Chief executive. Defaults used: none.

SUMMARY
Items on the auditors' list: 10. Not started 3. In progress 5. Ready for review 1. Approved to send 0. Sent 1. Late 1.
Flagged lines: 14. Decisions and questions: 14.

REQUEST TRACKER
General
A1 Trial balance at 30 September 2026. Owner: Controller. Auditors' date: Tuesday 10 November 2026. Our date: Thursday 5 November 2026. Format: Excel. Document: TB_FY2026.xlsx. Status: in progress. Approved by: not yet. Note: Two late supplier bills still to post. FLAG, late: our date passed on Thursday 5 November and the auditors' date is tomorrow. See 1.

Cash
A2 Bank reconciliations for all accounts at 30 September 2026 with bank statements. Owner: Staff accountant. Auditors' date: Friday 13 November 2026. Our date: Tuesday 10 November 2026. Format: PDF. Document: not named. Status: in progress. Approved by: not yet. Note: September statement for the savings account not yet downloaded.

Revenue and receivables
A3 Receivables aging at 30 September 2026 tied to the general ledger. Owner: Staff accountant. Auditors' date: Monday 16 November 2026. Our date: Wednesday 11 November 2026. Format: Excel. Document: AR aging 30 Sep 2026 tied to GL.xlsx. Status: ready for review. Approved by: not yet.

Inventory
A4 Inventory count sheets and final valuation at 30 September 2026. Owner: Warehouse manager. Auditors' date: Monday 16 November 2026. Our date: Wednesday 11 November 2026. Format: Excel. Document: Count sheets 30 Sep 2026 (scanned). Status: in progress. Approved by: not yet. Note: Valuation not finished.

Fixed assets
A5 Fixed asset register with additions and disposals for the year. Owner: not assigned. Auditors' date: Wednesday 18 November 2026. Our date: Friday 13 November 2026. Format: Excel. Document: not named. Status: not started. Approved by: not yet. FLAG, no owner: the owner field is blank. See 2.

Payables
A6 Payables aging at 30 September 2026 and a search for unrecorded liabilities (payments 1 October to 6 November 2026). Owner: Payables clerk. Auditors' date: Wednesday 18 November 2026. Our date: Friday 13 November 2026. Format: Excel. Document: not named. Status: not started. Approved by: not yet.

Payroll
A7 Payroll register for the year and payroll tax filings. Owner: Payroll administrator. Auditors' date: Wednesday 18 November 2026. Our date: Friday 13 November 2026. Format: PDF. Document: not named. Status: in progress. Approved by: not yet. Note: Payroll provider sends the year summary on 12 November.

Debt
A8 Loan documents and covenant calculation at 30 September 2026. Owner: Controller. Auditors' date: Friday 20 November 2026. Our date: Tuesday 17 November 2026. Format: PDF. Document: Covenant calculation 30 Sep 2026.xlsx. Status: in progress. Approved by: not yet.

Governance
A9 Board minutes for the year. Owner: Chief executive. Auditors' date: Friday 20 November 2026. Our date: Tuesday 17 November 2026. Format: PDF. Document: Board minutes FY2026.pdf. Status: sent. Approved by: not yet. FLAG, not approved: the status is sent and nobody is named as approving it. See 3.
A10 List of related parties and transactions with them during the year. Owner: not assigned. Auditors' date: Friday 20 November 2026. Our date: Tuesday 17 November 2026. Format: Excel. Document: not named. Status: not started. Approved by: not yet. FLAG, no owner: A10 is not on the owner and status list. See 4.

Not on the auditors' list
A11. Owner: Controller. Document: not named. Status: in progress. Note: Lease schedule for the new warehouse. FLAG, not on the auditors' list. See 5.

CHANGES FROM LAST YEAR'S LIST
New this year: A10, List of related parties and transactions with them during the year.
Changed: A6: last year "Payables aging at 30 September 2025"; this year "Payables aging at 30 September 2026 and a search for unrecorded liabilities (payments 1 October to 6 November 2026)".
No longer requested: last year's A10, Lender's confirmation of the loan balance at 30 September 2025.

CONTROL EVIDENCE
C1 Supplier payments of $5,000 or more approved before release. Process: Supplier payments. Owner: Controller. Frequency: Each payment. Evidence: Approval record in the banking system. Kept at: Monthly approval report in the finance drive.
C2 Bank reconciliations reviewed and signed. Process: Cash. Owner: Controller. Frequency: Monthly. Evidence: Signed reconciliation. Kept at: Finance drive.
C3 Changes to a supplier's bank details confirmed by a call to a number already on file. Process: Supplier payments. Owner: Payables clerk. Frequency: Each change. Evidence: not named. Kept at: not stated. FLAG, no evidence named, not kept anywhere: the control leaves no record the auditors can test. See 6.
C4 Payroll changes approved before the pay run. Process: Payroll. Owner: Chief executive. Frequency: Each pay run. Evidence: Signed change form. Kept at: Payroll folder.
C5 Manual journal entries reviewed. Process: Manual journal entries. Owner: Chief executive. Frequency: Monthly. Evidence: Initialled journal list. Kept at: Finance drive.

WHO DOES WHAT
Supplier payments: approves Controller; records Payables clerk; handles the money Controller; checks Controller. FLAG, overlap with no compensating control: Controller approves, handles the money and checks. See 7.
Payroll: approves Chief executive; records Payroll administrator; handles the money Payroll provider; checks Controller. No overlap.
Manual journal entries: approves Controller; records Controller; handles the money n/a; checks Controller. Overlap: Controller approves, records and checks. Compensating control: Chief executive reviews and initials the monthly journal list, controller to confirm.
Cash receipts: approves n/a; records Staff accountant; handles the money Staff accountant; checks Staff accountant. Overlap: Staff accountant records, handles the money and checks. Compensating control: Controller reviews and signs the bank reconciliation each month, controller to confirm.

APPROVALS CHECK
Approval limit $5,000.00. 7 payments at or above the limit checked, $77,780.00. 1 below the limit, not checked.
2026-08-05 Supplier C $8,900.00: entered by Payables clerk; approved by none. FLAG, no approval recorded. See 8.
2026-09-02 Supplier D $5,000.00: entered by Controller; approved by Controller. FLAG, approved by the person who entered it. See 9.
Checked without a flag: 5.

LAST YEAR'S FINDINGS
F1 Count differences over $500 were not investigated before the inventory valuation was finished. Owner: Warehouse manager. What was done: Count procedure changed: every difference over $500 is recounted and signed off by the warehouse manager before valuation. Evidence: Signed recount sheets from the September 2026 count. Status: done. Related requests: A4.
F2 Two changes to supplier bank details were made without confirmation. Owner: Payables clerk. What was done: Payables clerk told to call suppliers before changing bank details. Evidence: none named. Status: done. Related requests: none. FLAG, no evidence named: the finding is marked done with nothing to show the auditors. See 10.
F3 Fixed asset register not reconciled to the general ledger during the year. Owner: Controller. What was done: nothing recorded. Evidence: none named. Status: open. Related requests: A5. FLAG, no action recorded: the finding is open and A5 has no owner. See 11.

MOVEMENTS THE AUDITORS WILL ASK ABOUT
Threshold: $25,000 and 10%, both. 9 accounts compared; 3 reach both.
Receivables: last year $812,400, this year $1,046,500, movement $234,100 (28.8%). Draft explanation: none. FLAG, no explanation. See 12.
Fixed assets (net): last year $1,675,300, this year $2,210,800, movement $535,500 (32.0%). Draft explanation: Additions of $612,000 for the new warehouse fit-out and two press brakes, less depreciation. Check: additions of $612,000 less the movement of $535,500 leave $76,500 for depreciation and any disposals; the support is in A5, the fixed asset register.
Loan: last year −$1,100,000, this year −$1,500,000, movement −$400,000 (36.4%). Draft explanation: Drew a further $400,000 on the term loan in March 2026 to fund the warehouse. Check: the note's $400,000 equals the movement, with nothing left over; the support is in A8, the loan documents.

DRAFT ANSWERS TO EXPECTED QUESTIONS
Q1 Did revenue recognition or customer pricing terms change during the year?
Draft answer: Neither changed during the year to 30 September 2026. The Company invoices on shipment, and its standard terms are 30 days.
Based on: Controller; standard terms of sale. To be approved by: Controller. Not yet approved.

Q2 Are there any legal claims or disputes outstanding?
Draft answer: not drafted.
Based on: Chief executive. To be approved by: Chief executive. Not yet approved.
FLAG, not drafted, for the Chief executive. See 13.

Q3 Has anything happened since the year end that could affect the accounts?
Draft answer: not drafted.
Based on: nothing supplied. To be approved by: Chief executive. Not yet approved.
FLAG, no facts supplied. See 14.

DECISIONS AND QUESTIONS
1. For Controller. A1, late. Our date was Thursday 5 November; the trial balance is in progress with two late supplier bills still to post, and the auditors' date is Tuesday 10 November. The Controller owns A1, so the Chief executive approves it. When will A1 be ready for the Chief executive's approval?
2. For Controller. A5, no owner. The fixed asset register is due to the auditors on Wednesday 18 November, our date Friday 13 November, and last year's finding F3 on the same register is still open. Who owns A5?
3. For Controller. A9, not approved. The board minutes are marked sent, owned by the Chief executive, with no approver named; items the Chief executive owns are approved by the Controller. Were they approved before they went, and by whom?
4. For Controller. A10, no owner. The related parties list is new this year, due Friday 20 November, our date Tuesday 17 November, and is not on the owner and status list. Who owns A10?
5. For Controller. A11, not on the auditors' list. The lease schedule for the new warehouse is in progress, owned by the Controller, and the auditors have not asked for it. Did the auditors ask for it outside the list, or is it being prepared ahead of a request?
6. For Controller. C3, no evidence named, not kept anywhere. The call that confirms a change to a supplier's bank details leaves no record, and last year's finding F2 was about the same kind of change. What record will show each call was made, and where will it be kept?
7. For Controller. Supplier payments, overlap with no compensating control. The Controller approves payments, handles the money and checks the result, and no compensating control is written. Is a compensating control carried out for supplier payments, and if so, what is it?
8. For Controller. 2026-08-05 Supplier C $8,900.00, no approval recorded. The payment is above the $5,000.00 limit, entered by the Payables clerk, with no approver in the export. Was it approved, and where is the record?
9. For Controller. 2026-09-02 Supplier D $5,000.00, approved by the person who entered it. The payment is at the limit, entered and approved by the Controller. Did anyone else approve it, and where is the record?
10. For Controller. F2, no evidence named. The finding is marked done; the action recorded is that the Payables clerk was told to call suppliers before changing bank details. What can be shown to the auditors to prove the change was made?
11. For Controller. F3, no action recorded. The fixed asset register was not reconciled to the general ledger last year; the finding is open with no action, and A5 has no owner. What has been done about F3?
12. For Controller. Receivables, no explanation. Receivables rose from $812,400 to $1,046,500, a movement of $234,100 (28.8%), and there is no movement note. What explains the rise?
13. For Chief executive. Q2, not drafted. The question asks about legal claims or disputes; the facts supplied mention a possible claim from a customer over a late delivery. This is for the Chief executive to answer with the company's advisers. Who will prepare the answer, and by when?
14. For Chief executive. Q3, no facts supplied. The auditors are expected to ask what has happened since 30 September 2026 that could affect the accounts. What should the answer say?

Prepared for the Controller's approval. Nothing has been sent to the auditors, assigned, approved, posted or changed.
```
