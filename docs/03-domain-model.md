# Initial Domain Model (MVP)

## Core Entities
- `Game`: metadata, status, turn number, settings.
- `Player`: user-to-game participation, civilization state.
- `Map`: hex tiles, terrain, resources.
- `Tile`: axial coordinate, terrain type, resource, visibility.
- `Unit`: type, owner, location, movement points, health.
- `City`: owner, location, population, yields, queue.
- `Turn`: deadline, phase, resolution metadata.
- `Order`: player-submitted actions for a turn.
- `TechProgress`: unlocked techs and research accumulation.
- `EventLogEntry`: immutable event history.

## Value Objects
- `HexCoord(q, r)`
- `Yield(food, production, gold)`
- `CombatResult`

## Aggregate Boundaries (suggested)
- `Game` aggregate roots turn lifecycle and consistency checks.
- `City` aggregate for queue/population logic.
- `Unit` aggregate for movement/combat validity.

## Invariants
- Orders can only target the active turn.
- A unit cannot exceed movement points.
- Two ownership states cannot conflict on same entity version.
- Turn resolution is idempotent.
