# Qualys Report Automation

**Focus:** Security reporting automation  
**Stack:** Python, desktop GUI, Word and Excel document generation  
**Availability:** Private implementation; public project overview

## Problem

A single vulnerability scan needs to serve two audiences: technical teams need detailed findings, while decision-makers need an executive report. Preparing those outputs manually creates repetitive work and opportunities for inconsistent formatting.

## Implementation

The desktop application accepts a **Qualys CSV scan export** and generates an executive **.docx** report, a detailed **.xlsx** report, or both.

- Select the scan input, report templates, and output directory.
- Set a business unit or use automatic detection from the CSV header.
- Run preflight validation before report generation.
- Generate reports through background worker threads.
- Remember previously selected paths and provide output links in the run log.

The GUI and report-generation scripts are separated so the report logic can be updated independently of the launcher.

## Workflow

```text
Qualys CSV + report templates
            |
      Preflight validation
            |
      Report generation
         /       \
Executive .docx  Detailed .xlsx
```

## Skills demonstrated

Vulnerability-data processing, input validation, modular Python design, desktop usability, and communication of security findings.

## Availability

Source code and employer-specific templates remain private. This page documents the tool without including scan results or internal reporting material.
