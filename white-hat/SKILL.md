---
name: white-hat
description: >-
  Analyse a document or idea purely through the lens of facts, data, and
  information gaps. Separates verified facts from unverified claims, identifies
  missing information, and flags data that may be fabricated or assumed. Use
  when the user asks for a "white hat" analysis, fact-check, data audit, or
  wants to know what's actually known vs. assumed. Part of the Six Thinking
  Hats framework (see thinking-hats skill for the full sequence).
---

# White Hat — Facts & Information

The White Hat is strictly empirical. No opinions, no judgments, no
interpretations. Its job is to sort what we know, what we think we know,
and what we don't know — and to be ruthlessly honest about which category
each piece of information falls into.

This is harder than it sounds. Most documents blur the line between fact
and claim. The White Hat's value is in making that line visible.

## Process

### Step 1: Extract factual claims

Read the document and extract every statement that presents itself as
factual. Include:

- Quantitative claims (numbers, metrics, dates, percentages)
- Qualitative facts (who, what, where — verifiable statements)
- Historical claims (things that allegedly happened)
- Technical claims (what systems do, how they work, what exists)

### Step 2: Classify each claim

Sort every extracted claim into one of three categories:

**Verified facts** — statements that are evidenced within the document
or are independently verifiable. Note the source of verification.

**Unverified claims** — statements presented as fact but without
supporting evidence. These aren't necessarily wrong — they're just
unearned. Common patterns:
- Statistics without sources
- "We have X" without demonstrating X exists
- Market claims without citations
- Technical capabilities described in present tense without proof
- Customer sentiment claims without research

**Contested or contradicted** — statements that conflict with other
information in the document, with user-supplied context, or with each
other. Internal contradictions are particularly revealing.

### Step 3: Map information gaps

Identify what the document *doesn't* say that a well-informed reader
would need to know. Categorise gaps by impact:

- **Decision-blocking gaps** — you cannot make a sound judgment without
  this information
- **Risk-obscuring gaps** — the absence of this information hides a
  potential problem
- **Context gaps** — missing background that would change interpretation

### Step 4: Assess data quality

For quantitative claims, consider:
- How old is the data? Is it current enough to be relevant?
- What's the sample size or scope? Is it representative?
- Is it presented with appropriate precision? (False precision — "we'll
  capture 23.7% of the market" — is a red flag)
- Could the same data support a different conclusion?

### Step 5: Flag LLM-generated content risks

If the document may have been generated or drafted with LLM assistance:
- Flag specific claims that have the hallmarks of confabulation:
  confident specificity without sources, plausible-sounding statistics,
  named frameworks or models that may not exist
- Note technical claims about libraries, APIs, or tools that may be
  outdated or fictional
- Watch for "authoritative hedging" — statements like "research shows"
  or "studies indicate" without citing which research or studies

## Output format

```markdown
## White Hat Analysis — Facts & Information

### Verified facts
- [statement] — *Source: [where this is evidenced]*
- ...

### Unverified claims
- [statement] — *Presented as fact but not evidenced. Would need: [what
  would verify this]*
- ...

### Contradictions
- [statement A] conflicts with [statement B] because [explanation]
- ...

### Information gaps

#### Decision-blocking
- [what we don't know that we must know]

#### Risk-obscuring
- [what we don't know that might hide a problem]

#### Context
- [background information that would change interpretation]

### Data quality concerns
- [issues with the quantitative claims]
```

## Tone

Clinical, precise, neutral. The White Hat is a researcher presenting
findings, not an advocate making a case. Use language like "the document
states" and "this is not evidenced" rather than "they claim" or "this is
wrong." The White Hat doesn't judge — it inventories.

## Standalone vs. sequenced use

**Standalone deep-dive:** Produce the full output above. Go into detail on
each category. This is the right mode when the user specifically asks for a
fact-check or data audit.

**As part of six-hat sequence:** Produce a condensed version — the most
important items in each category, not an exhaustive inventory. Focus on
facts and gaps that will matter most to the subsequent hats (especially
Black and Yellow). Aim for roughly one page of output.
