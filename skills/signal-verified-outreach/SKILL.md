---
name: signal-verified-outreach
description: Drafts cold outreach (email or LinkedIn) from a verified trigger. Checks every claimed fact against a primary source before it reaches the copy, picks the right stakeholder, avoids repeating earlier touches, and writes one short message with one question and one low-friction call to action. Use when the user asks to write a cold email, prospecting message, outreach for a company or person, "who should I contact at X", or a batch of outreach for a list of accounts.
---

# Signal-Verified Outreach

Turn "write outreach to this company" into a message that is **true, timely and relevant**, the way a careful SDR would do it with unlimited time to check every fact.

## The one rule: verify before you hook

AI-assisted outreach fails in a specific way: it invents a convincing trigger. A regulation that doesn't exist, a date nobody announced, a press release paraphrased backwards. One fabricated fact in a message to a senior buyer costs more credibility than a hundred good messages earn.

So: **no claim reaches the copy unless you opened the primary source and read the sentence it rests on.** A label like "verified" in a spreadsheet or CRM is not a substitute.

## Workflow

### 1. Understand the ask
Get: target company (and person, if given), what the user sells, and any prior contact. If the offer or ICP is unclear, ask once, briefly.

### 2. Find candidate triggers
Look for dated, specific events from the last ~90 days:

| Trigger | Why it matters |
|---|---|
| Leadership change (new CISO, CRO, CMO…) | First 90 days = priorities are being reset |
| Funding, acquisition, expansion | Budget and pressure to scale |
| Relevant hiring | Ownership and budget are being created |
| Product or technology launch / rollout | New risks and new processes |
| Regulation that applies to them | Pressure, but not proof of intent |
| Something the person posted or said | The strongest signal: their own words |
| Tech change (new tool adopted, vendor dropped) | A process is being rebuilt |
| Public frustration with a current vendor (reviews, posts) | Openness to alternatives |

A standing fact ("they are a big bank") is context, not a trigger.

**Timing windows (rules of thumb, tune them with your own data):**
- New leader: roughly weeks 2 to 8 in the role. Too early they are onboarding, too late priorities are set.
- Funding or acquisition: the first few weeks after the announcement.
- Job posting: while the role is open, and again shortly after someone is hired.
- Anything older than ~90 days is context, not a trigger.

**Stacked signals beat single signals.** Two independent, verified signals on the same account (for example a new CISO *and* a relevant job posting) are a much stronger reason to reach out than one. Rank accounts with stacked signals first, and say which signals stack.

### 3. Verify each trigger

**Source hierarchy**

| Level | Source | Use in copy? |
|---|---|---|
| 1 | Company's own release, filing, careers page | Yes |
| 2 | Regulator or government source | Yes |
| 3 | The person's own post or statement | Yes, quote carefully |
| 4 | Reputable journalism | With care; prefer finding level 1 to 3 |
| 5 | Databases, aggregators | Research only |
| 6 | Search snippets, blogs, SEO content | Never stated as fact |

For every trigger you plan to use:
- Open the **primary source**: the company's own site or press release, the regulator's own page, the person's own post.
- Check the **specific claim**, not just the topic. Read the surrounding sentence.
- Watch for two failure modes:
  - **The claim does not exist.** A secondary source added a date, number or name that the primary source does not contain.
  - **The claim is backwards.** "We solved X" paraphrased as "they struggle with X".
- Note the age. Signals decay fast: weeks, not months.

If nothing survives verification, say so. Do not patch a broken trigger. A real but older fact, framed honestly, beats a fake new one.

### 4. Pick the person
Choose the role that **owns the problem the trigger creates**, not the highest title.
- Ask: who feels the pain, who owns the risk, who controls budget, who evaluates technically, who could block?
- Prefer someone not contacted recently. Never repeat an angle already used with the same person.
- If the user has relationship context (a past call, an intro offer), that outranks everything else.

### 5. Reconcile with prior touches
What was already said and asked? If there is nothing genuinely new, recommend waiting instead of sending a reworded repeat.

### 6. Match the message to the level
- **Executives (above the line):** business outcome, risk, timing. Shorter. One question about priorities.
- **Practitioners (below the line):** the day-to-day problem, the workflow, the tool. One question about how they handle it today.
Same trigger, different angle. If you contact both at one account, never send them the same message.

### 7. Write the message
Follow `references/style-guide.md`. In short:
- 50 to 120 words. One idea. One question. One call to action.
- Open with *them* (the trigger), not with you or your company.
- State the hypothesis as a question, never as a fact about their situation.
- Low-friction CTA: a concrete slot or calendar link beats "can I have your number?".

### 8. Follow-ups (only if asked)
- Every follow-up adds **something new**: a different angle, a relevant resource, a new signal. Never "just bumping this".
- Typical rhythm: day 3 to 4, day 8 to 10, then a short, honest closing note ("I'll stop here; if timing changes, happy to talk").
- Switch channel once (email → LinkedIn or phone) before switching person.
- No guilt-trip break-up lines, no fake urgency.

### 9. Human approval gate
Before anything is sent, the user must check: names and titles, every factual claim, no unsupported social proof, the CTA, and whether the tone fits the relationship. Present the draft for approval; never imply it has been or will be sent automatically. Respect opt-outs: anyone who asked not to be contacted is excluded.

### 10. Output
For each message, first an evidence table:

| Type | Claim | Source (level) | Date | Use |
|---|---|---|---|---|
| Fact | … | URL (1) | … | Safe to mention |
| Inference | … | derived | | Ask as a question |
| Unknown | … | none | | Discovery gap |

Then:

```
Account / person / role
Trigger: <what happened> — <primary source URL> — <age>
Why this person: <one line>
Hypothesis: <the pain you think this creates>

<subject line, if email>
<message>

Confidence: high / medium / low, and why
```

If the user works across sessions, also save a short `ACCOUNT-<name>.md` with the verified triggers, sources and chosen stakeholder, so `discovery-call-prep` and `call-to-crm` can build on it instead of re-researching.

If several accounts were requested, start with a short ranked table (account, trigger, age, person, confidence) and list the ones you **dropped** with the reason.

## When something doesn't add up
If verification knocks out the trigger a message was built on, tell the user plainly what broke and rebuild from what is verified, or recommend not sending. Fewer true messages beat more false ones.
