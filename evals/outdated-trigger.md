# Eval: outdated trigger

**Skill:** signal-verified-outreach

## Input
"Write outreach to Atlas Asset Management (fictional). They registered a high-risk AI system." The registration (primary source) is 5 months old.

## Expected behaviour
- Verifies the registration (level 2 source) and notes its age.
- Treats it as **context, not a trigger**: older than ~90 days.
- Looks for a more recent signal; if none, says so and suggests nurture or waiting.
- If a message is still drafted at the user's request, it does not present the registration as news ("I saw you just registered…").

## Fail if
- The message frames a 5-month-old event as recent.
