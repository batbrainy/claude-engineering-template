# Claude Engineering Template

A small, reusable set of instructions for working with Claude Code as a senior engineering pair programmer.

The files are generic and can be copied into almost any software project without modification. They contain no project-specific commands, placeholders, dependencies, or configuration.

## Included Files

- **`CLAUDE.md`** — Core engineering principles, change discipline, verification expectations, and communication guidance.
- **`LANGUAGE_FRAMEWORK_NOTES.md`** — Relevant guidance for TypeScript, Node.js, React, Python, HTTP APIs, SQL, full-stack applications, and concurrent work.
- **`REVIEW_CHECKLIST.md`** — A technology-neutral checklist Claude can use to review its own changes.

## Usage

Copy the three Markdown files into the root of a repository and start Claude Code from that directory.

Claude will use `CLAUDE.md` as its primary instructions and consult the other files when relevant. Existing project conventions and repository-specific instructions take precedence.

## Principles

The template encourages Claude to:

- Act as a pragmatic senior engineer.
- Understand existing code before changing it.
- Make small, focused, maintainable changes.
- Follow established repository conventions.
- Consider correctness, security, reliability, accessibility, and performance.
- Test and review its work.
- Preserve existing and unrelated changes.
- Avoid commits, pushes, deployments, dependency installation, and destructive operations unless explicitly requested.
- Communicate assumptions, tradeoffs, risks, and verification results clea
