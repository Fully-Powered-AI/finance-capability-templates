# Spreadsheet check before sharing: an invented example

*Illustrative example with invented data.* The company, the people, the bank and every figure below are invented. Coldwater Joinery is an invented 30-person joinery workshop applying to its bank for an equipment loan. Its finance manager built a three-year projection and is about to send it to the bank's lending officer. People are referred to by role.

The inputs come first, in full, so the template can be run on them. The report follows.

## The inputs

### 1. Sending note

```
File: Coldwater_Projection_2027-2029_v7.xlsx
Sending to: the bank's lending officer, Friday 13 November 2026, with the
  equipment loan application.
Sender: finance manager, who built the model and is its owner. The
  operations director supplied the cost figures.
Check run: Tuesday 10 November 2026.
Headline figures the bank will read:
  Summary!B5  Revenue 2027
  Summary!B8  Operating profit 2027
  Summary!D8  Operating profit 2029
  Summary!B10 Loan cover 2027
Known design choices: Projection!B5 is a typed opening figure for 2027
  revenue, taken from the 2026 forecast.
```

### 2. Workbook structure

```
Sheets: Projection (visible), Summary (visible), Old_v5 (hidden).
Hidden rows and columns: Projection row 14.
Comments: one, on Projection!B15: "Ops dir says 6% not 5% - update
  before sending".
```

### 3. Projection, formulas

```
Sheet: Projection
Range: A1:D15
Shows: formulas
Row | A | B | C | D
1 | Coldwater Joinery: three-year projection ($000) | | |
2 | | | |
3 | Line | 2027 | 2028 | 2029
4 | Revenue growth | | 0.1 | 0.1
5 | Revenue | 2400 | =B5*(1+C4) | =C5*(1+D4)
6 | Materials | =B5*0.4 | =C5*0.4 | =D5*0.4
7 | Wages | 800 | =B7*(1+$B$15) | =C7*(1+$B$15)
8 | Rent | 96 | 96 | 96
9 | Equipment lease | 60 | 60 | 60
10 | Other overheads | =B5*0.05 | =C5*0.05 | 135
11 | Total costs | =SUM(B6:B10) | =SUM(C6:C10) | =SUM(D6:D9)
12 | Operating profit | =B5-B11 | =C5-C11 | =D5-D11
13 | Loan repayments | 120 | 120 | 120
14 | Director loan repayment | 40 | 40 | 40
15 | Wage increase | 0.05 | |
```

### 4. Projection, values

```
Sheet: Projection
Range: A1:D15
Shows: values
Row | A | B | C | D
1 | Coldwater Joinery: three-year projection ($000) | | |
2 | | | |
3 | Line | 2027 | 2028 | 2029
4 | Revenue growth | | 0.1 | 0.1
5 | Revenue | 2400 | 2640 | 2904
6 | Materials | 960 | 1056 | 1161.6
7 | Wages | 800 | 840 | 882
8 | Rent | 96 | 96 | 96
9 | Equipment lease | 60 | 60 | 60
10 | Other overheads | 120 | 132 | 135
11 | Total costs | 2036 | 2184 | 2199.6
12 | Operating profit | 364 | 456 | 704.4
13 | Loan repayments | 120 | 120 | 120
14 | Director loan repayment | 40 | 40 | 40
15 | Wage increase | 0.05 | |
```

### 5. Summary, formulas

```
Sheet: Summary
Range: A1:D10
Shows: formulas
Row | A | B | C | D
1 | Coldwater Joinery: summary of projection 2026 to 2028 ($000) | | |
2 | Prepared: | =TODAY() | |
3 | | | |
4 | | 2027 | 2028 | 2029
5 | Revenue | =Projection!B5 | =Projection!C5 | =Projection!D5
6 | Total costs | =Projection!B11 | =Projection!C11 | =Projection!D11
7 | | | |
8 | Operating profit | =Projection!B12 | =Projection!C12 | =Projection!D12
9 | | | |
10 | Loan cover (times) | =Projection!B12/(Projection!B13+Projection!B14) | =Projection!C12/(Projection!C13+Projection!C14) | =Projection!D12/#REF!
```

### 6. Summary, values

```
Sheet: Summary
Range: A1:D10
Shows: values
Row | A | B | C | D
1 | Coldwater Joinery: summary of projection 2026 to 2028 ($000) | | |
2 | Prepared: | 10 Nov 2026 | |
3 | | | |
4 | | 2027 | 2028 | 2029
5 | Revenue | 2400 | 2640 | 2904
6 | Total costs | 2036 | 2184 | 2199.6
7 | | | |
8 | Operating profit | 364 | 456 | 704.4
9 | | | |
10 | Loan cover (times) | 2.275 | 2.85 | #REF!
```

## The report

