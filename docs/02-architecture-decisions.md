# Architecture Decisions (Living ADR)

## ADR-001: Frontend choice for MVP
**Decision:** Use **React + TypeScript** for the player client and admin panel.

**Why:**
- Faster ecosystem for game-oriented UI libraries and map rendering.
- Easier onboarding for mixed contributor pools.
- Strong state/tooling ecosystem (Redux Toolkit, Zustand, TanStack Query).

**Alternative considered:** Blazor WebAssembly.
- Strength: full .NET stack consistency.
- Tradeoff: smaller ecosystem for browser game rendering patterns compared with React.

## ADR-002: Backend
**Decision:** **ASP.NET Core (.NET 10 when stable)** with Clean Architecture layering.

Layers:
- API (controllers/minimal endpoints)
- Application (use cases, commands/queries)
- Domain (entities/value objects/rules)
- Infrastructure (EF Core, persistence, auth providers)

## ADR-003: Data storage
**Decision:** Start with **SQLite (file-based) via EF Core**, designed for migration to PostgreSQL.

Rules:
- Avoid provider-specific SQL in application layer.
- Keep migrations disciplined from day one.
- Use optimistic concurrency tokens for turn submission safety.

## ADR-004: Turn model
**Decision:** Hybrid asynchronous turns.
- Each turn has a deadline.
- Players submit orders independently.
- Resolution occurs when all ready or deadline reached.

## ADR-005: Engine determinism
**Decision:** Server simulation must be deterministic.
- Seeded RNG per match/turn.
- Ordered command execution pipeline.
- Replay-friendly event stream for debugging.
