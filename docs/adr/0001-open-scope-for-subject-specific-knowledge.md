# Open scope for subject-specific knowledge

The agent does not maintain a predefined list of permitted motifs. Any motif the user asks about can enter the corpus through the pending-and-promote workflow. This was chosen over a fixed scope list (predefined anatomy appendices for human figures, animals, vehicles, etc.) because the corpus should grow to reflect what users actually need rather than what was anticipated at build time, and because maintaining a predefined list to the three-source standard before any user had asked would require substantial upfront research that may never be used.

## Considered options

**Fixed scope list:** Pre-write appendices for a defined set of motifs (human figure, quadruped, vehicle, architectural form). Complete from day one for those motifs; useless outside them. Requires significant upfront work; fails silently when a user asks about a motif not on the list.

**Open scope (chosen):** No predefined list. Every motif gap is handled at runtime by the pending-and-promote workflow. Corpus grows organically from actual usage. Requires the workflow to be the only quality gate, which means the workflow must be robust.

## Consequences

The pending-and-promote workflow is load-bearing. If it is bypassed or fails, unverified content enters the corpus with no fallback gate. Scope drift is possible over time — the corpus can grow into adjacent domains if the scope check in the six checks is not applied rigorously.
