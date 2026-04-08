---
name: git-commit
description: Write commit message of staged files in current working directory
---

## Tools
- Current working directory: !`pwd`
- Current git diff (staged): !`git diff --cached`
- Current branch: !`git branch --show-current`

## What I do

1. **Gather context** :
   - Analyze the staged changes in current working directory.
   - Get the task number based on current branch name after "/" character <task-number>

2. **Writing commit message** :
   - Start with a type (feat/fix/docs/chore/refactor) according your judgement of the changes as <prefix>.
   - Write clear, concise, and developer-friendly sentence in under 160 characters <commit-title>
   - Accurately describe what the code changed in the current staged files only.
   - Use present tense and imperative mood. Explain what and why, not how.
   - Add task number with "#" character at the end of the commit message title. eg: <prefix>: <commit-title> #<task-number>
   - Lists the specific implementation details how the change are if the commit message title isn't enough to explain the changes:
     - Write as bullet points add new blank line before writing it
     - This lists aren't necessary when the commit message title is already clear and self-explanatory describing the  changes
     - The explanation for each point must be unique one each other; there should be no repetition of information or context.

3. **Output Format**
   - Format as plain text without any markdown format character
   - DON'T ADD YOUR SIGNATURE at the end of the commit message.
   - DON'T EXECUTE git commit message command

## When to use me

Ask clarifying questions if there's no staged files for commit or the code changes are massive.

