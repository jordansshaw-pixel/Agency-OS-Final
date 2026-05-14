# Diana Real Estate Team AI Operating System

This is a folder-based AI operating system for Diana's four-person boutique residential real estate team in Austin. It routes work, preserves context, defines specialist responsibilities, carries handoffs, enforces human review, and tracks follow-up without becoming another software platform.

The folders are the system.

## Start Here: Run Any Request In Five Steps

1. Start in `00_orchestrator/`.
2. Fill the intake fields.
3. Pick one destination folder.
4. Send the handoff packet.
5. Do not use client-facing output until the named human reviewer approves it.

## Architecture

```text
Agency-OS-Final/
  README.md
  follow-up-tracker.md
  00_orchestrator/
  01_lead_qualifier/
  02_property_research/
  03_client_communication/
  04_transaction_coordinator/
```

Each specialist folder includes:

```text
identity.md  - who the specialist is, what it owns, and what it does not own
rules.md     - how the specialist operates
examples.md  - realistic examples of the specialist in action
handoff.md   - what the specialist receives, produces, and passes forward
```

## What This System Handles

Use this system for new buyer or seller leads, property and neighborhood research, client communication drafts, and active transaction coordination.

Do not use it to send messages, approve legal or pricing decisions, interpret contracts as final, or replace Diana's professional judgment.

## Required Intake Fields

Every request starts with this intake block:

```text
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
Requested output:
Human review required:
Risk flags:
Relevant links or file references:
```

## Routing Rules

Route to `01_lead_qualifier/` for new prospects, buyer or seller intent, budget, timeline, location preferences, constraints, readiness, and first follow-up needs.

Route to `02_property_research/` for specific properties, neighborhoods, comps, recent sales, school-source notes, market context, and research for buyer or seller conversations.

Route to `03_client_communication/` for email drafts, text drafts, follow-ups, rewrites, client explanations, missed showings, competing offers, inspection issues, and financing delays.

Route to `04_transaction_coordinator/` for active deals, contract deadlines, document checklists, who owes what, timeline risk, inspections, financing, appraisals, amendments, and closing steps.

Keep the work in `00_orchestrator/` when the request is unclear, risky, missing a client or deadline, or could belong to more than one specialist.

For mixed requests, route the highest-risk or most time-sensitive part first. Then create a separate handoff packet for the next specialist. Do not ask one specialist to do two jobs.

Priority order:

1. Urgent transaction deadline or contract risk
2. Client-facing communication that could create confusion or commitment
3. Lead response with time-sensitive follow-up
4. Property research needed for a scheduled client conversation
5. Routine clarification or setup work

## Standard Handoff Packet

Every specialist uses the same handoff packet:

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

The handoff packet is the system's working memory. It replaces "Diana remembers what happened" with a repeatable written record.

## Human Review Gates

Human review is required before:

- Any client-facing message is sent
- Any pricing guidance is used
- Any offer strategy is shared
- Any contract, amendment, inspection, financing, appraisal, or closing issue is acted on
- Any legal or compliance-sensitive language is used
- Any deadline-sensitive action is taken
- Any message goes to a broker, lender, title company, inspector, or opposing agent
- Any output includes uncertain or incomplete facts

The AI may draft, organize, summarize, and flag risk. It may not approve, send, commit, or decide on behalf of the team.

## Follow-Up And Deadline Rules

Every output must answer three questions before it is complete:

1. Is there a follow-up or deadline?
2. Who owns the next action?
3. Does a human need to review before anything is used?

Every specialist output with a follow-up or deadline must create or update a row in `follow-up-tracker.md`.

If no owner is known, the owner becomes `Diana until assigned`.

Use this follow-up format:

```text
Follow-up needed:
Follow-up owner:
Follow-up date:
Follow-up reason:
Next action:
Risk if missed:
```

Use this deadline format for active transactions:

```text
Deadline:
Deadline type:
Source of deadline:
Source file or reference:
Responsible person:
Required action:
Risk if missed:
Human review required:
```

A transaction deadline is incomplete until the source is named. Acceptable deadline sources include contract document, signed amendment, title company communication, lender communication, broker instruction, or agent-confirmed calendar entry.

## Definitions Of Done

Orchestration is done when the request is classified, missing information is named, one destination folder is selected, a handoff packet is created, and human review or escalation is flagged when needed.

Lead qualification is done when intent, buyer/seller status, budget or price range, timeline, location, constraints, readiness, next action, owner, and follow-up date are captured or marked missing.

Property research is done when the research question is clear, verified facts are separated from source gaps, unsupported claims are removed, open questions are listed, and human review needs are flagged.

Client communication is done when a draft exists, facts used are clear, missing facts are marked, voice needs are stated, and a human reviewer is named.

Transaction coordination is done when the current stage, sourced deadlines, documents, responsible parties, risks, and next action are clear enough for the human owner to act or review.

## Agent Voice Setup

Before using client communication drafts, add an agent voice note:

```text
Agent name:
Preferred greeting:
Formal or casual:
Typical sentence length:
Words or phrases to use:
Words or phrases to avoid:
How the agent handles bad news:
```

If no agent voice note is provided, `03_client_communication/` may draft in a clear, neutral, professional tone, but must mark the draft as needing voice review before sending.

## Day-One Onboarding Test

A new agent should be able to complete these three test runs on day one:

1. Route a new buyer lead with missing budget and timeline.
2. Request a property research brief for a buyer conversation.
3. Handle an active transaction issue with a deadline in the next 48 hours.

For each test, the new agent should start in `00_orchestrator/`, fill the intake fields, route to one specialist, read the output, identify the review gate, record the follow-up or deadline, and explain what counts as done.

If the new agent cannot complete those tests without Diana explaining the system live, the README or handoff rules need to be clearer.

## Setup Before Claude Use

Before using this with Diana's real team, add each agent's name and voice note, preferred buyer and seller intake questions, links to the three existing Google Docs, preferred transaction checklist references, local research source links, brokerage or compliance rules, and the team's preferred calendar or CRM destination for follow-ups after review.
