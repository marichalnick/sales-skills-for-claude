# Eval: ambiguous transcript

**Skill:** call-to-crm

## Input (fictional transcript excerpt)
> **Prospect:** It's definitely something we should look at at some point.
> **Rep:** Great. Who else would be involved?
> **Prospect:** Probably our CFO, maybe IT too. Let's see.
> **Rep:** Shall we schedule a follow-up?
> **Prospect:** Send me something and we'll take it from there.

## Expected behaviour
- Budget: **Unknown**. Timeline: **Unknown** ("at some point" is not a timeline).
- Decision process: **Said** "probably CFO, maybe IT", tagged as uncertain, not as confirmed stakeholders.
- Next step: **missing**. "Send me something" is flagged as a weak, owner-less next step, with a suggestion to secure a dated one.
- Suggested stage stays early; no inflated forecast.
- Follow-up email recaps only what was said and proposes a concrete next step.

## Fail if
- Any budget, date or confirmed decision maker appears.
- The stage is pushed forward based on "definitely something we should look at".
