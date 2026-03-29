# Custom Agents and Skills Repository

This repository contains reusable VS Code Copilot customizations for:

- custom agents (`.agent.md`)
- task-specific skills (`SKILL.md`)
- workspace guidance (`AGENTS.md`)

The goal is to provide reliable, discoverable AI workflows for React implementation, documentation quality, diagrams, testing, and RSuite component work.

## Repository Structure

```text
.github/
  AGENTS.md
  agents/
    senior-react-portfolio.agent.md
    docs-diagrams-specialist.agent.md
  skills/
    communication-grammar-coach/
      SKILL.md
    playwright-test-maker/
      SKILL.md
    rsuite-component-generator/
      SKILL.md
    vitest-test-maker/
      SKILL.md
```

## Included Agents

### Senior React Portfolio

Use for:

- architecture decisions
- performance analysis
- accessibility reviews
- test strategy and implementation
- maintainable React refactors

Handoff behavior:

- routes docs-only and diagram tasks to `Docs and Diagrams Specialist`

File:

- `.github/agents/senior-react-portfolio.agent.md`

### Docs and Diagrams Specialist

Use for:

- README and docs rewrites
- architecture explanations
- Mermaid authoring and validation
- docs consistency checks

Handoff behavior:

- routes runtime/component implementation requests back to `Senior React Portfolio`

File:

- `.github/agents/docs-diagrams-specialist.agent.md`

## Included Skills

### vitest-test-maker

Use for:

- failing unit tests
- async test reliability
- mocking and coverage improvements

File:

- `.github/skills/vitest-test-maker/SKILL.md`

### playwright-test-maker

Use for:

- screenshot mismatches
- selector timeout failures
- diagram and e2e spec updates

File:

- `.github/skills/playwright-test-maker/SKILL.md`

### rsuite-component-generator

Use for:

- RSuite forms, modals, layouts, and cards
- props API cleanup
- accessibility-focused component updates

File:

- `.github/skills/rsuite-component-generator/SKILL.md`

### communication-grammar-coach

Use for:

- rewriting docs and README text
- improving tone and clarity
- recruiter-friendly technical writing

File:

- `.github/skills/communication-grammar-coach/SKILL.md`

## How to Use in Chat

1. Open the agent picker.
2. Choose `Senior React Portfolio` or `Docs and Diagrams Specialist`.
3. Prompt naturally (the descriptions include trigger phrases).
4. Allow automatic handoff when task scope shifts.

## Prompt Examples

Implementation-focused:

- "Refactor this React component and add tests for edge cases."
- "Why is this test red, and can you fix it?"

Docs and diagram-focused:

- "Go over this README and make it more professional."
- "I have a screenshot mismatch in diagram snapshots."

RSuite-focused:

- "Build this RSuite modal form and clean up the props API."

## Discovery Checklist

Use this quick checklist after changes:

1. Agent picker shows both agents.
2. Docs task from `Senior React Portfolio` routes to `Docs and Diagrams Specialist`.
3. Runtime task from `Docs and Diagrams Specialist` routes to `Senior React Portfolio`.
4. A Vitest failure prompt loads `vitest-test-maker` behavior.
5. A Playwright snapshot prompt loads `playwright-test-maker` behavior.
6. A writing polish prompt loads `communication-grammar-coach` behavior.

## Authoring Rules

- Keep skill `name` lowercase-hyphen and matched to folder name.
- Keep descriptions explicit with trigger wording.
- Use YAML spaces (not tabs) in frontmatter.
- Keep each skill focused on one workflow domain.

## License

Add your preferred license for reuse and distribution.
