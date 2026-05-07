# Test-Driven Development

## Philosophy

**Core principle**: Tests should verify behavior through public interfaces, not implementation details. Code can change entirely; tests shouldn't.

**Good tests** are integration-style: they exercise real code paths through public APIs. They describe _what_ the system does, not _how_ it does it.

**Bad tests** are coupled to implementation. They mock internal collaborators, test private methods, or verify through external means.

## Anti-Pattern: Horizontal Slices

**DO NOT write all tests first, then all implementation.** Use vertical slices via tracer bullets. One test → one implementation → repeat.

```
RIGHT (vertical):
  RED→GREEN: test1→impl1
  RED→GREEN: test2→impl2
  RED→GREEN: test3→impl3
```

## Workflow

### 1. Planning

Before writing any code:

- Confirm with user what interface changes are needed
- Confirm with user which behaviors to test (prioritize)
- Design interfaces for testability
- List the behaviors to test (not implementation steps)
- Get user approval on the plan

### 2. Tracer Bullet

Write ONE test that confirms ONE thing about the system:

```
RED:   Write test for first behavior → test fails
GREEN: Write minimal code to pass → test passes
```

### 3. Incremental Loop

For each remaining behavior:

```
RED:   Write next test → fails
GREEN: Minimal code to pass → passes
```

Rules: One test at a time. Only enough code to pass current test. Don't anticipate future tests.

### 4. Refactor

After all tests pass: extract duplication, deepen modules, apply SOLID principles. Run tests after each refactor step. **Never refactor while RED.**
