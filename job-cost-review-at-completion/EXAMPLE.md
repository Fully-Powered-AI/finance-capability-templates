# Job cost review at completion: an invented example

*Illustrative example with invented data.* The shop, the customer, the suppliers, the job and every figure below are made up for this page. They stand for a small steel fabrication and installation shop closing out one job in October 2026, and describe nothing that happened anywhere.

## What the controller supplies

**The estimate** (default headers):

```
cost_code,description,cost_type,est_hours,est_cost
100,Shop drawings,labour,40,2400.00
200,Fabrication,labour,220,11000.00
200,Fabrication,material,,18500.00
300,Galvanizing,subcontract,,4200.00
400,Installation,labour,120,6600.00
400,Installation,material,,900.00
500,Crane,subcontract,,2800.00
900,Shop overhead,overhead,,6080.00
```

**The job-cost export** (default headers; a negative amount is a credit):

```
job,date,cost_code,cost_type,source,reference,vendor_or_employee,hours,amount,memo
J-2417,2026-09-08,100,labour,timesheet,TS-0908,Drafter 1,36,2160.00,
J-2417,2026-09-22,200,labour,timesheet,TS-0922,Shop crew,180,9000.00,
J-2417,2026-09-29,200,labour,timesheet,TS-0929,Shop crew,46,2300.00,rework beam connections after fit-up
J-2417,2026-09-30,200,labour,timesheet,TS-0930,Shop crew,36,2700.00,overtime to meet galv pickup
J-2417,2026-09-15,200,material,AP invoice,INV-5521,Supplier B,,17950.00,beams and columns per PO-3302
J-2417,2026-09-24,200,material,AP invoice,INV-5560,Supplier B,,2640.00,additional plate for revised stair landing
J-2417,2026-10-02,200,material,AP credit,CR-0117,Supplier B,,-210.00,return unused angle
J-2417,2026-10-06,300,subcontract,AP invoice,INV-7740,Supplier C,,3900.00,
J-2417,2026-10-13,400,labour,timesheet,TS-1013,Field crew,130,7150.00,
J-2417,2026-10-27,400,labour,timesheet,TS-1027,Field crew,12,660.00,return trip for punch list
J-2417,2026-10-14,400,material,AP invoice,INV-2290,Supplier F,,1020.00,
J-2417,2026-10-15,450,material,AP invoice,INV-2301,Supplier F,,385.00,field touch-up paint
J-2417,2026-10-16,,material,AP invoice,INV-8812,Supplier E,,240.00,freight
J-2417,2026-10-31,900,overhead,applied,OH-1031,,,7040.00,shop rate 16.00 per labour hour
```

**The change orders** (default headers):

```
change_order,cost_code,cost_type,hours,cost,status
CO-01,400,labour,16,880.00,approved
CO-01,400,material,,150.00,approved
CO-02,200,material,,1300.00,pending
CO-03,500,subcontract,,600.00,rejected
```

**The open commitments** (default headers):

```
commitment,vendor,cost_code,cost_type,committed,invoiced_to_date
PO-3302,Supplier B,200,material,17950.00,17950.00
PO-3310,Supplier C,300,subcontract,4200.00,3900.00
SC-0412,Supplier D,500,subcontract,2800.00,0.00
```

**Settings:** job J-2417, mezzanine and stair for Customer A (invented); completed 2026-10-31; amounts in the shop's own currency; files named "J-2417 estimate", "J-2417 cost detail to 2026-10-31", "J-2417 change orders" and "J-2417 open commitments"; control total from the job-cost report 56,935.00; limits 10 percent and 500.00. The job lead is the project manager who ran the job, the estimator priced it, and the bookkeeper owns the records. The review goes to the controller.

## What comes out

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

## How to read it

The job finished 3,425.00 over its revised estimate, but that is not yet its final cost. The crane subcontract has nothing recorded and a 2,800.00 commitment not invoiced, and galvanizing has 300.00 still to come; if both are invoiced in full, the job ends 6,525.00 over. That is why subcontract shows 3,100.00 under: the review counts nothing recorded as nothing, never as a saving, and asks about it.

Three lines pass both limits. Fabrication labour is the largest, and the review splits it into 42 extra hours and a higher average rate, then quotes the two timesheet notes as the records wrote them. It does not say the notes are the reason; the job lead answers that. Fabrication material has a change order still pending that would cover most of its difference if approved as stated. Shop drawings came in 10.0 percent under, but at 240.00 it is below the amount limit, so it is shown and not asked about.

The installation change order, CO-01, is already in the revised estimate, so installation is compared against 7,480.00 rather than the original 6,600.00. The touch-up paint and the freight row sit outside every line until the estimator and the bookkeeper answer. Nothing has been recoded, and the controller approves the final cost.
