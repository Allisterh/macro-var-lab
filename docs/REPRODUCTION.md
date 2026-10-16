# Reproducing the saved results

The public repository contains aggregate tables, figures and reports. Raw observations, fitted objects, bootstrap arrays and repetition-level checkpoints are excluded. [DATA.md](../DATA.md) describes access and source terms.

## Checks and report builds

Python 3.11 and uv are needed for checks; Tectonic is needed for PDF compilation.

```sh
make setup
make test lint quick
```

The quick example is synthetic. With Tectonic installed and its TeX cache populated, `REPORT_OFFLINE=1 make report` builds the technical paper from saved aggregates. `make policy-note` also rebuilds the short note, but its presentation script regenerates this README, figures and summary files from the older embedded template. Run presentation rebuilds in a separate clone to retain the current editorial text. The same side effect applies to `make figures`, `make readme-numbers` and `make v3-outputs`.

## Empirical reruns

The original acquisition pipeline uses official sources and a local ignored `.env` with FRED_API_KEY and EVDS_API_KEY. `make v3-methods` needs the locally acquired panel and the exact EA-MPD workbook identified by its frozen hash. Refreshed observations or a different workbook are not equivalent inputs.

The original `make all` pipeline predates the final extensions. It overwrites aggregate outputs and is not a self-contained reconstruction of the final private checkpoint history. The dated protocols retain the exact specifications, seeds and execution budgets; a new source vintage need not reproduce the saved estimates. Use a separate clone for reruns.

The public snapshot was exported from local source commits without merging the private research history. Publication did not change learners, identification assumptions or causal estimands.
