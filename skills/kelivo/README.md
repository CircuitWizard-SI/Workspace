# Kelivo-compatible skills

These skill folders are adapted for Kelivo and can be imported individually from the public GitHub repository. In Kelivo, open **Skills → + → Import from GitHub** and enter the folder URL shown below.

| Skill | GitHub import URL | Notes |
|---|---|---|
| Circuit Theory Coach | https://github.com/CircuitWizard-SI/Workspace/tree/main/skills/kelivo/circuit-840-coach | Circuit theory learning and problem-solving practice. |
| Math I/II Gap Diagnoser | https://github.com/CircuitWizard-SI/Workspace/tree/main/skills/kelivo/math-i-ii-gap-diagnoser | Verify target exam version/year before diagnosing scope. |
| Apple Reminders for Kelivo | https://github.com/CircuitWizard-SI/Workspace/tree/main/skills/kelivo/apple-reminders-kelivo | Requires Kelivo iOS reminders tools and permission; query/create/complete only. |
| Web Content Extractor for Kelivo | https://github.com/CircuitWizard-SI/Workspace/tree/main/skills/kelivo/web-content-extractor-kelivo | Requires a conversation-bound workspace with shell and network access. |
| Internal Comms for Kelivo | https://github.com/CircuitWizard-SI/Workspace/tree/main/skills/kelivo/internal-comms-kelivo | Includes examples and the upstream Apache-2.0 license. |

## Import and enable

Import one URL at a time. Kelivo fetches the public repository archive and extracts the selected skill directory. After import, enable the skills for the desired assistant; the skill files alone do not enable Kelivo's built-in device tools.

- **Study assistant:** `circuit-840-coach-kelivo`, `math-i-ii-gap-diagnoser-kelivo`.
- **Everyday assistant:** `apple-reminders-kelivo`; optionally enable `web-content-extractor-kelivo` and `internal-comms-kelivo`.

The reminders skill can only query, create, and complete reminders because these are the operations exposed by Kelivo's current iOS local tools. The web extractor requires a bound workspace and network access. Internal-comms was adapted from Anthropic's skill; source-derived files carry adaptation notices and the Apache-2.0 license is included.
