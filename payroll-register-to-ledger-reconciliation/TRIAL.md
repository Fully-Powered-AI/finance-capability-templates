# Payroll register to ledger reconciliation: tried once on its example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-12

The inputs were the invented example in [example.md](example.md): the settings, the payroll register summary, the ledger summary, the journal detail, the payment report, the last reconciliation and the payroll administrator's notes for the invented Company M, October 2026. No client data was used. The assistant that ran the template did not write it. It was given the template's instruction block and output format and only the example's inputs. It produced the worksheet before it opened the example's published worksheet, and compared the two afterwards.

## What came out

The worksheet below is the substance of what the run produced. It is shortened only where noted (the sign-convention parenthetical on the section 2 heading is omitted from this record, and the closing statement); every figure is as produced.

```
PAYROLL REGISTER TO LEDGER RECONCILIATION: Company M, 1 October 2026 to 31 October 2026

Prepared for: Controller. Files as supplied on 6 November 2026. Runs are taken by pay date within the period.

1. Source checks
Register: 4 runs paid in the period (PR-2620, PR-2621, OC-1023, PR-2622). Gross less employee taxes and deductions equals net pay for every run: yes. Period totals: gross 340,500.00; employee taxes 74,910.00; deductions 29,810.00; net pay 235,780.00; employer taxes 27,237.03. Runs paid after the period end: None.
Ledger: 6010, opening 1,008,350.00, debits 225,450.00, credits 1,240.00, closing 1,232,560.00; 6020, opening 98,120.00, debits 18,348.40, credits 0.00, closing 116,468.40; 2210, opening 0.00 (agrees to the last reconciliation), debits 101,895.00, credits 67,635.00, closing 34,260.00; 2220, opening 0.00 (agrees to the last reconciliation), debits 9,850.00, credits 18,590.00, closing -8,740.00. Lines agree to the summary for all four. Payroll journals balance on the lines supplied: yes (J-7001, J-7004, J-7008). Net pay account 1010 is a bank account: only lines in payroll journals are compared and its balance is not proved. Journals posted after the period end: J-7008, 2026-11-02, PR-2622; J-7009, 2026-11-02, DED-1016.
Observations: 2210 closes October with a debit balance of 34,260.00, because the deposit TAX-1017 is posted in October and the run it pays, PR-2622, is posted on 2 November. 2220 closes with a credit balance of 8,740.00 against 9,980.00 expected.

2. Result for October 2026
L1 Gross pay to 6010: register 340,500.00; ledger 224,210.00; difference -116,290.00. Timing -114,200.00 (T1). Miscoding -1,240.00 (M1). Unexplained -850.00 (U1). Remainder 0.00.
L2 Employer taxes to 6020: register 27,237.03; ledger 18,348.40; difference -8,888.63. Timing -9,136.00 (T1). Miscoding 0.00 (none). Unexplained 247.37 (U1 -65.03; U2 312.40). Remainder 0.00.
L3 Taxes owed to 2210: register 102,147.03; ledger 67,635.00; difference -34,512.03. Timing -34,260.00 (T1). Miscoding 0.00 (none). Unexplained -252.03 (U1). Remainder 0.00.
L4 Deductions to 2220: register 29,810.00; ledger 18,590.00; difference -11,220.00. Timing -9,980.00 (T1). Miscoding -1,240.00 (M1). Unexplained 0.00 (none). Remainder 0.00.
L5 Net pay to 1010: register 235,780.00; ledger 156,021.00; difference -79,759.00. Timing -79,096.00 (T1). Miscoding 0.00 (none). Unexplained -663.00 (U1). Remainder 0.00.
P Payments: payment report 121,725.00 (taxes 101,895.00; deductions 19,830.00); ledger 111,745.00; difference -9,980.00. Timing -9,980.00 (T2). Unexplained 0.00 (none). Remainder 0.00.
B Closing balances: 2210: expected 0.00 + 102,147.03 - 101,895.00 = 252.03; ledger -34,260.00; difference -34,512.03 = T1 -34,260.00 + U1 -252.03 + remainder 0.00. 2220: expected 0.00 + 29,810.00 - 19,830.00 = 9,980.00; ledger 8,740.00; difference -1,240.00 = T1 -9,980.00 + T2 +9,980.00 + M1 -1,240.00 + remainder 0.00.

3. Matched
Runs agreeing on every line: PR-2620. Runs agreeing except for listed items: PR-2621 (M1). Payments agreeing: TAX-1015, DED-1015, TAX-1016, TAX-1017.

4. Timing differences (proposed; the controller decides each)
T1. PR-2622, paid 2026-10-30 (register), posted 2026-11-02 (ledger), gross 114,200.00. Effects: L1 -114,200.00; L2 -9,136.00; L3 -34,260.00; L4 -9,980.00; L5 -79,096.00; B 2210 -34,260.00; B 2220 -9,980.00. Evidence: J-7008, agrees to the register line by line. Preparer's note: none supplied.
T2. DED-1016, 9,980.00, dated 2026-10-30 (report), ledger debit posted 2026-11-02. Effects: P -9,980.00; B 2220 +9,980.00. Evidence: J-7009, same payment ID and amount. Preparer's note: none supplied.

5. Miscoding
M1. PR-2621, deductions 9,980.00: 8,740.00 reached 2220 and 1,240.00 reached 6010, where the settings name 2220. Effects: L1 -1,240.00; L4 -1,240.00; B 2220 -1,240.00. Evidence: J-7004, 6010 line, credit 1,240.00, "Deduction code R4". Preparer's note: deduction code R4 was added in the payroll system on 12 October (statement, not checked).

6. Unexplained
U1. OC-1023, off-cycle run, paid 2026-10-23: gross 850.00, employee taxes 187.00, deductions 0.00, net pay 663.00, employer taxes 65.03. No journal with this reference is in the files, and the payment report holds no payment for it. Effects: L1 -850.00; L2 -65.03; L3 -252.03; L5 -663.00; B 2210 -252.03. Preparer's note: OC-1023 was an off-cycle correction run on 23 October (statement, not checked).
U2. MJ-0388, journal J-7006, posted 2026-10-27: 312.40 debited to 6020 and credited to 1010, "State unemployment rate adjustment". No run or payment reference, and not an accrual. Effects: L2 +312.40. Preparer's note: none supplied.

7. Questions, in order
1. U1, for the payroll preparer: did the provider send OC-1023 (taxes owed 252.03, net pay 663.00) to the ledger, under what reference and on what date?
2. U2, for the controller: what supports MJ-0388, 312.40 to 6020 on 27 October, and which period does it belong to?
3. M1, for the payroll preparer: which account does the provider's mapping use for deduction code R4, given J-7004 sent 1,240.00 to 6010 and J-7008 credits the full deductions to 2220?
4. T1, for the controller: PR-2622 was paid on 30 October and J-7008 is posted on 2 November. Is it accepted as timing?
5. T2, for the controller: DED-1016 is dated 30 October and posted on 2 November. Is it accepted as timing?

8. Entries that may be needed (questions for the controller; none prepared or posted)
M1: should 1,240.00 move from 6010 to 2220 for PR-2621?
U1: if OC-1023 never reached the ledger, should it be recorded on the accounts in the settings (6010 850.00 and 6020 65.03; 2210 252.03; 1010 663.00)? The files do not show the net pay was paid from 1010.
U2: not known from the files.
T1, T2: none if accepted as timing.

9. Employee detail used
None used: runs are shown by run ID and headcount only.

10. Not assessed
Whether any pay, tax or deduction amount is right for any employee or under tax rules. Agreement with payroll tax returns. The balance of 1010, a bank account. Whether the expense accounts' opening balances are right (only the two liability openings were checked against the last reconciliation). Any tax payment for OC-1023, because none is in the report.

[closing statement as in the format]
```

