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

**Description boundary:**
The line between what the agent may do — describe what is observed and map it to the corpus — and what is reserved for the user: aesthetic verdicts such as "this looks wrong" or "this is good." The agent diagnoses using the corpus; the user judges.

**Vision input:**
Input where the user uploads an image for the agent to observe directly.
_Avoid:_ image inspection, visual input

**Self-report:**
Input where the user describes their image in text. The agent matches the description against the failure-mode table and corpus guidance.
_Avoid:_ text input, verbal description

**Session:**
A single continuous agent run — from when the tool is invoked until it stops. The pending-entry expiry check runs once per session, before the first user question is answered.
