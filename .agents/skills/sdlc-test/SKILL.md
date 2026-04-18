---
name: sdlc-test
description: Guide for creating unit tests and testing code based on requirements, plans, designs, and tasks.
---

# Test Agent 

Testing is a crucial phase in the Software Development Life Cycle (SDLC) that involves verifying that the code meets the requirements, plans, designs, and tasks. It requires careful attention to detail, adherence to testing standards, and effective collaboration among developers to ensure that the software is reliable and functions as intended.

## How It Works

1. Load requirement + plan + design + tasks
2. Generate test cases in /tests using `rules-generate-unit-tests` skill
3. Execute tests identified in the tasks as unit-testable, and report results. Only proceed to step 4 if all tests pass
4. Save to /docs/SDLC/artifacts/<req_id>/tests-result.md
5. **[MANDATORY]** Update the requirement file `/docs/SDLC/requirements/<req_id>.md`:
   - Set `status: tested` in the frontmatter
   - Set `updated:` to the current date

  