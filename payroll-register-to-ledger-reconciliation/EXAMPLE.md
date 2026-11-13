# Payroll register to ledger reconciliation: an invented example

*Illustrative example with invented data.* The company, the people, the pay runs, the journals and the figures below are all invented. Company M is an invented 60-person building maintenance contractor that pays its staff every two weeks through an outside payroll provider, whose integration posts each run to the ledger. The size, the pay schedule and the integration are framing only; they are not in the inputs. Its controller wants October's payroll agreed to the books before the month is signed off. First come the inputs the staff accountant supplied, in full, then the worksheet the workflow template returned.

## The inputs

### 1. Settings

```
Company: Company M
Period start: 2026-10-01
Period end: 2026-10-31
Files run on: 2026-11-06
Currency: dollars (all amounts)
Tolerance: 0.00
Gross pay account: 6010 Salaries and wages
Employer tax expense account: 6020 Employer payroll taxes
Tax liability account: 2210 Payroll taxes payable
Deductions liability account: 2220 Employee deductions payable
Net pay account: 1010 Operating bank (a bank account)
Controller: Controller
Payroll preparer: Payroll administrator
```

### 2. Payroll register summary

```
pay_run_id,run_type,pay_date,employees,gross_pay,employee_taxes,deductions,net_pay,employer_taxes
PR-2620,regular,2026-10-02,58,112400.00,24728.00,9850.00,77822.00,8992.00
PR-2621,regular,2026-10-16,58,113050.00,24871.00,9980.00,78199.00,9044.00
OC-1023,off-cycle,2026-10-23,1,850.00,187.00,0.00,663.00,65.03
PR-2622,regular,2026-10-30,59,114200.00,25124.00,9980.00,79096.00,9136.00
```

### 3. Ledger summary for October 2026

```
account,account_name,opening_balance,debits,credits,closing_balance
6010,Salaries and wages,1008350.00,225450.00,1240.00,1232560.00
6020,Employer payroll taxes,98120.00,18348.40,0.00,116468.40
2210,Payroll taxes payable,0.00,101895.00,67635.00,34260.00
2220,Employee deductions payable,0.00,9850.00,18590.00,-8740.00
```

### 4. Journal detail, posted 1 October to 6 November 2026

```
journal_id,posting_date,source,reference,account,description,debit,credit
J-7001,2026-10-02,PR,PR-2620,6010,Gross wages,112400.00,
J-7001,2026-10-02,PR,PR-2620,6020,Employer taxes,8992.00,
J-7001,2026-10-02,PR,PR-2620,2210,Taxes withheld and employer taxes,,33720.00
J-7001,2026-10-02,PR,PR-2620,2220,Employee deductions,,9850.00
J-7001,2026-10-02,PR,PR-2620,1010,Net pay,,77822.00
J-7002,2026-10-02,CB,TAX-1015,2210,Tax deposit,33720.00,
J-7002,2026-10-02,CB,TAX-1015,1010,Tax deposit,,33720.00
J-7003,2026-10-09,CB,DED-1015,2220,Deductions remittance,9850.00,
J-7003,2026-10-09,CB,DED-1015,1010,Deductions remittance,,9850.00
J-7004,2026-10-16,PR,PR-2621,6010,Gross wages,113050.00,
J-7004,2026-10-16,PR,PR-2621,6020,Employer taxes,9044.00,
J-7004,2026-10-16,PR,PR-2621,2210,Taxes withheld and employer taxes,,33915.00
J-7004,2026-10-16,PR,PR-2621,2220,Employee deductions,,8740.00
J-7004,2026-10-16,PR,PR-2621,6010,Deduction code R4,,1240.00
J-7004,2026-10-16,PR,PR-2621,1010,Net pay,,78199.00
J-7005,2026-10-16,CB,TAX-1016,2210,Tax deposit,33915.00,
J-7005,2026-10-16,CB,TAX-1016,1010,Tax deposit,,33915.00
J-7006,2026-10-27,MJ,MJ-0388,6020,State unemployment rate adjustment,312.40,
J-7006,2026-10-27,MJ,MJ-0388,1010,State unemployment rate adjustment,,312.40
J-7007,2026-10-30,CB,TAX-1017,2210,Tax deposit,34260.00,
J-7007,2026-10-30,CB,TAX-1017,1010,Tax deposit,,34260.00
J-7008,2026-11-02,PR,PR-2622,6010,Gross wages,114200.00,
J-7008,2026-11-02,PR,PR-2622,6020,Employer taxes,9136.00,
J-7008,2026-11-02,PR,PR-2622,2210,Taxes withheld and employer taxes,,34260.00
J-7008,2026-11-02,PR,PR-2622,2220,Employee deductions,,9980.00
J-7008,2026-11-02,PR,PR-2622,1010,Net pay,,79096.00
J-7009,2026-11-02,CB,DED-1016,2220,Deductions remittance,9980.00,
J-7009,2026-11-02,CB,DED-1016,1010,Deductions remittance,,9980.00
```

