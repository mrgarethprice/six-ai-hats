---
name: blue-hat
description: >-
  Synthesise findings from multiple perspectives into a clear recommendation.
  Frames the question, identifies key tensions, names the pivotal decision, and
  proposes concrete next actions. Use when the user asks for a "blue hat"
  analysis, wants a synthesis of different viewpoints, needs a decision
  framework, or wants to wrap up a discussion with a clear recommendation. Part
  of the Six Thinking Hats framework (see thinking-hats skill for the full
  sequence). Also useful standalone as a facilitation/synthesis tool after any
  complex discussion.
---

# Blue Hat — Process & Synthesis

The Blue Hat is the chair of the meeting. It frames the question at the
start and synthesises findings at the end. It doesn't contribute new
analysis — it orchestrates and concludes.

When used standalone, the Blue Hat acts as a synthesis tool: it takes
disparate inputs (prior analysis, discussion threads, conflicting views)
and produces a structured recommendation.

## Opening (used when framing an analysis)

### Step 1: Frame the question

State clearly in 3–5 sentences:

- What is being analysed? (the idea, document, proposal)
- What decision does this inform? (go/no-go, invest/don't, build/buy)
- What is the scope? (are we evaluating the whole thing or a specific
  aspect?)
- What constraints exist? (time, budget, team, prior commitments)
- What additional context has the user provided? (insider knowledge,
  ground truth that the document may not reflect)

### Step 2: Set the agenda

If orchestrating a full six-hat sequence, state the order and note any
hats that deserve extra attention based on the nature of the input:

- Fact-heavy proposal → emphasise White Hat
- Emotionally charged decision → emphasise Red Hat
- Idea with obvious risks → emphasise Black Hat
- Idea that's been heavily criticised → emphasise Yellow Hat
- Team that's stuck → emphasise Green Hat

---

## Closing (used when synthesising findings)

### Step 3: Identify key tensions

The most valuable synthesis is not a summary — it's a map of where the
hats disagreed and why. Common tensions:

- **White vs. Red** — the facts say one thing, but it feels wrong
  (or right). Why the disconnect?
- **Black vs. Yellow** — real risks vs. real value. Are the risks
  addressable, or do they invalidate the value?
- **Red vs. Green** — intuition points one direction, but alternatives
  exist that feel less exciting but might be sounder
- **White vs. the document** — the facts on the ground don't match
  what's being claimed

Name each tension explicitly. Don't resolve them prematurely — sometimes
the right output is "this tension exists and must be resolved before
proceeding."

### Step 4: Name the pivotal question

What is the single most important thing that, if resolved, would most
change the assessment? This is the question that unlocks the decision.

Good pivotal questions:
- "Can the data layer actually be unified within 12 months?"
- "Will customers pay 3× more for an integrated platform?"
- "Is the team capable of executing this alongside BAU?"

Bad pivotal questions:
- "Should we do this?" (too broad)
- "Is this a good idea?" (that's what the analysis answers)

### Step 5: Recommendation

Provide a clear directional recommendation. Use one of these framings:

- **Proceed** — the idea is sound, the risks are manageable, and the
  value justifies the investment
- **Proceed with conditions** — the idea has merit but specific things
  must be true or resolved first. Name each condition.
- **Rework** — the core insight is worth preserving but the approach
  needs significant changes. Name what to keep and what to change.
- **Stop** — the risks outweigh the benefits, the assumptions are
  unfounded, or there's a clearly better alternative. Name why and
  what to do instead.

Don't hedge with "it depends" without saying what it depends on.

### Step 6: Next actions

Not vague "think about this more" — concrete steps:

1. What should happen first? (and who does it, if context allows)
2. What decision needs to be made, and by when?
3. What information needs to be gathered before that decision?
4. What should explicitly *not* happen until the pivotal question
   is resolved?

## Output format

### Opening

```markdown
## Blue Hat — Framing

**Subject:** [what we're analysing]
**Decision:** [what this informs]
**Scope:** [boundaries of the analysis]
**Key context:** [user-provided ground truth or constraints]
```

### Closing

```markdown
## Blue Hat — Synthesis & Recommendation

### Key tensions
- **[Hat] vs. [Hat]:** [description of the tension]
- ...

### The pivotal question
[Single most important question to resolve]

### Recommendation
**[Proceed / Proceed with conditions / Rework / Stop]**

[2–4 sentences explaining the recommendation. Be direct.]

[If "proceed with conditions," list the conditions:]
- Condition 1: ...
- Condition 2: ...

### Next actions
1. [Concrete first step]
2. [Concrete second step]
3. [What to defer or avoid until the pivotal question is resolved]
```

## Tone

Authoritative, concise, decisive. The Blue Hat is a good chair closing
a productive meeting. It doesn't re-litigate what the other hats found —
it distils and decides. Every sentence should earn its place.

## Standalone use

When used without the other hats (e.g., "give me a blue hat on this
discussion"), treat any prior conversation, analysis, or documents as
the input that would normally come from the other hats. Synthesise
whatever exists into the closing format above. The Blue Hat doesn't
need the other hats to have been formally run — it can synthesise any
set of inputs into a structured recommendation.
