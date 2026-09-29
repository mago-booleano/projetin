---
name: create-skill
description: "Create a reusable SKILL.md from a recurring workflow, review checklist, or debugging pattern. Use when turning a multi-step process into an on-demand skill for this project or for a personal workflow."
argument-hint: "Describe the workflow, decision points, and quality checks to capture in the skill"
user-invocable: true
---

# Create a reusable skill

## When to use
- A multi-step process is being repeated in conversation or work
- The user wants to turn a workflow into a reusable skill
- A debugging, review, implementation, or validation routine needs to be formalized
- The team needs a repeatable task pattern with decision points and completion checks

## What this skill produces
A `SKILL.md` file that captures:
- the task or outcome the skill is for
- the trigger phrases or situations that should load it
- the step-by-step process
- branching logic and decision points
- quality gates or completion checks
- the appropriate scope: project-level or personal

## Procedure

### 1. Review the workflow
Look for the process already being followed in the discussion or task.
Extract:
- the exact sequence of steps
- the decision points
- what counts as success or completion
- any quality criteria or validation checks

### 2. Generalize the pattern
Convert the observed workflow into reusable instructions.
Ask: what is the underlying method, not just the one-off example?

Capture:
- When to use the skill
- What it produces
- Step-by-step actions
- Branches when requirements are unclear or incomplete
- Completion criteria

### 3. Clarify if the workflow is ambiguous
If the process is not clear enough, confirm:
- what outcome should the skill produce
- whether it is workspace-scoped or personal
- whether the user wants a quick checklist or a full multi-step workflow
- which decision points are required

### 4. Draft the `SKILL.md`
Create a file in the correct location:
- Project-level: `.github/skills/<skill-name>/SKILL.md`
- Personal: `~/.copilot/skills/<skill-name>/SKILL.md`

Use this format:

```yaml
---
name: skill-name
description: "What and when to use. Include trigger words for discovery."
argument-hint: "Optional hint shown when invoked"
user-invocable: true
---
```

Then include the body with:
- `## When to Use`
- `## Procedure`
- `## Decision Points`
- `## Completion Checklist`

### 5. Validate the skill
Before finishing, verify:
- the `name` matches the folder name
- the description is keyword-rich and specific
- the workflow is clear and actionable
- the steps are practical and repeatable
- completion checks are defined
- no broken or unnecessary relative references are included

### 6. Iterate
Improve the skill by addressing weak or ambiguous sections.
Focus on:
- unclear triggers
- missing decision branches
- vague completion criteria
- overlong or monolithic instructions

## Completion checklist
The skill is ready when all of the following are true:
- It captures a real, reusable workflow
- It states when to use it
- It contains a clear step-by-step procedure
- It includes decision points and branching logic
- It defines quality checks or completion criteria
- It is saved in the correct skill directory
- Its frontmatter is valid and consistent with the folder name

## Example prompts
- "Turn this debugging workflow into a reusable skill"
- "Create a skill for code review and validation"
- "Package this implementation routine as a project skill"
- "Draft a skill that captures when to ask clarifying questions and when to proceed"

## Related customizations to create next
- A project instruction for coding conventions
- A prompt for one-off analysis or validation tasks
- A custom agent for specialized multi-step workflows
- A hook for deterministic validation or formatting steps
