# MVP Backlog (Ordered)

## Epic 1 — Foundation
- [ ] Scaffold solution structure (frontend, backend, shared contracts).
- [ ] Setup CI for build, lint, tests.
- [ ] Add coding standards and formatting automation.

## Epic 2 — Accounts & Lobby
- [ ] User auth and profile.
- [ ] Create/list/join games.
- [ ] Game settings DTO + persistence.

## Epic 3 — World & Turns
- [ ] Hex map generator.
- [ ] Basic fog-of-war visibility system.
- [ ] Turn entity + order submission endpoint.
- [ ] Turn deadline worker/service.

## Epic 4 — Core Gameplay
- [ ] Unit movement validation and execution.
- [ ] Settler found city action.
- [ ] City production queue.
- [ ] Basic combat.

## Epic 5 — Progression
- [ ] Minimal tech tree and unlock handling.
- [ ] Yield update per turn.

## Epic 6 — Admin
- [ ] Admin auth role.
- [ ] Moderate users/games.
- [ ] Inspect game events and turn state.

## Epic 7 — Hardening
- [ ] Deterministic replay test harness.
- [ ] Concurrency and conflict tests for order submissions.
- [ ] Basic telemetry and health checks.
