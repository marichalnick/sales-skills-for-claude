# Sales Skills for Claude

**Sales workflows that think before they send.**

Evidence-based sales workflows for Claude: verified signals, hypothesis-led discovery and CRM-safe handoffs.

`5 skills` · `4 eval cases` · `Claude Code & Claude.ai` · `MIT`

*Illustrative session:*

```
> prep me for my call with Helios tomorrow

  ✓ Loaded ACCOUNT-Helios.md (Fact: AI Governance Lead job posting, careers page, 10 days old)
  ✓ 3 hypotheses, each with evidence and what not to assume
  ✓ 3 must-ask questions, 1 disqualifying question, 1 next-step question
  ⚠ Unknown: budget, decision process. Marked as gaps, not guessed.
```

It is not a prompt library. It is a small, guardrailed workflow system: verify facts, keep hypotheses as questions, preserve unknowns, and hand off cleanly.

## The skills

| Skill | Use it when | What you get |
|---|---|---|
| [signal-verified-outreach](.claude/skills/signal-verified-outreach/SKILL.md) | "Write outreach to X" | A short message built on a trigger checked against its primary source, sent to the person who owns the problem |
| [discovery-call-prep](.claude/skills/discovery-call-prep/SKILL.md) | "Prep me for my call with X" | A one-page control panel: evidence-linked hypotheses, prioritised questions, objections, MEDDICC gaps |
| [objection-handler](.claude/skills/objection-handler/SKILL.md) | "They said it's too expensive" | What's behind it, a clarifying question, spoken and written responses, and when the honest answer is "not a fit" |
| [call-to-crm](.claude/skills/call-to-crm/SKILL.md) | "Log this call" + transcript | CRM update, MEDDICC, AE handoff and follow-up, every line tagged Said / Interpreted / Unknown |
| [sales-router](.claude/skills/sales-router/SKILL.md) | "What's next with X?" | Routes to the right skill and reuses verified context across the deal |

## Try it in 60 seconds

**Claude Code**
```bash
git clone https://github.com/marichalnick/sales-skills-for-claude
cd sales-skills-for-claude
claude
> prep me for a discovery call with a fictional insurer that just posted an AI Governance Lead job
```
Skills in `.claude/skills/` are picked up when you run Claude Code in this folder. To use them everywhere, copy them to your personal skills folder:
```bash
cp -R .claude/skills/* ~/.claude/skills/
```

**Claude.ai / desktop:** zip one skill folder (for example `.claude/skills/discovery-call-prep`) and upload it under *Settings → Capabilities → Skills*.

*Install paths and menus can change. If a step doesn't match, check the [Claude docs on skills](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview).*

## The deal flow

```
signal-verified-outreach  →  ACCOUNT-<name>.md   facts with sources, inferences, unknowns
        ↓
discovery-call-prep       →  PREP-<name>.md      hypotheses, questions, MEDDICC gaps
        ↓
     [the call]  ←  objection-handler
        ↓
call-to-crm               →  CRM update, handoff, follow-up
```

Verified context is persisted in structured Markdown files and reused by downstream skills, so facts are checked once instead of being re-researched or re-invented at every step. There is no database or CRM integration: the files are the state. When files conflict, the router flags the conflict instead of picking one.

## Design principles

1. **Evidence before assertion.** Every claim is a *Fact* (with a source level), an *Inference* (asked as a question) or *Unknown* (a discovery gap).
2. **Source hierarchy.** The company, a regulator or the person's own words may support a claim. Blogs, snippets and aggregators are research only.
3. **Hypothesis-led discovery.** Each question is tied to a hypothesis, its evidence, and what would confirm it.
4. **Human approval gates.** Explicit checkpoints before anything is sent or logged.
5. **Fit over persuasion.** An objection that reveals a real lack of fit is a reason to stop, not to push.

## How this is different

Many sales prompt libraries optimise for volume and impressive-looking output. These skills optimise for being right:

- **No scores without evidence.** If budget wasn't stated, it's *Unknown*, not "22/25".
- **No invented social proof.** No "a peer at a Tier-1 bank just…" or "[mutual connection] suggested I reach out" unless it is real.
- **No benchmarks without a source.** Timing windows are labelled as rules of thumb to tune with your own data.
- **Failure-aware.** The examples and evals show what the skills refuse to do, not only what they produce.

## Examples and evals

- [Outreach with a dropped, unverifiable trigger](examples/signal-verified-outreach.md)
- [Handling "we already have tools for that"](examples/objection-handler.md)
- [Eval cases with expected behaviour and a scoring rubric](evals/README.md): fabricated trigger, outdated trigger, sparse account, ambiguous transcript.

The evals are run by hand: give Claude the input, compare against the expected behaviour, score with the rubric.

## Status

A prototype of workflows I use in enterprise B2B business development, generalised. Not yet benchmarked: the evals are the first step toward measuring it. Next: more adversarial cases, and a structured (JSON) format for account context.

## Data and privacy

All companies, people, triggers and outcomes in this repository are fictional. No company-specific playbooks, customer data or internal workflows are included. Don't commit real prospect data, transcripts or CRM exports (the `.gitignore` excludes the usual ones).

These workflows support judgment. They do not guarantee factual accuracy, legal compliance (including GDPR) or sales outcomes.

## Related

- [GTM Signal Engine](https://github.com/marichalnick/gtm-signal-engine): the same verify, score, draft, measure logic in Python.
- [Pipeline Math](https://marichalnick.github.io/pipeline-math/): work backwards from a target to the meetings you need.

## License
MIT
