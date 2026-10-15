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

Q4 experiment evidence will also be added to this repository.
