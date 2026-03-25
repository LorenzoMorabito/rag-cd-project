# Promo OAS XML Analysis

## Scope

Source analyzed:
- `C:\work\MEN_Marketing\PBI_ProductAnalysis_POC\data_source\xml_oas\esempio_dashboard_promotional_xml.txt`

This is a mixed dump, not a pure promotional export.
Detected subject areas:
- `OPERA - Calls&Mentions`: 22 reports
- `OPERA2`: 6 reports
- `MKR2_BC - Sell OUT`: 1 report

This document analyzes only the 22 reports in subject area `OPERA - Calls&Mentions`.

Important limitation:
- this is a sample dashboard export, not the full OAS promotional catalog
- the extracted inventory represents measures actually used in this sample
- it is a migration input, not yet the complete promotional measure universe

## What The Sample Dashboard Uses

The OAS promotional sample is materially richer than the finance sample and is organized in recurring report families.

### 1. Promotional Benchmarking

Observed measures:
- `Investments`
- `% Share of Investments`
- `Product Details`
- `% Share of Voice`
- splits by `Digital / Traditional`

Observed time frames:
- `MON`
- `MQTR` via `PERIODROLLING(...,-2,0)`
- `QTR`

Business meaning:
- promotional pressure and share-of-voice benchmarking on market/product/channel slices

### 2. Promotional Outlook 1/2 and 2/2

Observed dynamic measure family:
- `@{var_mea}{Contact Number}`
- `% of @{var_mea}{Contact Number}`
- `+/- vs PY`
- `+/-% vs PY`

Observed breakdowns:
- specialty
- presentation position
- contact type
- contact channel
- corporations

Important note:
- the dump exposes the placeholder `@{var_mea}` but does not unambiguously enumerate all prompt values
- the default visible value is `Contact Number`
- this implies a dynamic measure family, not a single static metric

### 3. Monthly Prescription Overview

Observed measures:
- `Spending Total Euro` in absolute
- `% on Spending Total Euro`

Observed axes:
- `Prescription Current`
- `Prescription Future`

Business meaning:
- spend distribution across current/future prescribing states

### 4. Performance Measurement

Observed measures:
- `Contact Number`
- `Share of Contact Number`
- `Contact Number with intention to increase Rx`
- `% of Contact Number with intention to increase Rx`
- `Product Details`
- `Product Details with Positive Prescribing`
- `Contacts with Positive Prescribing`
- `Conversion rate - % of Calls converted in intention to prescribe`
- `Conversion rate - % of Contacts converted in intention to prescribe`

Observed time frames:
- `MON`
- `MQTR`
- `QTR`

Business meaning:
- quality and effectiveness of promotional execution

### 5. Weighted Calls / SOV / Index / Ranking

Observed measures:
- `@{measure}{WCalls}`
- `SOV%`
- `SOV% MQTR`
- `+/- %`
- `+/- % mqtr`
- `Index`
- `% Corp on total`
- `% Market on Total`

Observed dimensions:
- corporation / promoter / manufacturer
- specialty / GPs-Spec
- contact type
- contact quality
- channel split

Important note:
- the OAS sample uses a true analytical family on `Weighted Calls`
- not just a single additive measure

## Core OAS Promo Measure Families Detected

Base promotional measures explicitly referenced:
- `Spending Total Euro`
- `Product Details`
- `Contact Number`
- `Weighted Calls`

Business-derived promotional KPI families:
- `% Share of Investments`
- `% Share of Voice`
- `% Share of Contact Number`
- positive prescribing metrics
- conversion rates
- delta vs PY
- growth % vs PY
- weighted-calls index family

Time patterns actually used in the sample:
- `MON`
- `MQTR`
- `QTR`

What is notably absent from the OAS promotional sample:
- explicit `YTD`
- explicit `MAT4Q` as a user-facing promotional frame

There is one isolated `WCalls MAT` reference, but only as helper logic in a flag calculation, not as the main user-facing frame.

## Mapping To Current Power BI Promo Measures

