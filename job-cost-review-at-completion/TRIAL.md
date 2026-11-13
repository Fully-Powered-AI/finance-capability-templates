# Trial of "Job cost review at completion" on its invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-12

This is the second trial run of this template on 12 November 2026. The first ran on the earlier wording and found the points that the template now fixes; this run follows the revised instruction block and output format in `member/template.md`. It used only the invented inputs from `public/example.md` (the J-2417 estimate, job-cost export, change orders, open commitments and settings, now including the four file names). No client data was used. I did not write the template.

## A limit on this trial

This trial is not blind. I had read the published example's output, and the earlier trial's output, before I produced this one, so it is not an independent reproduction. To limit the damage I recomputed the line totals, the 14-row sum (56,935.00) and the 52,480.00 estimate total with a short script, and I rewrote the free-wording parts of the questions from the template's rules rather than copying them. The matching figures show the arithmetic is right; they do not show that a fresh run would phrase everything the same way.

## What came out

```
JOB COST REVIEW AT COMPLETION: J-2417, mezzanine and stair for Customer A

For: the controller. Completed 2026-10-31. Amounts in the shop's own currency, to the cent; hours to two decimals. "Over" means recorded cost above the revised estimate; "under" means below. A line is asked about when its difference reaches both 10 percent and 500.00. A difference is a question, not a cause.
Files: estimate J-2417 estimate; job-cost export J-2417 cost detail to 2026-10-31, 14 rows; change orders J-2417 change orders; open commitments J-2417 open commitments.
Lines: 8 in the revised estimate. Compared: 7. Estimated, nothing recorded: 1. Recorded, not in the estimate: 1. Uncoded rows: 1. Lines over the limits: 3. Questions: 7. Rejected change orders not used: 1.

WHOLE JOB
Labour: estimate 20,000.00 + approved change orders 880.00 = 20,880.00 (396.00 h). Recorded 23,970.00 (440.00 h). 3,090.00 over, 14.8%.
Material: estimate 19,400.00 + approved change orders 150.00 = 19,550.00. Recorded 22,025.00. 2,475.00 over, 12.7%.
Subcontract: estimate 7,000.00 + approved change orders 0.00 = 7,000.00. Recorded 3,900.00. 3,100.00 under, 44.3%.
Overhead: estimate 6,080.00 + approved change orders 0.00 = 6,080.00. Recorded 7,040.00. 960.00 over, 15.8%.
Whole job: estimate 52,480.00 + approved change orders 1,030.00 = 53,510.00. Recorded 56,935.00. 3,425.00 over, 6.4%.
Open commitments not invoiced: 3,100.00 in 2 commitments. Recorded plus those commitments: 60,035.00, 6,525.00 over the revised estimate, 12.2%.
Pending change orders, not in any estimate figure above: 1,300.00 in 1.

BY COST CODE
100 Shop drawings, labour: revised estimate 2,400.00 (2,400.00 + 0.00); recorded 2,160.00. 240.00 under, 10.0%.
- Hours: revised 40.00 h, recorded 36.00 h. Hours part 240.00 under (4.00 h fewer at the estimate's 60.00). Rate part 0.00 (average recorded rate 60.00).
200 Fabrication, labour: revised estimate 11,000.00 (11,000.00 + 0.00); recorded 14,000.00. 3,000.00 over, 27.3%. Over the limits.
- Hours: revised 220.00 h, recorded 262.00 h. Hours part 2,100.00 over (42.00 h more at the estimate's 50.00). Rate part 900.00 over (average recorded rate 53.44).
- In the records: 2026-09-30, timesheet TS-0930, 2,700.00: "overtime to meet galv pickup". 2026-09-29, timesheet TS-0929, 2,300.00: "rework beam connections after fit-up".
200 Fabrication, material: revised estimate 18,500.00 (18,500.00 + 0.00); recorded 20,380.00. 1,880.00 over, 10.2%. Over the limits.
- In the records: CO-02 pending, 1,300.00; if approved as stated, 580.00 over would remain. 2026-09-15, AP invoice INV-5521, 17,950.00: "beams and columns per PO-3302". 2026-09-24, AP invoice INV-5560, 2,640.00: "additional plate for revised stair landing". 2026-10-02, AP credit CR-0117, -210.00: "return unused angle".
300 Galvanizing, subcontract: revised estimate 4,200.00 (4,200.00 + 0.00); recorded 3,900.00. 300.00 under, 7.1%. Not final: PO-3310, 300.00 not invoiced.
400 Installation, labour: revised estimate 7,480.00 (6,600.00 + 880.00); recorded 7,810.00. 330.00 over, 4.4%.
- Hours: revised 136.00 h, recorded 142.00 h. Hours part 330.00 over (6.00 h more at the estimate's 55.00). Rate part 0.00 (average recorded rate 55.00).
400 Installation, material: revised estimate 1,050.00 (900.00 + 150.00); recorded 1,020.00. 30.00 under, 2.9%.
900 Shop overhead, overhead: revised estimate 6,080.00 (6,080.00 + 0.00); recorded 7,040.00. 960.00 over, 15.8%. Over the limits.
- In the records: 2026-10-31, applied OH-1031, 7,040.00: "shop rate 16.00 per labour hour".

NOT COMPARED
Estimated, nothing recorded: 500 Crane, subcontract: revised estimate 2,800.00. Not final: SC-0412, 2,800.00 not invoiced.
Recorded, not in the estimate: 450, material: 385.00. Rows: 2026-10-15, AP invoice INV-2301, 385.00: "field touch-up paint".
Uncoded rows: 2026-10-16, material, AP invoice INV-8812, Supplier E, 240.00: "freight".

RECORD FLAGS
Open commitments not invoiced: PO-3310 (Supplier C, 300 subcontract): 4,200.00 committed, 3,900.00 invoiced, 300.00 not invoiced. SC-0412 (Supplier D, 500 subcontract): 2,800.00 committed, 0.00 invoiced, 2,800.00 not invoiced.
Invoiced above a commitment: None.
Rows dated after completion: None.
Labour rows with no hours: None.
Pending change orders: CO-02, 200 material, 1,300.00.
Rejected change orders, not used: CO-03, 500 subcontract, 600.00.

QUESTIONS FOR THE CONTROLLER, THE ESTIMATOR, THE JOB LEAD AND THE RECORDS OWNER
1. 200 Fabrication, labour: recorded 14,000.00 for 262.00 h against a revised estimate of 11,000.00 for 220.00 h; 3,000.00 over, 27.3%, of which the hours part is 2,100.00 and the rate part 900.00. Job lead: what do you know about the cost on this line? Estimator: what hours and rate did the estimate use for fabrication labour?
2. 200 Fabrication, material: recorded 20,380.00 against a revised estimate of 18,500.00; 1,880.00 over, 10.2%; CO-02, 1,300.00, is pending on this line. Job lead: what do you know about the cost on this line, and what is the status of CO-02? Estimator: what quantity and price did the estimate use for fabrication material?
3. 900 Shop overhead, overhead: recorded 7,040.00 against a revised estimate of 6,080.00; 960.00 over, 15.8%. Controller: what basis applied this overhead, and did the estimate use the same basis?
4. 300 Galvanizing, subcontract, commitment not invoiced: PO-3310 (Supplier C) has 300.00 of its 4,200.00 not invoiced; the line is 300.00 under. Job lead: will more be invoiced on PO-3310, or will it be closed?
5. 450, material, not in the estimate: 385.00 on INV-2301, "field touch-up paint". Estimator: was this work in the estimate under another code? Job lead: what was this cost for, beyond the memo quoted?
6. 500 Crane, subcontract, nothing recorded: the revised estimate is 2,800.00 and no row is recorded; SC-0412 (Supplier D) has 2,800.00 committed and 0.00 invoiced. Records owner: is cost for this line posted elsewhere, or still to come? Job lead: will SC-0412 be invoiced, or closed?
7. Uncoded row, INV-8812: Supplier E, material, 240.00, "freight". Records owner: which cost code should this row carry?

TIE-OUT
Estimate: lines 52,480.00 + approved change orders 1,030.00 = revised estimate 53,510.00.
Records: 14 rows add to 56,935.00; control total 56,935.00; agree.
Difference: compared lines 5,600.00 + recorded, not in the estimate 385.00 + uncoded 240.00 - estimated, nothing recorded 2,800.00 = 3,425.00; recorded 56,935.00 less revised estimate 53,510.00 = 3,425.00.
By type: labour 3,090.00 + material 2,475.00 + subcontract -3,100.00 + overhead 960.00 = 3,425.00.
(Signed amounts: over is positive, under is negative.)

Every figure traces to J-2417 estimate, J-2417 cost detail to 2026-10-31, J-2417 change orders and J-2417 open commitments. The review changes no estimate, rate or record, and closes nothing.
```

