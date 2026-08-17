# Language and Framework Notes

Apply only the sections relevant to the current project. Existing repository conventions take precedence.

## TypeScript and Node.js

- Preserve useful types at boundaries; do not use `any` merely to silence uncertainty.
- Treat parsed JSON, environment input, query parameters, and external responses as untrusted.
- Be deliberate about whether missing, `undefined`, and `null` have different meanings.
- Await promises intentionally and handle rejected work.
- Clean up timers, streams, listeners, and abort signals.
- Define ordering, limits, cancellation, timeout, and failure behavior for concurrent work.
- Distinguish expected operational failures from programming errors.
- Follow the project's existing module, formatting, and testing conventions.

## React

- Keep server state, form state, and derived display state conceptually separate.
- Avoid effects for values that can be derived during rendering.
- Give effects correct dependencies and cleanup behavior.
- Use stable identifiers as list keys.
- Represent loading, empty, success, and error states explicitly.
- Prevent accidental repeated submissions and show progress or failure near the initiating action.
- Prefer semantic HTML, associated labels, visible focus, and keyboard-accessible interactions.
- Treat server-side validation and authorization as the security boundary.
- Test behavior from the user's perspective rather than component internals.

## Python

- Use clear domain types and validate untrusted input at boundaries.
- Avoid mutable default arguments and overly broad exception handling.
- Preserve useful exception context.
- Use context managers for files, locks, sessions, and transactions.
- Be explicit about timezone-aware dates and serialization behavior.
- Avoid blocking I/O on an asynchronous event loop and define cancellation behavior.
- Follow the project's existing formatting, linting, typing, and testing conventions.

## HTTP APIs

- Design around resources and user outcomes rather than implementation details.
- Validate path, query, header, and body inputs.
- Use status codes and error responses consistently.
- Keep authentication separate from object-level authorization.
- Set intentional request-size, pagination, and resource limits.
- Define idempotency and retry behavior for writes where necessary.
- Do not expose stack traces, internal details, or sensitive data.
- Preserve compatibility when changing external contracts.

## SQL and Relational Data

- Design from access patterns and domain invariants.
- Use database constraints for rules that must always hold.
- Parameterize queries and never construct SQL from raw user input.
- Select only needed columns and bound potentially large results.
- Add indexes for demonstrated access paths while considering write cost.
- Use transactions when related changes must succeed or fail together.
- Consider isolation, lost updates, uniqueness races, and lock duration.
- Avoid N+1 queries and unnecessary round trips.
- Make migrations backward-compatible when the rollout may involve mixed application versions.

## Full-Stack Applications

- Keep contracts consistent across the interface, API, and persistence layers.
- Prove a small end-to-end path before expanding individual layers.
- Validate input at both the user-experience boundary and the trusted server boundary.
- Handle loading, empty, success, and failure states coherently.
- Avoid duplicating domain rules in ways that can silently diverge.
- Test important integration boundaries in addition to isolated units.

## Concurrency and Background Work

- Define maximum concurrency, fairness, and ordering.
- Define success, failure, timeout, cancellation, and shutdown behavior.
- Clarify whether timed-out work continues in the background.
- Bound retries and use backoff where appropriate.
- Make repeated or duplicate delivery safe when necessary.
- Clean up resources on every completion path.
- Prefer deterministic tests using controlled promises, clocks, or dependencies.
LANGUAGE_FRAMEWORK_NOTES.md
