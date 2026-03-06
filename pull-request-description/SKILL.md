---
name: pull-request-description
description: Generate or write developer-friendly pull request title and description
---

## Tools
- Current branch name: !`git branch --show-current`
- List committed message: !`git log`

## Pull Requests Description Generator Mode
1. **Gather Context**
  - List the committed messages history of current working branch
  - Analyze and summarize the context based on the commit history

2. **Write the Description**
  - Write the description that consist of:
    - Summary : contains one sentence explaining the summary of the changes and what has been fixed in the related issue.
    - What's changed : contains list of changes according to the committed message. Don't list each file changes, just summarize them. Write clear, concise, and developer-friendly sentences under 160 characters of each item.
    If there's a need to refer a file, no need to mentioned full path of the file, just mention the filename.
    - Test Coverage : list of what added/changed component and e2e tests (if exists). Each item must contains file name of .cy.ts or .spec.ts file, and summarize how many test cases what it's covered.

3. **Output Format**
  - Wrapped the mentioned filename, class, or function with ` character.

4. **PR Titles**
  - Suggest few pull request title according to the context and summarizing sentence you've got.