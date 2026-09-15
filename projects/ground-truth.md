# Ground Truth

**Focus:** Purple-team lab, detection engineering, and DFIR evaluation  
**Stack:** PowerShell, Python, Active Directory lab tooling, Sigma, GitHub Actions  
**Status:** Early build

## Research question

How can an investigator or an AI forensic assistant be evaluated against what actually happened, rather than against a plausible explanation?

Ground Truth is designed around scripted lab scenarios with a timestamped answer key. The intended workflow compares detection output and forensic reports against that answer key.

## Present in the repository

- Project plan and lab setup documentation.
- A PowerShell mini-lab build script and GOAD setup notes.
- A scenario schema describing the intended evidence contract.
- A detection-test workflow and a placeholder test scaffold.

## Planned capabilities

- Scripted Active Directory scenarios producing evidence bundles and ground truth.
- Sigma detection validation against saved logs.
- An LLM forensic analyst and evaluation scorer.
- Metrics for technique recall, timestamp error, key-question accuracy, and hallucination rate.

These are development goals, not completed benchmark results. No leaderboard results are claimed.

## Design principles

Isolated lab networking, synthetic evidence, and offline analysis of saved bundles keep the project reproducible and separate from production systems.

## Skills demonstrated

Lab design, reproducible security experiments, evidence modeling, and a testable approach to detection engineering.