## What was observed

- **Every required part was produced:** header, whole job, by cost code, not compared, record flags, questions, tie-out and trace line. Every tie-out line balanced. No stop condition fired: headers matched, all 14 rows carry J-2417, all cost types are valid, no estimate pair repeats, all change order statuses are valid, every figure is a plain number, and the rows add to the control total.
- **Differences from the published example:** figures are identical throughout. The wording differs in three places only, all in free wording: the second question's wording ("what is the status of CO-02", "what quantity and price"), the fourth question ("will more be invoiced on PO-3310, or will it be closed?") and the fifth question ("beyond the memo quoted"). The Files line, the trace line, the "Not final" mark on the crane line, the heading and the role names ("Records owner") follow from the revised template and match the example.
- **Fixes from the earlier trial that this run confirmed:** the file names now come from the settings, so the Files and trace lines name them; the questions heading includes the controller, who is asked question 3; the crane line, which has nothing recorded, carries the "Not final" mark under Not compared; questions print "Records owner" rather than a job title; the header says a line is asked about when its difference reaches both limits.
- **Facts in the output not in the inputs:** none found.
- **Ambiguities left:**
  - The wording of the questions is not fixed beyond the figures and the one question per role, so two runs will word them differently.
  - An overhead row has no hours and no vendor, so the overhead line gets no hours split; the template says the split applies to labour lines.
  - No acceptance test covers a pending change order on a line under the limits; the example has none.
  - The new currency check (a symbol or code in a figure, or a second currency named by the person) was not exercised: the example has one currency.
- **Was anything told to stop for:** no.
- **Checker items I could verify from the output:** reviewer checklist items 2, 4, 5, 7 and 8 are visibly met (CO-01 is in the revised estimate once, CO-02 is not added; labour parts add to differences; the crane line is not a saving; memos are word for word; every line over the limits has a question and no other compared line has one). Items 1, 3, 6, 9 and 10 need a controller or records owner and were not testable here.
- **Not tested:** only one example was run. The acceptance tests (stops, header mismatch, credit rows, requests for a cause and so on) were not run.
