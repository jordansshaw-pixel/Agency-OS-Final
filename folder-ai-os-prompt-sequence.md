# Prompt Sequence For Building A Folder-Based AI Operating System

Date: 2026-05-14

Source question:

> Before building a folder-based AI operating system for a real estate agency, what are the core design questions we must answer to make sure the system can route work, preserve context, define specialist responsibilities, carry handoffs, enforce human review, support scheduled follow-up, and prove it works for a new agent?

## How To Use This

Use these prompts in order. The goal is not to get one large answer. The goal is to force the design process through the same sequence a strong operator would use:

1. Extract facts.
2. Identify gaps.
3. Make explicit assumptions.
4. Define operating rules.
5. Design handoffs.
6. Define specialist responsibilities.
7. Build proof scenarios.
8. Review against the assignment criteria.
9. Prepare the final submission.

The most important rule: do not build the folder system until the README-level operating decisions and handoff protocol are clear.

## Prompt 1: Extract Facts From The Brief

Purpose: Separate what the brief actually says from what still needs to be designed.

Prompt:

```text
Read the real estate agency client brief and assignment text.

Extract only the factual requirements. Do not invent solutions yet.

Organize the output into:
1. Client profile
2. Business problems
3. Required folder architecture
4. Required files in each folder
5. Required specialist responsibilities
6. Root README requirements
7. Handoff requirements
8. Success criteria
9. Submission requirements
10. Gaps not answered by the brief

For every item, label it as:
- explicitly stated
- strongly implied
- missing

Do not write the operating system yet.
```

Expected output: A clean requirements map.

Feeds next prompt by giving a verified source layer before assumptions are made.

Prevents: Building from vibes, overfitting to imagined client needs, or missing hard assignment requirements.

## Prompt 2: Map The Core Design Questions

Purpose: Determine which operating-system decisions are already answered, partially answered, or missing.

Prompt:

```text
Using only the extracted requirements, evaluate the core design questions for the folder-based AI operating system.

Questions to evaluate:
1. What work types should the system handle?
2. What request types route to each specialist?
3. What information must be captured at intake?
4. Where does context live?
5. Who are the specialists?
6. What is each specialist responsible for?
7. What is each specialist not allowed to do?
8. What does a proper handoff include?
9. Where is human review required?
10. How are scheduled follow-ups, reminders, deadlines, and overdue items tracked?
11. What counts as done for each workflow?
12. How are unclear, risky, urgent, or incomplete requests escalated?
13. How do we prove a new agent can use the system in one day?

For each question, provide:
- status: answered, partially answered, or missing
- evidence from the brief
- what still must be decided
- why the decision matters

Do not write the final files yet.
```

Expected output: A decision coverage table.

Feeds next prompt by showing where prototype assumptions are needed.

Prevents: Treating unanswered areas as if they were already solved.

## Prompt 3: Create Prototype Assumptions

Purpose: Move forward without Diana while staying honest about what is known and assumed.

Prompt:

```text
For every missing or partially answered design question, create a reasonable prototype assumption for a competition-ready folder-based AI operating system.

For each item, provide:
- what the brief says
- what is unknown
- the prototype assumption
- why the assumption is reasonable for a boutique Austin real estate team
- where the assumption should appear: README.md, identity.md, rules.md, examples.md, or handoff.md

Constraints:
- Do not wait for Diana's input.
- Make every assumption explicit.
- Separate known-from-brief from assumed-for-prototype.
- The final system must be teachable in one week and usable by a new agent in one day.

Do not write the folder files yet.
```

Expected output: An assumptions register.

Feeds next prompt by giving the README concrete decisions to define.

Prevents: Hidden assumptions, vague README language, and client-specific overclaims.

## Prompt 4: Define README-Ready Operating Rules

Purpose: Turn the design assumptions into the operating manual for the whole system.

Prompt:

