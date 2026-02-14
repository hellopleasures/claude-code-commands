# Implement Plan

Execute the agreed plan step-by-step.

## Requirements

1. Follow the plan sequentially, noting any deviations
2. Write **real, functional code** — no stubs, placeholders, or TODOs
3. Handle errors and edge cases as you go
4. Commit logical chunks with clear explanations

## Rules

- If you encounter blockers or the plan needs revision, **STOP and discuss** before proceeding
- Always implement fully finished, fully fleshed out working production code
- Do NOT use unnecessary try/catch or fallbacks unless truly needed
- Do NOT stub code, add TODOs, or simplify — always do the complete version
- Follow the project's coding standards from CLAUDE.md
- Include proper TypeScript types for all code
- Add validation with Zod for user inputs
- Include audit logging for data mutations

## Quality Checks

Before marking each step complete:
- [ ] Code compiles without errors
- [ ] Types are complete (no `any`)
- [ ] Validation is in place for inputs
- [ ] Error handling is appropriate
- [ ] Code follows existing patterns in the codebase
