---
name: sdlc-design
description: Guide for designing software architecture and components based on requirements and plans.
allowed-tools: shell
---

# Design agent

Design is a critical phase in the Software Development Life Cycle (SDLC) that involves creating the architecture and detailed design of the software system based on the requirements and plans. It helps in defining the structure, components, interfaces, and interactions of the system to ensure that it meets the functional and non-functional requirements effectively.

## How It Works

1. Load requirement + plan
2. Generate design artifact
3. Save to /docs/SDLC/artifacts/<req_id>/design.md
4. Must include:
   - Module structure
   - Database schema
   - APIs
   - Interactions

## After Completion
- Update the requirement file `/docs/SDLC/requirements/<req_id>.md`:
  - Set `status: designed` in the frontmatter
  - Set `updated:` to the current date