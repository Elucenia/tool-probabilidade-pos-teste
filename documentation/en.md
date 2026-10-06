<!-- ELUCENIA technical documentation · probabilidade-pos-teste · en · no clinical/professional/rights approval -->

# Post-test probability (Bayes’ theorem)

[conditions, sources and permissions](https://elucenia.org/en/tools/probabilidade-pos-teste)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Pretest probability (prevalence or clinical estimate)

`pre`

% · range: 0.1–99.9

### Likelihood ratio of the result (LR+ if positive, LR− if negative)

`rv`

range: 0.001–1000

## Method edition

Bayes odds: Fagan 1975; pretest odds×LR, posttest conversion; Deeks–Altman 2004 likelihood ratios

## Documented formula

Pretest odds = p / (1 − p) · Posttest odds = Pretest odds × LR · Posttest probability = Posttest odds / (1 + Posttest odds).

This is the odds form of Bayes theorem, solved graphically by the Fagan nomogram.

## Limits and population

Pre-test probability must represent the population and clinical context assessed; the likelihood ratio must correspond to the test and result category. Probability and odds are different quantities: updating multiplies odds by the likelihood ratio and only then converts back to probability. Predictive values vary with prevalence and do not transfer automatically between studies and services. The calculation updates an estimate; it does not independently confirm or exclude a disease.

## References

- [Fagan TJ. Nomogram for Bayes's theorem. N Engl J Med, 1975.](https://doi.org/10.1056/NEJM197507312930513)

- [Deeks JJ, Altman DG. Diagnostic tests 4: likelihood ratios. BMJ, 2004.](https://doi.org/10.1136/bmj.329.7458.168)

- [Deeks/Altman2004,Diagnostic tests4:likelihood ratios](https://pmc.ncbi.nlm.nih.gov/articles/PMC478236/)

- [Fagan1975](https://doi.org/10.1056/NEJM197507313930513)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Documented results

The information below preserves the method outputs for synthetic examples. It does not constitute independent clinical validation.

### 1

Post-test probability of 72.7% (LR between 5 and 10: moderate increase)

| Result details | |
| --- | --- |
| Pre-test odds | 0.333 |
| Post-test odds | 2.667 |
| Absolute change | +47.7 percentage points |


### 2

Post-test probability of 9.1% (LR ≤ 0.1: large reduction in probability)

| Result details | |
| --- | --- |
| Pre-test odds | 1.000 |
| Post-test odds | 0.100 |
| Absolute change | −40.9 percentage points |


### 3

Post-test probability of 10.0% (LR between 0.5 and 2: the test barely changes the probability)

| Result details | |
| --- | --- |
| Pre-test odds | 0.111 |
| Post-test odds | 0.111 |
| Absolute change | +0.0 percentage points |

