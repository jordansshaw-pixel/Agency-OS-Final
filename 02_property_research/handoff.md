# 02 Property Research Handoff

## Receives From

- `00_orchestrator/`
- `01_lead_qualifier/`

## Sends To

- `03_client_communication/` when research needs a client-facing draft
- `00_orchestrator/` when the research question is unclear or risky

## Required Sending Packet

```text
Short research summary:
Source status:
  Provided and usable:
  Missing:
  Needs human verification:
Supplied facts:
Open questions:
Source limitations:
Client conversation angles:
Claims to avoid:
Review needs:
```

## Output Classification

Every research output must mark one:

```text
Internal-only:
May become client-facing after review:
Needs more source confirmation:
```

## Complete When

Research is complete when the agent can understand the useful supplied facts, the limits of those facts, what not to claim, and what conversation the research supports.
