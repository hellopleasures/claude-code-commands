# Production Readiness Validation

Final checklist before deployment. Verify each item with **evidence, not assertions**.

## Checklist

### Testing
- [ ] All tests pass with **real execution**, not mocked
- [ ] Run: `npm test` — show output
- [ ] Run: `npm run typecheck` — show output
- [ ] Run: `npm run lint` — show output

### Error Handling
- [ ] Error handling covers failure modes with proper logging
- [ ] User-facing errors are helpful (not stack traces)
- [ ] Errors are logged with context for debugging

### Configuration
- [ ] No hardcoded secrets in code
- [ ] All config uses environment variables
- [ ] Required env vars are documented

### Security
- [ ] Authentication required on protected routes
- [ ] Input validation with Zod on all user inputs
- [ ] SQL/NoSQL injection prevented (parameterized queries)
- [ ] XSS prevented (proper escaping)
- [ ] Rate limiting on public endpoints

### Performance
- [ ] Database queries are indexed appropriately
- [ ] No N+1 query problems
- [ ] Pagination implemented for list endpoints
- [ ] Large operations are async/background

### Dependencies
- [ ] Dependencies are pinned versions
- [ ] No known security vulnerabilities: `npm audit`

### Operations
- [ ] Rollback path exists (what to do if deployment fails)
- [ ] Logging is in place for debugging
- [ ] Health check endpoint available

## Rules

- Demonstrate each item is satisfied with **evidence** (command output, code snippets)
- If anything fails, create a TODO and fix it before proceeding
- Do NOT mark items complete without verification

## Output

For each checklist item:
```
[x] Item description
    Evidence: [command output or code reference]
```

Or if failed:
```
[ ] Item description
    Issue: [what's wrong]
    Fix: [what was done to fix it]
```
