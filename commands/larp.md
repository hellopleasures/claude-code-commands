# LARP Assessment

Critically evaluate whether this code is real or performative (LARPing = Live Action Role Playing).

> "AI doesn't write bad code because it's bad at coding; it writes bad code because we give it permission to."

## Check For

1. **Stubbed functions** that return fake/hardcoded data
2. **Hardcoded values** masquerading as dynamic behavior
3. **Tests that mock away** the actual logic being tested
4. **Error handling** that silently swallows failures
5. **Async code** that doesn't actually await
6. **Validation** that doesn't actually validate
7. **Code paths that haven't been executed** and verified

## Red Flags

```typescript
// BAD: Stubbed function
function getUser(id: string) {
  return { id, name: "Test User" }; // Fake data!
}

// BAD: Hardcoded "dynamic" value
const apiUrl = "https://api.example.com"; // Should be env var

// BAD: Mock that defeats the purpose
jest.mock('./database'); // Now we're not testing real DB logic

// BAD: Silent failure
try { await riskyOperation(); } catch { } // Error swallowed!

// BAD: Fake async
async function fetchData() {
  return staticData; // Not actually fetching anything
}

// BAD: Validation theater
function validateInput(input: any) {
  return true; // Always passes!
}
```

## Rules

- Report findings **honestly**
- If something looks functional but isn't proven to work, **flag it**
- Once review is complete, fix every issue from most complicated to simplest
- Track fixes with a TODO list

## Output Format

### LARP Detected

| Issue | Location | Severity | Type |
|-------|----------|----------|------|
| [Description] | [file:line] | High/Med/Low | Stub/Hardcode/Mock/etc |

### Fixes Required

1. [ ] [Most complex fix first]
2. [ ] [Next fix]
...

### Fixes Applied

For each fix:
```
Issue: [what was wrong]
File: [location]
Before: [old code]
After: [new code]
Verified: [how it was tested]
```
