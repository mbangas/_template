---
name: agile-refinement
description: A skill to perform agile refinement, which is a process of breaking down user stories into smaller, more manageable tasks.
---


# Agile Refinement Skill

Agile refinement, also known as backlog grooming, is a crucial process in agile software development. It involves breaking down user stories into smaller, more manageable tasks, estimating their complexity, and prioritizing them for future sprints. This skill enables agents to perform agile refinement effectively, ensuring that the development team has a clear and organized backlog to work from.

## How It Works


The agent must internally follow this lifecycle and matches a skill to each step:

- **Input**: The agent receives a <REQ-ID>
- **Plan** → `sdlc-plan` → Output: Implementation plan for the requirement
- **Define** → `sdlc-define` → Output: List of tasks with estimates
- **tasks** → `sdlc-tasks` → Output: Task breakdown with dependencies and priorities


