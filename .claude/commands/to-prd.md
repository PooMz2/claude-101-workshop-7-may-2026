This skill takes the current conversation context and codebase understanding and produces a PRD. Do NOT interview the user — just synthesize what you already know.

## Process

1. Explore the repo to understand the current state of the codebase, if you haven't already.

2. Sketch out the major modules you will need to build or modify to complete the implementation. Check with the user that these modules match their expectations.

3. Write the PRD using the template below and submit it as a GitHub issue.

## PRD Template

### Problem Statement

The problem that the user is facing, from the user's perspective.

### Solution

The solution to the problem, from the user's perspective.

### User Stories

A numbered list of user stories in the format: "As an <actor>, I want a <feature>, so that <benefit>"

### Implementation Decisions

- The modules that will be built/modified
- Architectural decisions
- Schema changes
- API contracts

Do NOT include specific file paths or code snippets.

### Testing Decisions

- Which modules will be tested
- What makes a good test (only test external behavior, not implementation details)

### Out of Scope

A description of things that are out of scope for this PRD.
