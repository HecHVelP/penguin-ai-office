# PENGUIN HQ — The AI Workforce 🐧

A personal, mobile-friendly AI agent office with an animated 3D workspace, penguin characters, and real agent execution.

> **Project status:** discovery and foundation. No agents are running yet. The first milestone is a working local prototype; the 3D office must never claim that an agent is working unless its execution state confirms it.

## Product direction

- Use [Munizada/agent-office](https://github.com/Munizada/agent-office) as the primary technical and interaction reference.
- Preserve the lively 3D office experience: animated characters, desks, workstations, selectable agents, and individual activity panels.
- Create an original PENGUIN HQ identity: custom penguin characters, cinematic dark environment, ice-blue lighting, and a polished mobile interface.
- Separate the **visual simulation** from the **real execution state**. Ambient walking/idle animations are presentation; working, waiting for approval, failed, and completed states must come from real runtime events.
- Prioritize the Pixel 9 / Android browser experience.
- Target operating budget: €0. Prefer free/open-source components and existing local tools. Do not assume unlimited free model inference or hosting.

## Initial team

| Codename | Responsibility | First deliverable |
|---|---|---|
| PIP | Orchestration and review | Architecture decisions, task breakdown, acceptance checks |
| PIX | Research and visual design | Reference audit, original visual direction, asset plan |
| BYTE | Application engineering | Runtime and frontend integration plan, first working scaffold |
| NEO | Data, reliability and security | Agent-state model, event flow, permissions and mobile performance review |

These are planned roles, not currently running autonomous agents.

## Technical direction to validate

The Munizada project currently documents React, TypeScript, React Three Fiber, Three.js, and a Node/Express server. Its README describes independent CLI task executions and explicitly notes that its profiles do not yet form a coordinated multi-agent system. We will verify the current upstream code and dependencies before deciding whether to fork it, adapt selected components, or build a clean implementation around compatible ideas.

### Non-negotiable principles

1. Never display a simulated task as real execution.
2. Require explicit approval for sensitive or destructive actions.
3. Keep API keys and credentials out of the browser and Git history.
4. Isolate parallel coding tasks with separate worktrees or branches.
5. Show clear states: idle, working, needs-input, completed, failed, and offline.
6. Make the interface usable on a narrow Android screen.
7. Preserve upstream MIT notices and attribution if code is reused; audit third-party assets and dependencies separately.

## Milestones

- [ ] M0 — Repository foundation and upstream technical audit
- [ ] M1 — Local application boots with a minimal office scene
- [ ] M2 — Original penguin character and animation system
- [ ] M3 — Selectable agents and live individual dashboards
- [ ] M4 — One real CLI agent executes a task and reports truthful status
- [ ] M5 — Multiple isolated agents, task queue, review and approval flow
- [ ] M6 — Mobile polish, reliability, security and zero-cost deployment review

## Upstream reference

- [Munizada Agent Office](https://github.com/Munizada/agent-office) — MIT licensed; primary reference, not yet vendored or forked into this repository.

## Development rule

Do not start by building a decorative mockup that cannot connect to real work. Deliver a small vertical slice: one penguin, one workstation, one real agent process, truthful status reporting, and a usable mobile view. Expand only after that slice works.
