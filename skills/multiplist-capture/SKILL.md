---
name: multiplist-capture
description: "Save user-supplied notes, conversations or documents to Multiplist when the user asks to capture or remember them; append or revise saved content when requested."
---

# Capture user-supplied content

1. Identify the requested text, title and intended connection. Preserve supplied wording; use task context to resolve ordinary choices. Clarify only an ambiguous content boundary or destination.
2. Call create_source with the current schema. For saving without AI processing, set autoExtract=false and abstract=false. Honor explicit processing preferences.
3. Inspect the returned identity and deduplication reason. A same-title match can return older content even when the submission differs. Read it before claiming the new text was saved. For a clearly separate note, use a distinct appropriate title; clarify only when separate capture versus revision is ambiguous. Do not force skipDedup or replace content as implicit recovery.
4. Read the returned Source and compare its stored text with the input. Prefer include=["content"], format="document" when supported. Use JSON separately when structured processing or mark metadata is needed.

Storage, abstract generation and extraction are separate outcomes. autoExtract=true is a request, not proof extraction ran. If extraction was requested but did not start, use an exposed explicit extraction operation within that authorization and follow its result. Do not start a second run while one is pending or infer completion from an aggregate seed count.

For an update, read the existing Source and preserve append versus replacement intent and processing preferences. After an uncertain append, check whether the intended text is already present before replaying it. For an uncertain creation, reconcile by returned ID or narrow source lookup before retrying. Use an externalId only for a real origin identity.

See [primitive distinctions](../multiplist-orient/references/primitives.md) if counts or marks are confusing. Saving source text does not turn it into an author annotation.

Lead with the verified outcome and Source title, with a returned link when available. Include the saved text or a small relevant excerpt; show actual IDs when requested or needed for recovery. State processing status separately when relevant. If readback is unavailable, distinguish the successful write response from unverified persistence.

