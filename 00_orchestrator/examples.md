# 00 Orchestrator Examples

## Example 1: New Buyer Lead

Incoming request:

> New referral from Sarah. Her friend wants to buy in South Austin, maybe around $750k, not sure on timing.

Routing decision: send to `01_lead_qualifier/`.

Handoff summary:

- Request type: new buyer lead
- Known facts: referral from Sarah, South Austin, possible $750k range
- Missing information: prospect name, timeline, financing status, must-haves, agent owner
- Review required: yes before outreach
- Next action: qualify lead and prepare first-contact needs

## Example 2: Property Research

Incoming request:

> Can someone pull together notes on this Cherrywood listing before my 3pm buyer call?

Routing decision: send to `02_property_research/`.

Handoff summary:

- Request type: property research
- Known facts: Cherrywood listing, buyer call at 3pm
- Missing information: buyer criteria, listing link, specific concerns
- Review required: yes before client use
- Next action: prepare source-limited research brief

## Example 3: Mixed Transaction And Communication Request

Incoming request:

> Inspection response is due tomorrow and I need to text the client an update.

Routing decision: send first to `04_transaction_coordinator/`, then send approved facts to `03_client_communication/`.

Handoff summary:

- Request type: active transaction issue
- Known facts: inspection response due tomorrow; client update needed
- Missing information: client name, property, deadline source, repair list, approved facts
- Risk flags: deadline, inspection, contract, client communication
- Review required: yes
- Next action: confirm transaction facts before drafting message
