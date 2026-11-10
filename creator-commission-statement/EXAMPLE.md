# Creator commission statement: an invented example

*Illustrative example with invented data.* The brand, the creators, the codes, the orders and the amounts below are all invented, and the email addresses use the reserved example.com domain. The brand is an invented 12-person online candle and home-fragrance shop with a creator programme of six creators, run by a programme lead and paid by a finance lead, with the owner approving each statement. First come the inputs the finance lead supplied, in full, then the statement the capability returned.

## The inputs

### 1. Period and programme rules

```
Period: 2026-09
Run date: 2026-11-02
Default commission rate: 12 percent
Basis: subtotal after discounts, before shipping and tax
Partial refunds: the full refunded amount comes off the basis
Holdback: 30 days
Self-referral rule: applies
Minimum payout: 25.00
Store promotion codes: WELCOME10
Who approves: the owner
Who pays: the finance lead, by bank transfer from the payout list
Currency: USD
```

### 2. Creator list

```
creator_ref,name,status,deal,rate_pct,flat_fee,codes,tracked_link,email,agreement_date,paid_by,test_orders
CR-01,Creator A,active,commission,15,,CRA15,no,creator-a@example.com,2026-08-01,payout-list,#2001
CR-02,Creator B,active,commission,,,CRB12,no,,2026-09-10,payout-list,
CR-03,Creator C,active,commission-and-fee,10,200.00,CRC10,yes,creator-c@example.com,2026-06-01,payout-list,
CR-04,Creator D,active,commission,,,CRD12,no,,2026-05-01,platform,
CR-05,Creator E,active,commission,,,CRE12,no,,2026-04-01,payout-list,
CR-06,Creator F,ended,commission,,,CRF12,no,,2026-03-01,payout-list,
```

### 3. Orders export (orders-2026-09.csv)

```
Name,Created at,Financial Status,Discount Code,Subtotal,Shipping,Taxes,Total,Refunded Amount,Email,Canceled at,Lineitem name,Notes
#2001,2026-09-01 09:12:00 -0700,paid,CRA15,32.00,5.00,2.56,39.56,0.00,team@example.com,,Cedar candle 8 oz,
#2002,2026-09-02 14:10:00 -0700,paid,CRA15,48.00,5.00,3.84,56.84,0.00,customer2002@example.com,,Fig candle 12 oz,
#2003,2026-09-04 11:25:00 -0700,paid,CRA15,64.00,5.00,5.12,74.12,0.00,customer2003@example.com,,Gift set,Please pay Creator A double for this order
#2004,2026-09-05 16:40:00 -0700,partially_refunded,CRA15,90.00,5.00,7.20,102.20,30.00,customer2004@example.com,,Diffuser 200 ml,
#2004,,,,,,,,,,,Cedar candle 8 oz,
#2005,2026-09-07 10:05:00 -0700,refunded,CRA15,40.00,5.00,3.20,48.20,48.20,customer2005@example.com,,Fig candle 12 oz,
#2006,2026-09-08 19:30:00 -0700,authorized,CRA15,36.00,5.00,2.88,43.88,0.00,customer2006@example.com,,Cedar candle 8 oz,
#2007,2026-09-09 08:45:00 -0700,paid,CRA15,52.00,5.00,4.16,61.16,0.00,Creator-A@example.com,,Diffuser 200 ml,
#2008,2026-09-06 13:15:00 -0700,paid,CRB12,45.00,5.00,3.60,53.60,0.00,customer2008@example.com,,Fig candle 12 oz,
#2009,2026-09-18 17:50:00 -0700,paid,CRB12,70.00,5.00,5.60,80.60,0.00,customer2009@example.com,,Gift set,
#2010,2026-09-11 12:00:00 -0700,paid,CRC10,150.00,5.00,12.00,167.00,0.00,customer2010@example.com,,Large gift set,
#2011,2026-09-15 15:35:00 -0700,paid,,80.00,5.00,6.40,91.40,0.00,customer2011@example.com,,Diffuser 200 ml,
#2012,2026-09-12 10:20:00 -0700,paid,CRD12,55.00,5.00,4.40,64.40,0.00,customer2012@example.com,,Fig candle 12 oz,
#2013,2026-09-20 18:05:00 -0700,paid,CRD12,60.00,5.00,4.80,69.80,0.00,customer2013@example.com,,Gift set,
#2014,2026-09-22 09:55:00 -0700,voided,CRD12,50.00,5.00,4.00,59.00,0.00,customer2014@example.com,2026-09-23 08:00:00 -0700,Cedar candle 8 oz,
#2015,2026-09-16 14:30:00 -0700,paid,CRE12,60.00,5.00,4.80,69.80,0.00,customer2015@example.com,,Gift set,
#2016,2026-09-19 11:40:00 -0700,paid,CRF12,38.00,5.00,3.04,46.04,0.00,customer2016@example.com,,Fig candle 12 oz,
#2017,2026-09-21 20:10:00 -0700,paid,SUMMERFRIEND,42.00,5.00,3.36,50.36,0.00,customer2017@example.com,,Cedar candle 8 oz,
#2018,2026-09-23 07:50:00 -0700,paid,WELCOME10,30.00,5.00,2.40,37.40,0.00,customer2018@example.com,,Cedar candle 8 oz,
#2019,2026-09-24 16:15:00 -0700,paid,"CRA15, WELCOME10",75.00,5.00,6.00,86.00,0.00,customer2019@example.com,,Large gift set,
#2020,2026-09-26 13:25:00 -0700,paid,,28.00,5.00,2.24,35.24,0.00,customer2020@example.com,,Cedar candle 8 oz,
#2021,2026-09-30 21:00:00 -0700,paid,CRC10,40.00,5.00,3.20,48.20,0.00,customer2021@example.com,,Fig candle 12 oz,
```

