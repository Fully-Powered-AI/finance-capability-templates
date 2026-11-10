# Spreadsheet check before sharing: one run on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-09

The inputs are the invented example in `public/example.md` (Coldwater Joinery, an invented workshop). No client data was used. The run used the sending note, the workbook structure note and the four pasted ranges (Projection and Summary, each as formulas and as values).

The run was a fresh session with no tools and no file access. Its instructions were the template's instruction block followed by its output format, as the template says to paste them, and its one message was the example's inputs. It did not see the rest of the template or the example's report. The session that made the template's last edits (Claude Opus 5.5) started the run and compared its report with the example's afterwards; the comparison below is that session's.

This was a single run by a model that did not write the template, on the template as it now stands. It shows what this one run produced. It is not a test in a client environment.

An earlier run on 9 November 2026, by the same model, was made before the template's last edits. This run replaces it.

## What came out

The full report, as produced:

```
SPREADSHEET CHECK BEFORE SHARING: Coldwater_Projection_2027-2029_v7.xlsx

For: finance manager, sending to the bank's lending officer on Friday 13 November 2026, with the equipment loan application. Model owner: finance manager (the operations director supplied the cost figures). Checked on 10 November 2026.
Read: Projection A1:D15 and Summary A1:D10, pasted, formulas and values.
Headline figures: Summary!B5 Revenue 2027, 2400; Summary!B8 Operating profit 2027, 364; Summary!D8 Operating profit 2029, 704.4; Summary!B10 Loan cover 2027, 2.275.
Known design choices: Projection!B5 is a typed opening figure for 2027 revenue, taken from the 2026 forecast.
Found: 5 to fix before sending, 4 to confirm, 0 to tidy, 3 flagged but fine. What the recipient can see: 3 items.

COVERAGE
Read in full: Projection A1:D15 (formulas and values); Summary A1:D10 (formulas and values).
Not read: Old_v5 (hidden sheet), because its contents were not supplied. No formula in the ranges read refers to it.
Not checked: values are as supplied and were not recalculated; no macro was run; no linked file was opened; file properties (not readable from pasted ranges); numbers stored as text, stray spaces in labels and merged cells (pasted text does not show them).

FIX BEFORE SENDING
1. Projection!D11: the 2029 total costs formula stops one row short and leaves out Other overheads.
Shows: =SUM(D6:D9), 2199.6.
Evidence: B11 and C11 are =SUM(B6:B10) and =SUM(C6:C10). D6:D9 adds to 1161.6+882+96+60 = 2199.6, which is the shown value, so D10 (135) is not counted.
Effect: feeds Summary!D8 (Operating profit 2029). As it stands it shows 704.4. With this fix alone, D11 becomes 2334.6 and D8 becomes 569.4. If Projection!D10 is also fixed (item 3), D8 becomes 559.2. If the wage rate also becomes 6% (Confirm 4), D8 becomes 542.32. It also moves Summary!D6 (Total costs 2029, 2199.6 now; 2334.6 with this fix alone) and Summary!D10 once item 2 is fixed.
Fix: =SUM(D6:D10). The owner must confirm that all five cost lines belong in the total.
Checklist: 3, 4.

2. Summary!D10: the 2029 loan cover shows #REF! because its denominator is a broken reference.
Shows: =Projection!D12/#REF!, #REF!.
Evidence: B10 and C10 are =Projection!B12/(Projection!B13+Projection!B14) and =Projection!C12/(Projection!C13+Projection!C14), giving 2.275 and 2.85.
Effect: no named headline figure. The bank will see an error value in the loan cover row. Once the formula is repaired it reads 4.4025 on today's Projection!D12 (704.4). It reads 3.55875 after item 1 (569.4), and 3.495 after items 1 and 3 (559.2).
Fix: =Projection!D12/(Projection!D13+Projection!D14). The owner must confirm that the denominator should include row 14 (see Confirm 3).
Checklist: 1, 2.

3. Projection!D10: a typed number sits where the neighbouring cells hold a formula.
Shows: 135, 135.
Evidence: B10 and C10 are =B5*0.05 and =C5*0.05 (120, 132). D5*0.05 is 145.2. 135 is 5% of 2700, not of the 2029 revenue of 2904.
Effect: no headline figure as the workbook stands, because D11 stops at row 9 (item 1). After item 1, Summary!D8 is 569.4 with 135 and 559.2 with 145.2.
Fix: =D5*0.05. The owner must confirm that 135 was not a deliberate override.
Checklist: 4.

4. Summary!A1: the title gives the wrong period.
Shows: "Coldwater Joinery: summary of projection 2026 to 2028 ($000)".
Evidence: the column headers are 2027, 2028, 2029, and the Projection title and headers cover 2027 to 2029.
Effect: no headline figure.
Fix: "Coldwater Joinery: summary of projection 2027 to 2029 ($000)".
Checklist: 11.

5. Summary!B2: the "Prepared" date is calculated, not typed.
Shows: =TODAY(), 10 Nov 2026.
Evidence: the cell recalculates each time the file is opened, so the bank will see its own opening date, not the preparation date.
Effect: no headline figure.
Fix: replace it with a typed date. The owner must confirm which date to show.
Checklist: 9, 11.

CONFIRM BEFORE SENDING
1. Projection!B6:D6: the materials rate of 40% is written into the formulas.
Shows: =B5*0.4, 960; =C5*0.4, 1056; =D5*0.4, 1161.6.
Evidence: the rate is the same across the row, but no labelled cell or note states it.
Effect: feeds Summary!B8 (364), Summary!D8 (704.4) and Summary!B10 (2.275). The figures stay the same if the same rate is moved to a labelled cell.
Question for the model owner: is 40% of revenue the materials rate the operations director supplied for all three years, and should it move to a labelled input cell?
Checklist: 5.

2. Projection!B10:C10: the overhead rate of 5% is written into the formulas.
Shows: =B5*0.05, 120; =C5*0.05, 132.
Evidence: the rate is the same in both cells, with no labelled input. D10 is typed (see Fix 3).
Effect: B10 feeds Summary!B8 (364) and Summary!B10 (2.275). C10 feeds only the 2028 Summary figures, which are not headline figures.
Question for the model owner: is 5% the overhead rate meant, and should it move to a labelled cell that B10:D10 all use?
Checklist: 5.

3. Projection!A14:D14: a hidden row feeds the loan cover the bank will read.
Shows: "Director loan repayment", 40, 40, 40.
Evidence: Summary!B10 is 364/(120+40) = 2.275. Without row 14 it would be 364/120 = 3.033. Summary!C10 is 456/(120+40) = 2.85, against 3.8 without row 14.
Effect: feeds Summary!B10, Loan cover 2027 (2.275). No other headline figure.
Question for the model owner: is the director loan repayment meant to be in the loan cover denominator, and should row 14 be unhidden so the bank can see what the 2.275 includes?
Checklist: 6, 12.

4. Projection!B15: the wage increase is 5% while the comment on the cell says 6%.
Shows: 0.05. The comment reads "Ops dir says 6% not 5% - update before sending".
Evidence: C7 and D7 use $B$15, giving 840 and 882. At 6% they would be 848 and 898.88.
Effect: feeds Summary!D8. As it stands it shows 704.4. At 6% with nothing else changed, D8 becomes 687.52; with Fix 1 and Fix 3 as well it becomes 542.32, against 559.2 at 5%. Summary!B8 and B10 do not change, because B7 is typed. Other figures it moves: Summary!C8 456 becomes 448, Summary!C6 2184 becomes 2192, Summary!C10 2.85 becomes 2.8.
Question for the model owner: has the operations director's 6% been confirmed, so that B15 should read 0.06 before sending? The comment should be removed or the sender should decide what to do with it (see WHAT THE RECIPIENT CAN SEE).
Checklist: 12.

TIDY IF TIME
None.

FLAGGED BUT FINE
Projection!B5: typed 2400 where C5:D5 are formulas. Fine because it is the known design choice, the opening 2027 revenue from the 2026 forecast. B4 is blank for the same reason. Checklist: 4.
Projection!B7: typed 800 at the start of the wages chain (C7:D7 are formulas). Fine because it is the first figure of a chain. Checklist: 4.
Projection!C4:D4, B8:D9, B13:D13: rows of typed inputs (growth, rent, equipment lease, loan repayments) among rows of formulas. Fine because each row is typed inputs throughout, with no formulas to depart from. Checklist: 4.

WHAT THE RECIPIENT CAN SEE
Hidden row Projection!A14:D14 ("Director loan repayment", 40, 40, 40). See Confirm 3.
Hidden sheet Old_v5, contents not supplied and not read. Sender to decide.
Comment on Projection!B15: "Ops dir says 6% not 5% - update before sending". See Confirm 4.
Also looked for, nothing found: placeholder text (TBD, XXX, "draft"), other organizations' names, links showing another file's name or folder, passwords, account numbers or bank details, and personal details of named people, all within the ranges read.
Not checked: file properties (not readable from pasted ranges); contents of Old_v5 (not supplied).

CHECKLIST RUN
1 Error values on show: found: Summary!D10 (Fix 2).
2 Broken links: found: Summary!D10, #REF! inside the formula (Fix 2). No missing sheet or other-file link in the cells read.
3 Totals: found: Projection!D11 (Fix 1). B11 and C11 recompute to 2036 and 2184; Summary links match their sources.
4 Broken patterns: found: Projection!D10 (Fix 3) and D11 (Fix 1). Typed inputs cleared under Flagged but fine.
5 Buried assumptions: found: Projection!B6:D6 (Confirm 1), B10:C10 (Confirm 2).
6 Hidden structure: found: Projection row 14 feeds Summary!B10 and C10 (Confirm 3). Old_v5 was not read, though no formula read refers to it.
7 Figures that will not add: nothing found for lookups or duplicate keys (the ranges hold no lookups). Not checked: numbers stored as text, stray spaces and merged cells, because pasted text does not show them.
8 Swallowed errors: nothing found.
9 Loops and moving parts: found: Summary!B2 =TODAY() (Fix 5).
10 Financial sense: nothing found. Periods 2027 to 2029 are complete, cost and revenue signs are consistent, and the Summary figures match the cells they report.
11 Labels: found: Summary!A1 (Fix 4), Summary!B2 (Fix 5).
12 What the recipient can see: found: Projection!A14:D14, Old_v5, Projection!B15 comment (see above).

Prepared for the finance manager's review. The workbook has not been changed and nothing has been sent. It covers the twelve checks above on what was supplied, and vouches for nothing beyond them.
```

