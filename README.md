# Daily Reflection Tree

## Overview
This project is a deterministic reflection tool that guides users through an end-of-day reflection using a structured decision tree.

## Structure
- reflection-tree.csv → Tree data
- write-up.md → Design explanation
- transcripts/ → Example user journeys

## How it works
- Fixed questions (no free text)
- Deterministic branching using decision nodes
- Tracks signals across 3 axes:
  - Locus (Victim vs Victor)
  - Orientation (Entitlement vs Contribution)
  - Radius (Self vs Others)

## Key Constraint
No LLM is used at runtime. The system is fully deterministic.

## Design Intent
This system is designed to feel like a guided internal dialogue rather than a survey. Each branch adapts tone and framing based on the user’s mindset, while remaining fully deterministic.

## Author
Nisha Manuskare
