# 04 Transaction Coordinator Examples

## Example 1: Inspection Deadline Tomorrow

Input:

> Inspection response is due tomorrow and we need to know what is still missing.

Output:

- Current stage: inspection response
- Deadline: tomorrow
- Source of deadline: missing, must be confirmed
- Missing: repair list, inspection report, client approval status
- Risk flags: deadline, inspection, contract
- Recommended next action: gather missing documents and review with agent or Diana
- Communication needed: yes, after facts are confirmed

## Example 2: Financing Delay

Input:

> Lender says approval may slip by two days.

Output:

- Current stage: financing
- Risk flags: financing, deadline, client expectation
- Missing: affected contract deadline, lender details, contingency impact
- Recommended next action: human review before any client or seller-side update
- Handoff: send approved facts to `03_client_communication/`

## Example 3: Document Routing Question

Input:

> New agent asks where the amendment needs to go.

Output:

- Current stage: amendment or document routing
- Missing: client, property, amendment type, signed status, destination
- Risk flags: document, contract
- Recommended next action: collect document details and ask agent or Diana before routing
- Human review required