## What was observed

- **Every required part was produced.** The header lines, Coverage, the four finding sections (Tidy if time as "None."), What the recipient can see, the twelve-item checklist run and the closing line are all present. Nothing in the inputs made the template stop, and nothing asked the assistant to change the workbook, send it or certify it.
- **The same problems as the published example.** Both reports find the 2029 total that stops a row short, the loan cover showing #REF!, the title naming 2026 to 2028, the two rates typed inside formulas, the typed 135, the hidden director loan row, the wage increase with its 6% comment, the TODAY() date and the unread hidden sheet Old_v5. The shared figures match: 2,334.6 and 569.4 after the total is fixed, 4.4025 and 3.55875 for the repaired loan cover, 145.2 against the typed 135, 3.033 loan cover without the hidden row, 687.52 and 552.52 at a 6% wage rise, and 2028 operating profit falling from 456 to 448. The figures the run added (559.2, 542.32, 3.495, 2,192, 2.8 and 3.8) were checked against the inputs and are correct.
- **Three points the template settled before this run were followed.** The 2029 total took items 3 and 4, as in the example. The hidden row was named Projection!A14:D14, as in the example. The questions on the two buried rates asked whether the rate is the one meant and whether it should move to a labelled cell, as in the example.
- **Differences from the published example.**
  - The typed 135 (Projection!D10) went under Fix before sending, with =D5*0.05 as the fix and the owner asked to confirm it was not a deliberate override. The example puts it under Confirm before sending as a question. The template lists "a typed number among formulas" as an example of an unclear item, while its definition of a mistake (a cell that departs from the rule its neighbours follow and was meant to follow it) can also be read to cover it. The run took the second reading.
  - The TODAY() date (Summary!B2) went under Fix before sending. The example puts it under Tidy if time. The cell trips item 9 (a volatile function, listed as housekeeping) and item 11 (a prepared date should be typed, a label check); the template does not say which sorting wins when one cell trips both. The run's counts are therefore 5 to fix, 4 to confirm and 0 to tidy, where the example has 3, 5 and 1.
  - Checklist item 7: the run reported merged cells as not checked from pasted text. The template says merged cells that can be seen are checked; the example reports none in the ranges.
  - Flagged but fine: three entries, the example has four. The run grouped the growth inputs with the rent, lease and loan rows, which the template allows.
  - The run wrote "no named headline figure" for the loan cover, where the format offers "no headline figure", and gave its "Read:" line without naming the workbook structure note as a source.
  - Extra detail the run added: the combined effect of several fixes on operating profit and loan cover, the 2028 loan cover with and without the hidden row, and "personal details of named people" among the kinds looked for.
- **Facts not in the inputs.** None of the run's figures came from outside the inputs; each is arithmetic on supplied values. The observation that 135 is 5% of 2,700 is arithmetic, not a claim about where the figure came from. The question on the materials rate assumes the operations director supplied it, which the inputs support only in general (the director supplied "the cost figures").
- **Where the instructions were ambiguous and the assistant had to choose.**
  - Whether a typed number that breaks a row of formulas is a mistake or an unclear item, as above.
  - Which section a cell takes when it trips both a housekeeping item and a label item, as above.
  - Whether merged cells count as visible in pasted text.
- **Shortcomings of the trial itself.** One run, one model, one example. The example's inputs are small (two sheets, 25 rows), so the template's handling of a large workbook, a password-protected file, a values-only file, or instruction-like text in a cell was not exercised. The acceptance tests in the template were not run.
