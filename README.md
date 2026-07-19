# Propfan Experimental

> A reproducible conceptual-design platform for a geared, single-rotor open propfan.

![Project status](https://img.shields.io/badge/status-foundation-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## Overview

The objective is to develop and document a conceptual open-rotor propulsion system for a reference regional aircraft, from mission requirements through preliminary CAD and verification activities.

The repository treats the propfan as a system rather than an isolated CAD model. The engineering workflow links aircraft performance, gas-turbine cycle analysis, gearbox sizing, propeller aerodynamics, optimisation, CAD parameters, structural assessment and technical reporting.

> **Scope notice:** this is an educational, conceptual-design project. It is not intended to produce a certifiable, manufacturable or flight-ready engine.

## Objectives

- Build transparent Python models using SI units.
- Implement a Blade Element Momentum Theory (BEMT) solver from first principles.
- Explore design trade-offs between efficiency, mass, diameter, blade-tip Mach number and relative noise.
- Create a parameter-linked CAD assembly in Fusion 360.
- Validate models progressively against analytical cases and public reference data.
- Publish a clear and reproducible technical case study.

## System boundary

The baseline concept is a geared, variable-pitch, single-rotor open propfan driven by a conceptual gas-turbine core. The intended installation is a reference regional aircraft; the aircraft and engine requirements will be frozen during the first project milestone.

## Roadmap

| Milestone | Main outputs |
| --- | --- |
| 01 — Definition | Project plan, reference aircraft, requirements and assumptions register |
| 02 — Aircraft model | Atmosphere, mission, drag polar and performance model |
| 03 — Powerplant | Brayton-cycle model, core architecture and gearbox sizing |
| 04 — Propfan | Preliminary geometry, BEMT solver, optimisation and noise screening |
| 05 — Integration | Materials, parametric CAD assembly and preliminary structural assessment |
| 06 — Evidence | Validation, sensitivity analysis, final design selection and portfolio package |

The detailed plan is available in [docs/PROJECT_PLAN.md](docs/PROJECT_PLAN.md).

## Repository layout

```text
.
├── cad/          Fusion 360 models, exports and CAD guidance
├── cfd/          CFD cases, meshing notes and post-processing guidance
├── config/       Versioned model input files
├── data/         Airfoil data and curated public datasets
├── docs/         Engineering plan, assumptions and technical reports
├── notebooks/    Exploratory analysis only
├── results/      Selected figures and reproducible result tables
├── src/propfan/  Reusable Python model modules
└── tests/        Automated model verification tests
```

## Planned software stack

- **Python**: numerical models, optimisation, plots and report tables.
- **Fusion 360**: parametric CAD, assembly and preliminary structural studies.
- **XFOIL**: 2D airfoil polar generation.
- **OpenFOAM + ParaView**: optional, scoped CFD and visualisation.
- **GitHub**: version control, issue tracking and portfolio publication.
- **Zotero + Quarto**: references and reproducible technical documentation.

## Getting started

The Python environment will be introduced with the first analysis module. The intended setup is:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -e ".[dev]"
```

Until then, start by reading the [project plan](docs/PROJECT_PLAN.md), recording decisions in the [assumptions register](docs/ASSUMPTIONS.md) and opening a GitHub Issue for each substantial engineering task.

## Engineering principles

- SI units are mandatory at module boundaries.
- Every model input must have a source, assumption or justification.
- Results are never presented without their assumptions and limitations.
- Exploratory notebooks do not replace tested modules in `src/`.
- Large CAD and simulation artifacts require Git LFS or external archival storage; do not commit them casually.

## License

The code and documentation are released under the [MIT License](LICENSE). Third-party datasets, publications and manufacturer material remain subject to their original licences and terms.