### 5. Payment report from the payroll provider

```
payment_id,payment_date,liability,amount,pay_run_id
TAX-1015,2026-10-02,taxes,33720.00,PR-2620
DED-1015,2026-10-09,deductions,9850.00,PR-2620
TAX-1016,2026-10-16,taxes,33915.00,PR-2621
TAX-1017,2026-10-30,taxes,34260.00,PR-2622
DED-1016,2026-10-30,deductions,9980.00,PR-2621
```

### 6. Last reconciliation

```
Payroll reconciliation at 30 September 2026, signed by the controller:
2210 Payroll taxes payable 0.00; 2220 Employee deductions payable 0.00.
No open items.
```

### 7. Notes from the payroll administrator, 5 November 2026

```
- OC-1023 was an off-cycle correction run on 23 October.
- Deduction code R4 was added in the payroll system on 12 October.
```

## The worksheet

```
PAYROLL REGISTER TO LEDGER RECONCILIATION: Company M, 1 October 2026 to 31 October 2026

Prepared for: Controller. Files as supplied on 6 November 2026. Runs are taken by pay date within the period.

1. Source checks
Register: 4 runs paid in the period (PR-2620, PR-2621, OC-1023, PR-2622). Gross less employee taxes and deductions equals net pay for every run: yes. Period totals: gross 340,500.00; employee taxes 74,910.00; deductions 29,810.00; net pay 235,780.00; employer taxes 27,237.03. Runs paid after the period end: None.
Ledger: 6010 Salaries and wages, opening 1,008,350.00, debits 225,450.00, credits 1,240.00, closing 1,232,560.00; lines agree to the summary. 6020 Employer payroll taxes, opening 98,120.00, debits 18,348.40, credits 0.00, closing 116,468.40; lines agree to the summary. 2210 Payroll taxes payable, opening 0.00 (agrees to the last reconciliation), debits 101,895.00, credits 67,635.00, closing 34,260.00; lines agree to the summary. 2220 Employee deductions payable, opening 0.00 (agrees to the last reconciliation), debits 9,850.00, credits 18,590.00, closing -8,740.00; lines agree to the summary. Payroll journals balance on the lines supplied: yes (J-7001, J-7004, J-7008). Net pay account 1010 Operating bank is a bank account: only lines in payroll journals are compared and its balance is not proved. Journals posted after the period end: J-7008, 2 November 2026, PR-2622; J-7009, 2 November 2026, DED-1016.
Observations: 2210 Payroll taxes payable closes October with a debit balance of 34,260.00. The deposit TAX-1017 is posted in October and the run it pays, PR-2622, is posted in November (T1).

2. Result for October 2026 (difference = ledger minus register; expense lines as net debits, liability and net pay lines as credits, payments as debits, closing balances credit positive)
L1 Gross pay to 6010 Salaries and wages: register 340,500.00; ledger 224,210.00; difference -116,290.00. Timing -114,200.00 (T1). Miscoding -1,240.00 (M1). Unexplained -850.00 (U1). Remainder 0.00.
L2 Employer taxes to 6020 Employer payroll taxes: register 27,237.03; ledger 18,348.40; difference -8,888.63. Timing -9,136.00 (T1). Miscoding 0.00 (none). Unexplained 247.37 (U1 -65.03; U2 312.40). Remainder 0.00.
L3 Taxes owed to 2210 Payroll taxes payable: register 102,147.03; ledger 67,635.00; difference -34,512.03. Timing -34,260.00 (T1). Miscoding 0.00 (none). Unexplained -252.03 (U1). Remainder 0.00.
L4 Deductions to 2220 Employee deductions payable: register 29,810.00; ledger 18,590.00; difference -11,220.00. Timing -9,980.00 (T1). Miscoding -1,240.00 (M1). Unexplained 0.00 (none). Remainder 0.00.
L5 Net pay to 1010 Operating bank: register 235,780.00; ledger 156,021.00; difference -79,759.00. Timing -79,096.00 (T1). Miscoding 0.00 (none). Unexplained -663.00 (U1). Remainder 0.00.
P Payments: payment report 121,725.00 (taxes 101,895.00; deductions 19,830.00); ledger 111,745.00; difference -9,980.00. Timing -9,980.00 (T2). Unexplained 0.00 (none). Remainder 0.00.
B Closing balances: 2210 Payroll taxes payable: expected 0.00 + 102,147.03 − 101,895.00 = 252.03; ledger -34,260.00; difference -34,512.03 = T1 -34,260.00 + U1 -252.03 + remainder 0.00. 2220 Employee deductions payable: expected 0.00 + 29,810.00 − 19,830.00 = 9,980.00; ledger 8,740.00; difference -1,240.00 = T1 -9,980.00 + T2 9,980.00 + M1 -1,240.00 + remainder 0.00.

3. Matched
Runs agreeing on every line: PR-2620. Runs agreeing except for listed items: PR-2621 (M1). Payments agreeing: TAX-1015, DED-1015, TAX-1016, TAX-1017.

4. Timing differences (proposed; the controller decides each)
T1. PR-2622, regular run, 59 employees, gross 114,200.00. Register: paid 30 October 2026. Ledger: posted 2 November 2026. Effects: L1 -114,200.00; L2 -9,136.00; L3 -34,260.00; L4 -9,980.00; L5 -79,096.00; B 2210 -34,260.00; B 2220 -9,980.00. Evidence: J-7008, posted 2 November 2026, reference PR-2622; it agrees to the register line by line. Preparer's note: none supplied.
T2. DED-1016, deductions remittance for PR-2621, 9,980.00. Payment report: 30 October 2026. Ledger: posted 2 November 2026. Effects: P -9,980.00; B 2220 9,980.00. Evidence: J-7009, posted 2 November 2026, reference DED-1016, same amount. Preparer's note: none supplied.

5. Miscoding
M1. PR-2621, deductions, 9,980.00 in the register: 8,740.00 reached 2220 Employee deductions payable and 1,240.00 reached 6010 Salaries and wages, where the settings name 2220. Effects: L1 -1,240.00; L4 -1,240.00; B 2220 -1,240.00. Evidence: J-7004, line on 6010, credit 1,240.00, "Deduction code R4". Preparer's note: deduction code R4 was added in the payroll system on 12 October (the payroll administrator's statement, not checked).

6. Unexplained
U1. OC-1023, off-cycle run, 1 employee, paid 23 October 2026 (a one-person run, so these are one person's run totals, shown because the difference is the whole run): gross 850.00, employee taxes 187.00, deductions 0.00, net pay 663.00, employer taxes 65.03. No journal with this reference is in the files posted from 1 October to 6 November 2026, and the payment report holds no payment for it. Effects: L1 -850.00; L2 -65.03; L3 -252.03; L5 -663.00; B 2210 -252.03. Preparer's note: OC-1023 was an off-cycle correction run (the payroll administrator's statement, not checked).
U2. MJ-0388, manual journal J-7006 posted 27 October 2026: 312.40 debited to 6020 Employer payroll taxes and credited to 1010 Operating bank, "State unemployment rate adjustment". No pay run reference, no payment in the report, and no support in the files. Effects: L2 312.40. Preparer's note: none supplied.

7. Questions, in order
1. U1, for the payroll administrator: OC-1023 was paid on 23 October (its figures are in U1), and no journal for it is in the ledger files to 6 November. Did the provider send it to the ledger, under what reference, and does the provider show a tax payment for it?
2. U2, for the controller: what supports MJ-0388, 312.40 debited to 6020 on 27 October and paid from 1010, and which period does it belong to?
3. M1, for the payroll administrator: J-7004 sends 1,240.00 for deduction code R4 to 6010, while J-7008 for PR-2622 credits the full 9,980.00 of deductions to 2220. Which account does the provider's ledger mapping use for R4 now, and was it changed between the two runs?
4. T1, for the controller: PR-2622 was paid on 30 October, and J-7008, which agrees to the register line by line, is posted on 2 November. Is it accepted as timing, or should October carry the run?
5. T2, for the controller: DED-1016, 9,980.00, is dated 30 October in the payment report and posted on 2 November as J-7009. Is it accepted as timing?

8. Entries that may be needed (questions for the controller; none prepared or posted)
M1: should 1,240.00 move from 6010 Salaries and wages to 2220 Employee deductions payable for PR-2621 (debit 6010, credit 2220)?
U1: if OC-1023 never reached the ledger, should a journal record it in October on the accounts in the settings (debit 6010 850.00 and 6020 65.03; credit 2210 252.03 and 1010 663.00)? These accounts come from the settings, not from a journal, and the files do not show the net pay was paid from 1010.
U2: not known from the files; it depends on the support for MJ-0388.
T1: should J-7008 carry an October posting date, or stand as timing? No entry if it stands.
T2: none if accepted as timing.

9. Employee detail used
None used: runs are shown by run ID and headcount only.

10. Not assessed
Whether any pay, tax or deduction amount in the register is right for any employee or under tax rules. Agreement with payroll tax returns. The balance of 1010 Operating bank, which is a bank account. Runs paid before 1 October 2026, except through the opening balances agreed to the last reconciliation. Whether the opening balances of the expense accounts are right (nothing is checked against them; only the two liability openings were agreed to the last reconciliation).

This worksheet shows how the payroll register and the ledger differ for October 2026 and what the files say about each item. It does not show that any pay, tax or deduction amount is right, and it gives no tax, audit or employment-law opinion. The controller decides each item and any entry. The worksheet changes no records and sends nothing.
```

Every figure traces to the seven inputs above. The register's four runs add to gross 340,500.00, employee taxes 74,910.00, deductions 29,810.00, net pay 235,780.00 and employer taxes 27,237.03, and 340,500.00 − 74,910.00 − 29,810.00 = 235,780.00. In the ledger, 6010 holds 112,400.00 + 113,050.00 − 1,240.00 = 224,210.00 for October; 6020 holds 8,992.00 + 9,044.00 + 312.40 = 18,348.40; 2210 was credited 33,720.00 + 33,915.00 = 67,635.00 and debited 33,720.00 + 33,915.00 + 34,260.00 = 101,895.00; 2220 was credited 9,850.00 + 8,740.00 = 18,590.00 and debited 9,850.00; net pay credited to 1010 in October's payroll journals is 77,822.00 + 78,199.00 = 156,021.00. The October payments in the report add to 33,720.00 + 9,850.00 + 33,915.00 + 34,260.00 + 9,980.00 = 121,725.00.
