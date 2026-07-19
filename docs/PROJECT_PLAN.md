# Project plan

## Purpose

Develop a technically honest, reproducible conceptual design of a geared, single-rotor open propfan over an 18-month period. The project is organised around evidence and iterations, not a one-way sequence of isolated analyses.

## Work packages

| ID | Work package | Primary evidence |
| --- | --- | --- |
| WP-00 | Project management | Scope, schedule, risks, issues and change log |
| WP-01 | State of the art | Referenced comparison of historical and current open-rotor concepts |
| WP-02 | Requirements and mission | Reference aircraft and traceable mission requirements |
| WP-03 | Aircraft performance | ISA, mission, drag-polar and performance models |
| WP-04 | Thermodynamic cycle | Design and off-design shaft-power cycle model |
| WP-05 | Propfan and gearbox | BEMT, geometry, gearbox sizing and design-space exploration |
| WP-06 | Integration | Materials, CAD assembly and preliminary structural assessment |
| WP-07 | Verification | Tests, public-data comparisons, sensitivity and uncertainty analysis |
| WP-08 | Communication | Technical report, software guide, renders, video and portfolio case study |

## Milestones

### M1 — Requirements baseline (months 1–2)

- Define the reference aircraft and system boundary.
- Publish the assumptions register and risk register.
- Complete a source-backed state-of-the-art comparison.

### M2 — Aircraft and mission model (months 3–4)

- Implement and test an ISA atmosphere module.
- Establish mission segments, power required and fuel/energy accounting.
- Benchmark the reference-aircraft model against public data.

### M3 — Core and transmission concept (months 5–6)

- Build the shaft-power Brayton-cycle model.
- Establish preliminary component efficiencies, temperature limits and gearbox ratio.

### M4 — Propfan design space (months 7–8)

- Implement the BEMT solver, including documented loss and correction models.
- Generate the preliminary blade geometry and compare candidate configurations.
- Use a Pareto view rather than claiming a single universally optimal design.

### M5 — CAD and engineering assessment (months 9–13)

- Parameterise blade, hub, spinner, gearbox envelope and installation.
- Complete preliminary FEA of the blade/root/hub load cases.
- Treat CFD as a bounded comparison study, not as a substitute for model verification.

### M6 — Validation and portfolio (months 14–18)

- Run analytical and public-data validation cases.
- Perform sensitivity and uncertainty analysis.
- Freeze a documented baseline configuration and publish the portfolio package.

## Definition of done for an analysis module

An analysis module is complete only when it includes:

1. Clearly named SI-unit inputs and outputs.
2. Sources and assumptions recorded in `docs/ASSUMPTIONS.md`.
3. At least one automated test or independently checkable case.
4. A plot or table that explains the result and its limits.
5. A short technical note linked from the relevant GitHub Issue.
