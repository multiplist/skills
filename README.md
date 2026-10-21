# Multiplist

Give Claude cited memory of your own thinking.

Multiplist is a private vault for the work you do with AI. It saves your conversations, notes and documents, extracts the decisions, frameworks and key passages inside them, and anchors every extraction to the exact characters you wrote. When you come back weeks later, Claude can recall what you decided and quote it back with a citation that traces to the original — instead of you re-explaining your own project.

This plugin bundles the Multiplist connector with six skills that tell Claude when and how to use it.

## Use it

Connect the Multiplist connector from this plugin's **Connectors** tab and sign in to your Multiplist account. Then just talk:

- **"Save this conversation to my vault"** — captures it and extracts the meaning
- **"What did I decide about pricing back in July?"** — recalls the passage with its citation
- **"How has my thinking on this architecture changed?"** — synthesizes a research brief across sources
- **"Set up a workspace for this project"** — organizes containers, studios and lanes
- **"Flag that this contradicts what I said earlier"** — records a reader mark on the source

If you're new, ask *"what can Multiplist do?"* and the orientation skill will walk you through it.

## Skills

| Skill | When Claude uses it |
| :--- | :--- |
| `multiplist-orient` | Getting started, or choosing a workflow for a goal |
| `multiplist-capture` | Saving notes, conversations or documents to the vault |
| `multiplist-recall` | Finding and quoting a saved passage, decision or framework |
| `multiplist-research` | Creating or following a stored research or evolution brief |
| `multiplist-workspace` | Finding or organizing project work into workspaces |
| `multiplist-author-marks` | Recording an annotation, correction or tension on a source |

## What you need

A Multiplist account at [multiplist.ai](https://multiplist.ai). The free tier covers capture, extraction, search and reading; workspaces, research briefs and marks are on the paid tiers. The connector only exposes the tools your account's plan includes, so you will see the surface you're entitled to and nothing you can't use.

## Data

The plugin itself stores nothing and contains no credentials. Content you ask Claude to save, and the search queries you make, go to your own Multiplist account at `multiplist.ai` over HTTPS, authenticated through OAuth with your own login. Extraction runs against the AI provider configured on your account. Multiplist holds your vault; your sources are partitioned to your account and realm, and are not shared with other users. See the [privacy policy](https://multiplist.ai/privacy) for collection, retention and third-party details.

## Links

- [multiplist.ai](https://multiplist.ai) · [Documentation](https://multiplist.ai/docs) · [Privacy](https://multiplist.ai/privacy)
- Support: `support@multiplist.ai`

MIT licensed.
