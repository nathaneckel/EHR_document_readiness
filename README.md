# Document Readiness Before Crisis

Healthcare transitions and care decisions often require specific documents to be available and **legally valid at the exact moment a clinical or administrative decision must be made**.

When documents are **missing, outdated, inaccessible, or legally mismatched with the patient present,** staff and families may experience **delays, confusion, unexpected expenses, insurance complications, and repeated administrative work.**

In this repository, these events are treated as **document-readiness failures.**

These failures are rarely studied as a system problem, but they appear repeatedly during hospital admissions, assisted living transitions, and other healthcare decision points.

These problems are usually handled reactively. This project explores whether document readiness failures can be classified, tracked, and analyzed as operational events rather than treated as isolated paperwork problems.

The goal of this repository is to build a simple dataset structure that models document-readiness failure patterns and enables exploratory analysis of when and how they occur.

This repository **contains only synthetic or illustrative data** and **does not include protected health information.**

## Failure-Type Framework

This project uses three primary document failure categories.

#### 1. Missing Document

A required document is not available at the moment it is needed.

Examples:

healthcare proxy not available at admission

DNR or MOLST form unavailable during urgent care decisions

identification or insurance documentation missing during intake

Operational impact may include delays, additional staff time, and unresolved decision authority.

#### 2. Outdated or Inaccessible Document

A document exists but cannot be used effectively at the moment it is required.

Examples:

document stored at home while care occurs elsewhere

outdated advance directive

records stored in inaccessible systems

paper copies not available during care transitions

Operational impact often includes staff searching for documentation or requesting additional copies.

#### 3. Authority Mismatch

The individual present during a decision event may not have the legal authority required for the specific decision.

Examples:

family member present but not the legal healthcare proxy

financial authorization required but different authority holder

multiple family members unsure who has decision authority

Operational impact may include decision delays or additional verification steps.

## Dataset Structure

The dataset models document-readiness events as rows in a table, where each row represents a single operational situation in which paperwork issues appeared.

Example fields include:

Field	Description
event_id	Unique identifier for each event
care_setting	Setting where the issue occurred (hospital, rehab, hospice, assisted living, etc.)
trigger_event	Operational moment where the issue appeared (admission, discharge, transfer, consent, etc.)
failure_type	Category of document readiness failure
document_type	Type of document involved (POA, MOLST, insurance card, etc.)
decision_urgency	Urgency level of the situation
authority_present	Whether a decision-maker was present
authority_verified	Whether authority could be confirmed
accessibility_issue	Whether the document existed but could not be accessed
staff_time_impact	Estimated operational burden
family_confusion_level	Observed confusion level among participants
downstream_delay	Whether the issue caused a delay
preventable_upstream	Whether the issue appears preventable before the event
notes	Additional context about the situation

This structure allows exploration of patterns across different care settings and event types.

### Observation Files

The observation files in the `observations/` directory represent individual document-readiness events.

The first few observations currently contain **synthetic example cases used to illustrate the structure of the dataset**. These will be replaced or supplemented with real-world observations over time.

## Example Analysis Questions

This dataset structure allows several types of exploratory questions.

Examples include:

#### Failure Pattern Questions

Which failure type occurs most frequently?

Which document types appear most vulnerable to failure?

Which care settings experience the most document readiness problems?

#### Operational Impact Questions

Which failure types correlate with the highest staff time burden?

Which events most often lead to downstream delays?

Which scenarios create the highest family confusion levels?

#### Preventability Questions

Which document failures appear most preventable upstream?

Are certain trigger events predictable points where readiness failures emerge?

Do certain document types consistently cause problems during transitions?
