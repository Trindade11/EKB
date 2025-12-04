# Project Workplan

> Agent orchestration plan: which agents to call, in what order, and current status.

---

## Current Phase

**Active Phase**: 0 – Setup  
**Next Recommended Action**: Run `/speckit-context` to initialize project context  

---

## Agent Execution Plan

| # | Phase | Agent | Goal | Status | Notes |
|---|-------|-------|------|--------|-------|
| 0 | Setup | `/speckit-context` | Initialize project context | ⬜ TODO | Required for new projects |
| 1 | Triage | `/speckit-triage` | Clarify scope, macro view, backlogs | ⬜ TODO | Multi-round |
| 2 | Constitution | `/speckit-constitution` | Consolidate principles & rules | ⬜ TODO | After triage stabilizes |
| 3 | Specification | `/speckit-specify` | Create feature specs | ⬜ TODO | Per feature |
| 4 | Planning | `/speckit-plan` | Technical design & structure | ⬜ TODO | Includes DP1 |
| 5 | Tasks | `/speckit-tasks` | Break plan into tasks | ⬜ TODO | – |
| 6 | Implementation | `/speckit-implement` | Execute tasks, create code | ⬜ TODO | – |

**Legend**: ⬜ TODO | 🔄 IN_PROGRESS | ✅ DONE | ⏭️ SKIPPED

---

## Decision Points

| ID | Decision | Description | Status | Decided At | Link |
|----|----------|-------------|--------|------------|------|
| DP1 | Project Structure | Define folder structure and module organization | ⬜ PENDING | – | `folder-structure.md` |
| DP2 | Tech Stack | Core technologies, frameworks, and constraints | ⬜ PENDING | – | `constitution.md` |

---

## Triage Rounds Log

<!-- Each triage round should be logged here to track progressive refinement -->

| Round | Date | Focus | Outputs Updated | Gaps Remaining |
|-------|------|-------|-----------------|----------------|
| 1 | – | – | – | – |

---

## Backlog Summary

### Constitution Backlog

<!-- Items identified during triage that should become project principles/rules -->

- (none yet)

### Specification Backlog

<!-- Features/capabilities identified during triage that need specs -->

- (none yet)

---

## Project Start Checklist

Use this checklist to ensure proper project initialization:

- [ ] **Step 0**: Run `/speckit-context` to create project context structure
- [ ] **Step 1**: Run `/speckit-triage` (first round) to capture initial scope
- [ ] **Step 2**: Continue `/speckit-triage` (N rounds) until macro view is stable
- [ ] **Step 3**: Decision Point DP1 – Define project structure
- [ ] **Step 4**: Run `/speckit-constitution` to consolidate principles
- [ ] **Step 5**: Run `/speckit-specify` for priority features
- [ ] **Step 6**: Run `/speckit-plan` for technical design
- [ ] **Step 7**: Run `/speckit-tasks` to break into actionable items
- [ ] **Step 8**: Run `/speckit-implement` to execute

---

## Quick Links

- [Project Overview](./project-overview.md)
- [Folder Structure](./folder-structure.md)
- [Constitution](../memory/constitution.md)
- [Learnings](./learnings.md)

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| V1 | – | Initial workplan created |
