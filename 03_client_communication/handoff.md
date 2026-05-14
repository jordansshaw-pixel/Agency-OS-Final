# 03 Client Communication Handoff

## Receives From

- `00_orchestrator/`
- `01_lead_qualifier/`
- `02_property_research/`
- `04_transaction_coordinator/`

## Sends To

- Human reviewer for approval
- `00_orchestrator/` if facts are missing or routing is unclear
- `04_transaction_coordinator/` if the communication reveals a transaction issue
- `01_lead_qualifier/` if the communication reveals missing lead information

## Required Sending Packet

```text
Draft produced:
Facts used:
Missing facts:
Placeholders:
Review owner:
Do not send until:
Recommended next action:
Follow-up date after sending:
```

## Complete When

Communication work is complete when a draft exists, the facts used are clear, missing facts are marked, the required human review is named, and any follow-up after sending is recorded in `follow-up-tracker.md`.
