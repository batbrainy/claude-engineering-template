# Review Checklist

Use this checklist to review your own work. Apply only the items relevant to the change, prioritize correctness and risk, and distinguish confirmed problems from optional improvements.

## Requirements and scope

- The change satisfies the requested outcome and stated constraints.
- Assumptions are reasonable and material ambiguities are surfaced.
- The implementation does not introduce unrelated changes or unrequested behavior.
- Public behavior and compatibility are preserved unless intentionally changed.

## Correctness and reliability

- Main paths, boundary cases, and expected failures behave correctly.
- State transitions cannot become contradictory or permanently stuck.
- Errors preserve useful context without exposing sensitive information.
- Async behavior accounts for races, duplicate work, timeouts, retries, cancellation, and cleanup where relevant.
- Contracts remain consistent across components, APIs, and persistence layers.

## Design and maintainability

- The solution follows existing architecture and conventions.
- Names, control flow, and abstractions are clear and proportional to the problem.
- Logic is not unnecessarily duplicated.
- There is no dead code, temporary debugging output, or stale commentary.
- Dependencies and configuration changes are necessary and justified.

## Security and privacy

- Inputs are validated at trust boundaries.
- Authentication and object-level authorization are enforced where required.
- User-controlled values are handled safely.
- Secrets and sensitive data are absent from code, output, errors, and logs.
- Access is no broader than necessary.

## Data and performance

- Data constraints reflect domain invariants.
- Writes are atomic where partial completion would be unsafe.
- Queries and loops are bounded and avoid obvious repeated work.
- Concurrency cannot silently corrupt or overwrite state.
- Performance complexity is appropriate for expected use.

## User experience and accessibility

- Loading, empty, success, disabled, and error states are coherent where relevant.
- User-facing errors are clear and actionable.
- Interactions use appropriate semantics, labels, focus behavior, and keyboard support.
- Repeated actions cannot accidentally create duplicate effects.

## Verification and delivery

- Tests cover observable changed behavior and important failure cases.
- Relevant tests, type checks, linting, and builds were run when available.
- The complete diff contains only intended changes.
- Existing work was preserved.
- Verification results and any remaining limitations are reported accurately.
