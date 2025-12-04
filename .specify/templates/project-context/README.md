# Project Context Templates

> Templates for documenting project-specific technical context

## Overview

These templates help you document critical project information that AI agents need to work effectively. This documentation lives in your project's `project-context/` folder (outside `.specify/`).

## Quick Start

1. Run `/speckit-context` to initialize your project context
2. Fill in each template with your project's specific information
3. AI agents will automatically read this context when processing requests

## Templates

| Template | Purpose | When to Fill |
|----------|---------|--------------|
| `project-workplan.md` | **Agent orchestration plan** | **First file - created by context/triage** |
| `project-overview.md` | **Macro view + status + gaps** | **Created with workplan by triage** |
| `env-vars.md` | Environment variables documentation | After setting up `.env` |
| `database-schema.md` | Semantic database schema | When designing data model |
| `tools-registry.md` | Available tools and MCPs | After configuring integrations |
| `agent-framework.md` | Agent architecture documentation | If building agentic system |
| `folder-structure.md` | Project organization guide | At project start |
| `learnings.md` | Project learnings and decisions | Ongoing throughout project |

### Project Workplan (Required)

`project-workplan.md` is the **orchestration artifact** for the project. It:

- Tracks **which agent to call next** in the workflow
- Shows the **status of each phase** (TODO/IN_PROGRESS/DONE)
- Logs **triage rounds** for progressive refinement
- Tracks **decision points** (project structure, tech stack)
- Maintains **backlog summaries** for constitution and specs
- Provides a **project start checklist** for new projects

### Project Overview (Required)

`project-overview.md` is the **central artifact** for the project. It:

- Shows the **macro view** with the main functional blocks
- Tracks the **completion status** of all artifacts
- Lists **identified gaps** that need attention
- Is **automatically updated** by all main Spec Kit commands
- Acts as a **visual dashboard** for project progress

## File Structure

After running `/speckit-context`, your project will have:

```
project-root/
├── .specify/              # Spec Kit (generic toolkit)
│   └── templates/
│       └── project-context/  # These templates
│
├── project-context/       # YOUR PROJECT'S CONTEXT (specific)
│   ├── project-workplan.md   # 🎯 ORCHESTRATION (required, created first)
│   ├── project-overview.md   # 🎯 MACRO VIEW (required, created with workplan)
│   ├── env-vars.md
│   ├── database-schema.md
│   ├── tools-registry.md
│   ├── agent-framework.md
│   ├── folder-structure.md
│   └── learnings.md
│
├── tests/                 # All test files
├── agents/                # Agent definitions (if applicable)
├── docs/                  # Project-specific documentation & diagrams
│   └── flows/             # Mermaid diagrams for project flows
└── ...
```

## Why This Matters

### For AI Agents

- **Faster context loading**: Agents read structured docs instead of scanning code
- **Consistent understanding**: Same context interpretation across all interactions
- **Reduced hallucination**: Real env vars, real schemas, real tools
- **Better suggestions**: Agents know what's available and what's not

### For Humans

- **Onboarding**: New team members understand project setup quickly
- **Documentation**: Single source of truth for technical context
- **Decision history**: Learnings file captures why decisions were made

## Best Practices

1. **Keep it current**: Update context when things change
2. **Be specific**: Use actual values, not placeholders
3. **Add semantic meaning**: Explain WHAT things are, not just list them
4. **Link to details**: Reference external docs when needed
5. **Review periodically**: Context can drift from reality

## Related

- Constitution principle IX: Project Context Documentation
- Constitution principle X: Folder Organization
- `/speckit-context` command

