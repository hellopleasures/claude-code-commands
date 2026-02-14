# Code Quality Pass

Review and refactor the current code for quality.

## Criteria

| Attribute | Description |
|-----------|-------------|
| **Compact** | Remove dead code, redundancy, over-abstraction |
| **Concise** | Simplify verbose logic, use idiomatic patterns |
| **Clean** | Consistent naming, clear structure, proper formatting |
| **Capable** | Handles edge cases, fails gracefully, performs well |

## Checklist

- [ ] No unused imports or variables
- [ ] No duplicate code that should be extracted
- [ ] No over-engineered abstractions
- [ ] Consistent naming conventions per CLAUDE.md
- [ ] Proper TypeScript types (no `any`)
- [ ] Idiomatic patterns for the framework (Next.js, React, Mongoose)
- [ ] Error messages are helpful and actionable
- [ ] Edge cases are handled appropriately

## Rules

- Make sure work is fully finished before this pass
- Show the refactored code with brief explanations of changes
- Do NOT introduce new features during quality pass
- Focus on the code that was recently modified

## Output

For each change:
1. What was changed
2. Why it improves quality
3. The refactored code