```text
Using the requirements map and assumptions register, create the root README.md operating structure for Diana's agency-system.

The README must define:
1. What the system does
2. What work enters the system
3. Where every request starts
4. The required folder architecture
5. What each specialist owns
6. What each specialist does not own
7. How routing decisions are made
8. Required intake fields before routing
9. The standard handoff packet
10. Human review gates
11. Scheduled follow-up and deadline handling
12. Definition of done for each workflow
13. Exception and escalation rules
14. Day-one onboarding test for a new agent
15. Setup needed before dropping the folder into a Claude project

Write the README as an operating manual for a stranger, not as a marketing overview.

Do not create specialist files yet.
```

Expected output: A README outline or full README draft.

Feeds next prompt by establishing the system-wide rules every specialist must follow.

Prevents: A README that introduces the project but does not actually operate it.

## Prompt 5: Design The Handoff Packet

Purpose: Solve the assignment's most important requirement: explicit handoffs.

Prompt:

```text
Design the handoff protocol for Diana's multi-folder real estate agency operating system.

First define the universal handoff packet. It must include:
- source folder
- destination folder
- request type
- client or prospect name
- agent owner
- current status
- known facts
- missing information
- client goal
- urgency and deadline
- recommended next action
- required human review
- risk flags
- follow-up date or deadline
- output produced
- links or file references

Then define the specific handoff rules for:
1. 00_orchestrator to 01_lead_qualifier
2. 00_orchestrator to 02_property_research
3. 00_orchestrator to 03_client_communication
4. 00_orchestrator to 04_transaction_coordinator
5. 01_lead_qualifier to 03_client_communication
6. 02_property_research to 03_client_communication
7. 04_transaction_coordinator to 03_client_communication
8. Any specialist back to 00_orchestrator

For each handoff, define:
- when it happens
- what the receiving folder needs
- what the sending folder must produce
- what human review is required
- what counts as complete
- what happens if information is missing

Output this as reusable content for the root README and each folder's handoff.md.
```

Expected output: The standard packet plus folder-to-folder handoff rules.

Feeds next prompt by giving every specialist the same operating language.

Prevents: Hand-waved handoffs, context loss, unclear next steps, and specialist confusion.

## Prompt 6: Define Specialist Responsibilities And Boundaries

Purpose: Make each folder narrow enough to be useful and safe.

Prompt:

```text
Using the README operating rules and handoff protocol, define each specialist folder.

Folders:
- 00_orchestrator
- 01_lead_qualifier
- 02_property_research
- 03_client_communication
- 04_transaction_coordinator

For each folder, produce:
1. identity.md content
2. rules.md content
3. examples.md content with two or three realistic examples
4. handoff.md content

Each specialist must clearly define:
- who it is
- what it owns
- what it does not own
- what it always does
- what it never does
- what context it requires before acting
- what it produces
- when it escalates
- when human review is required
- how it hands work to another folder

Keep specialists narrow. Do not let one folder quietly become the whole system.
```

Expected output: Draft contents for every required specialist file.

Feeds next prompt by creating a system that can be tested with real scenarios.

Prevents: Overlapping responsibilities, skipped review, and folders that are just generic prompts.

## Prompt 7: Add Follow-Up, Deadline, And Review Mechanics

Purpose: Make the system operational instead of just descriptive.

Prompt:

```text
Strengthen the operating system with explicit follow-up, deadline, and human-review mechanics.

Define:
1. How follow-up actions are captured
2. How transaction deadlines are captured
3. How overdue items are surfaced
4. Who owns follow-up after each specialist output
5. Which outputs require Diana or agent review before use
6. Which outputs are internal-only
7. Which outputs may become client-facing drafts
8. Which actions the AI system must never take without a human

Then update the README-level rules and the relevant specialist handoff rules.

Assume this is still a folder-based system, not new software.
```

Expected output: Review and follow-up rules that can be inserted into README.md and handoff.md files.

Feeds next prompt by ensuring scenarios test the most operational parts of the system.

Prevents: A static folder demo that cannot carry deadlines, follow-ups, or human approvals.

## Prompt 8: Create New-Agent Proof Scenarios

Purpose: Prove the system can be used by Diana's newest agent in one day.

Prompt:

```text
Create realistic proof scenarios for Diana's newest agent to test the folder-based operating system.

Create at least three scenarios:
1. New buyer or seller lead with missing information
2. Property or neighborhood research request
3. Active transaction issue with deadline pressure

For each scenario, show:
- incoming request
- starting folder
- routing decision
- intake fields captured
- handoff packet
- specialist output
- human review gate
- follow-up or deadline record
- definition of done
- what the new agent should do next

The scenarios should prove whether a new agent can use the system without Diana explaining it over a call.
```

Expected output: Scenario tests and example walkthroughs.

Feeds next prompt by providing evidence for quality review.

Prevents: Claiming the system is usable without testing whether a new agent can actually run it.

## Prompt 9: Review Against The Assignment Criteria

Purpose: Catch weak architecture before finalizing the repo.

Prompt:

```text
Review the proposed folder-based AI operating system against the assignment criteria.

Score the system on:
1. Does the architecture make sense for a real estate team?
2. Are the handoff protocols actually defined?
3. Is the README good enough to onboard a stranger?
4. Did the design make real decisions instead of filling out a template?

Also check:
- unclear routing
- weak specialist boundaries
- missing intake fields
- missing handoff fields
- missing review gates
- missing follow-up or deadline tracking
- missing definition of done
- missing escalation rules
- places where Diana would still need to explain the system live

For every weakness, recommend an exact fix and where it belongs.
```

Expected output: A pre-submission quality review.

Feeds next prompt by identifying final changes before packaging.

Prevents: Submitting a system that looks complete but fails the actual judging criteria.

## Prompt 10: Prepare The Submission Writeup

Purpose: Produce the public-facing competition note after the system is built.

Prompt:

```text
Write the final 100-word submission comment for the Diana real estate agency operating system.

It must cover:
- what was built
- one design decision and why it matters
- one thing to add with another week

Make it specific to:
- Diana's four-person Austin real estate team
- the multi-folder ICM architecture
- the explicit handoff protocol
- new-agent onboarding

Keep it clear, practical, and competition-ready.
```

Expected output: A concise submission comment.

Prevents: A generic writeup that does not explain the design decision or why the system is usable.

## Optional Master Prompt

Use this only if you need one long-pass prompt. The sequenced prompts above will usually produce a cleaner result.

```text
You are designing a folder-based AI operating system for Diana, owner of a four-person boutique residential real estate team in Austin.

Start from the client brief and assignment text. Do not build immediately.

Work in this sequence:
1. Extract factual requirements from the brief.
2. Identify which operating-system design questions are answered, partially answered, or missing.
3. Create explicit prototype assumptions for missing decisions.
4. Define README-ready operating rules.
5. Design the universal handoff packet and folder-to-folder handoff rules.
6. Define specialist responsibilities, boundaries, review gates, and outputs.
7. Define scheduled follow-up, deadline, overdue, and human-review mechanics.
8. Create day-one proof scenarios for a new agent.
9. Review the system against the assignment criteria.
10. Draft the final 100-word submission writeup.

The required folders are:
- 00_orchestrator
- 01_lead_qualifier
- 02_property_research
- 03_client_communication
- 04_transaction_coordinator

Each folder must include:
- identity.md
- rules.md
- examples.md
- handoff.md

The root README must explain:
- the architecture
- the typical request flow
- onboarding for a new team member
- setup before use in a Claude project
- routing rules
- handoff packet rules
- human review gates
- follow-up and deadline handling
- definition of done
- escalation rules

Important constraints:
- Do not wait for Diana's input.
- Make assumptions explicit.
- Separate known-from-brief from assumed-for-prototype.
- The folder structure is the product.
- The system must be teachable in one week.
- A fifth agent should be operational in one day.
- Handoff quality is the main test.

Output the full design package in clearly labeled sections, with file-ready content where appropriate.
```

## Final Build Logic

The original question asked for the core design questions. The better instruction asks for the workflow that produces those questions, answers them, turns them into operating rules, and tests the result.

The efficient build path is:

```text
Brief facts -> design gaps -> prototype assumptions -> README rules -> handoff protocol -> specialist files -> proof scenarios -> quality review -> submission writeup
```

That sequence prevents the most common failure: building five folders that look complete but do not actually route work, preserve context, carry handoffs, enforce review, support follow-up, or prove usability for a new agent.