Current PBI promo layer already includes:
- `Promo Spend`
- `% Share of Investments`
- `Promo Details`
- `Promo SOV%`
- `Promo SOV% (ATC4)`
- `Promo Contacts`
- `Promo Weighted Calls`
- `Promo Quality Index`
- `Promo Calls with Positive Prescribing`
- `Promo Contacts with Positive Prescribing`
- `Promo Conversion Rate Calls %`
- `Promo Conversion Rate Contacts %`
- `Promo ESOV`
- LP and switch logic

### Covered at business-concept level

- `Investments`
- `% Share of Investments`
- `Product Details`
- `% Share of Voice`
- `Contact Number`
- `Weighted Calls`
- positive prescribing family
- conversion rate family

### Derivable but not yet packaged explicitly

- spend by `Current/Future Prescribing`
- spend share by prescribing segment
- some share measures on contact families
- some corporation-filtered slices

### Missing or only partially covered

- dynamic `@{var_mea}` contact-metric family
- `Delta vs PY` and `+/-% vs PY` families for the full outlook battery
- weighted-calls `SOV%` family as an explicit governed measure set
- weighted-calls `Index` family
- `% Corp on total` / `% Market on total`
- ranking-oriented analytic measures used by OAS

## Structural Gap Vs OAS

This is the most important technical finding.

The current PBI promo model is not aligned to the temporal behavior of the OAS sample.

Evidence:
- OAS promotional reports are mainly built on `MON`, `MQTR`, and `QTR`
- the current PBI promo fact table relates to `T_DIM_QUARTER`, not directly to `T_DIM_MONTH`
- the current `SwitchPeriodMode` exposes only:
  - `QTR`
  - `MAT (4Q)`

Implication:
- even when the business concept of a measure already exists in PBI, OAS parity is not guaranteed
- the gap is often temporal and structural, not just formula-based

In practice, the current PBI promo model is stronger on:
- quarter analysis
- LP quarter analysis
- MAT4Q logic

The OAS promotional sample is stronger on:
- monthly views
- moving-quarter (`MQTR`) views based on 3-month rolling windows
- dynamic analytical slices on weighted calls and contact families

## Specific Comparison With Current PBI Promo UX Layer

The current promo selector in PBI exposes only:
- `Spending`
- `Details`
- `Contacts`
- `Weighted Calls`

This is narrower than the OAS sample, which also operationally uses:
- share measures
- delta/growth comparator measures
- positive prescribing measures
- conversion measures
- weighted-calls index measures

So the semantic layer is richer than the selector, but still not rich enough for full OAS parity.

## Migration Implications

From this XML sample, the minimum promo migration backlog should include 3 separate layers.

### 1. Core promo battery

- `Promo Spend`
- `Promo Details`
- `Promo Contacts`
- `Promo Weighted Calls`
- `% Share of Investments`
- `% Share of Voice`
- positive prescribing family
- conversion family

### 2. Time-intelligence / compare battery aligned to OAS

- `MON`
- `MQTR`
- `QTR`
- `Δ vs PY`
- `Δ% vs PY`

This is different from the current PBI emphasis on `QTR`, `LP`, and `MAT4Q`.

### 3. Advanced analytical battery

- weighted-calls `SOV%`
- weighted-calls `Index`
- corporation share vs market share families
- dynamic contact/outlook metric family
- ranking helpers when needed for OAS parity

## Key Conclusion

The promo world is only partially covered by the current PBI semantic model.

The situation is different from finance:
- on business concepts, PBI promo is already fairly rich
- on OAS parity, the biggest gaps are time grain and analytical packaging

Main gaps discovered from the XML sample:
- lack of a true `MON/MQTR` promo layer in the current model
- absence of the weighted-calls index family
- missing dynamic `Delta vs PY` and `Δ% vs PY` families for the promotional outlook battery

## Next Recommended Step

Use this promo OAS inventory as the second migration baseline, then:

1. decide whether the new semantic model must support promo at true monthly grain, not only quarter grain
2. define a governed `MON / MQTR / QTR` policy for the promo world
3. add the missing weighted-calls analytical family
4. run the same XML extraction on the OAS sales dump
5. compare OAS sales coverage against `Msr Sales`, to verify whether the current PBI report/model already covers the real business perimeter or still misses critical measures
