# BUS5001 Assessment 3 – ESG AI Evidence

This repository contains experiment logs and supporting evidence for BUS5001 Assessment 3.

## Q3 – ESG Message Triage

An LLM-based ESG operational message triage approach was tested using three scenarios:

1. Critical environmental incident – ongoing water leak near electrical equipment.
2. Governance/procurement concern – supplier sustainability policy compliance.
3. Social/accessibility incident – blocked accessible entrance involving sensitive employee medical information.

The LLM classified each message by:
- issue category
- urgency
- sentiment
- follow-up requirement
- recommended team
- escalation reason
- data sensitivity risk
- summary

A transparent rule-based Python classifier was developed as a baseline comparison.

### Key findings
- The LLM and rule-based baseline agreed across the common structured fields for all three test scenarios.
- The LLM provided richer contextual reasoning but introduced some inconsistencies in recommended escalation teams.
- In the accessibility scenario, the model correctly identified high data sensitivity but repeated personal and medical information in its generated summary, demonstrating a privacy and data-minimisation risk.
- The rule-based approach was deterministic and transparent but depends heavily on predefined keywords and is less robust to unfamiliar phrasing.

## Repository contents

- `Q3_ESG_Message_Triage_RuleBased_Baseline.ipynb` – Python rule-based baseline and test scenarios.
- `Q3_Evidence/` – prompt screenshots, LLM outputs and baseline comparison evidence.

## Q4 – NotebookLM ESG Reporting Standards Experiment

NotebookLM was evaluated using three official sustainability-reporting sources: IFRS S1, IFRS S2 and GRI 1: Foundation 2021.

### Features tested
1. Source-grounded question answering and inline citations.
2. Recognition of unsupported claims and missing evidence.
3. Structured Data Table generation for framework comparison.
4. Executive briefing generation from selected sources.

### Key findings
- NotebookLM produced clear comparisons of IFRS S1, IFRS S2 and GRI 1 with inline source citations.
- When asked to identify the best framework for La Trobe University and provide an exact implementation cost, it correctly stated that the selected sources did not contain enough evidence rather than inventing an answer.
- The Data Table feature efficiently structured purpose, audience, scope, materiality perspective and disclosure focus across the three standards.
- Some generated fields, such as likely use in a briefing, were explicitly inferred and therefore require human verification rather than being treated as direct source evidence.
- The executive briefing feature produced concise, source-grounded synthesis suitable as a starting point for academic or organisational analysis.
- NotebookLM remains dependent on the quality and completeness of the uploaded sources, so human review and source verification remain necessary.

### Q4 Evidence
The `Q4_Evidence/` folder contains screenshots of the NotebookLM source setup, source-grounded responses, citation behaviour, limitation testing, structured comparison and executive briefing generation.