## What was observed

- **Every required part was produced,** in the fixed order, with no stop. All proofs passed: every run adds up, every ledger account adds to its summary, both liability openings agree to the last reconciliation, and the three payroll journals balance.
- **Result matched the template's own acceptance test 1:** L1 difference -116,290.00 with remainder 0.00, one timing run, one timing payment, one miscoding, two unexplained items, and no employee detail used. Every line's remainder came to 0.00.
- **Nothing in the run told the assistant to stop,** which is right for this example. The stop conditions were not exercised; the other acceptance tests were not run.
- **Compared with the published worksheet,** the classification, every figure, every effect, every remainder, the matched lists and the order of the questions were the same. The differences were in wording and in a few choices:
  - Section 8: the published worksheet writes out the U1 entry in full (debit 6010 850.00 and 6020 65.03; credit 2210 252.03 and 1010 663.00). The run wrote the same accounts and amounts but added that the files do not show the net pay came from 1010. The published version did not say so. Corrected afterwards: the published worksheet now says it.
  - Section 10: the run added two items the published version leaves out (the expense accounts' openings were not checked against anything; no tax payment for OC-1023 is in the report). The published version adds one the run left out (runs paid before 1 October, except through the opening balances).
  - Sections 4 to 6: the published text is fuller (headcount, the full set of run figures, the reference in the evidence line); the run's was shorter.
- **Facts in the published example that are not in its inputs:** the introduction says Company M is a 60-person building maintenance contractor, pays every two weeks, and has a provider integration that posts each run to the ledger. None of that is in the seven inputs. The worksheet itself added nothing that is not in the inputs. The run's own output added nothing either, apart from the note on 1010 above, which is a limit on what the files show, not a fact. Corrected afterwards: the introduction now says these details are framing only and not in the inputs.

### Where the instructions were ambiguous or the assistant had to guess

- **Who gets the question for an unexplained run with no journal.** The template sends what the register or provider shows to the payroll preparer and what the ledger shows to the controller. A run missing from the ledger is both. The run chose the payroll preparer, as the published example does, but the template does not settle it.
- **Who gets the question for a miscoding.** The same split: the mapping is the provider's, the correction is the controller's. The run asked the preparer about the mapping and left the correction to section 8.
- **Entries for an item with no journal (U1).** Step 11 says to write an entry as a question where the files show the accounts and amount. For U1 only the settings show them, not any journal, and the credit to the bank account is an assumption. The template does not say whether that counts as "shown".
- **The sign of a timing payment on a closing balance.** The template says closing balances are credit positive and payments are debits, but never states that a missing debit makes the ledger's credit balance higher, so the +9,980.00 for T2 on 2220 had to be worked out.
- **Zero effects.** The format gives "Timing [amount] ([items])" for every line but not what to write when an item touches a line with no effect, as U1 does on deductions. The run wrote "0.00 (none)", as the published example does.
- **Opening balances of the expense accounts** are not checked against anything, and the template does not say so under "Not assessed". The run added it.
- **Net debits on gross pay.** "Net debits" includes the 1,240.00 credit on 6010; only the acceptance test's -116,290.00 confirms that is meant.

### Shortcomings found in the template's own text

- Its version notes, and the profile's "what has been checked" paragraph, still say it has not been tried on its invented example. They need updating now there is a trial. This run did not change them. Corrected afterwards: the version notes and the profile have since been updated.
- Its acceptance tests are marked "Proposed tests. None has been run." Only test 1 was effectively run here, and only by comparing the result with its expected figures.
- The run was one pass by one model on one invented example. It shows the template can be followed to the right answer on clean files, not that it holds up on messier ones or with other products.
