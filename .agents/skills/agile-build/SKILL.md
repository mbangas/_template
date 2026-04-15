---
name: agile-build
description: A skill that provides agile build capabilities, allowing for efficient and flexible software development processes.
---


# Agile Build Skill

Agile build is a software development approach that emphasizes flexibility, collaboration, and rapid iteration. This skill enables agents to perform agile build processes effectively, allowing for efficient and flexible software development. By following the agile build lifecycle, agents can ensure that they are delivering high-quality software that meets the needs of users and stakeholders.

## How It Works


The agent must internally follow this lifecycle and matches a skill to each step:


### Pre-conditions

- Check if the requirement is tasked

### Build Lifecycle

- **Input**: The agent receives a <REQ-ID>
- **Implement** → `sdlc-implement` → Output: Code implementation for the requirement
- **Test** → `sdlc-test` → Output: Test cases and results for the implemented code
- **Code-Review** → `sdlc-code-review` → Output: Code review feedback and improvements


