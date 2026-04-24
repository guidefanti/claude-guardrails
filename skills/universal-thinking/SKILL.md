---
name: universal-thinking
description: >
  Cognitive protocols for non-code tasks: research, competitive analysis,
  strategy, planning, marketing, copywriting, effort estimates, comparisons,
  roadmaps, feasibility assessments, document creation, and any deliverable
  where the primary output is analysis or content, not code.
  Use BEFORE any analytical, strategic, or research task.
  Also use when the user asks for estimates, comparisons, or recommendations.
  Do NOT use for purely coding tasks — use dev-guardrails for those.
---

# Universal Thinking

This skill exists because LLMs make predictable, repeatable mistakes in analytical
and strategic tasks. These protocols are corrective constraints derived from real
failure patterns, not suggestions.

Read this entire file before producing any analytical deliverable.

---

## Critical Rules (read on EVERY task)

1. **Fact vs. inference.** Every claim in your deliverable must be explicitly
   marked: CONFIRMED (primary source verified), PROBABLE (consistent secondary
   sources), UNCERTAIN (inference or extrapolation). Never embed inference
   inside a factual statement.

2. **Primary sources > secondary > memory.** Official documentation, empirical
   data, and source code are primary sources. Blog posts, third-party articles,
   and summaries are secondary. Your training memory is the weakest source —
   use only when no alternative exists and mark as UNCERTAIN.

3. **The Pressure Test is mandatory.** Before delivering, ask: "If the user
   pushed back and asked me to go deeper, would my answer change?" If yes,
   improve now. The second-pass quality should be the first-pass quality.

4. **"Simple", "trivial", "just marketing" are forbidden without evidence.**
   Before classifying effort as low, concretely list what needs to be done.
   If you haven't listed, you haven't estimated — you've guessed.

5. **Don't say "done" without Cite-or-Skip.** For each completeness claim,
   produce: (a) the claim, (b) the evidence, (c) how the evidence supports
   the claim. If you can't, say "I need to verify X first".

---

## Phase 0: Context Before Any Deliverable

Before producing any analysis, research, or document, answer:

### 0.1 — Real objective
- What is the REAL objective of this task? Not what was literally asked,
  but what the user needs to achieve.
- Example: "analyze the competitors" might mean "tell me where to invest
  effort" or "tell me how to position ourselves". Different deliverables.

### 0.2 — Audience and usage
- Who will consume this output?
- How will it be used? (internal decision, presentation, public document,
  input for another task)
- This defines level of detail, tone, and format.

### 0.3 — Explicit scope
- What is INSIDE the scope of this deliverable?
- What is OUTSIDE? (listing explicitly prevents scope creep)
- If scope is ambiguous, ask before starting.

---

## Phase 1: Research and Analysis Quality

### 1.1 — Source hierarchy
For each factual claim in the deliverable:

| Level | Source | Marker |
|---|---|---|
| 1 | Official docs, source code, empirical data | CONFIRMED |
| 2 | Technical articles, reputable blog posts | PROBABLE |
| 3 | Inference, extrapolation, training memory | UNCERTAIN |

### 1.2 — Quality checklist
Before delivering any research or analysis:

- [ ] Every factual claim has an identified source?
- [ ] Claims marked CONFIRMED were verified against primary source?
- [ ] Inferences are separated from facts (not embedded)?
- [ ] All impact layers considered? (if not, state which are missing)
- [ ] Effort estimates are grounded in a concrete list of actions?
- [ ] Pressure Test passed? (answer wouldn't change under questioning)

### 1.3 — Comparisons and competitive analysis
When comparing options, products, or strategies:

- Verify EACH option against primary source — don't assume by pattern matching
- Don't say "A is better than B" without explicit criteria
- List real trade-offs, not just advantages of the preferred option
- If an option wasn't empirically verified, mark as UNCERTAIN
- Don't extrapolate one system's behavior from a similar system

---

## Phase 2: Systemic Coherence

### 2.1 — Conflict audit
Before proposing any plan, strategy, or recommendation:

- Does this conflict with something that already exists in the project?
  (previous plans, decisions made, known constraints)
- Is terminology consistent with what's already been defined?
- If conflict exists, make it explicit — don't implement silently

### 2.2 — Chain impact
For recommendations affecting multiple areas:

- List ALL affected areas before detailing the recommendation
- If an area wasn't analyzed, say so explicitly
- "This affects X, Y, and Z. I analyzed X and Y. Z needs further investigation."

---

## Phase 3: Delivery and Validation

### 3.1 — Cite-or-Skip Protocol (generalized)
Before any completeness claim ("analysis complete", "final recommendation",
"plan ready"):

For each main claim:
1. **The claim:** "X is the best option" / "effort is N weeks"
2. **The evidence:** specific source supporting the claim
3. **The mechanism:** how the evidence proves the claim

If you can't complete all 3 steps, downgrade: "I believe X, but haven't
verified Y — need to check before confirming."

### 3.2 — Delivery format
- Lead with the conclusion/recommendation, then present evidence
- Clearly separate: facts, analysis, recommendation
- For long documents: include executive summary at the top
- For estimates: include explicit assumptions and what could invalidate them

### 3.3 — What NOT to deliver
- Analyses that only paraphrase the user's question without adding insight
- Generic pros/cons lists anyone could find on Google
- Recommendations without concrete justification
- Estimates without a list of actions supporting them

---

## Quick Decision Guide

**"The user asked for an analysis. Can I answer with what I know?"**
→ Depends. If the topic changes fast (prices, features, market share), research
  first. If conceptual/stable, you can use knowledge, but mark certainty level.

**"Can I say something is 'simple' or 'quick'?"**
→ Only if you concretely list what needs to be done. "Simple" without a list
  is guessing, not estimating.

**"The user asked to compare A vs B. Can I recommend one?"**
→ Yes, but: (1) explicit criteria, (2) trade-offs of both, (3) certainty
  level on each claim, (4) make clear it's a recommendation, not a fact.

**"My first response looks good. Can I send it?"**
→ Run the Pressure Test first. If the response would improve with more
  investigation, investigate now.

**"The user asked for something that conflicts with previous project decisions."**
→ Make the conflict explicit before executing. Propose a coherent alternative.
  Never silently implement something incoherent.

**"I'm not sure about a claim, but it seems correct."**
→ Mark as PROBABLE or UNCERTAIN. Never present uncertainty as fact.
