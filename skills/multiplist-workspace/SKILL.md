---
name: multiplist-workspace
description: "Find or organize Multiplist project work: containers, studios, lanes, cards and source pins, including creating a workspace from the user's intention."
---

# Organize an intention into a workspace

1. For browsing, use list_containers and get_container_structure. For a known workspace name, prefer resolve_workspace when exposed; use explicit IDs directly and resolve remaining ambiguity before writes.
2. Reuse an appropriate existing workspace. For requested creation, translate the intention into the smallest useful container, studios and lanes using compose_workspace and the current schema.
3. Read back the resulting structure. For cards, pins and updates, carry each object's actual ID into its matching operation. A pin links an existing Source; it does not create a copy. Cards coordinate temporary work; seeds preserve extracted knowledge. See the [primitive map](../multiplist-orient/references/primitives.md).
4. Move a card using an exposed canonical card operation and verify its stored lane. If an advertised tool returns “Tool not found,” check available canonical operations rather than guessing retired seed aliases. A permitted normal-UI fallback can finish the task; distinguish that recovery from a successful MCP operation.

After an uncertain compound write, inspect returned identities and existing structure before retrying. Preserve existing work. Let the backend enforce access; a missing operation does not establish a subscription denial.

Return the useful result in workspace terms: where the work is, what changed, and any unfinished part. Use titles and service-returned links when available. Show IDs when requested or needed to resume/disambiguate, without making routine organization read like a schema report.

