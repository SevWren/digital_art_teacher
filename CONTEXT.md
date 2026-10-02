# Digital Art Teaching Assistant

A stage-aware advisory agent that helps users plan and complete digital art pieces. The agent advises from the verified corpus; the user retains all creative authorship and all aesthetic judgment.

## Language

### Corpus and knowledge

**Corpus:**
The verified body of art-theory and technical knowledge the agent draws from. All agent responses cite a corpus source.
_Avoid:_ knowledge base, knowledge store

**Tier 1:**
The verified corpus — source documents whose claims have been confirmed against the three-source standard. The agent checks Tier 1 first for every response.
_Avoid:_ primary sources, verified sources

**Tier 2:**
Web retrieval — used only when a subject-specific gap exists in Tier 1 and the user has given explicit approval to search. Tier 2 content is flagged as unverified until promoted.
_Avoid:_ fallback, secondary sources

**Open item:**
A claim or capability known to be unresolved in the corpus — not yet verified, not yet removed. Open items are surfaced as open, never invented.

**Three-source standard:**
The minimum evidentiary bar for any claim entering the verified corpus: at least three independent published sources must confirm it. Independence means each source arrived at the claim through separate research; they cannot all derive from a single common origin.

**Evidence rule:**
Every numerical and technical claim in a response cites its Tier 1 source. Claims without a citation are not made.

**Six checks:**
The defined review applied to every pending entry before promotion is offered to the user: source count, source quality, independence, conflict, language, and scope.

### Pending workflow

**Pending entry:**
A piece of subject-specific knowledge retrieved from the web, held in the pending area, and awaiting the six-check review and user approval. It is not corpus knowledge until promoted.
_Avoid:_ staged entry, staging entry, quarantined entry

**Approve:**
The user's explicit decision to allow a pending entry to be promoted into the corpus. Approval is always a deliberate user action; the agent never approves on the user's behalf.
_Avoid:_ confirm, accept, promote (promote is what the agent does after approval)

**Promote:**
The agent's act of writing an approved pending entry into the corpus, updating the bibliography, and marking the entry closed. Promotion happens only after the user approves.
_Avoid:_ approve (that is the user's action), merge, add

**Reject:**
The user's decision to discard a pending entry without promoting it. The entry is marked closed and remains as a record.

**Defer:**
The user's choice to postpone a decision on an overdue pending entry. Deferral resets the 3-day clock without promoting or rejecting the entry.

### Subject and motif

**Subject:**
What a particular piece of artwork depicts — defined by the user in their project brief. Each piece has its own subject. Subject is piece-specific.
_Avoid:_ motif (when referring to a specific piece's content)

**Motif:**
A recognizable category of subject that carries its own established construction landmarks, anatomy, or surface systems — for example: human figure, quadruped, vehicle, architectural form. Motifs are the unit at which the gap protocol fires.
_Avoid:_ subject type, subject category, topic

**Universal principles:**
Art theory that applies regardless of motif — value, composition, gesture, edge control, perspective, color, and the production pipeline. Universal principles are always in the corpus.
_Avoid:_ general principles, core principles

**Subject-specific knowledge:**
Construction landmarks, anatomy, markings, or surface systems specific to a particular motif. Not covered by universal principles. Subject-specific knowledge enters the corpus only through the pending-and-promote workflow.

**Gap:**
The state that exists when a user asks about subject-specific knowledge for a motif not found in Tier 1. A gap triggers the retrieval protocol.

### Pipeline

**Pipeline step:**
One of the 13 numbered production stages in the art-making sequence (brief through export). The user works through pipeline steps to complete a piece.
_Avoid:_ stage (reserved in this project for usage in "pending/staging" contexts where it would conflict), phase

### Authorship and boundaries

**Authorship boundary:**
The rule that the user creates every image, makes every artistic judgment, and exports every file. The agent never creates, edits, or modifies an image regardless of input channel.

**Critique:**
An independent aesthetic or quality judgment — a verdict on whether something is good, bad, strong, weak, or better than an alternative. Critique is reserved for the user. The agent never produces a critique.
_Avoid:_ aesthetic verdict, quality judgment, comparative ranking (these are all forms of critique)

**Description boundary:**
The line between what the agent may do — describe what is observed and map it to the corpus — and what is reserved for the user: aesthetic verdicts such as "this looks wrong" or "this is good." The agent diagnoses using the corpus; the user judges.

**Description (guardrail sense):**
The act of observing what is present in an image and mapping that observation to a section of the corpus. Description is the agent's permitted action. A description states what is there — not whether it is good.
_Avoid:_ evaluation, assessment, opinion

**Observation:**
The precursor to description — the act of noting what the agent can see or infer from vision input or a self-report. Observation has no evaluative content.
_Avoid:_ judgment, appraisal

**Diagnosis:**
A corpus-grounded match between an observation and a known failure mode in the reference doc. Diagnosis identifies what pattern is present and what the corrective action is. It does not evaluate whether the image is good or bad.
_Avoid:_ criticism, verdict, opinion

**Deflection:**
The guardrail's response to a prohibited request (a request for critique, verdict, rating, or comparative ranking). A deflection is not a flat refusal — it is a redirect into a technique block that addresses the underlying need behind the prohibited request.
_Avoid:_ refusal, rejection

**Guardrail:**
The three-layer intercept architecture that enforces the description boundary. When a request would produce a critique, verdict, or quality judgment, the guardrail intercepts and redirects into a technique block. Governed by `CLAUDE/skills/art-guidance/critique-vs-assist-guardrail/SKILL.md`.
_Avoid:_ filter, rule, check

**Vision input:**
Input where the user uploads an image for the agent to observe directly. When both vision input and self-report are active simultaneously, vision is the primary observational channel — what the agent sees takes precedence over what the user describes for the purpose of forming observations. See **Input channel conflict** below.
_Avoid:_ image inspection, visual input

**Self-report:**
Input where the user describes their image in text. The agent matches the description against the failure-mode table and corpus guidance. When both self-report and vision input are active, self-report is the intentional/contextual channel — it tells the agent where the user's attention is and what they expect to find, not necessarily what is objectively present. See **Input channel conflict** below.
_Avoid:_ text input, verbal description

**Input channel conflict:**
The state that exists when vision input and self-report are both active and materially contradict each other. The resolution is: (1) describe what vision shows; (2) note plainly that this differs from the self-report; (3) ask the user to clarify before proceeding with advice. Neither channel is silently discarded. See ADR-0007 for the full protocol.
_Avoid:_ channel priority, channel override

**Session:**
A single continuous agent run — from when the tool is invoked until it stops. The pending-entry expiry check runs once per session, before the first user question is answered.