```
SPREADSHEET CHECK BEFORE SHARING: Coldwater_Projection_2027-2029_v7.xlsx

For: finance manager, sending to the bank's lending officer on Friday 13 November 2026. Model owner: finance manager. Checked on Tuesday 10 November 2026.
Read: pasted ranges Projection!A1:D15 and Summary!A1:D10, formulas and values; the sheet list, hidden row and comment from the workbook structure note.
Headline figures: Summary!B5, Revenue 2027, 2,400; Summary!B8, Operating profit 2027, 364; Summary!D8, Operating profit 2029, 704.4; Summary!B10, Loan cover 2027, 2.275.
Known design choices: Projection!B5 is a typed opening figure for 2027 revenue, from the 2026 forecast.
Found: 3 to fix before sending, 5 to confirm, 1 to tidy, 4 flagged but fine. What the recipient can see: 3 items.

COVERAGE
Read in full: Projection!A1:D15 and Summary!A1:D10, formulas and values.
Not read: the hidden sheet Old_v5, whose contents were not supplied; anything outside the two pasted ranges.
Not checked: values are as supplied and were not recalculated; no macro was run; no linked file was opened; numbers stored as text and stray spaces in labels do not show in pasted text; file properties were not supplied.

FIX BEFORE SENDING
1. Projection!D11: the 2029 total costs stop a row short and leave out other overheads.
Shows: =SUM(D6:D9), 2,199.6.
Evidence: the 2027 and 2028 totals add rows 6 to 10 (=SUM(B6:B10), =SUM(C6:C10)). D11 stops at row 9, so other overheads in D10 (135) are not counted: 1,161.6 + 882 + 96 + 60 = 2,199.6.
Effect: total costs 2029 (Summary!D6) are 2,199.6 now and 2,334.6 after the fix. Operating profit 2029 (Projection!D12, headline Summary!D8) is 704.4 now and 569.4 after the fix.
Fix: =SUM(D6:D10).
Checklist: 3, 4.

2. Summary!D10: loan cover for 2029 shows #REF!, because its divisor points at a deleted reference.
Shows: =Projection!D12/#REF!, #REF!.
Evidence: B10 and C10 divide operating profit by loan repayments plus the director loan repayment, =Projection!B12/(Projection!B13+Projection!B14) and the same for column C, giving 2.275 and 2.85.
Effect: no headline figure; loan cover 2029 shows #REF! on the summary page as it stands, and would be 4.4025 after the fix as the figures stand (704.4 / 160), or 3.55875 after fix 1 as well (569.4 / 160).
Fix: =Projection!D12/(Projection!D13+Projection!D14), if 2029 is meant to be worked out like 2027 and 2028. The finance manager confirms the reference; confirm before sending 3 bears on it.
Checklist: 1, 2.

3. Summary!A1: the title names the wrong years.
Shows: Coldwater Joinery: summary of projection 2026 to 2028 ($000).
Evidence: the columns beneath are headed 2027, 2028 and 2029 (Summary!B4:D4), and the Projection sheet covers 2027 to 2029 (Projection!B3:D3).
Effect: no headline figure; the title heads the Summary sheet, which the bank can see.
Fix: Coldwater Joinery: summary of projection 2027 to 2029 ($000).
Checklist: 11.

CONFIRM BEFORE SENDING
1. Projection!B6:D6: the materials rate is typed inside the formulas.
Shows: =B5*0.4, =C5*0.4, =D5*0.4 (960, 1,056, 1,161.6).
Evidence: materials are taken as 40% of revenue, and the rate sits in no labelled cell. The wage increase, by contrast, has its own cell, B15.
Effect: feeds total costs and operating profit, so the operating profit headlines (Summary!B8, Summary!D8) rest on it.
Question for the finance manager: is 40% the materials rate you mean the bank to rely on? If so, would you put it in a labelled cell beside the wage increase, so the bank can see it?
Checklist: 5.

2. Projection!B10:C10: the overheads rate is typed inside the formulas.
Shows: =B5*0.05, =C5*0.05 (120, 132).
Evidence: other overheads are taken as 5% of revenue, and the rate sits in no labelled cell.
Effect: feeds total costs and operating profit 2027 (headline Summary!B8) and 2028 (Summary!C8).
Question for the finance manager: is 5% the overheads rate you mean the bank to rely on? If so, would you put it in a labelled cell, as for materials?
Checklist: 5.

3. Projection!A14:D14: a hidden row, director loan repayment, 40 a year, feeds the loan cover.
Shows: 40, 40, 40, typed, in the row the structure note lists as hidden.
Evidence: Summary!B10 and C10 divide operating profit by loan repayments (120) plus this row (40).
Effect: loan cover 2027 (headline Summary!B10) is 2.275 with the row and would be 3.033 without it (364 / 120). The row would also feed loan cover 2029 after fix 2.
Question for the finance manager: do you mean the bank's loan cover to include the director loan repayment? If so, should the row be visible? A hidden row is still in the file the bank receives.
Checklist: 6, 12.

4. Projection!B15: the wage increase is 5%, and a comment on the cell says it should be 6%.
Shows: 0.05. Comment: "Ops dir says 6% not 5% - update before sending".
Evidence: C7 and D7 grow wages by B15 (=B7*(1+$B$15), =C7*(1+$B$15)), giving 840 and 882.
Effect: at 6%, wages would be 848 in 2028 and 898.88 in 2029. Operating profit 2028 (Summary!C8) would fall by 8, from 456 to 448. Operating profit 2029 (headline Summary!D8) would fall by 16.88: from 704.4 to 687.52 as the figures stand, or from 569.4 to 552.52 after fix 1.
Question for the finance manager: which rate is right, 5% or 6%? Whichever it is, the comment should come out before the file goes; the bank can read it.
Checklist: 12.

5. Projection!D10: a typed 135 where the row's formula would give 145.2.
Shows: 135.
Evidence: B10 and C10 are =B5*0.05 and =C5*0.05. Following them, D10 would be =D5*0.05, which gives 145.2.
Effect: none as the workbook stands, because D11 leaves D10 out (fix 1). After fix 1, operating profit 2029 (headline Summary!D8) is 569.4 with 135, or 559.2 with 145.2.
Question for the finance manager: is 135 a quoted or agreed figure for 2029 overheads? If so, would you note its source beside it? If not, should D10 be =D5*0.05?
Checklist: 4.

TIDY IF TIME
1. Summary!B2: the prepared date is worked out with TODAY().
Shows: =TODAY(), 10 Nov 2026.
Effect: no headline figure. The cell will show whatever day the bank opens the file.
Fix: type the date the projection was prepared in place of the formula.
Checklist: 9, 11.

FLAGGED BUT FINE
Projection!C4:D4: typed growth rates of 0.1 above the rows of formulas that read them. Fine because: a row of typed inputs, which C5 and D5 use. Checklist: 4.
Projection!B5: a typed 2,400 at the start of a row of formulas. Fine because: it is the opening revenue figure from the 2026 forecast, as the sending note says. Checklist: 4.
Projection!B7: a typed 800 at the start of the wages row. Fine because: it is the opening figure that C7 and D7 grow from. Checklist: 4.
Projection!B8:D8, B9:D9 and B13:D13: typed figures between rows of formulas. Fine because: each is a whole row of typed inputs (rent, equipment lease, loan repayments), not a figure typed among formulas. Checklist: 4.

WHAT THE RECIPIENT CAN SEE
Hidden sheet Old_v5, contents not supplied. Sender to decide.
Hidden row 14 on Projection, director loan repayment. See confirm before sending 3.
Comment on Projection!B15: "Ops dir says 6% not 5% - update before sending". See confirm before sending 4.
Also looked for, nothing found: placeholder or internal text in cells, other organizations' names, links to other files, passwords, account numbers or bank details.
Not checked: the contents of Old_v5, not supplied; file properties, not supplied.

CHECKLIST RUN
1 Error values on show: found: Summary!D10 (fix before sending 2).
2 Broken links: found: Summary!D10 (fix before sending 2). No links to other files.
3 Totals: found: Projection!D11 (fix before sending 1). Projection!B11 and C11 recomputed and agree with their parts. No table carries both row and column totals.
4 Broken patterns: found: Projection!D11 (fix before sending 1), Projection!D10 (confirm before sending 5); Projection!C4:D4, B5, B7 and rows 8, 9 and 13 flagged but fine.
5 Buried assumptions: found: Projection!B6:D6 (confirm before sending 1), Projection!B10:C10 (confirm before sending 2).
6 Hidden structure: found: Projection row 14 (confirm before sending 3). The hidden sheet Old_v5 feeds no formula in the pasted ranges.
7 Figures that will not add: not checked for numbers stored as text and stray spaces, which do not show in pasted text. No lookup and no merged cell in the pasted ranges.
8 Swallowed errors: nothing found.
9 Loops and moving parts: found: Summary!B2 (tidy if time 1). No circular references.
10 Financial sense: nothing found. There is no balance sheet; revenue and costs carry the expected signs; the periods 2027 to 2029 run without a gap; Summary!B5:D5, B6:D6 and B8:D8 equal the Projection cells they report.
11 Labels: found: Summary!A1 (fix before sending 3), Summary!B2 (tidy if time 1).
12 What the recipient can see: found: hidden sheet Old_v5; Projection row 14 (confirm before sending 3); the comment on Projection!B15 (confirm before sending 4).

Prepared for the finance manager's review. The workbook has not been changed and nothing has been sent. It covers the twelve checks above on what was supplied, and vouches for nothing beyond them.
```
