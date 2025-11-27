---
description: Triage user input to separate Constitution principles from Specification features. Use when user provides broad/mixed content.
handoffs: 
  - label: Create Constitution
    agent: speckit.constitution
    prompt: Use the Constitution content extracted below
  - label: Create Specification
    agent: speckit.specify
    prompt: Use the Specification content extracted below
---

## User Input

```text
$ARGUMENTS
```

You **MUST** analyze the user input and separate it into appropriate categories.

## Purpose

This command helps users who provide broad, mixed content (combining principles and features) by automatically separating what belongs to Constitution vs. Specification.

**Use this when**:
- User describes a project mixing general rules with specific features
- User provides voice transcription or unstructured thoughts
- User is unsure what goes where

## Triage Process

### Step 1: Analyze the Input

Read the entire input and identify:

1. **Constitution Content** (principles, rules, constraints):
   - Statements that apply to ALL features (not just one)
   - Long-term principles that won't change per feature
   - Quality standards, coding practices, architectural constraints
   - User profile/preferences that affect how AI should behave
   - Technology stack preferences (without specific implementation)
   - Compliance, security, or regulatory requirements
   
   **Indicators**:
   - "Always...", "Never...", "All features must..."
   - "The system should always...", "We prefer..."
   - "Our stack is...", "We use..."
   - "I'm not a developer, so..."

2. **Specification Content** (features, behaviors, capabilities):
   - Specific functionality to be built
   - User stories and journeys
   - Particular screens, APIs, or interactions
   - Feature-specific requirements
   - Measurable outcomes for a specific capability
   
   **Indicators**:
   - "Build a...", "Create a...", "I want to..."
   - "The user should be able to..."
   - "When the user clicks...", "The screen shows..."
   - Specific workflow descriptions

3. **Ambiguous Content** (needs clarification):
   - Statements that could be either principle or feature
   - Incomplete thoughts that need more context

### Step 2: Present the Triage

Output the separation in this format:

```markdown
# Triage Result

## 📜 Constitution (Principles & Rules)

> These will be added to your project's Constitution using `/speckit.constitution`

### Extracted Principles:

1. **[Principle Name]**: [Description]
2. **[Principle Name]**: [Description]
...

### Raw Text for Constitution:

```text
[Cleaned up text ready to paste into /speckit.constitution]
```

---

## 📋 Specification (Features & Behaviors)

> These will create feature specifications using `/speckit.specify`

### Extracted Features:

1. **[Feature Name]**: [Brief description]
2. **[Feature Name]**: [Brief description]
...

### Raw Text for Specification:

```text
[Cleaned up text ready to paste into /speckit.specify]
```

---

## ❓ Needs Clarification

> These items are ambiguous. Please clarify:

1. **"[Quote from input]"**
   - If this is a PRINCIPLE (applies to all features): → Constitution
   - If this is a FEATURE (specific functionality): → Specification
   - **Your choice**: _[Wait for user]_

---

## Next Steps

1. Review the separation above
2. Clarify any ambiguous items
3. Choose how to proceed:
   - **Option A**: I'll execute both `/speckit.constitution` and `/speckit.specify` with the separated content
   - **Option B**: You want to review/edit the content first
   - **Option C**: Only execute one of them (specify which)

**Your choice**: _[A/B/C]_
```

### Step 3: Execute Based on User Choice

**If user chooses A (execute both)**:
1. First, run `/speckit.constitution` with the Constitution content
2. Wait for completion
3. Then run `/speckit.specify` with the Specification content

**If user chooses B (review first)**:
1. Wait for user edits
2. Re-present the edited content for confirmation
3. Execute as directed

**If user chooses C (only one)**:
1. Execute only the specified command

## Guidelines

### What Goes to Constitution:

- User profile: "I'm not a developer", "I prefer visual explanations"
- Stack preferences: "We use MongoDB", "Prefer official drivers"
- Quality standards: "Always include tests", "Use established libraries"
- Communication style: "Explain commands before running", "Use simple language"
- Architectural principles: "Event-driven", "Microservices", "Multi-tenant"
- Compliance: "LGPD compliance required", "Audit trail mandatory"

### What Goes to Specification:

- Specific features: "Build a dashboard", "Create login screen"
- User stories: "User can upload files", "Admin can manage users"
- Workflows: "When user submits form, system validates and saves"
- Integrations: "Connect to payment gateway X"
- Specific screens/pages: "Home page shows...", "Settings screen has..."

### Handling Voice Transcriptions:

Voice input often mixes topics. When processing voice transcriptions:
1. Clean up repetitions and filler words
2. Identify topic shifts (often indicated by "also", "another thing", "by the way")
3. Group related thoughts even if scattered in the input
4. Ask for clarification on truly ambiguous parts

## Example

**User Input**:
> "Quero criar um sistema de gestão de conhecimento. Sempre usar MongoDB Atlas, nunca outro banco. O usuário pode criar pastas e arquivos. Eu não sou desenvolvedor então preciso de explicações claras. O sistema deve ter um dashboard com métricas. Usar sempre componentes consolidados."

**Triage Output**:

### Constitution:
- Stack: "Sempre usar MongoDB Atlas, nunca outro banco"
- User Profile: "Não sou desenvolvedor, preciso de explicações claras"
- Components: "Usar sempre componentes consolidados"

### Specification:
- Feature 1: "Sistema de gestão de conhecimento"
- Feature 2: "Usuário pode criar pastas e arquivos"
- Feature 3: "Dashboard com métricas"

