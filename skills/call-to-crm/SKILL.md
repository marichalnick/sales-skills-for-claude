---
name: call-to-crm
description: Turns a sales call transcript or rough notes into a structured CRM update, a MEDDICC summary with gaps, a handoff note for the account executive and a short follow-up email. Never invents facts that are not in the notes. Use when the user pastes a transcript or call notes and asks to "log this", "summarise the call", "write the recap", "update the CRM", "prepare the handoff", or "draft the follow-up".
---

# Call → CRM

Turn a messy call into four clean outputs, using **only what was actually said**.

## No-invention list
Never infer, only record when explicitly said: **budget, authority, timeline, pain severity, competitor, buying intent, next-step owner.** If it wasn't said, it is **Unknown**.

## Rules
- Every field is filled from the transcript or notes, or marked **unknown**. Never infer a budget, a decision maker or a date that wasn't stated.
- Quote the prospect's own words for pain and impact when possible. Their words are stronger than a paraphrase.
- Tag every line as **Said** (they said it, with a quote where possible), **Interpreted** (your read, labelled) or **Unknown** (not discussed). An interpretation must never reach the CRM as a fact.

## Workflow

### 1. Extract
- Attendees and roles.
- Current situation, pain points (with quotes), impact, desired outcome.
- Decision process, other stakeholders, timing, budget signals.
- Objections raised and how they were left.
- Agreed next steps, owners, dates.

If a prep brief from `discovery-call-prep` exists, compare: which hypotheses were confirmed, rejected or not tested?

### 2. Score qualification (MEDDICC)
For each letter: what we know, the evidence (quote or note), and what is still missing.
End with the **top 3 gaps** to close in the next conversation.

### 3. Write the outputs

**A. CRM update**
```
Stage: <suggested stage + why>
Next step: <action> — owner — date
Pain (in their words): "<quote>"
Stakeholders: <name, role, stance if known>
Risks: <what could stall this>
```

**B. MEDDICC table** with known / evidence / missing.

**C. Handoff note for the AE**: account, contact and role, problem confirmed (quote), business impact, urgency, decision process, current solution, other stakeholders, objections, commitments made, next step, unknowns, recommended follow-up. Each item tagged Said / Interpreted / Unknown.

**D. Follow-up email to the prospect** (under 120 words): thank them, recap their situation in their words, confirm the next step and date. No new pitch.

## Human approval gate
The user reviews the CRM update and follow-up email before anything is logged or sent.

## Quality check
- [ ] No field contains information that isn't in the notes.
- [ ] Next step has an owner and a date, or is flagged as missing.
- [ ] Follow-up email matches what was actually agreed.
