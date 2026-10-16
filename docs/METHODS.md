# Methods guide

The main euro-area comparison holds the estimation sample, variables, transformations, deterministic terms and shock scale fixed within p = 3 and p = 7 panels. It compares recursive VARs, sign restrictions, recursive-shock local projections and a proxy VAR; local projections use fewer supported origins at longer horizons.

I kept these choices explicit because a change in sample or lag order can otherwise be mistaken for an identification effect. Sign-admissible ranges, HAC bands and bootstrap bands have different interpretations. Proxy inference is conditional on the instrument and fitted dynamics. Slightly unstable VAR dynamics remain visible rather than being removed by specification changes.

- [Initial design](DESIGN.md): source selection, transformations and the original scope.
- [Initial estimation methods](G2_METHODS.md): formulas, diagnostics, bootstrap and regime details.
- [Dated comparison protocol](V3_PROTOCOL.md): fixed samples, lags, inference settings and the documented VIX wording erratum.
- [Provenance](PROVENANCE.md): current result lineage and reproduction boundaries.
- [Technical paper](../report/technical_report.pdf): equations, estimates and limitations.

The dated protocols record decisions at their original stages. Later methods and results are identified separately in the provenance record.
