---
name: design-heuristics
description: >
  Evaluate any UI or visual design against Nielsen Norman Group's 10 usability heuristics
  and core visual design principles (contrast, spacing, hierarchy, alignment, color).
  Produces a scored, actionable audit report.

  Use this skill whenever the user asks to review, audit, or critique a design - including
  phrases like "check this design", "heuristics review", "NN heuristics", "Nielsen Norman",
  "design audit", "usability check", "evaluate this UI", "what's wrong with this screen",
  "review my mockup", "critique this interface", or "is this UX good". Works with Figma
  screenshots, code-rendered UIs, verbal descriptions, or any other design artifact.
  Trigger even if the user does not name Nielsen Norman explicitly - any design quality
  question is a good reason to use this skill.
---

# Design Heuristics Audit

Your job is to produce a rigorous, honest, and actionable design audit. The user wants
real insight, not reassurance - surface real issues with concrete evidence, then give
them something to act on.

## Step 1 - Understand what you are looking at

Before scoring anything, orient yourself:

- What is this product / screen / flow?
- Who are the likely users and what are they trying to do?
- What stage is this? (early sketch, high-fidelity mockup, live product?)

If it is unclear from context, ask one focused question. A single well-chosen question
is better than stalling.

If you have a screenshot or Figma link, look carefully at the actual UI before writing
anything. If you only have a verbal description, state that your audit is based on the
description and flag where seeing the real thing would change your confidence.

## Step 2 - Run the Nielsen Norman audit

Score each heuristic on a 1-5 scale:

| Score | Meaning |
|-------|---------|
| 5     | No issues - well implemented |
| 4     | Minor friction, not blocking |
| 3     | Noticeable problem, worth fixing soon |
| 2     | Significant violation, hurts usability |
| 1     | Critical failure - users will get stuck or confused |

For each heuristic, write:
- The score with an emoji indicator
- One or two sentences explaining the finding, citing a specific element if possible
- A concrete fix (what to change, not just "improve this")

Skip the fix if the score is 4 or 5.

### The 10 heuristics

**H1 - Visibility of system status**
Does the UI tell users what is happening? Loading states, progress indicators, confirmation
feedback, active/selected states - do they exist and are they timely?

**H2 - Match between system and real world**
Does the language match how users think? Are metaphors and icons recognizable? Does the
mental model of the interface match how the real-world task works?

**H3 - User control and freedom**
Can users undo mistakes, exit flows, go back, cancel, or recover from wrong paths easily?
Are escape hatches visible?

**H4 - Consistency and standards**
Are similar things treated the same way throughout the interface? Does it follow platform
conventions (button placement, icon meanings, interaction patterns)?

**H5 - Error prevention**
Does the design prevent errors before they happen? Constraints, confirmation dialogs for
destructive actions, inline validation, sensible defaults?

**H6 - Recognition rather than recall**
Can users see what they need without memorizing it? Are options visible, not hidden behind
memory-dependent commands? Is context preserved across steps?

**H7 - Flexibility and efficiency of use**
Are there shortcuts or accelerators for power users? Can experts work faster without
losing the simple path for novices? Keyboard shortcuts, bulk actions, saved preferences?

**H8 - Aesthetic and minimalist design**
Is every element earning its space? Is there visual noise, redundant information, or
elements that compete for attention without adding value?

**H9 - Help users recognize, diagnose, and recover from errors**
When errors happen, are messages in plain language? Do they explain the problem and tell
the user what to do next - not just "Error 403"?

**H10 - Help and documentation**
If users get stuck, is help findable? Is it task-oriented rather than feature-oriented?
Is documentation needed at all (a sign the UI itself may be unclear)?

## Step 3 - Visual design check

After the heuristics, run a quick pass on basic visual design quality.

Check and comment on:

- **Contrast** - Can text be read comfortably? WCAG AA: 4.5:1 for normal text, 3:1 for large.
- **Spacing consistency** - Does spacing follow a system (4/8px grid) or is it arbitrary?
- **Typography hierarchy** - Is there a clear visual hierarchy (H1 > H2 > body > caption)?
- **Alignment** - Are elements aligned to a grid? Mixed alignment without reason?
- **Proximity** - Are related elements grouped? Unrelated elements accidentally close?
- **Color usage** - Is color used consistently and purposefully? Color as sole differentiator?

## Step 4 - Write the report

Use this exact structure:

---

## Design Audit: [Screen/Product Name]

**Overall UX Score: X/10**
*(Average of 10 heuristic scores x 2. Round to one decimal.)*

### Summary
2-3 sentences on the overall state of the design. Be direct - is this solid work with
polish needed, a functional draft with structural issues, or something that needs rethinking?

---

### Top 3 Issues
The three most impactful problems. Lead with the one that costs users the most.

1. **[Issue name]** - [One sentence. Why it matters. What to do.]
2. **[Issue name]** - [One sentence. Why it matters. What to do.]
3. **[Issue name]** - [One sentence. Why it matters. What to do.]

---

### Quick Wins
Changes that are low-effort but high-impact. Things that could be done today.

- [Fix]
- [Fix]
- [Fix]

---

### Heuristics Breakdown

**H1 - Visibility of system status** [score emoji]
Score: X/5
[Finding + fix if score <= 3]

**H2 - Match between system and real world** [score emoji]
Score: X/5
[Finding + fix if score <= 3]

*(continue for all 10)*

---

### Visual Design

- **Contrast**: [finding]
- **Spacing**: [finding]
- **Typography**: [finding]
- **Alignment**: [finding]
- **Proximity**: [finding]
- **Color**: [finding]

---

## Score emoji guide

Use these in heuristics breakdown headings:

- ✅ Score 5 — Solid
- 🟡 Score 4 — Minor issue
- ⚠️ Score 3 — Needs attention
- 🔴 Score 2 — Significant violation
- ❌ Score 1 — Critical failure

## Language

Write the entire audit in the same language the user wrote their message in.
If the user wrote in Russian, audit in Russian. If in English, audit in English.
Apply this to all sections: Summary, Top 3 Issues, Quick Wins, Heuristics Breakdown,
Visual Design, and all Fix suggestions. The heuristic names (H1-H10) and their
English titles can stay as-is since they are proper names, but everything else
should match the user's language.

## Tone

Be honest and specific, not diplomatic and vague. "The empty state is missing" is useful.
"Could be improved" is not. If something is done well, say so briefly and move on.

When you do not have enough information to score something (e.g., only one screen of a
multi-step flow), note that explicitly rather than guessing. A score with a caveat is
more useful than a confident wrong score.
