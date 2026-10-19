---
name: sales-router
description: Entry point for sales work. Use when the user asks what to do next with a prospect or account, or wants to prepare, follow up, qualify, handle an objection or log a sales call without naming a specific skill. Routes a request to the right skill (signal-verified-outreach, discovery-call-prep, objection-handler, call-to-crm) and chains them across a deal, from first touch to CRM update.
---

# Sales Router

Pick the right workflow, and carry context from one step to the next.

## Routing

| The user wants… | Use |
|---|---|
| To contact a company or person, a cold email, a batch of outreach, a follow-up | `signal-verified-outreach` |
| To prepare a call or meeting | `discovery-call-prep` |
| To answer pushback, live or written | `objection-handler` |
| To process a call: transcript, notes, recap, CRM, handoff | `call-to-crm` |

If the request fits two, do them in deal order: outreach → prep → objection → CRM.
If it fits none, help directly and say which skill would be closest.

## The deal flow

```
signal-verified-outreach  →  ACCOUNT-<name>.md   (verified triggers, stakeholder)
        ↓
discovery-call-prep       →  PREP-<name>.md      (hypotheses, questions, MEDDICC gaps)
        ↓
     [the call]  ←  objection-handler when pushback comes up
        ↓
call-to-crm               →  CRM update, handoff, follow-up email
```

Each step reads the previous file if it exists, so facts are verified once and reused, not re-researched or re-invented.

## "What should I do next with [account]?"
Look at what exists for that account and answer with one concrete next action:
- No verified trigger yet → research and verify one, or recommend waiting.
- Outreach sent, no reply → a follow-up with something new, or a different stakeholder.
- Meeting booked → prep brief.
- Call done, notes available → CRM update and follow-up.
- Gaps in MEDDICC → which question to ask, and to whom.

## Context resolution protocol
1. Look for `ACCOUNT-<name>.md` and `PREP-<name>.md` in the working folder.
2. Load only facts marked **Fact** with a source. Treat **Inference** as a hypothesis, never as a fact.
3. Re-check the age of every trigger. Older than ~90 days: context, not a reason to reach out.
4. If two files disagree, do not silently pick one: show the conflict and ask.
5. Keep unknowns as unknowns. Never fill a gap to make a file look complete.
6. Write new facts back only after verifying them or after the user confirms them.
7. No file found: start fresh and say so.

## Shared rules
1. Verify before you claim. Unknown is an acceptable answer.
2. Hypotheses are questions, not statements about the prospect.
3. A human approves anything that leaves the building.
