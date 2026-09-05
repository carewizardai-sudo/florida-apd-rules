# Florida APD Rules — effective dates dataset

Every rule in every Florida Administrative Code chapter the **Agency for
Persons with Disabilities (APD)** administers — all sixteen of them — with the
effective date the state publishes for each one.

**140 rules · 16 chapters · re-verified daily**

Widened on 3 September 2026 from the seven chapters that govern a group home to
the complete set (adding 65G-3, 5, 6, 9, 11, 12, 14, 15 and 16), because "every
chapter APD has" is a boundary a reader can check and "the ones that matter" is
a judgement that quietly drifts.

| File | Format |
|---|---|
| [`data/florida-apd-rules.csv`](data/florida-apd-rules.csv) | CSV |
| [`data/florida-apd-rules.json`](data/florida-apd-rules.json) | JSON |

Licensed **CC0-1.0** — public domain. Use it for anything, no attribution
required (though a link back is appreciated).

---

## ⚠️ Read this before using the data

**These are CURRENT effective dates, not a complete amendment history.**

A rule amended in 2012 and again in 2026 appears here **only as 2026**, because
that is what the state's rule index publishes.

This matters because the obvious analysis is the wrong one. If you group by year
and see 12 rules against 2008, that does **not** mean APD amended 12 rules in
2008. It means **12 rules have not been touched since 2008** — which is a
different and arguably more interesting fact.

If you need a full amendment history for a specific rule, the rulemaking history
line at the bottom of each rule document on
[flrules.org](https://www.flrules.org) lists every amendment date.

## What is in it

| Column | Meaning |
|---|---|
| `chapter` | F.A.C. chapter, e.g. `65G-2` |
| `chapter_official_title` | The chapter title Florida publishes, verbatim |
| `chapter_topic` | Our plain-English description of what the chapter covers |
| `rule_number` | Full rule number, e.g. `65G-2.008` |
| `rule_title` | The rule's official title |
| `effective_date` | Current effective date, ISO `YYYY-MM-DD` |

### Chapters covered

<!-- chapters:start -->

| Chapter | Florida's title | What it covers |
|---|---|---|
| 65G-1 | Waiver Enrollment for Children in the Child Welfare System | Waiver enrollment for children in the child welfare system |
| 65G-2 | Licensure of Residential Facilities and Adult Day Training Programs | Licensing and staffing of residential facilities |
| 65G-3 | Termination, Suspension or Reduction of Client Services by Service Providers | Stopping, reducing or suspending client services |
| 65G-4 | Service Delivery Practice and Procedure | iBudget, support plans and eligibility |
| 65G-5 | Supported Living Services | Supported Living services |
| 65G-6 | Foster Care, Group Home, Developmental Training, and Supported Employment Programs Trust Fund | Trust fund loans for foster care, group homes and supported employment |
| 65G-7 | Medication Administration | Medication administration |
| 65G-8 | Reactive Strategies | Reactive strategies |
| 65G-9 | Forensic Client Services | Forensic client services |
| 65G-10 | Provider Training | Provider training |
| 65G-11 | DD Preenrollment Categories | Pre-enrollment categories - the waiting list |
| 65G-12 | Agency Data Management Systems | Agency data systems, including Electronic Visit Verification |
| 65G-13 | Individual and Family Supports | Individual and family supports, and the in-home subsidy |
| 65G-14 | Qualified Organizations and Waiver Support Coordination | Qualified Organizations and waiver support coordination |
| 65G-15 | State Institution Claims Program | State institution claims |
| 65G-16 | Unique Abilities Partnership Program | Unique Abilities Partnership Program |

<!-- chapters:end -->

Repealed and transferred rules are **included**, because they still appear on
the state index and their absence would be misleading.

## Method

1. Fetch the official [flrules.org](https://www.flrules.org) chapter index for
   each chapter above.
2. Extract each row: rule number, title, and the effective date printed beside
   it.
3. Re-check daily. When the state amends a rule, its effective date moves and
   the change is picked up automatically.

The extraction is deliberately structural rather than clever: each table row on
the index becomes one record. There is no interpretation step, so there is
nothing to get subtly wrong.

## A finding worth knowing

**26 March 2026 is the largest single amendment day in this dataset: 27 rules
took effect at once** — 19 in Chapter 65G-2 and 8 in Chapter 65G-7. The next
largest day in the record is 12.

APD does not amend rules gradually. It amends in batches, and the batches are
large — which is why a provider can go two years without a change and then face
twenty-seven in one morning.

## Citing this

> Care Wizard, *Florida APD Rules — effective dates dataset*, 2026-08-28,
> https://github.com/carewizardai-sudo/florida-apd-rules

Found an error? [Open an issue](https://github.com/carewizardai-sudo/florida-apd-rules/issues).
Corrections get made and noted — accuracy matters more here than looking right.

## Why this exists

We maintain this because we have to. [Care Wizard](https://carewizard.ai) is
compliance tracking for Florida APD group homes, and it re-reads these indexes
every day so providers hear when a requirement changes. Having assembled the
data, publishing it costs nothing and it is more useful in the open.

Related, all free and no signup:

- [What changed in Florida APD rules](https://carewizard.ai/whats-changed) — the running record
- [Every rule with its effective date](https://carewizard.ai/florida-apd-rules) — browsable
- [The full data report](https://carewizard.ai/florida-apd-rules/report) — charts and analysis

## Disclaimer

This is a reference, not legal advice, and not an official APD publication.
Always read the rule itself on [flrules.org](https://www.flrules.org) before
acting on it. Care Wizard is an independent company and is not affiliated with
or endorsed by the Agency for Persons with Disabilities or any government
agency.
