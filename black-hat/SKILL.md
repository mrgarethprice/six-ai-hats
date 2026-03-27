---
name: black-hat
description: >-
  Critically analyse documents for unfounded claims, untested assumptions,
  circular reasoning, and gaps between narrative and reality. Use when the user
  asks for a "black hat" analysis, critique, stress-test, or
  wants to poke holes in strategy documents, ADRs, PRFAQs, vision pieces,
  implementation plans, technical proposals, or any document that makes claims
  about the future or presents aspirations as facts. Part of the Six Thinking
  Hats framework (see thinking-hats skill for the full sequence).
---

# Black Hat — Risks, Critique & Unfounded Claims

Perform a rigorous, adversarial analysis of a document. The goal is not to
dismiss the document but to surface where it makes claims it hasn't earned —
assertions presented as facts, hypotheses presented as proven, aspirations
presented as current state, and examples that sound compelling but wouldn't
survive contact with reality.

## When to Use

- Strategy / vision documents
- Architecture Decision Records (ADRs)
- PRFAQs and press-release-style proposals
- Implementation plans (especially LLM-generated ones, which are fluent but often uncritical)
- Technical proposals and RFCs
- Pitch decks and investor narratives
- Any document where someone is making a case for something

This is the deep-dive critical analysis hat. For a balanced multi-perspective
analysis (facts, feelings, risks, benefits, alternatives), use the
`thinking-hats` skill to run all six hats in sequence.

## Process

### Step 1: Read the full document

Read it once to understand the overall argument before critiquing individual claims.

### Step 2: Identify the structural claims

Extract the document's core thesis and supporting claims. Map the dependency chain: which claims depend on which other claims being true? This reveals which assumptions are load-bearing — if they fall, everything above them falls too.

### Step 3: Apply the analysis lenses

Work through each lens below. Not every lens applies to every document — skip those that don't apply, but check each one.

#### Lens 1: Present tense vs. future state
Does the document describe something that exists today or something the author wants to build? Flag anywhere the language uses present tense ("our platform does X") for capabilities that are aspirational, planned, or partially built. This is the single most common form of strategic dishonesty — describing a roadmap as a current asset.

For LLM-generated plans: these are especially prone to this because the model confidently describes implementation steps as if the architecture or dependencies already exist.

#### Lens 2: Unfounded uniqueness claims
Does the document claim the organisation has something no competitor has? Probe: is this actually unique, or do competitors have comparable capabilities that are dismissed without evidence? "No one else has X" is a strong claim that requires strong evidence.

#### Lens 3: Untested assumptions
Identify claims that are presented as self-evident but are actually hypotheses. Common patterns:
- "Users will want X" (have you asked them?)
- "This will reduce churn" (have you measured the correlation?)
- "These systems will integrate" (what's the engineering cost?)
- "This is technically feasible" (has anyone prototyped it?)

#### Lens 4: The analogy problem
If the document draws an analogy to another company or model (e.g., "we're the Uber of X"), examine where the analogy breaks down. Analogies are persuasive but hide structural differences between the source and target domains.

#### Lens 5: Speculative examples
Look for scenarios presented as obvious benefits. For each one, ask: has this been tested? Is the causal mechanism proven? Could a simpler approach achieve the same result? Would the target audience actually value this?

#### Lens 6: Frameworks that can't say no
If the document introduces a decision framework or evaluation criteria, check whether every item on the roadmap conveniently passes. A useful framework should be able to reject things. If it approves everything, it's not a filter — it's a rubber stamp.

#### Lens 7: Missing economics
Does the document address whether the proposed approach is economically viable? Strategy documents often describe what could be built without asking whether the target customer will pay enough to fund it. Plans often describe what could be built without costing the engineering time.

#### Lens 8: Circular reasoning
Watch for arguments where the conclusion is baked into the premise:
- "We need X because our strategy requires X" (but who validated the strategy?)
- "This is the right architecture because it supports our vision" (but does the vision reflect reality?)

#### Lens 9: Static competitors
Does the document assume competitors will stand still while the organisation executes its plan? Any competitive advantage described should be evaluated against the assumption that well-funded competitors are also moving.

#### Lens 10: Integration and execution risk
Does the document hand-wave over implementation difficulty? "Once we integrate X, Y becomes possible" — how hard is the integration? How long will it take? What does it cost? Who is doing it? Documents that depend on hard technical work happening should address whether that work is funded, staffed, and scheduled.

For LLM-generated implementation plans: check whether the plan assumes libraries, APIs, or patterns exist as described. LLMs confidently reference tools and approaches that may be outdated, deprecated, or imaginary.

### Step 4: Produce the output

Write a markdown document with the following structure.

#### Executive summary
A concise (1–2 paragraphs) assessment of the document's overall credibility, naming the most material weaknesses. Lead with the most important finding. Use a numbered list of findings, ordered by severity. Each finding gets one bolded sentence followed by 1–2 sentences of explanation. This summary should be sufficient for a reader who won't read the full analysis.

#### Detailed analysis
One numbered section per finding, matching the numbering in the executive summary. Each section includes:
- **The claim** — what the document says (quote or paraphrase)
- **The problem** — why this claim is unfounded, untested, or misleading
- **What's missing** — what evidence, analysis, or acknowledgement would make the claim credible

Where a finding relates to or deepens another finding, add cross-references between sections.

#### Risk summary table
A table with columns: Risk | Severity | Status. Severity uses: Critical, High, Medium-High, Medium, Low-Medium, Low. Status uses short phrases like: Untested, Unfounded, Unmodelled, Misrepresented, Structural flaw, Under-acknowledged.

#### Recommendations
Numbered, actionable recommendations. Each starts with a bolded imperative verb phrase. Order by priority — the most important remediation steps first.

## Tone

Be direct and specific, not snarky. The goal is to make the document better, not to mock it. Acknowledge what is genuinely sound before dissecting what isn't. Where claims are directionally correct but overstated, say so — the analysis should distinguish between "this is wrong" and "this is unproven."

Avoid hedging language that softens findings into uselessness. "This might be worth considering" is not useful. "This claim has no supporting evidence and the document should either provide it or remove the claim" is useful.

## Handling additional context from the user

The user may provide additional context about the real state of affairs that contradicts the document's claims (e.g., "these systems don't actually talk to each other"). Treat this as high-priority signal: it likely identifies the most important gap between narrative and reality. Integrate it as a primary finding, not a footnote, and trace its implications through all dependent claims in the document.
