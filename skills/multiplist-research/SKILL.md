---
name: multiplist-research
description: "Create and follow a stored Multiplist research brief or evolution brief when the user requests a saved synthesis or research handoff."
---

# Follow one research brief

1. Identify the question and intended sources or date range. Resolve named Sources to actual IDs. Answer ordinary conversational questions from available evidence; use request_brief for a requested stored brief.
2. Submit one request using supported scope, depth and mode arguments. Retain each returned job/brief identity and Source identity separately.
3. Follow the service-directed status path. Use get_brief_status only when its current schema accepts an identity actually returned or mapped. If directed to get_source with a Source ID, use that path. Never assume Source and brief IDs are interchangeable.
4. Follow the same job through pending, complete or failed states, honoring retry guidance with spaced, bounded reads. A status read must not restart generation. If waiting must end while pending, report the resumable identity and observed state; do not invent progress or a deadline.
5. On completion, read the actual finished Source. For its text, prefer include=["content"], format="document" when supported; JSON may supply metadata without the body. Job completion, a readable document and a well-supported answer are separate checks.
6. Check requested source coverage and consequential citations. Compare actual contributor IDs when available; citation numbers and seed counts are not source counts. The hosted flow can depend on extracted seeds: readable raw text or authored marks alone do not establish research coverage. Report gaps without silently broadening scope.
7. Check claims against the relevant passages, including qualifications and later changes. Preserve original speaker, chronology and uncertainty. Category labels do not prove adoption; historical proposals do not establish current decisions or independently validated facts. Apply [primitive distinctions](../multiplist-orient/references/primitives.md) when needed.

Resolve evidence through returned citation mappings or a supported source/export view. If mappings are unavailable, report that limitation rather than asserting full verification. A generated brief's own seedCount describes its extraction view, not the seeds cited in its research.

If a completed test demonstrates a specific failure, retain the result. A retest should have a reason and the same acceptance criteria; a clearer prompt alone does not prove a backend repair. Do not create a generation job merely to probe access, or repeat a request whose outcome is uncertain. Generation can use the account's configured AI provider.

Lead with the brief's title, observed status and useful findings. Include a service-returned link when available, an ID when needed to resume or identify the result, and concise material evidence gaps. Keep detailed test diagnostics for a requested audit.

