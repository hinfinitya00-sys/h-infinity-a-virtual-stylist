# MVP_020_USER_PROFILE (Frozen) — 3D Real-Self Avatar First

## Purpose
This document freezes the **Lite MVP user profile and capture pipeline** required to deliver the core value:

**A real, recognizable 3D self-avatar** that the user can rotate 360° and view from a third-person perspective,
so they can discover:
- “I thought this would suit me, but it feels off.”
- “I thought this wouldn’t suit me, but it actually looks great.”

This product must deliver **try-on realism close to real life**.
We do not optimize for ease at the cost of impact.

---

## Core Promise (Lite MVP)
1. The user becomes a **recognizable 3D self** on screen.
2. The avatar is rotatable **360°** (third-person view).
3. Virtual try-on must be **close to real-world wearing quality**.
4. Any styling guidance is **informational**; final judgment belongs to the user.

---

## Required User Inputs (Lite MVP — Fixed)

### A) Mandatory Capture (3 photos)
Users must provide exactly the following images:

1. Front (full body)
2. Side (full body)
3. Back (full body)

Capture constraints (must be enforced with UI guidance and checks):
- Same clothing for all 3 shots (simple outfit recommended)
- Neutral lighting (avoid strong backlight)
- Full body inside frame
- Upright posture
- No heavy filters

### B) Mandatory Metadata
- Height (cm)
- Gender presentation (men / women / unisex)

---

## System-Derived Profile (No Manual Input)
The system must infer the following from the captures:

- Body proportions and silhouette
- Shoulder/torso/leg balance
- Skin tone tendency (for color harmony suggestions later; no blocking)
- Hair region / rough hairstyle tendency (for neckline harmony later; no blocking)
- Approximate body-shape class (internal use)

No inferred attribute may be used to:
- block outfits
- hide categories
- prohibit styling choices

---

## Output Requirements (Lite MVP)

### 1) 3D Self Avatar (Required)
- The system must generate a 3D representation of the user that is recognizable as “self”.
- The user must be able to:
  - rotate 360°
  - zoom in/out
  - view front/side/back quickly

### 2) Realism Gate (Required)
The product must NOT claim success unless:
- self-recognition is achieved
- third-person viewing is smooth
- try-on visuals are close enough to real-world perception to avoid misleading purchases

If realism confidence is below threshold:
- the system must request recapture
- and must not unlock purchase-driving flows

---

## Quality Gates (Lite MVP — Fixed)

### Capture Quality Gate
The system must detect and reject captures when:
- body not fully visible
- severe blur
- severe backlight
- extreme pose
- inconsistent framing across 3 shots

### Self-Recognition Gate (User Feedback)
After generation, ask a single confirmation:
- “Does this feel like you?”
Options:
- Yes
- Not sure
- No

If "Not sure" or "No":
- prompt recapture with specific guidance
- do not proceed to purchase-intent flows

---

## Explicitly Excluded (Reserved for Standard / Pro)
- Any daily usage mechanics
- Preference memory / learning optimization
- Detailed manual measurements (shoulder/chest/waist/hip/inseam)
- Personal color deep diagnostics
- TPO / event styling
- Weather logic
- Closet management
- Physical item delivery

---

## Governance Rule
No required input, capture step, derived attribute, or quality gate may be changed
without updating this document and committing the change to Git.