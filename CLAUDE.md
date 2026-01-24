# Project: cybershield-rural

## Workflow Instructions for Claude

When starting a new conversation in this project:

1. **Query GitHub for current state** - Run `./scripts/get-status.sh` or use `gh` commands
2. **Announce the current state** - Tell the user what phase we're in and what's active
3. **Show available actions** - Based on the phase, show what they can do

### How to Get Current State

```bash
# Run the status script (if available)
./scripts/get-status.sh

# Or query directly with gh CLI
gh issue list --label "status:active" --json number,title

# Get sub-issues for an epic
gh sub-issue list <epic-number>
```

### Workflow Phases

| Phase | Condition | Available Actions |
|-------|-----------|-------------------|
| IDLE | No active epic | `plan [feature]`, `status` |
| PLANNING | Active epic, no active task | `approve plan`, `revise plan`, `cancel` |
| EXECUTING | Active epic + active task | `continue`, `pause`, `complete task`, `blocked` |

### Commands I Respond To

- `status` - Query GitHub and show current project state
- `plan [feature]` - Create a new epic with tasks (as sub-issues)
- `approve plan` - Start executing the first task
- `revise plan` - Modify the epic/tasks in GitHub
- `cancel` - Close the epic without executing
- `continue` - Work on the active task
- `complete task` - Close current task, move to next
- `blocked [reason]` - Mark current task as blocked

### The `plan` Command Flow

When user says `plan [feature]`, use chat-based planning with iteration:

1. **Enter plan mode** - Call `EnterPlanMode` for safe exploration (restricted tools)
2. **Explore and analyze** - Research the codebase, gather context, break into tasks
3. **Present plan in chat** - Show the epic and tasks directly in conversation (no plan file)
4. **Iterate in chat** - User says "change X" → Claude revises and shows updated plan
5. **On approval** - User says "approved" → Exit plan mode → Create GitHub issues
6. **Show the user the GitHub links** - Epic URL and task URLs

**Example flow:**
```
User: plan user auth
Claude: [enters plan mode, explores]
Claude: "Here's the plan:

         **Epic: User Authentication**
         Vision: Enable users to securely log in and maintain sessions

         **Tasks:**
         1. Add login endpoint
         2. Add session management
         3. Add logout endpoint

         Want me to revise anything?"
User: "Add password reset"
Claude: [shows updated plan with task 4]
User: "Approved"
Claude: [exits plan mode, creates GitHub issues]
```

**Why this approach:**
- Plan mode enables safe exploration (can't accidentally edit code)
- Chat-based iteration is fast - no intermediate files
- GitHub issues are created only after approval (reduces noise)
- Plan graduates to GitHub as the permanent source of truth

**Do NOT:**
- Skip `EnterPlanMode` - always use plan mode for safe exploration
- Create GitHub issues before user says "approved"
- Write to a plan file - iterate in chat instead
- Start implementing before GitHub issues exist

### Creating Epics and Tasks

```bash
# Create an epic
gh issue create --title "Epic: Feature Name" --label "status:active" --body "..."

# Create tasks as sub-issues
gh sub-issue create --parent <epic-number> --title "Task name" --label "status:planned"

# Mark a task as active
gh issue edit <task-number> --remove-label "status:planned" --add-label "status:active"

# Complete a task
gh issue close <task-number>
```

### Issue Structure (Specification-Driven)

Issues are structured as executable specifications. Key sections:

**For Epics:**
- Vision, User Stories, Technical Architecture
- Success Criteria (verifiable), Constraints (MUST/MUST NOT/SHOULD)
- Task Breakdown with dependencies, Decisions Log
- Session Notes (update during work)

**For Tasks:**
- Objective (WHAT/WHY, not HOW)
- Context (parent epic, current state, related files, pattern references)
- Requirements (numbered, independently testable)
- Constraints and Non-Goals (prevent scope creep)
- Acceptance Criteria (machine-verifiable with commands)
- Verification Commands (copy-paste block)
- Examples (input/output pairs)
- Session Notes (update when pausing/resuming)

### Working on a Task (Explore → Plan → Code → Commit)

1. **Explore**: Read files listed in Context section
2. **Plan**: Create implementation plan from Requirements, respect Constraints
3. **Code**: Implement within boundaries, reference Examples
4. **Commit**: Run Verification Commands, confirm Acceptance Criteria pass

**Session Handoff**: Update Session Notes before ending work:
```markdown
## Session Notes
**Latest update**: 2025-01-12
- **Status**: In progress - 70% complete
- **Files modified**: `src/auth/session.ts`, `tests/auth/session.test.ts`
- **Decisions made**: Used existing RateLimiter class
- **Blockers**: None
- **Next step**: Add error handling for edge case
```

### Session Start Announcement Format

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
 PROJECT: cybershield-rural
 PHASE: [from GitHub query]
 EPIC: [from GitHub query]
 TASK: [from GitHub query]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Available actions:
  • [based on phase]

What would you like to do?
```

### For Onboarded Projects

If this project was onboarded to pm-workflow (vs created fresh), on first session:

1. **Audit the codebase** - Explore to understand structure, patterns, existing code
2. **Check for existing issues** - Run `gh issue list` to see any open work
3. **Look for TODOs** - Search for TODO/FIXME comments that could become tasks
4. **Ask the user** - Clarify what they want to work on

---

## Project Context

**Description:** **Managed Cybersecurity for Critical Access Hospitals**

**Tech Stack:** Unknown

**Repo:** https://github.com/CdrAppDev/cybershield-rural

---

## Labels Reference

| Label | Purpose |
|-------|---------|
| `status:active` | Currently being worked on |
| `status:planned` | Queued for future work |
| `status:blocked` | Waiting on something |

Note: Issue close state = done. Sub-issue hierarchy = epic/task type.

---

<!--
STATE IS NOT STORED HERE

All project state (epics, tasks, progress) lives in GitHub:
- Epics = Issues with sub-issues
- Tasks = Sub-issues under epics
- Status = Labels on issues
- History = Issue comments and activity

Query GitHub for current state, don't duplicate it here.
-->
