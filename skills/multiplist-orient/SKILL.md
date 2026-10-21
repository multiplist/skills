---
name: multiplist-orient
description: "Help the user get started with Multiplist, discover what this connection can do, or choose a workflow for their goal."
---

# Orient to Multiplist

Start with the user's intention and one useful next action. Keep the explanation in their language; introduce Multiplist terms only when they help.

| User's intention | Packaged workflow |
| --- | --- |
| Find a saved passage, idea or prior decision | multiplist-recall |
| Save a note or conversation | multiplist-capture |
| Add an author note or later-reader comment | multiplist-author-marks |
| Create a stored research or evolution brief | multiplist-research |
| Find or organize project work | multiplist-workspace |

Load the relevant workflow, not every skill. Other exposed tools remain usable for requests these recipes do not cover. Packaged workflow skills are distinct from Multiplist's internal extraction and production recipes.

Inspect the tools actually exposed in the selected connection. If get_capabilities is available, read effective access using its current schema; use a compact option only when supported. If absent, continue with available tools. Neither visibility nor absence establishes a subscription tier. Local desktop capabilities are not automatically hosted MCP capabilities.

For a requested vault overview, use get_vault_summary with includeRecent=3 and includeTopics=false unless more is needed. Summarize useful counts and recent material rather than reproducing every category. Skip this overview when the user already has a concrete task.

Use the established connection. Resolve genuinely ambiguous accounts before writes; do not make the user choose the same account again. Let the backend enforce authorization.

Read [Multiplist primitives](references/primitives.md) when identity, citation, category, count or ownership changes the next action. Sources hold saved material, including briefs; seeds preserve extracted knowledge; cards coordinate work.

On “Tool not found,” look for an exposed canonical operation for the right primitive. Do not guess retired aliases or change permissions. On authentication failure, use the supported sign-in flow. For SESSION_LIMIT or rate limiting, honor retry guidance, retain the existing job or object, and retry the read after backoff rather than restarting work.

Lead the reply with what the user can do and the relevant next action. Use titles and service-returned links when available; show IDs when requested or needed to resume or disambiguate. Keep verification detail available without turning an ordinary task into a diagnostic report.

