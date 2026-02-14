# Thorough Testing

Review and expand test coverage beyond the happy path.

## Requirements

1. Test **boundary conditions** and edge cases
2. Test **error handling** and invalid inputs
3. Test **integration points** with real dependencies where possible
4. Test **concurrent/async behavior** if applicable
5. **Verify actual outputs** match expected — inspect the data

## Test Categories

### Unit Tests
- Individual functions with various inputs
- Edge cases (empty, null, max values, special characters)
- Error conditions and exception handling

### Integration Tests
- API endpoints with real database (use test database)
- Authentication flows
- Data validation with Zod schemas

### Boundary Tests
- Maximum file sizes
- Rate limiting thresholds
- Pagination limits
- String length limits

## Rules

- Tests must exercise **real code paths**, not mocks of the code under test
- Mocks are only acceptable for external services (email, IPFS, etc.)
- Every test should have a clear assertion
- Test files go in `__tests__/` directory
- Run tests with `npm test`

## Output

1. List of test cases to add
2. The test code
3. Results of running the tests
