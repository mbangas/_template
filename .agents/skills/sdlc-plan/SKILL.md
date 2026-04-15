---
name: sdlc-plan
description: Guide for planning the Software Development Life Cycle (SDLC) for a given requirement.
allowed-tools: shell
---

# Planning agent

Planning is a crucial phase in the Software Development Life Cycle (SDLC) that involves defining the scope, objectives, and approach for a software project. It helps in setting clear expectations, allocating resources effectively, and identifying potential risks early on.

## How It Works

1. Understand & Expand (Divergent): Restate the idea, ask sharpening questions, and generate variations.
2. Evaluate & Converge: Cluster ideas, stress-test them, and surface hidden assumptions.
3. Sharpen & Ship: Produce a concrete markdown one-pager moving work forward.


## Planning instruction for agent

1. Find requirement in /docs/SDLC/requirements/<req_id>.md
2. Extract:
   - functional requirements
   - constraints
   - acceptance criteria
3. Generate implementation plan based on the extracted information and best practices for SDLC planning.
4. Create folder /docs/SDLC/artifacts/<req_id> 
5. Save to /docs/SDLC/artifacts/<req_id>/plan.md
6. Plan must include:
   - Overview
   - Architecture
   - Major components
   - Implementation phases
   - Risks


## After Completion
- Update the requirement file `/docs/SDLC/requirements/<req_id>.md`:
  - Set `status: planned` in the frontmatter
  - Set `updated:` to the current date

  