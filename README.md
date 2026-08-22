# Tender Intelligence Agent

> A sanitized portfolio case study. Real tender records, internal criteria, credentials, and production automation are not published.

I automated a daily tender-monitoring workflow that had previously required manual searching and forwarding.

## The problem

Keyword searches produced a large, noisy set of notices. A person still had to inspect each result, judge business relevance, distinguish active tenders from advance notices, and identify strategically useful leads.

## What I built

- Batch retrieval using multiple keyword groups
- Agent-assisted second-pass relevance screening
- Business-rule classification into first- and second-priority leads
- Separation of tender notices and advance notices
- Special retention rules for strategically relevant issuers
- A human-in-the-loop calibration process for improving rules and prompts

## Workflow

```text
Tender sources → Keyword retrieval → Agent + business-rule filtering
               → Priority classification → Human review → Daily brief
```

## How the system improved

I repeatedly compared agent output with a manager's manual labels, identified false positives and missed cases, then refined the rules and prompts until the daily results became stable enough for routine use.

## Public portfolio scope

This repository documents the workflow and product decisions. A mock input/output example and sanitized report preview are planned.

