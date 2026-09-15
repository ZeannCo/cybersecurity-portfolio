# ePLDT VM Tracker & Automation

**Focus:** Vulnerability management, remediation tracking, and security reporting  
**Stack:** Python, FastAPI, SQLAlchemy, PostgreSQL, React, TypeScript, Vite  
**Availability:** Internal application; public project overview

## Problem

Vulnerability-management work involves more than running a scanner. Asset inventories need cleaning, findings need context, and remediation progress needs to be communicated consistently.

## Project

I built a vulnerability registry to replace separate spreadsheet trackers with an analyst dashboard. It brings together scan ingestion, finding triage, remediation status, risk-acceptance and false-positive dispositions, and report-generation workflows.

The application separates two jobs: importing current vulnerability posture from Qualys, and producing reports from a specific CSV scan export. The related [report generator](qualys-report-automation.md) is documented separately because it also has a desktop interface.

## Key engineering decisions

- **A missing finding is not automatically a fixed finding.** Coverage gaps, unreachable assets, and failed authentication must not create false remediation claims.
- **Scanner status and analyst disposition stay distinct.** Accepting a risk does not erase the underlying scanner observation.
- **Preview before commit.** Analysts can inspect changes before accepting a posture snapshot; repeat commits are designed to avoid double-counting.
- **Traceable findings.** Scan provenance and scope help explain where a count came from.
- **Role-based workflows.** Analyst and administrator responsibilities are separated.

## Architecture

```text
Qualys posture data             Scan CSV
        |                          |
Snapshot / coverage checks     Report workflow
        |                          |
Vulnerability registry         Report documents
        |
React analyst dashboard
```

The repository includes backend tests for status derivation, normalization, imports, reporting, and coverage handling, plus frontend unit and end-to-end test tooling. This portfolio review did not rerun the application test suites.

## Skills demonstrated

- Connecting vulnerability findings to operational follow-up.
- Preparing asset data for useful scanning and reporting.
- Translating technical findings into reporting for different audiences.
- Building automation around an existing security process.

## Scope

This overview describes the work at a professional level. It does not publish the tracker source, employer templates, asset inventories, customer findings, or internal endpoints. The live application is not offered as a public demo.
