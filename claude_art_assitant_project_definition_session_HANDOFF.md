# Project Handoff — Digital Art Teacher (Agentic Art-Theory Assistant)

**Repo:** https://github.com/SevWren/digital_art_teacher
**Handoff point:** End of the project-definition phase — immediately *before* any work began on sequencing the critique-vs-assist guardrail against vision-input scoping. No guardrail spec, hook design, or vision-capability scoping has been written yet. This doc stops right before that work starts, on purpose.
**Purpose:** Let a fresh session (human or AI) pick up project-definition work with full grounding context, without re-deriving it from scratch or re-litigating corrections already made.

---

## 1. What this project is

A portable agentic coding environment — buildable in Claude Code, Codex, Gemini CLI, Grok, and similar tools — providing a stage-aware digital-art teaching assistant. The assistant's entire body of art-theory and technical knowledge comes from two source documents supplied by the project owner:

- **`Art_Theory_Digital_Practice_Reference_v5.pdf`** (12 pages) — subject-agnostic reference covering classical art theory (§3), modern/contemporary theory (§4), a 13-stage production pipeline mapped stage-by-stage to governing theory (§5.0–§5.12), digital/technical standards including color management and a resolution/canvas catalog (§6), a self-run quality-check protocol (§7), a failure-mode → corrective-action table (§8), and appendices including a 92-source bibliography (§9–§10).
- **`Claims_Inventory_and_Source_Verification_v5.pdf`** (1 page) — companion audit log documenting the verification discipline behind the reference doc: a minimum of three independent published sources required before any claim is accepted, deliberately non-absolute wording for consensus-practice claims, and an explicit list of items still open.

Both files were read in full during this phase; nothing in this handoff is inferred from titles or partial reads.

## 2. Non-negotiable constraints established from the source text

- **No invented numbers.** Every technical/numerical claim must trace to a cited source in the bibliography (Reference doc, p.1, "Evidence rule").
- **Subject-agnostic.** No anatomy, markings, or subject-specific systems (Reference doc, p.1, "Subject rule"; §3.4).
- **Authorship boundary — does not change with input channel.** The AI never creates, edits, or exports the artwork; the user performs every act of creation. ("You create every image. The AI only advises from this document." / "Neither the document nor the AI ever creates, edits, or modifies any image." — p.1)
- **Critique boundary.** Independent aesthetic/quality judgment of the piece stays with the user; the AI's role is advisory/diagnostic, not evaluative. Rooted in §7 ("All checks below are performed by you... The AI cannot see your image and will not pretend to.") — see §4 below for why this line is now only partially accurate.
- **Time-sensitive/incomplete figures stay unresolved on purpose.** E.g. secondary platform export pixel dimensions are explicitly *not* hard-coded; the Claims Inventory flags them as an open item to be closed through the three-source verification process — not something the deployed agent resolves on the fly.

## 3. Two accepted input channels — different grounding status

| Channel | Status |
|---|---|
| **Self-reported description (text)** — user reports what they notice; matched against the §8 failure-mode table | Fully supported by the corpus as written. This is exactly what §8 is designed for. |
| **Direct image inspection (vision)** — user uploads the piece; AI observes it directly | **Confirmed in scope** by the project owner (explicit decision: "both should be supported, as separate capabilities"). **Not yet authorized by the corpus as written** — §1.3 ("The AI never sees or edits your image") and §7 ("The AI cannot see your image and will not pretend to") both explicitly assume this doesn't happen. |

## 4. Open contradiction in the corpus (flagged, not yet resolved)

Because vision-based inspection is now confirmed in scope, §1.3 and §7 of the Reference doc currently assert something false about the deployed system. This is a real gap, not a wording nuance. It needs one of:

- a v6 annotation to those two lines acknowledging the AI does have visual access when the user supplies an image, or
- an explicit override tracked as an open item the same way the Claims Inventory tracks its other unresolved figures.

This should go through the same evidentiary rigor as any other corpus change (see maintenance workflow in the achieve-statement, §6 below) — not get patched silently.

## 5. Queued follow-up work — NOT started

A **critique-vs-assist guardrail** is queued as explicit, high-priority follow-up, flagged by the project owner as needing to be defined **before** vision-input inspection is built, not after.

Reasoning on record: without vision, the AI can only ever respond to what the user already typed — an accidental circuit-breaker against the AI originating unrequested opinions. Vision removes that circuit-breaker; "describe what's there" and "judge whether it's good" become one step apart with nothing structurally preventing the drift, unless the boundary is locked down as a hard rule first.

**This is the next open question for the project.** As of this handoff, no sequencing plan, guardrail spec, hook design, or enforcement mechanism has been written or committed anywhere — do not assume otherwise.

## 6. Current project achieve-statement (final text as of this handoff)

