---
name: discovery-call-prep
description: Prepares a one-page brief for a discovery or first sales call. Researches the company and attendees, forms pain hypotheses, and builds a call plan with opening, SPIN/GAP questions, likely objections and a clear next step to ask for. Use when the user says "prep me for my call with X", "discovery prep", "I have a meeting with [company]", "what should I ask [prospect]", or shares a meeting invite and wants to be ready.
---

# Discovery Call Prep

Goal: walk into the call knowing **what might be true**, **what you need to find out**, and **what next step you will ask for**. Not a company encyclopedia.

## Workflow

### 1. Collect the inputs
- Company, attendees (names, titles), meeting length, how the meeting came about (inbound, outbound, referral).
- What the user sells, and what a good outcome of this call looks like.
- Any prior notes, emails or CRM history the user can share.
- If an `ACCOUNT-<name>.md` from `signal-verified-outreach` exists, start from it: the triggers there are already verified.

### 2. Research, briefly and verifiably
- **Company:** what they do, size, recent news (last ~6 months) relevant to the offer. Use primary sources and cite them.
- **Attendees:** role, tenure, what they likely own, anything they have said publicly that relates.
- Mark anything uncertain as uncertain. Do not fill gaps with guesses.

### 3. Form 2 to 3 pain hypotheses
For each one:

```
Hypothesis:  <what might be true>
Evidence:    <verified fact + source>
Don't assume: <budget, owner, timing… whatever the evidence doesn't prove>
Question:    "<how to test it>"
Strong signal if: <what answer would confirm it>
```

These are things to **test**, not to state.

### 4. Build the call plan

**Opening (first 2 minutes)**
- Thank, confirm time, propose an agenda: "I'd like to understand your situation first, then share briefly how we work, and agree together whether a next step makes sense. OK?"

**Questions**: a control panel, not an essay
- **3 must-ask** questions (tied to your hypotheses)
- **3 optional** questions (if time allows)
- **1 disqualifying** question (what answer would mean this is not a fit?)
- **1 next-step** question

Draw them from:
- *Situation:* how things work today.
- *Problem:* where it breaks or slows down.
- *Implication:* what that costs (time, money, risk, growth).
- *Need-payoff:* what solving it would be worth.
- *Decision:* who else is involved, how they decide, timing, budget process.

Tie every question to a hypothesis. Avoid questions the research already answers.

**Likely objections** (2 to 3) with a short response each, using: acknowledge → clarify → reframe → advance.

**Next step to ask for**
A specific, dated step: a second call with another stakeholder, a demo with the technical evaluator, a workshop. Never end on "I'll send some info".

### 5. Qualification checklist
Map what is known and unknown before the call (MEDDICC):

| | Known | To find out |
|---|---|---|
| Metrics | | |
| Economic buyer | | |
| Decision criteria | | |
| Decision process | | |
| Identify pain | | |
| Champion | | |
| Competition | | |

## Output
One page, in this order: 30-second summary, attendees, hypotheses, call plan (opening, questions, objections, next step), MEDDICC table, sources.
Keep it scannable: the user reads it five minutes before the call.

After the call, `call-to-crm` can use this brief to check which hypotheses were confirmed and which MEDDICC gaps were closed.
