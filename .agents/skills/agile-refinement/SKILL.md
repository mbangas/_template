---
name: agile-refinement
description: A skill to perform agile refinement, which is a process of breaking down user stories into smaller, more manageable tasks.
---


# Agile Refinement Skill

Agile refinement, also known as backlog grooming, is a crucial process in agile software development. It involves breaking down user stories into smaller, more manageable tasks, estimating their complexity, and prioritizing them for future sprints. This skill enables agents to perform agile refinement effectively, ensuring that the development team has a clear and organized backlog to work from.

## How It Works


### Pre-conditions
- Read `/docs/SDLC/requirements/<req_id>.md`
- Verify the file exists and has valid frontmatter (`id`, `title`, `status`)
- Verify that the required sections are filled in (Description, Functional Requirements, Acceptance Criteria)
- If `status` is not `draft`, warn the user that this requirement has already been processed and ask for confirmation before proceeding


### Refinement Lifecycle

The agent must internally follow this lifecycle and matches a skill to each step:

- **Input**: The agent receives a <REQ-ID>
- **Plan** → `sdlc-plan` → Output: Implementation plan for the requirement
- **Design** → `sdlc-design` → Output: List of tasks with estimates
- **Tasks** → `sdlc-tasks` → Output: Task breakdown with dependencies and priorities


