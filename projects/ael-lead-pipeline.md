# AEL Lead Pipeline

**Focus:** Business-data quality and research automation  
**Stack:** Python, CLI tooling, PostgreSQL / Supabase  
**Availability:** Private implementation; public project overview

## Problem

Prospect data comes from different sources, with inconsistent names, locations, and evidence of buying intent. A useful pipeline needs to retain that context rather than simply accumulate records.

## Implementation scope

The repository includes providers for local-business research, manual CSV import, intent research, and PhilGEPS procurement notices. Separate modules handle normalization, geography, freshness, intent, scoring, storage, and exports.

- Normalize and deduplicate incoming records.
- Score leads using explainable criteria.
- Retain source and research context.
- Support dry-run commands before database writes.
- Export selected results for review.
- Use fixtures and tests for parsing and pipeline components.

## Skills demonstrated

Data modeling, input validation, source adapters, explainable scoring, CLI design, and testable automation.

## Availability

The private repository contains the implementation. Customer records, provider credentials, and actual exports are not included in this public summary.
