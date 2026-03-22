# Global Empires — Product Vision

## Mission
Build a **turn-based, asynchronous, online strategy game** inspired by classic 4X gameplay (explore, expand, exploit, exterminate), designed for many concurrent real players and maintainable long-term development.

## Product Principles
1. **MVP-first**: each milestone must produce a playable increment.
2. **Asynchronous by default**: players can submit turns on their own schedule.
3. **Server-authoritative simulation**: prevent cheating and desync.
4. **Performance-aware from day one**: deterministic rules, efficient state updates.
5. **LLM-friendly development**: requirements and tasks stay explicit, small, and testable.
6. **Contributor-friendly**: clean architecture, docs, tests, and clear conventions.

## Non-Goals (MVP)
- Full Civilization feature parity.
- Real-time combat.
- AAA graphics pipeline.
- Advanced diplomacy AI and mod ecosystem.

## Success Criteria (MVP)
- Players can create/join matches, take turns asynchronously, and see map/city/unit updates.
- Hex map with fog-of-war, movement, city founding, basic production, and simple combat.
- Turn processing is deterministic and reproducible.
- Admin can moderate matches and users.