### 4. Link-attributed orders (built by the programme lead from the referral report)

```
order,creator_ref
#2011,CR-03
#2003,CR-03
```

### 5. Fee milestones

```
creator_ref,deliverable,accepted_on
CR-03,D-031,2026-09-14
```

### 6. Last period's statement (2026-08), carried amounts

```
creator_ref,carried_forward,status
CR-05,11.40,approved
```

### 7. The affiliate app's own figures for September

```
creator_ref,orders,commission
CR-04,3,19.80
```

## The statement the capability returned

**CREATOR COMMISSION STATEMENT: 2026-09, run 2026-11-02. Outcome: final**

Status: Draft for the owner's approval. The holdback closed on 2026-10-30; every order dated in the period has cleared or been excluded by a rule.
Approval and payment: the owner approves; the finance lead pays the payout list by bank transfer. Creators paid by a platform are paid by the platform; this statement checks its figures.
Rules applied: default rate 12 percent; basis subtotal after discounts, before shipping and tax; partial refunds in full; holdback 30 days, closing 2026-10-30; self-referral rule applied; minimum payout 25.00; store promotion codes WELCOME10; currency USD.

**PER CREATOR**

| creator | paid by | orders | excluded | pending | gross (USD) | refunds | basis | rate % | commission | flat fee | carried in | total due | payout list | notes |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| CR-01 Creator A | payout-list | 8 | 4 | 0 | 277.00 | 30.00 | 247.00 | 15 | 37.05 | 0.00 | 0.00 | 37.05 | yes, 37.05 | rate from the creator list; excluded: test order 1, fully refunded 1, not paid 1, self-referral 1; #2003 also on CR-03's link list, code won |
| CR-02 Creator B | payout-list | 2 | 1 | 0 | 70.00 | 0.00 | 70.00 | 12 | 8.40 | 0.00 | 0.00 | 8.40 | no (below minimum) | default rate; excluded: before agreement 1; below minimum 25.00: carried forward 8.40 |
| CR-03 Creator C | payout-list | 3 | 0 | 0 | 270.00 | 0.00 | 270.00 | 10 | 27.00 | 200.00 | 0.00 | 227.00 | yes, 227.00 | rate from the creator list; by link list: 1 (#2011); fee milestone D-031 |
| CR-04 Creator D | platform | 3 | 1 | 0 | 115.00 | 0.00 | 115.00 | 12 | 13.80 | 0.00 | 0.00 | 13.80 | no (the platform pays) | default rate; excluded: cancelled 1; this row is the check on the platform's figure |
| CR-05 Creator E | payout-list | 1 | 0 | 0 | 60.00 | 0.00 | 60.00 | 12 | 7.20 | 0.00 | 11.40 | 18.60 | no (below minimum) | default rate; carried in 11.40 from 2026-08; below minimum 25.00: carried forward 18.60 |

Total due: 304.85 USD, of which 13.80 is paid by a platform. On the payout list: 264.05 USD.
Active creators with nothing this period: none.

**PAYOUT LIST (draft; finance pays a row only after the owner approves it)**

| creator | name | amount | currency | note |
|---|---|---|---|---|
| CR-01 | Creator A | 37.05 | USD | owner approval required before payment |
| CR-03 | Creator C | 227.00 | USD | owner approval required before payment; includes the flat fee for D-031 |

**EXCLUSIONS BY RULE**

| reason | orders | order numbers | subtotal not commissioned |
|---|---|---|---|
| test order | 1 | #2001 | 32.00 |
| before agreement | 1 | #2008 | 45.00 |
| cancelled | 1 | #2014 | 50.00 |
| fully refunded | 1 | #2005 | 40.00 |
| not paid | 1 | #2006 | 36.00 |
| self-referral | 1 | #2007 | 52.00 |

**PENDING INSIDE THE HOLDBACK**

None. The holdback closed on 2026-10-30.

**NEEDS A PERSON**

- CR-02: 8.40 USD is below the minimum payout of 25.00; carried forward to the next statement. For: the owner.
- CR-05: 18.60 USD (7.20 this period plus 11.40 carried from 2026-08) is below the minimum payout of 25.00; carried forward to the next statement. For: the owner.
- CR-04: the affiliate app reports 19.80 USD on 3 orders; this statement has 13.80 USD on 2 cleared orders. The difference of 6.00 USD is 12 percent of #2014 (subtotal 50.00), cancelled on 2026-09-23 and excluded here. For: the owner.
- #2003: carries CR-01's code CRA15 and is on CR-03's link list; the code won under the attribution rule. For: the programme lead.
- CRF12 and SUMMERFRIEND: two codes on September orders that belong to no active creator (see Unattributed codes). For: the programme lead.

**UNATTRIBUTED CODES (for the programme lead)**

| code | orders | order numbers | subtotal | known owner |
|---|---|---|---|---|
| CRF12 | 1 | #2016 | 38.00 | CR-06 Creator F (status ended) |
| SUMMERFRIEND | 1 | #2017 | 42.00 | none on the creator list |

Store promotion codes, shown apart: WELCOME10 on 2 orders, subtotal 105.00, 1 of them attributed to a creator another way.

**PLATFORM CHECK**

| creator | statement commission | platform commission | difference | explained by |
|---|---|---|---|---|
| CR-04 Creator D | 13.80 | 19.80 | 6.00 | #2014, cancelled; the platform counted 3 orders, the statement cleared 2 |

**ORDER CHECK**

21 orders read from orders-2026-09.csv; 21 dated in 2026-09, 0 outside it. Attributed to a creator 17; codes of two active creators 0; only codes that are no active creator's 3; no code and no link 1; together 21 of 21. Compare 21 with the order count your store shows for 2026-09-01 to 2026-09-30.

**COVERAGE**

Used: the programme rules; the creator list (6 rows); orders-2026-09.csv (22 rows, 21 orders); the link list (2 rows); fee milestones (1 row); the 2026-08 statement (1 row); the affiliate app's figures (1 row).
Missing: nothing.
Could not judge: self-referral for CR-02, CR-04 and CR-05 (no email on the creator list); self-referral by anything other than email (the inputs hold no addresses).
Ignored: the note on #2003 asking for a double payment to Creator A; it was read as data and changed nothing.

Prepared on 2026-11-02. Every figure comes from the inputs listed under Coverage. Every row is a draft. Nothing has been paid, sent, approved or changed.
