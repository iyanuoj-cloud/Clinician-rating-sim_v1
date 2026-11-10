# Clinician rating simulation (v0.1)

A browser-based simulation for calibrating red/yellow respiratory-concern thresholds with clinicians.
A clinician watches an animated newborn and an 8-minute breathing-rate trend, then rates the baby
green, yellow or red. Ratings and timings are recorded for analysis.

Part of Team Pulse Check's neonatal respiratory monitoring project (NOVA and RIBBON).

## Status

v0.1: one hard-coded scenario, plus test scenarios. The scenario generator, consent screen and
automatic data collection are not built yet.

## Run it

Open `index.html` in any browser. No build step and no installs.
Add `#dev` to the address to show a dropdown of test scenarios.

## Data

At the end of a scenario the page shows a copyable JSON record: every rating change with its
live timestamp, the rate shown on the graph, the true underlying rate, the see-saw level, and
whether the baby was still.

## Notes

- Scenarios are defined as data in the `SCENARIOS` object in `index.html`. Each has a seed, so a
  rerun is identical.
- The pause is defined as chest and belly movement stopping.
- Thresholds, decay constants and scenario values are preliminary engineering choices, not
  clinically validated parameters.
