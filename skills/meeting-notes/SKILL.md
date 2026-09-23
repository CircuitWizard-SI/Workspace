---
name: meeting-notes
description: Turn meeting transcripts or rough notes into concise minutes, explicit decisions, and an actionable follow-up list. Also use to prepare a timeboxed, outcome-focused agenda or assess whether a meeting can be handled asynchronously.
license: MIT
metadata:
  source: https://github.com/alirezarezvani/claude-skills/tree/main/productivity/meetings
  adaptation: Portable instructions; no scripts, APIs, connectors, or runtime dependencies.
---

# Meeting Notes — decisions and owned actions

Use the material the user supplied to prepare an agenda, summarize a meeting, or extract follow-ups. Do not claim to have attended, heard, or checked a recording that was not provided.

## Before a meeting

1. Identify the decision or outcome the meeting is meant to produce.
2. If the purpose is only to share routine status or information, recommend an async update as an option; do not refuse to draft the meeting materials if the user still wants them.
3. Draft an agenda with topic, desired outcome, and duration. Put decisions before general discussion, reserve a short closing slot for actions, and ensure the total fits the stated meeting length.
4. If no meeting length is supplied, provide a reasonable proposed length and label it as an assumption.

## After a meeting

Return a compact record with:

- **Summary:** key discussion points, without turning debate into agreement.
- **Decisions:** only decisions clearly made. Label proposals or unresolved choices separately.
- **Actions:** table with `Action | Owner | Due date | Status/evidence`.
- **Unassigned / undated:** explicitly flag actions where the notes do not name an owner or due date. Never guess these fields.
- **Open questions / risks:** include only items present in the source material.

## Accuracy rules

- Preserve names, dates, numbers, and terminology as stated. Flag ambiguous names or dates.
- Distinguish a commitment (“I will send it Friday”) from a suggestion (“someone should send it Friday”).
- When the source is noisy or incomplete, label the result as a draft and identify the uncertain passages.
- Do not invent quotations, decisions, owners, deadlines, or consensus.
- Do not automatically send minutes, invite attendees, or create tasks/calendar events. Do so only when the user explicitly requests it and an authorized tool is available.
- Use the user's language unless they ask for another language.

## Output size

Keep routine minutes scannable. Put detail in an appendix only when the transcript is long or the user requests a full record. For a short transcript, return the decisions and action list without padding.
