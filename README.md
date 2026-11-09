# COS - chief of staff agent

An AI chief of staff for the CEO of Bright Software Group, built on Claude Managed Agents. Version 1 reads, prepares and drafts. It never acts.

## Documents

| Document | Purpose | Status |
|---|---|---|
| [Job specification](docs/job-spec/chief-of-staff-agent-job-spec.md) | What the agent is for: mission, responsibilities, authority, guardrails, measures | v0.7 draft |
| [Design specification](docs/design/chief-of-staff-agent-design-spec.md) | How it is built, tested and rolled out, mapped to the Anatomy of an AI Agent framework | v0.1 draft |

## Planned layout

```
docs/          specifications
agents/        agent, environment and deployment definitions, synced to the platform
.claude/skills/ task skills
knowledge/     seed files for memory stores
harness/       run start, archive, lint, delivery
evals/         replay sets, rubrics, red-team cases
```

Only `docs/` exists today. The rest is created as each build phase starts (design specification section 8).

## Working rules

- Nothing in this repo holds a credential. Credentials live in the platform vault.
- A change to agent behaviour is a change to the job spec or a skill, made by pull request, tested against `evals/`, then released as a new agent version.
- These are working drafts in markdown. Final circulated versions are produced as Bright-branded documents.
