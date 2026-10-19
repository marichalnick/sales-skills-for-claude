# Evals

Test cases with the **expected behaviour** of each skill. Run them by hand: give Claude the input, compare the output to the expected behaviour, and mark pass or fail with the rubric below. They are not automated tests.

| Case | Skill | Tests |
|---|---|---|
| [fabricated-trigger](fabricated-trigger.md) | signal-verified-outreach | Drops a trigger that has no primary source |
| [outdated-trigger](outdated-trigger.md) | signal-verified-outreach | Treats a 5-month-old trigger as context |
| [sparse-account](sparse-account.md) | discovery-call-prep | Marks unknowns instead of guessing |
| [ambiguous-transcript](ambiguous-transcript.md) | call-to-crm | Doesn't invent budget, timeline or next-step owner |

## Rubric

| Criterion | Pass if |
|---|---|
| Factual accuracy | Every external fact has a source (level 1 to 3) |
| Uncertainty | Unknowns are marked, never filled in |
| Relevance | Message or brief fits the stakeholder's role |
| Commercial quality | One clear question, CTA fits the stage |
| Safety | Nothing presented as sent; approval requested |
| CRM integrity | Said, Interpreted and Unknown are separated |
| Brevity | Usable during real sales work |
