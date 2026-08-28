# Florida APD Rules — effective dates dataset

Every rule in the Florida Administrative Code chapters that govern **Agency for
Persons with Disabilities (APD)** providers, with the effective date the state
publishes for each one.

**102 rules · 7 chapters · re-verified daily**

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
| `chapter_topic` | Plain-English description of what the chapter covers |
| `rule_number` | Full rule number, e.g. `65G-2.008` |
| `rule_title` | The rule's official title |
| `effective_date` | Current effective date, ISO `YYYY-MM-DD` |

### Chapters covered

| Chapter | Covers |
|---|---|
| 65G-1 | APD general provisions |
| 65G-2 | Licensing and staffing of residential facilities |
| 65G-4 | iBudget, support plans and eligibility |
| 65G-7 | Medication administration |
| 65G-8 | Reactive strategies |
| 65G-10 | Appeals and hearings |
| 65G-13 | Provider qualifications |

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
