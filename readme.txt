## Pilot Experiment

This project also accompanies a small real-world experiment to test whether families are willing to proactively review healthcare paperwork before a crisis occurs.

The goal of the pilot is to observe:
• demand for proactive document readiness
• common paperwork failure patterns
• operational friction points for families and staff

No private or identifying information is collected or published in this repository.

# Healthcare Document Readiness Analysis

A small exploratory healthcare operations project focused on one practical question:

**What kinds of paperwork failure create avoidable friction for families, staff, and care transitions?**

This project is not legal advice and does not analyze private patient records. It is a framework for studying common **document readiness failure modes** at a systems level.

## Project Goal

The purpose of this project is to model how healthcare paperwork problems can be categorized, tracked, and analyzed as operational failure points.

Examples of operational friction may include:

- missing documents when a decision is needed
- outdated or inaccessible documents
- authority mismatch between the person present and the person legally authorized
- repeated staff time spent clarifying the same issues
- delayed decisions, discharge, or coordination due to document confusion

## Why This Matters

In many settings, document issues are handled reactively.  
This project explores whether those issues can be made more visible earlier through simple classification, structured intake, and basic analytics.

The broader question:

**Can document readiness be treated as a measurable operations problem rather than a last-minute paperwork scramble?**

## Initial Failure Mode Framework

This first version uses a simple three-part model:

### 1. Missing Document
A needed document is not available when a care, discharge, placement, or decision event occurs.

### 2. Outdated / Inaccessible Document
A document exists, but it is old, unclear, unavailable, not present, not retrievable, or functionally unusable in the moment.

### 3. Authority Mismatch
A family member or participant is involved, but the legal authority, signer status, or decision authority does not align with the actual need.

## Sample Questions This Project Can Explore

- Which document failure type appears most often?
- Which settings appear most vulnerable to document confusion?
- Which event types trigger the highest rate of readiness failure?
- Which failure types create the most staff friction?
- Which issues look preventable upstream?

## Initial Dataset Structure

The starter dataset uses one row per event or observed case pattern.

Example fields:

- event_id
- care_setting
- trigger_event
- failure_type
- document_type
- decision_urgency
- authority_present
- authority_verified
- accessibility_issue
- staff_time_impact
- family_confusion_level
- downstream_delay
- preventable_upstream
- notes

## Current Status

This is an early exploratory project intended to demonstrate:

- business analysis thinking
- healthcare operations framing
- dataset design
- failure mode classification
- practical analytics structure

## Planned Next Steps

- Add a small synthetic sample dataset
- Create summary counts by failure type
- Visualize friction patterns across event types
- Explore a simple “document readiness risk score”
- Build a basic dashboard or notebook view

## Files

- `data/document_readiness_sample.csv` — starter synthetic dataset
- `docs/data_dictionary.md` — field definitions
- `analysis/initial_questions.md` — business questions and hypotheses
- `visuals/` — charts and screenshots
- `notebooks/` — exploratory analysis notebook

## Disclaimer

This repository uses synthetic / illustrative structures only and is intended for operational analysis and portfolio demonstration. It does not contain protected health information.