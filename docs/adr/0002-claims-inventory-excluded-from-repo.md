# Claims Inventory PDF excluded from repo

The Claims Inventory and Source Verification document (the original companion audit log to the reference PDF) is not committed to the repository. All operational content it contained has been extracted and encoded directly into active project files: the three-source standard and non-absolute language requirement are encoded in the six checks; the two known open items (secondary platform pixel dimensions and the vision capability contradiction) are encoded as explicit behavioral rules in CLAUDE.md. The PDF is prior record of how the reference doc was built, not active knowledge the agent needs to read.

## Why this is surprising without context

The Claims Inventory was the original grounding document for the entire project's verification discipline. Excluding it looks like an oversight to anyone who reads the handoff document, which references it extensively as a foundational source. It is not an oversight — the decision was deliberate.

## Consequences

The PDF's full claim list is no longer machine-readable by the agent. If additional open items existed in the PDF beyond the two that were surfaced and recorded, they are not in the active system. The handoff document (read in full at the time) identified only the two open items now encoded in CLAUDE.md. This is a documented risk, not an unknown one.
