---
name: agile-review
description: A skill that is responsible for assuring documentation and tracking of user stories, tasks, and progress throughout the development lifecycle.
allowed-tools: shell
---


# Agile Review Skill

Agile review aims to ensure the documentation of all system instead of just a issue or requirement.


## How It Works

The agent must internally follow this lifecycle and matches a skill to each step:

- **Input**: The agent receives a <REQ-ID>
- **doc-solution-architecture** → `doc-solution-architecture` → Output: Application Solution architecture created or updated with this requirement. The document must describe the solution architecture of all the actual system, not just the requirement. 
- **doc-api** → `doc-api` → Output: API and interface design created or updated with API changes on this requirement
- **doc-onboarding** → `doc-onboarding` → Output: Onboarding documentation created or updated with this requirement, including how to set up the development environment, codebase structure, and contribution guidelines. Must include links to all relevant documentation, such as solution architecture and API documentation.
- **doc-requirement-list**: create or update file in /docs/SDLC/requirement-list.md, adding this requirement to the list with status and link to documentation. Index must include <REQ-ID>-<REQ-TITLE>
- **doc-create-readme-file** → `doc-create-readme-file` → Output: README file created or updated.

