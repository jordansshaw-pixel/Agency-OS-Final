# 02 Property Research Examples

## Example 1: Buyer Property Link

Input:

> Buyer asked what we think about this Cherrywood listing.

Output:

- Research topic: Cherrywood listing
- Known facts: listing link if supplied, buyer context if supplied
- Missing: buyer priorities, budget, deal-breakers
- Source status: mark missing items as `source not provided`
- Handoff: send verified conversation points to `03_client_communication/`

## Example 2: Seller Pricing Prep

Input:

> Seller in Travis Heights wants to know if now is a good time to list.

Output:

- Research topic: Travis Heights seller market
- Risk flag: pricing
- Source status: comps and recent sales require provided or verified sources
- Human review required before sharing
- Handoff: send only reviewed, source-backed points to `03_client_communication/`

## Example 3: School Question

Input:

> Buyer asked whether this neighborhood has good schools.

Output:

- Research topic: school context
- Risk flag: school rating and fair housing sensitivity
- Output: source-based school information only, no subjective claims
- Recommended next action: provide source links and suggest buyer verify fit directly
- Human review required
