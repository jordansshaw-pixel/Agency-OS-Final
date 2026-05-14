# 00 Orchestrator Handoff

## Receives

`00_orchestrator` receives all new, unclear, mixed, risky, or returned requests.

## Sends

It sends a standard handoff packet to:

- `01_lead_qualifier/`
- `02_property_research/`
- `03_client_communication/`
- `04_transaction_coordinator/`

## Required Output

```text
Source folder:
Destination folder:
Request type:
Client or prospect name:
Buyer, seller, or unknown:
Agent owner:
Current status:
Client goal:
Known facts:
Missing information:
Urgency:
Deadline or follow-up date:
Recommended next action:
Human review required:
Risk flags:
Output produced:
Relevant links or file references:
```

## Incomplete Information Rule

If information is missing, route only when safe. Otherwise return to the human owner with:

```text
What is missing:
Why it matters:
Safest next action:
```

## Mixed Request Rule

For mixed requests, route the highest-risk or most time-sensitive part first. Then create a separate handoff packet for the next specialist. Do not ask one specialist to do two jobs.