> I'm building a portable agentic coding environment — usable across Claude Code, Codex, Gemini CLI, Grok, and similar tools — that turns two existing documents into the operating knowledge base for a stage-aware digital-art teaching assistant: *Art Theory & Digital Practice Reference v5.0* and its companion *Claims Inventory & Multi-Source Verification* log.
>
> The reference document already encodes the knowledge (classical and modern art theory, a 13-stage production pipeline, technical/resolution standards, a self-run critique checklist, and a failure-mode diagnostic table), a hard evidence rule (no invented numbers — every technical claim traces to a cited source), and a hard authorship boundary that does not change regardless of input channel: the AI never creates, edits, or exports the image, and never renders independent aesthetic critique of it — the user remains the sole author and sole judge of the work. The companion document supplies the verification discipline that produced the knowledge base: a minimum-three-independent-source standard for any claim, non-absolute language for consensus-practice claims, and an explicit record of open items — the corpus is versioned and incomplete by design in places, not finished.
>
> The assistant needs to accept two distinct channels for what the piece currently contains, and they carry different grounding status right now:
> - **Self-reported description (text)** — the user reports what they notice, matched against the grounded failure-mode/corrective-action table. This is already fully supported by the current corpus; Section 8 is built around exactly this workflow.
> - **Direct image inspection (vision)** — the user uploads the piece and the AI observes it directly. This is a capability the current v5.0 text explicitly disclaims (§1.3, §7). It's in scope for the project, but it is not yet authorized by the corpus as written — it needs its own v6 annotation or explicit override, tracked the same way the Claims Inventory tracks its other open items, rather than treated as already covered.
>
> My goal is to encode the knowledge, the verification discipline, and both input channels into the agent's structure, so that:
>
> 1. The agent's instruction files (CLAUDE.md / AGENTS.md / GEMINI.md, one shared source of truth with thin tool-specific overrides) define it strictly as an advisory and diagnostic coaching partner — never an image generator, editor, or independent critic of the artwork — regardless of whether input arrives as text or as an uploaded image.
> 2. Skills break the reference into stage-addressable modules (classical theory, modern theory, each of the 13 pipeline stages, technical standards, the self-run checklist, the failure-mode table) so the assistant surfaces the right theory for whatever stage the user says they're at.
> 3. Hooks gate every response before it reaches the user: technical/numerical claims are checked against the bibliography/claims-inventory corpus, and anything not traceable to a source is blocked. Any corpus-flagged open item (secondary platform pixel dimensions, and now the vision-capability question itself) is relayed with its actual status, not invented or silently resolved.
> 4. A maintenance workflow mirrors the Claims Inventory process: closing an open item, or adding a new claim or capability, requires the same three-source verification and non-absolute wording before the corpus — and the agent's behavior — is updated. Authorizing vision-based inspection is itself one of the corpus updates this workflow needs to process.
> 5. A separate, explicit guardrail defines the line between *description* (reporting what's observed — permitted, and more load-bearing now that vision makes it easy to slide past) and *critique* (independent aesthetic/quality judgment — out of scope, reserved for the user) — this is the item already queued, and it now governs both input channels, not just the text one.
>
> The result should be an agent that, regardless of which underlying coding tool runs it, gives stage-appropriate advice grounded in cited theory and technical standards, accepts either a self-report or a direct look at the current piece, and never crosses from describing what it observes into rendering the aesthetic judgment that stays the user's alone.

## 7. Corrections made during this phase (grounding-discipline log)

Worth carrying forward — these show the evidentiary standard this project holds itself to, and the specific failure patterns to watch for when drafting anything new:

1. **Draft:** "...gives real-time, stage-appropriate art critique." → **Corrected:** "critique" belongs to the user per §7 ("performed by you... will not pretend to"); "real-time" was the project owner's own framing, never asserted by either source document. Corrected to: "gives stage-appropriate advice... while leaving all direct visual judgment and critique of the image to the user."
2. **Draft:** claimed the corpus's "verify current spec at time of delivery" line meant the *deployed agent* should perform a live web check. → **Corrected:** that line is addressed to the human artist (the document's consistent second-person voice), instructing *them* to verify at their own moment of export. The real project-level takeaway is that these figures are open items in the Claims Inventory, closed only through the three-source verification workflow — not something the agent resolves live in conversation.
3. **Draft:** cited "The AI cannot see your image and will not pretend to" as evidence the AI receives zero information about the piece's current state. → **Corrected:** that line only concerns who performs visual observation/judgment (the human). It doesn't preclude the user reporting image content in words (§8 already assumes this), and — per the project owner's explicit decision — doesn't preclude vision-based inspection either, since that's now a confirmed in-scope capability. See §4 above for the open contradiction this created in the corpus.

## 8. Persistent memory already recorded

For sessions with access to this Claude Project's memory:

- `/projects/01a0ee9d-0855-7440-b020-70c0b080db9b/areas/reference-documents.md` — records that both source documents are incomplete and still need improvement.
- `/projects/01a0ee9d-0855-7440-b020-70c0b080db9b/index.md` — records the project name and repo location.

## 9. Suggested skills for the next session

- **writing-for-agents** — once the guardrail spec exists, use when actually drafting CLAUDE.md / AGENTS.md / GEMINI.md content.
- **wayfinder** — the full build (instruction files + stage-mapped skills + grounding hooks + guardrail enforcement, across multiple target tools) is more than one session can hold; use to map it as decision tickets before diving into any one piece.
- **grill-me** or **grilling** — once a critique-vs-assist guardrail draft exists, use one of these to stress-test it against adversarial prompts ("what do you think of this?", "rate this piece") before treating it as locked.
- **to-spec** — once the guardrail-sequencing question (§5 above) is actually resolved, use this to turn the decision into a formal spec for the repo rather than leaving it only in conversation.

## 10. Explicitly NOT included in this handoff

- No guardrail spec text.
- No hook design or enforcement mechanism.
- No vision-input capability scoping.
- No repo file structure or actual CLAUDE.md / AGENTS.md / GEMINI.md content.

All of the above are queued, not started, as of this handoff point.
