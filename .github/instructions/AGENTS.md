# AGENTS.md

This file provides guidance to AI coding agents (Claude Code, Cursor, Copilot, Antigravity, etc.) when working with code in this repository.

## Core Rules

- If a task matches a skill, you MUST invoke it
- Skills are located in .agents/skills/<skill-name>/SKILL.md
- Never implement directly if a skill applies
- Always follow the skill instructions exactly (do not partially apply them)


## Intent → Skill Mapping
The agent should automatically map user intent to skills:

- Feature / new functionality → `sdlc-plan`, then `sdlc-design` and `sdlc-tasks`
- Planning → `sdlc-plan`
- Design → `sdlc-design`
- Tasks → `sdlc-tasks`
- Implement → `sdlc-implement`
- Test → `sdlc-test`
- Code review → `sdlc-code-review`
- API or interface design → `api-and-interface-design`
- UI work → `frontend-ui-engineering`



## AI Engineering Workflow

The repository follows a SDLC-driven workflow.

SDLC-driven development has seven phases.
   
`plan` → `design` → `tasks` → `implementation` → `testing` → `code review` → `ship`

Commands available:

/plan <req_id>
/design <req_id>
/tasks <req_id>
/implement <req_id>
/test <req_id>
/review <req_id>
/ship <req_id>

Rules:

1. Requirements are stored in /docs/SDLC/requirements
2. Artifacts are generated in /docs/SDLC/artifacts/<req_id>/
3. Always read the requirement before generating artifacts
4. Never overwrite artifacts without confirmation


   
