## What does this change?

<!-- One or two sentences. Link the issue: Closes #123 -->

## Why?

<!-- What was wrong, and what did it cost? The diff shows what changed;
     this is the part that is expensive to reconstruct in six months. -->

## Type of change

- [ ] New test coverage
- [ ] Fix for a failing or flaky test
- [ ] Framework, fixture or application change
- [ ] CI/CD pipeline change
- [ ] Documentation

## Test-quality checklist

- [ ] The test fails when the feature is broken (I checked by breaking it)
- [ ] No hard waits — auto-waiting or an explicit expectation only
- [ ] No hard-coded URLs or credentials — everything through config
- [ ] No dependency on another test's data or ordering
- [ ] Passes in parallel as well as serially
- [ ] Locators use role, label or test-id, not brittle CSS or XPath
- [ ] Correct marker or tag applied (`smoke` is the critical path only)
- [ ] Lint and type-check are clean

## CI

- [ ] All required checks are green
- [ ] If I changed a workflow, the description says why

## Evidence

<!-- A trace, a screenshot, or a link to the green run. For a fixed failure,
     the run that proves it. -->
