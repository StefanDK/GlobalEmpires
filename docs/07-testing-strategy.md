# Testing Strategy

## Test Pyramid
- **Unit tests**: domain rules (movement, combat, production, turn state).
- **Integration tests**: API + DB + turn resolution pipeline.
- **Contract tests**: API payload shape between frontend/backend.
- **E2E tests**: minimal “join game -> submit turn -> resolve”.

## Determinism Tests
- Same seed + same orders => same outcome.
- Re-run resolution idempotency checks.
- Event log replay reaches identical state hash.

## Non-Functional Checks
- Load test turn submission for concurrent players.
- Measure snapshot payload size and response time.
- Validate DB query plans for hot endpoints.
