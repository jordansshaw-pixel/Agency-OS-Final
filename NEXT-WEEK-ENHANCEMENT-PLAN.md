# If We Had Another Week

## Purpose

This plan describes what I would build next to make Diana's folder-based AI operating system more durable, easier to install, and easier to prove in real team use.

The current system is strong as a competition-ready folder OS: it has one front door, five required specialists, a universal handoff packet, review gates, follow-up tracking, source rules, and deadline-source requirements.

With another week, I would not add more generic prompts. I would build the operating layer around the system so it can hold real work over time.

## 1. Add Case Files For Real Work

The biggest upgrade would be a `case-files/` or `workflows/` folder where every lead, research request, or transaction gets its own working record.

Each case would include:

```text
status.md
action_register.md
audit_log.md
outputs/
```

Why this matters:

The current system moves work through handoff packets. That is enough for a clear prototype, but real agency work needs persistence. Diana's team should be able to reopen a lead or deal days later and see the current status, past decisions, next action, and specialist outputs without hunting through Slack or memory.

## 2. Add Agent Voice Profiles

The next upgrade would be a `voice-profiles/` folder with one short profile per agent.

Each profile would capture:

```text
Agent name:
Preferred greeting:
Tone:
Typical sentence length:
Phrases to use:
Phrases to avoid:
How this agent handles bad news:
Review preferences:
```

Why this matters:

`03_client_communication/` can already draft safely, but stronger voice profiles would make the drafts sound like Diana's team instead of a generic assistant. This is especially important for referral leads, inspection issues, financing delays, and disappointed clients.

## 3. Add A Team Setup Kit

I would add a small setup kit so Diana can install the OS into her real team without needing a live explanation.

The setup kit would include worksheets for:

- Team members and ownership rules
- Existing Google Docs and what each one is used for
- Preferred buyer intake questions
- Preferred seller intake questions
- Transaction checklist references
- Brokerage review rules
- Preferred property research sources
- Where follow-ups and deadlines live after review

Why this matters:

The system is intentionally not new software. A setup kit would help Diana connect the folder OS to the team's existing habits, documents, and review process.

## 4. Turn Proof Scenarios Into Runnable Tests

I would add a `proof-scenarios/` folder with realistic test inputs and expected outputs.

The first scenarios should be:

1. New buyer lead with missing budget and timeline
2. Property research request before a client call
3. Inspection response due in 48 hours
4. Mixed request that includes transaction risk and client communication

Each test would show:

```text
Incoming request
Starting folder
Expected route
Required handoff fields
Expected specialist output
Review gate
Follow-up or deadline record
Definition of done
```

Why this matters:

The assignment's practical test is whether Diana's newest agent can use the repo in one day. Runnable proof scenarios would make that claim visible instead of theoretical.

## 5. Add A Lightweight Nurture Layer

The current system handles new leads and follow-ups, but not a full long-term nurture process.

I would add a simple nurture rule set for leads that are not ready yet:

```text
Lead status:
Nurture reason:
Next check-in date:
Owner:
Suggested message:
What would make this lead active:
```

Why this matters:

Many real estate leads are not ready immediately. A nurture layer would prevent warm leads from disappearing after the first response.

## 6. Add A Quality Review Checklist

I would add one lightweight review checklist before anything client-facing leaves the system.

The checklist would confirm:

- Facts are supplied or sourced
- Missing facts are marked
- No legal advice is included
- No pricing or offer strategy is overstated
- Research source limits are named
- Deadline sources are named
- Agent voice has been reviewed
- Human owner approved the final version

Why this matters:

The current system already requires human review. A checklist would make that review repeatable and easier for a new agent to follow.

## Best One-Week Priority

If I had to choose only one improvement, I would build the case file system and proof scenarios first.

That combination would move the repo from a strong competition artifact to a more realistic operating system. Case files would preserve live work over time. Proof scenarios would show Diana that a new agent can actually run the system without needing her to explain the process on a call.

## Summary

The next week should focus on persistence and proof.

The current repo answers the design problem: how work starts, where it routes, what each specialist owns, how handoffs carry context, when humans review, and how follow-ups and deadlines are tracked.

The next version should prove the system under real operating conditions by adding case files, agent voice profiles, setup worksheets, proof scenarios, nurture rules, and a repeatable quality review checklist.
