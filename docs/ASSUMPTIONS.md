# Assumptions register

This register makes the conceptual nature of the project explicit. Every numerical model must link each non-derived input to a source, an assumption or a design decision.

## Status key

- **Open** — not yet selected; do not use as a final design value.
- **Working** — usable for exploration, but subject to change.
- **Frozen** — controlled baseline value for a documented study.
- **Retired** — superseded; retained for traceability only.

## Initial register

| ID | Subject | Status | Current statement | Evidence / next action |
| --- | --- | --- | --- | --- |
| A-001 | Architecture | Working | Geared, variable-pitch, single-rotor open propfan with conceptual gas-turbine core. | Compare with public open-rotor references in WP-01. |
| A-002 | Aircraft class | Open | Regional aircraft is the intended reference application. | Define passenger count, range, cruise condition and field performance in M1. |
| A-003 | Certification | Frozen | The project is educational conceptual design, not a certifiable engine programme. | State this in every technical report. |
| A-004 | Units | Frozen | SI units are used in source-code interfaces, configuration files and reports. | Add unit tests and documentation as modules are created. |
| A-005 | Validation | Working | Validation will use analytical cases, public propeller data and trend checks; proprietary engine performance is not assumed available. | Define the validation matrix before BEMT optimisation. |

## Adding an assumption

Give each item a stable ID, date it in the associated issue or report, record its origin and explain its expected effect on the model. Do not delete retired assumptions: mark them as retired and link to the replacement.
