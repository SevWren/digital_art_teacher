# Coaching Response Format Specification

**Status:** Accepted
**Source decisions:** ADR-0005 (Amendment: Coaching Response Format), GitHub issue #30
**Primary source:** `docs/specs/validated-response-examples.md` — two owner-approved examples that are the authoritative ground truth for this spec
**Blocks:** Issues #27 (output register must reference this), #7–21 (all knowledge files)

---

## 1. Purpose

This spec defines the required structure for every user-facing coaching response. It is derived directly from two validated example outputs. Any agent formulating a coaching response must produce output that matches this structure. Any agent authoring a knowledge base file must write its Plain-English Guide sections with this structure in mind.

This spec does not define when to produce a coaching response (that is the guardrail spec's territory). It defines what a coaching response must look like once the decision to respond has been made.

---

## 2. The Required Structure

Every coaching response has exactly three parts, in this order:

```
[1. Goal statement]
[2. Technique blocks — minimum 2, maximum 5]
[3. Quick exercise]
```

All three parts are required. A response missing any part does not conform to this spec.

---

## 3. Component Specifications

### 3.1 Goal Statement

**What it is:** One sentence. States what the response is trying to achieve.

**Rules:**
- Plain English only. No art theory terms.
- Connects directly to what the user said they want. Do not restate the user's words; restate their goal as a concrete outcome.
- One sentence. Not a paragraph.

**Correct form:**
> "To push the background far into the distance and make the scene feel huge, focus on these four techniques:"

**Wrong forms:**
- "I'll help you with atmospheric perspective." — uses an academic term; does not state the outcome
- "Here is some advice about your painting:" — does not name the goal
- Two or more sentences — exceeds the limit

---

### 3.2 Technique Blocks

**What they are:** Discrete, named steps for achieving the goal. Minimum 2, maximum 5 per response.

Each technique block has the following sub-components:

#### 3.2.1 Heading

**What it is:** A plain-English name for the technique. One short phrase or sentence.

**Rules:**
- Never the academic or corpus term. Translate it.
- Names something the user can visualize or act on.
- Not a question. Not a gerund phrase ("Doing X"). State it as a noun phrase or imperative.

**Examples:**
- Correct: `### Add a Layer of Soft Haze along the Horizon`
- Correct: `### Darken the Water Base`
- Wrong: `### Atmospheric Perspective` — academic term
- Wrong: `### Value Hierarchy Technique` — academic vocabulary in the name

---

#### 3.2.2 Current State (conditional — required when image is in scope)

**What it is:** A specific observation of what is in the user's current image right now.

**When required:** Whenever vision input is active OR the user has described their image.

**When omitted:** When no image is in scope and no description has been given.

**Rules:**
- Describes what IS there. Not what is wrong, not what it should be.
- Specific to the user's actual image. Not generic.
- Descriptive, never evaluative. States a fact about the image.

**Correct forms:**
> "Right now, your water is a light flat gray."
> "Right now, the cloud band looks like a flat cutout strip."

**Wrong forms:**
- "Your water looks bad." — evaluative, not descriptive
- "There are issues with your lighting." — vague, evaluative
- "Your clouds are poorly rendered." — verdict, not observation

---

#### 3.2.3 Steps

**What they are:** Numbered instructions for carrying out the technique.

**Rules — every step must:**
1. Name the tool, layer, or setting being used
2. Name the action being taken
3. Be specific enough that the user knows exactly what to do in their software
4. Use plain English throughout

**Correct form:**
> "On a new layer between your water and your clouds, use a large, soft airbrush with a low-opacity gray or soft white. Lightly brush across the horizon line."

**Wrong forms:**
- "Adjust your values." — no tool named, no specific action
- "Work on the atmospheric perspective in the distance." — academic term, no tool, no action
- "Make it look more realistic." — no tool, no action, verdict language

**Formatting:** Steps may be numbered lists or a short paragraph leading into a sub-list. Use whichever is clearest for the number of steps involved.

---

#### 3.2.4 Why It Works (optional, preferred)

**What it is:** One sentence explaining the observable change the user will see.

**When to include:** Whenever the reason the technique works is not self-evident from the steps. Preferred but not required.

**Rules:**
- One sentence only.
- Describes what the user will observe in their image — not the underlying principle.
- Plain English. No corpus vocabulary.

**Correct form:**
> "This knocks back the contrast, blurs the hard boundary between water and sky, and instantly makes the horizon feel miles away."

**Wrong forms:**
- "This works because of atmospheric perspective and value contrast." — corpus vocabulary
- "The reason this is effective is that it applies the principle of simultaneous contrast to your value groups." — corpus reasoning surfaced to user

---

### 3.3 Quick Exercise

**What it is:** One concrete, low-risk, fast, reversible action the user can take right now.

**Rules — the exercise must specify all four:**
1. Layer type or location (new layer, existing layer, specific layer name)
2. Tool and setting (brush type, opacity, size)
3. Specific action (what to do)
4. Observable result (what they will see happen)

**Additional rules:**
- One exercise per response. Not two, not zero.
- Placed at the end of the response, after all technique blocks.
- Low-risk: should not require irreversible changes to the existing image
- Fast: completable in under two minutes
- Reversible: user can undo or delete the layer without losing work

**Correct form:**
> "Create a blank layer just above your background clouds, grab a big soft brush set to 15% opacity, and gently spray along the bottom of the clouds where they meet the water. Watch how quickly that pushes them backward!"

> "Start by filling your water layer with a dark tone, then use a light brush on a new layer to trace out the bright side of the rings right under the thrusters."

**Wrong forms:**
- "Try adding more depth to your painting." — no tool, no action, no observable result
- "Experiment with atmospheric perspective in the distance." — academic term, no specifics
- A list of multiple exercises — only one is permitted

---

## 4. Reference-Image Variant

When the user provides a reference image alongside their current image, each technique block gains a comparison layer. The structure extends as follows:

```
[Technique block heading]

In your reference, [specific observation about what is present in the reference].
Right now, your image has [specific observation about what is present in the user's image].
[Gap-closing steps — same format as Steps in 3.2.3]
```

**Additional rule — better opportunities:**
If the user's image contains elements absent from the reference that create a stronger opportunity, the agent names it and builds on it:

> "Your reference has [X], but your image has [Y] — which means you can do [Z]."

The reference is a goal to learn from, not a template to copy exactly. The user's image may have features the reference lacks; those are assets, not problems.

---

## 5. The Corpus-as-Engine Principle

The corpus (Tier 1 files, §8 failure-mode table, pipeline files, fundamentals files) is the reasoning engine. It is the source of every technique block, every observation mapping, every corrective action. It is never cited or referenced in the response itself.

| What happens at the ICL layer | What appears in the response (UCL layer) |
|---|---|
| Agent checks §8 failure-mode table | Current-state observation describes the visual symptom in plain English |
| Agent identifies corrective action by name | Technique heading names the technique in plain English |
| Agent traces claim to Tier 1 file and section | Steps describe what to do; no citation appears |
| Agent runs PTM translation for corpus term | User reads the plain-English equivalent; never the corpus term |
| Agent identifies academic principle | "Why it works" sentence describes the observable change; never the principle name |

**What this means in practice:**

- "Atmospheric perspective" → "Soft haze along the horizon"
- "Value contrast" → "Dark base makes highlights pop"
- "§8 failure mode: flat value massing" → "Right now, your water is a light flat gray"
- "Per `fundamentals/light-and-value.md`" → never appears

---

## 6. Authorship Boundary

Every step in every technique block tells the user **HOW** to do something. No step decides **WHAT** the image should look like beyond the user's stated goal.

**HOW (permitted):**
> "Fill your water layer with a deep, near-black tone."
> "Use a large soft airbrush at 15% opacity."
> "Paint bright white-to-light-gray slivers where the wave ridges catch the light."

**WHAT (not permitted):**
> "Make the water darker." — decision, not instruction
> "The water needs to be near-black." — verdict on what it should look like
> "You should darken everything in the background." — aesthetic judgment

When the user's goal specifies a visual target ("I want it to look like the reference"), that target is the user's stated goal — the agent works toward it. The agent does not invent targets the user did not name.

---

## 7. What Never Appears in a Coaching Response

The following must never appear in any coaching response:

| Prohibited element | Example of what must NOT appear |
|---|---|
| Corpus file paths | `fundamentals/light-and-value.md` |
| Section references | §8, §7, §1.3 |
| Failure-mode row labels | "Type-3 value compression failure" |
| Academic corpus terms (untranslated) | atmospheric perspective, notan, simultaneous contrast, foreshortening, planar analysis |
| Internal workflow terms | ICL, UCL, PTM, six-checks, PENDING, PROMOTED |
| Citation lines | "According to…", "Per…", "Source:" |
| Quality verdicts | "this looks bad", "this is weak", "this is wrong" |
| General opinions | "I think", "in my opinion", "personally" |

See ADR-0005 and `docs/pedagogy/translation-matrix.md` (issue #28) for the full ICL/UCL boundary and term translations.

---

## 8. Self-Check Before Delivering a Response

Before delivering a coaching response, verify:

1. **Goal statement present?** One sentence, plain English, states the outcome.
2. **Technique blocks: 2–5?** Count them.
3. **Every block has steps?** Each step names a tool, a layer or location, and an action.
4. **Current state included when image is in scope?** Descriptive, not evaluative.
5. **Quick exercise at the end?** Specifies layer, tool/setting, action, observable result.
6. **No prohibited elements?** Run the checklist in Section 7.
7. **Authorship boundary held?** Every step is HOW, not WHAT.

If any check fails, reformulate before delivering.

---

## 9. Example Traces

The two validated examples in `docs/specs/validated-response-examples.md` are the authoritative ground truth. The traces below show how each maps to this spec.

### Example 1 trace — "Give me advice on how to give the background elements more depth"

| Spec component | Example text |
|---|---|
| Goal statement | "To push the background far into the distance and make the scene feel huge, focus on these four techniques:" |
| Technique block 1 heading | "Add a Layer of Soft Haze along the Horizon" |
| Technique block 1 steps | "On a new layer…use a large, soft airbrush…Lightly brush across the horizon line." |
| Technique block 1 why it works | "This knocks back the contrast, blurs the hard boundary…and instantly makes the horizon feel miles away." |
| Technique block 2 heading | "Give the Clouds 3D Form and Softness" |
| Technique block 2 current state | "Right now, the cloud band looks like a flat cutout strip:" |
| Technique block 2 steps | "Light the tops, shadow the bases…Soften the edges…" |
| Technique block 3 heading | "Create a Sky Dome Gradient" |
| Technique block 4 heading | "Layer the Distant Ripples Beneath the Fog" |
| Quick exercise | "Create a blank layer just above your background clouds, grab a big soft brush set to 15% opacity…" |

### Example 2 trace — "Draw the water and background in the style as seen in the example image"

| Spec component | Example text |
|---|---|
| Goal statement | "Here is how you can bring that dark, glowing water style from your reference into your spaceship piece:" |
| Technique block 1 heading | "Darken the Water Base" |
| Technique block 1 reference comparison | "In your reference, the water is as dark as the night sky — it acts like dark glass." |
| Technique block 1 current state | "Right now, your water is a light flat gray." |
| Technique block 1 steps | "Lay down a deep, near-black tone across the entire water surface." |
| Technique block 1 why it works | "This dark base is what makes highlights and glows really pop." |
| Better-opportunity note (block 3) | "Your reference only has starlight, but your ship has four massive rocket engines…" |
| Quick exercise | "Start by filling your water layer with a dark tone, then use a light brush on a new layer…" |
