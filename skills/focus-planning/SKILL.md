---
name: focus-planning
description: Convert a task list and known commitments into a realistic focus-day plan with time blocks, buffers, and explicit carryovers. Use when the user asks to plan a workday, protect focus time, time-block tasks, or balance deep work with routine tasks.
license: MIT
metadata:
  source: https://github.com/alirezarezvani/claude-skills/tree/main/productivity/deep-work
  adaptation: Portable instructions; no scripts, APIs, connectors, or runtime dependencies.
---

# Focus Planning — build a workable day

Turn the user's tasks and fixed commitments into a schedule they can actually follow. This skill is a planning aid, not a time-tracking or calendar-writing tool.

## Inputs and assumptions

- Use any fixed meetings, appointments, work hours, breaks, and task estimates the user supplies.
- If an authorized calendar tool is available and the user asks you to check conflicts, inspect it before scheduling. Otherwise say the plan is based only on the information provided; do not imply the calendar was checked.
- If a critical constraint is missing, either make one clearly labeled reasonable assumption or ask one concise question when no useful plan can be made without it.
- Distinguish estimates from fixed commitments. Never silently move an existing commitment.

## Build the plan

1. Identify the 1–3 most important outcomes; prioritize by deadline, impact, and dependencies rather than filling every minute.
2. Place demanding, concentration-heavy work in the best available focus windows. Use blocks long enough to make progress, but split work when the user's energy, task size, or available time calls for it.
3. Batch email, administration, and other shallow tasks into a small number of windows. Include realistic transition time and breaks; leave some slack for overruns.
4. If the user has specified that times must use five-minute increments, ensure every start time, end time, and duration is a multiple of five minutes. Apply this preference whenever that stable preference is available.
5. Do not force an arbitrary daily deep-work quota or claim that a plan is optimal. If the requested workload exceeds the available time, show the overage and propose what to defer, shorten, or split.
6. Do not create calendar events or reminders unless the user explicitly asks and an authorized tool is available.

## Output

Provide a table with `Time | Activity | Duration | Outcome/notes`, followed by:

- **Top priorities** (if not obvious from the table)
- **Assumptions or unchecked conflicts**
- **Carryovers / defer candidates** if capacity is exceeded

Use exact start and end times. Keep the plan concise and immediately usable. If the user asks to sync it, create separate events for separate time blocks rather than one all-day block, and report what was actually created.
