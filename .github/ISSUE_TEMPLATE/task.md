---
name: Task
about: A single unit of work (create as sub-issue of an epic)
title: ''
labels: status:planned
assignees: ''
---

## Objective
<!-- Single sentence: What changes and why? Separate WHAT from HOW. -->

## Context
<!-- Situational awareness for Claude Code -->
- **Parent epic**: #
- **Current state**:
- **Problem**:
- **Related files**: `src/`, `tests/`
- **Pattern reference**: <!-- e.g., "Follow pattern in `src/auth/login.ts`" -->

## Requirements
<!-- Numbered, independently testable outcomes. Not implementation steps. -->
1.
2.
3.

## Constraints
<!-- Boundaries to prevent scope creep. Use RFC 2119 language. -->
- **MUST**:
- **MUST NOT**:
- **SHOULD**:

## Non-Goals
<!-- Explicitly out of scope for this task -->
-

## Acceptance Criteria
<!-- Machine-verifiable conditions. Each should map to a command. -->
- [ ] Tests pass: `npm test -- --grep ""`
- [ ] Type check passes: `npm run typecheck`
- [ ] Lint passes: `npm run lint`
- [ ] Manual verification:

## Verification Commands
<!-- Copy-paste block for Claude Code to run -->
```bash
npm run typecheck
npm run lint
npm test -- --grep ""
npm run build
```

## Examples
<!-- Concrete input/output to reduce ambiguity -->
**Input:**
```json

```

**Expected output:**
```json

```

**Error case:**
-

## Implementation Steps
<!-- Optional: Will be tracked via TodoWrite -->
1. [ ]
2. [ ]
3. [ ]

## Session Notes
<!-- Claude Code updates this section during work -->
**Latest update**:
- **Status**:
- **Files modified**:
- **Decisions made**:
- **Blockers**:
- **Next step**:

---
<!--
CREATE AS SUB-ISSUE

This task should be linked to a parent epic. Use:

    gh sub-issue create --parent <epic-number> --title "Task name" --label "status:planned"

Or use the "Create sub-issue" button on the parent epic.

WORKFLOW: Explore → Plan → Code → Commit
1. Read files in Context section
2. Create plan based on Requirements
3. Implement within Constraints
4. Run Verification Commands
5. Update Session Notes if pausing
-->
