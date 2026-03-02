# MVP_040_RECOMMENDER (Frozen) — Lite Weekly Social Drop

## Purpose
This document freezes the Lite MVP recommender as a **pure social experience**.

The weekly drop must create:
- discovery
- excitement
- “I didn’t think this would work on me”

by showing **real examples from similar-body users**.

The system must never feel like:
- AI judgement
- AI coaching
- AI “best answer” recommendations

The core experience remains:
**the user discovering themselves through 3D try-on**.

---

## Frequency (Fixed)
- Exactly **once per week**
- No daily recommendations in Lite

---

## Output Format (Fixed)
Each weekly drop contains **4 style examples**:

### 1) Similar-Body Cluster Styles (3 examples)
Show:
- “People with a body similar to yours are enjoying these styles.”

Each example must include:
- a style/outfit set (top/bottom/shoes/optional outer)
- a short label (style name only, no evaluation)
- purchase links for each item (allowed, no pushing)

### 2) Assumption Breaker (1 example)
Show:
- “A style that people similar to you also tried — it might surprise you.”

This is the “wow” slot.
It must be meaningfully different in silhouette or vibe from the 3 cluster examples.

---

## Tendency Labels (Fixed)
Each example displays one tendency label:

- Easy Fit  
  "Likely to fit your body balance"

- Neutral  
  "Can work depending on styling choices"

- High Difficulty  
  "Technically possible, but requires balance adjustment"

These labels are informational only.
Final decision always belongs to the user.

---

## Composition Rules (Fixed)

### A) No AI voice
Forbidden:
- “We recommend…”
- “Best choice…”
- “You should…”
- long explanations
- any coaching / motivation language

Allowed:
- neutral prompts that invite try-on:
  - “Try it on once.”
  - “Rotate 360° and check proportions.”
  - “Just test it.”

### B) Diversity enforcement
The 4 examples must not collapse into one vibe.
The system must enforce diversity across:
- silhouette category (e.g., slim/regular/oversize)
- structure vs drape
- color tone group

### C) Purchase links allowed, but no pushing
- Include purchase links for all items
- Do not include sales pressure language

---

## Cold Start Rule (Fixed)
If the similar-body cluster population is insufficient,
the system must use a **near-body approximation cluster**
based on body ratio similarity.

This must not be surfaced as a “low data” warning in the UI.

---

## Failure Rules
The weekly drop fails if users feel:
- judged
- controlled
- lectured
- pushed to buy

---

## Governance Rule
No change to frequency, format, composition rules, or cold-start rule
without updating this document and committing to Git.