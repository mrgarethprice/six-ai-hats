---
name: thinking-hats
description: >-
  Run a full Six Thinking Hats analysis on an idea, proposal, or document.
  Applies six distinct modes of thinking — facts, feelings, risks, benefits,
  alternatives, and synthesis — in sequence to produce a balanced, structured
  assessment. Use when the user asks for "six hats," "thinking hats," "all
  angles," or wants a comprehensive multi-perspective analysis. For individual
  hat deep-dives, use the specific hat skill instead (white-hat, red-hat,
  black-hat, yellow-hat, green-hat, blue-hat).
---

# Six Thinking Hats — Full Analysis

Run all six hats in sequence to produce a comprehensive, balanced analysis.
Each hat is a distinct mode of thinking. The value is in the discipline of
keeping them separate — most analysis muddles facts with feelings, risks
with alternatives, and optimism with wishful thinking.

## The Hats

| Hat | Skill | Mode |
|-----|-------|------|
| Blue (opening) | `blue-hat` | Frame the question and set context |
| White | `white-hat` | Facts, data, information gaps |
| Red | `red-hat` | Feelings, intuition, gut reactions |
| Black | `black-hat` | Risks, critique, unfounded claims |
| Yellow | `yellow-hat` | Benefits, value, steelman |
| Green | `green-hat` | Alternatives, reframing, experiments |
| Blue (closing) | `blue-hat` | Synthesis, recommendation, next actions |

## Sequence

Run the hats in this order. The sequence is deliberate:

1. **Blue Hat (opening)** — frame what we're analysing, note any user-supplied
   context about the real state of affairs
2. **White Hat** — establish what's actually known before anyone starts
   interpreting. Condensed: focus on the most important facts, claims, and gaps
3. **Red Hat** — capture gut reactions while they're still honest, before
   logical analysis rationalises them away. Condensed: gut reaction, what feels
   right, what feels off, document tone
4. **Black Hat** — rigorous critique. In the sequenced version, use moderate
   depth: critical risks, unfounded claims, key assumptions to validate. For a
   deep-dive Black Hat, the `black-hat` skill provides the full 10-lens framework
5. **Yellow Hat** — constructive assessment with equal rigour. Condensed:
   structural strengths, top genuine benefits, the steelman
6. **Green Hat** — expand the solution space. Condensed: 2–3 alternatives, one
   reframing, minimum viable test for the original idea
7. **Blue Hat (closing)** — synthesise the tensions, name the pivotal question,
   give a clear recommendation with concrete next actions

## Output format

Write a single markdown document. Each hat gets a headed section (`## White Hat`,
`## Red Hat`, etc.) with Blue Hat appearing twice (`## Blue Hat — Framing` and
`## Blue Hat — Synthesis`).

Each hat section in the sequenced analysis should be roughly **half a page to
one page** — enough to capture the key insights without exhaustive detail. The
individual hat skills provide guidance on what to include in condensed vs.
deep-dive mode; use condensed mode here.

Total output should be approximately **4–8 pages** depending on the complexity
of the input.

## Key principles

- **Keep hats separate.** Don't critique in the White Hat section. Don't
  generate alternatives in the Black Hat section. The discipline of separation
  is the entire point.
- **Let hats build on each other.** The Red Hat can reference White Hat facts.
  The Black Hat should account for Red Hat intuitions. The Yellow Hat should
  acknowledge Black Hat risks. The Green Hat should address the weaknesses
  found by other hats.
- **Be honest, not balanced for its own sake.** If the idea is mostly bad, the
  Yellow Hat should say "the strongest thing here is X, but it's limited." If
  the idea is mostly good, the Black Hat should still name real risks but
  acknowledge they're manageable. Don't manufacture false symmetry.
- **User context is primary.** If the user has provided ground truth (e.g.,
  "these systems don't actually integrate"), it should thread through every hat
  — White (as a known fact), Red (how it makes you feel about the document's
  honesty), Black (as a critical gap), Yellow (value assessment must account for
  it), Green (alternatives should address the real situation).

## Handling partial requests

If the user asks for a subset of hats (e.g., "give me black and yellow"):
- Run only the requested hats at deep-dive depth (use the individual hat skill
  instructions, not the condensed versions)
- Always end with a brief Blue Hat synthesis, even if not explicitly requested
- Note which hats were skipped and what they might have contributed
