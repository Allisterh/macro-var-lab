# Monetary-policy transmission in the euro area and Türkiye

I study how estimated responses to monetary tightening change with the identification method and the response estimator. I assembled official monthly series, implemented VAR and local-projection comparisons, and traced the estimates back to their data and specifications.

![Monetary-policy response estimates](figures/headline.png)

## The comparison I built

I compare recursive VARs, sign restrictions, recursive-shock local projections and a proxy VAR on a common euro-area sample, April 2005–October 2025. Within p = 3 and p = 7 specifications, I hold variables, transformations, deterministic terms and the 100-basis-point shock constant. The Türkiye analysis compares three specifications and treats shorter regimes separately.

I report sign-admissible ranges separately from statistical confidence bands. Proxy estimates remain conditional on instrument validity.

## What I found

- The euro appreciates after tightening. At month 12, the proxy estimate is 4.551 log percent for p = 3 (1.889, 7.630) and 3.305 for p = 7 (0.648, 5.505); both conditional 90% bands exclude zero.
- The price response is uncertain. The corresponding estimates are 0.172 and -0.078 log percent, with bands including zero; the sign also changes across methods.
- For Türkiye, the recursive month-12 price estimate is -0.288 log percent. The recursive, FX-first and recursive-shock local-projection estimates are negative, but their bands include zero.

Both common-sample euro-area VARs have slightly unstable dynamics. Longer-horizon local projections have fewer observations, and latest-vintage data do not reconstruct what was known in real time. These limits matter for interpreting the response paths.

## Read the analysis

[Policy note](report/policy_note.pdf) · [Technical working paper](report/technical_report.pdf) · [Detailed results](report/report.md) · [Methods guide](docs/METHODS.md)

Data come from the ECB, Eurostat, CBRT/EVDS, TURKSTAT, FRED and EA-MPD. [DATA.md](DATA.md) records series IDs, transformations and source terms. Source observations are acquired separately and are not redistributed.

## Working with the repository

Python 3.11 and uv are required for the code checks:

```sh
make setup
make test lint quick
```

`quick` uses synthetic data. The PDFs and aggregate results can be read directly. [Reproduction notes](docs/REPRODUCTION.md) explain report rebuilding, the frozen-input requirements for empirical reruns, and which commands regenerate presentation files, including this README.

Original code: [MIT](LICENSE). Data retain their source terms.

Hakan Zeki Gülmez · [Portfolio](https://hakangulmez.github.io/) · [GitHub](https://github.com/hakangulmez)
