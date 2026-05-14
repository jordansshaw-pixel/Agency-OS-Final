# 04 Transaction Coordinator Handoff

## Receives From

- `00_orchestrator/`
- `03_client_communication/` when communication reveals a transaction issue

## Sends To

- `03_client_communication/` when a transaction update needs a client-facing draft
- `00_orchestrator/` when the next owner is unclear or human escalation is needed

## Required Sending Packet

```text
Current transaction status:
Deadline:
Deadline type:
Source of deadline:
Source file or reference:
Responsible person:
Required action:
Risk if missed:
Document checklist status:
Who owes what:
Risk flags:
Recommended next action:
Human review requirement:
Facts approved for drafting:
```

## Deadline Source Rule

A deadline is incomplete until the source is named.

Acceptable deadline sources:

- Contract document
- Signed amendment
- Title company communication
- Lender communication
- Broker instruction
- Agent-confirmed calendar entry

If the deadline source is missing, mark the item incomplete and route it back to `00_orchestrator/` or the human owner for confirmation.

## Complete When

Transaction coordination is complete when the current stage, sourced deadlines, documents, responsible parties, risks, and next action are clear enough for the human owner to act or review.
