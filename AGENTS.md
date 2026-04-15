# AGENTS.md

This file provides guidance to AI coding agents (Claude Code, Cursor, Copilot, Antigravity, etc.) when working with code in this repository.

## Core Rules

- If a task matches a skill, you MUST invoke it
- Skills are located in .agents/skills/<skill-name>/SKILL.md
- Never implement directly if a skill applies
- Always follow the skill instructions exactly (do not partially apply them)


## Lifecycle Rules 

- Requirements history are listed in /docs/SDLC/requirement-list.md
- Requirements are stored in /docs/SDLC/requirements
- Artifacts are generated in /docs/SDLC/artifacts/<req_id>/
- Always read the requirement before generating artifacts
- Never overwrite artifacts without confirmation

## System documentation

- System documentation are stored in /docs/Architecture
- APIs documentation are stored in /docs/APIs


   
