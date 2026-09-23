---
name: capture
description: Turn a user's brain dump, scattered notes, or mixed task-and-idea message into a faithful, organized, actionable capture. Use when they ask to capture or organize thoughts, or provide an unstructured bundle of plans, questions, decisions, and tasks.
license: MIT
metadata:
  source: https://github.com/alirezarezvani/claude-skills/tree/main/productivity/capture
  adaptation: Portable instructions; no scripts, APIs, connectors, or runtime dependencies.
---

# Capture — organize the dump without losing it

Use this skill when the user wants to get a jumble of thoughts out of their head and into a clear structure. Start organizing immediately; do not make them complete an intake form first.

## Rules

1. **Preserve every meaningful item.** Do not discard something because it seems minor. Keep the user's wording where it conveys intent or tone.
2. **Separate facts from interpretation.** Keep stated commitments, ideas, questions, and decisions distinct. Mark uncertainty instead of silently resolving it.
3. **Do not invent links to files, projects, people, or prior conversations.** Only report a connection if it is present in accessible context or has been verified with an available tool. If no such access exists, say so briefly.
4. **Ask at most one clarifying question, and only if an ambiguity would materially change the organization.** Otherwise make a clearly labeled best-effort draft.
5. **Do not create reminders, calendar events, send messages, or edit files unless the user explicitly asked for that action and the required tool is available.**
6. **Match the size of the response to the dump.** A few unrelated items need a short list, not an elaborate taxonomy.

## Default output

For a substantial dump, organize into:

### Projects and ideas
Group related multi-step efforts and preserve the user's original framing. Include relevant open questions or decisions under the project.

### Next actions
Use concrete verbs. Preserve any owner, deadline, status, or dependency the user actually supplied. Do not assign missing owners or dates.

### Decisions and open questions
List choices that need a decision and questions that block progress. Do not turn an idea into a commitment.

### Useful connections / next step
Mention only verified connections to accessible context. If none can be checked, state that. End with one practical next step or offer to carry out a specific item; do not ask a vague “what now?” when a reasonable next action is clear.

For a small dump, use a concise “Captured” list with any action items and unresolved questions.

## Safety and privacy

If the dump contains sensitive material, summarize only what is necessary. Do not repeat private details gratuitously. If the user asked only to organize, do not take follow-on actions on their behalf.
