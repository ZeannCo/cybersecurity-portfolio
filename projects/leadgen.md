# Leadgen Automation

**Focus:** Reliable data pipelines and business-system integration  
**Stack:** Python, Playwright, HTTP APIs, PostgreSQL / Supabase, Railway, GoHighLevel  
**Availability:** Private client system; public architecture overview

## Problem

Lead acquisition spans multiple sources and services. Manual collection and handoffs make it difficult to keep records consistent, avoid duplicates, and see where a workflow failed.

## Project

I design and maintain lead-generation automation, including data flow, integrations, and operational reliability. The codebase separates source collection, qualification, enrichment, routing, and downstream delivery.

```text
Scheduled source collection
            |
   Normalize and deduplicate
            |
     Qualify and enrich
            |
       Route records
            |
    CRM / downstream workflows
```

The system includes source-specific scrapers, service integrations, scheduled jobs, and dashboard pages for operations and search. Integrations include GoHighLevel and Bland.ai; the broader pipeline also contains eligibility, budget, calling-window, and suppression-check components.

## My contribution

Architecture and ongoing implementation work, including lead-pipeline features, caller search, name-search improvements, and fixes for HTTP-related storage and search failures.

## Skills demonstrated

API integration, asynchronous data collection, deduplication, workflow orchestration, production troubleshooting, and maintaining a system across multiple providers.

## Availability

The client repository, lead records, provider credentials, and operational configuration remain private. This page is a public summary of the engineering work, not a public lead dataset or live outreach demo.
