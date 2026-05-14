# 01 Lead Qualifier Examples

## Example 1: Referral Buyer With Missing Timeline

Input:

> Sarah referred a buyer looking in South Austin around $750k.

Output:

- Buyer lead
- Known: referral source, South Austin, possible $750k budget
- Missing: name, timeline, financing, must-haves, agent owner
- Next action: draft warm first-contact message asking for missing details
- Handoff: send to `03_client_communication/`

## Example 2: Seller Lead

Input:

> Past client may sell in Travis Heights this summer. Wants to know what their house could list for.

Output:

- Seller lead
- Known: past client, Travis Heights, possible summer timeline
- Missing: property address, motivation, desired timing, property condition
- Risk flag: pricing
- Next action: collect seller details, then route to `02_property_research/` for source-based context
- Human review required before price guidance

## Example 3: Online Lead With No Details

Input:

> Zillow inquiry came in. Just says, "I want to see this home."

Output:

- Buyer lead
- Known: source is Zillow inquiry, wants showing
- Missing: name, listing, timing, representation status, financing
- Next action: draft clarification message
- Handoff: send to `03_client_communication/`
