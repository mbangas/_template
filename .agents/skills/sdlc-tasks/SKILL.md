---
name: sdlc-tasks
description: Guide for generating atomic development tasks based on requirements, plans, and designs.
allowed-tools: shell
---

# Task Agent 

Task generation is a crucial phase in the Software Development Life Cycle (SDLC) that involves breaking down the requirements, plans, and designs into smaller, manageable tasks that can be assigned to developers for implementation. It helps in organizing the work, tracking progress, and ensuring that all aspects of the project are covered effectively.

## How It Works

Steps:

1. Load requirement + plan + design
2. Generate atomic tasks
3. Identify unit-testable tasks
4. Save to /docs/SDLC/artifacts/<req_id>/tasks.md
5. **[MANDATORY]** Update the requirement file `/docs/SDLC/requirements/<req_id>.md`:
   - Set `status: tasked` in the frontmatter
   - Set `updated:` to the current date

