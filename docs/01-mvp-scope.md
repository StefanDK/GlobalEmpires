# MVP Scope and Slicing Strategy

## Core MVP Loop
1. Register/login.
2. Join or create game.
3. Receive current game state snapshot.
4. Submit turn orders before deadline (or end-turn signal).
5. Server resolves turn and publishes next snapshot + events.
6. Repeat.

## MVP Feature Set (Phase 1)
- Authentication and player profiles.
- Lobby/game creation and invite flow.
- Hex map generation (single map type).
- Units: scout, warrior, settler.
- Cities: found city, population growth (simple), production queue.
- Resources: food, production, gold (minimal economy).
- Technology tree (tiny: ~5 techs).
- Simple combat resolution.
- Fog of war.
- Turn timer + async order submission.
- Match event log.
- Admin dashboard: users/games moderation.

## Out of Scope for MVP
- Religion, culture, tourism.
- Complex diplomacy treaties.
- Naval/air warfare.
- Trading system and market simulation.
- AI bots with advanced strategy.

## Task Sizing Policy (for LLM contributors)
Any implementation task should normally fit:
- **<= 300 LOC net change**,
- **<= 3 files touched** (except refactors),
- **<= 1 domain concept introduced**.

If a requested task exceeds this, contributors must:
1. Flag it as too large.
2. Propose 3–7 smaller steps.
3. Execute only the first approved slice.
