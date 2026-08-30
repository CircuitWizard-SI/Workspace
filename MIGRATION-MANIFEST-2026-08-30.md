# Skill Migration Manifest — 2026-08-30

- `circuit-840-coach` moved from `mocei_project`.
- `electric-circuit-exam-course` moved with its plugin, agent configuration, and knowledge-map reference.
- `cqu-ee-admissions-monitor` was an identical duplicate and was not overwritten.
- The Workspace version of `math-i-ii-gap-diagnoser` was retained by explicit confirmation.
- Local non-Minis skills were synchronized from `/var/minis/skills`; binary resources that cannot be represented safely as UTF-8 were skipped and reported locally.
- `global-markdown-math-render` and `minis-markdown-output` were removed from this repository's migration branch for relocation to `MinisConfig`.
- `My-computer-Codex` was explicitly excluded.
