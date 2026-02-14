# Review Last Task

Audit what was just completed with honesty.

## Questions to Answer

1. **Does it actually work?** — Did you verify the output with real execution?
2. **Does it solve the original problem?** — Or just part of it?
3. **Did anything get skipped or deferred?** — Any TODOs, stubs, or "for later"?
4. **Are there assumptions that should be documented?** — What might surprise someone?
5. **What could break this in production?** — Edge cases, scale, dependencies?

## Review Checklist

- [ ] Code compiles and runs without errors
- [ ] All acceptance criteria from the original request are met
- [ ] No placeholder or stub code remains
- [ ] Error handling covers realistic failure modes
- [ ] Security considerations addressed (auth, validation, injection)
- [ ] Performance is acceptable for expected usage
- [ ] Code follows project patterns from CLAUDE.md

## Rules

- Give an **honest assessment**, not a confident summary
- Flag uncertainties and potential issues
- After your assessment, create a TODO list for anything incomplete
- Then fix each TODO item

## Output Format

### Assessment
[Honest evaluation of what works and what doesn't]

### Issues Found
1. [Issue description] — [Severity: High/Medium/Low]
2. ...

### Action Items
- [ ] [Specific fix needed]
- [ ] ...

### Fixes Applied
[Show the fixes made for each item]
