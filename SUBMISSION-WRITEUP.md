# Submission Writeup

I built a folder-based AI operating system for Diana's four-person Austin real estate team. The system routes every request through one orchestrator, then hands work to specialists for lead qualification, property research, client communication, or transaction coordination. The main design decision was using one universal handoff packet across every folder, so context moves cleanly instead of staying in Diana's head or scattered Google Docs. I also added review gates, follow-up tracking, source rules, and deadline-source requirements so the system is usable by a new agent on day one. With another week, I'd add real team voice profiles and live case examples.

## Process Note

This repo was built with AI assistance. I started from my own original build, then compared it against five other public submissions to understand different approaches to routing, handoffs, persistence, review gates, and onboarding. From that comparison, I back-engineered a prompt sequence for designing a stronger folder-based AI operating system. I then worked through that sequence step by step: extracting requirements, identifying gaps, making assumptions explicit, defining README rules, designing handoffs, setting specialist boundaries, adding follow-up and review mechanics, testing new-agent scenarios, and reviewing against the judging criteria.

That process matters because the final repo was not generated from one broad prompt. It was rebuilt from a design method. The comparison phase exposed what made other systems stronger or weaker, and the prompt sequence forced the final build to answer the actual operating questions: where work starts, what each specialist owns, how context moves, when humans review, how deadlines are tracked, and whether a new agent can use the system without Diana explaining it live.

Repo: https://github.com/jordansshaw-pixel/Agency-OS-Final
