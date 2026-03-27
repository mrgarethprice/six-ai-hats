# Six AI Hats

AI-assisted thinking skills based on Edward de Bono's **Six Thinking Hats** — a framework for structured, parallel thinking. The core idea is simple: instead of trying to think about facts, feelings, risks, benefits, and alternatives all at once (which humans do badly), you separate them into distinct modes and think in one mode at a time.

De Bono's insight was that most bad decisions come from muddled thinking — optimism tangled with wishful thinking, criticism confused with analysis, gut feelings suppressed because they can't be justified yet. The hats force discipline: when you're wearing the Black Hat, you critique. When you're wearing the Yellow Hat, you find value. You don't do both at once.

These skills bring that discipline to AI-assisted analysis of documents, proposals, strategies, and ideas.

## The Hats

| Hat | Skill | Mode | Ask for it when you want… |
|-----|-------|------|--------------------------|
| White | `white-hat` | Facts & Information | A fact-check, data audit, or separation of what's known vs. assumed |
| Red | `red-hat` | Feelings & Intuition | A gut-check — honest emotional reactions without justification |
| Black | `black-hat` | Risks & Critique | A stress-test of claims, assumptions, and reasoning |
| Yellow | `yellow-hat` | Benefits & Value | A steelman — what's genuinely good and why, with rigour |
| Green | `green-hat` | Alternatives & Ideas | Different approaches, reframings, and experiments to try |
| Blue | `blue-hat` | Process & Synthesis | A decision framework, synthesis, and concrete next actions |

## Usage

### Full six-hat analysis

Ask for a complete multi-perspective analysis and all six hats run in sequence:

> "Run six hats on this document"
> "Give me a thinking hats analysis of this proposal"
> "Analyse this from all angles"

The sequence is deliberate: Blue (framing) → White (facts) → Red (feelings) → Black (risks) → Yellow (value) → Green (alternatives) → Blue (synthesis). Each hat builds on the ones before it.

### Individual hat deep-dives

Use a single hat when you want depth in one mode of thinking:

> "White hat this RFC" — fact-check it, separate claims from evidence
> "Red hat this strategy doc" — what's your gut reaction?
> "Black hat this implementation plan" — where are the holes?
> "Yellow hat this idea" — steelman it, find the genuine upside
> "Green hat this proposal" — what else could we do?
> "Blue hat this discussion" — synthesise and recommend

Individual hats produce deeper output than they do in the full sequence, where each hat is condensed to keep the total analysis manageable.

### Partial combinations

Ask for any subset:

> "Give me black and yellow on this" — risks and value, with a synthesis
> "Run white and red hats" — facts and feelings

When running a subset, skipped hats are noted and a brief Blue Hat synthesis is always included.

### Providing context

The analysis gets sharper when you provide ground truth the document might not reflect:

> "Black hat this architecture doc — note that the data layer they describe doesn't actually exist yet"
> "Six hats on this strategy, keeping in mind we've already tried approach B and it failed"

User-supplied context threads through every hat as primary signal, not a footnote.

## Installation

Each hat is a standalone skill directory with a `SKILL.md` file. Install them into your AI tool's skills directory, or point your tool at this repository.

## Credit

Based on Edward de Bono's *Six Thinking Hats* (1985). The framework is adapted here for AI-assisted document analysis rather than group facilitation, but the core principle is the same: better thinking comes from thinking one way at a time.
