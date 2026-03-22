# LLM Contributor Playbook

Use this protocol for every task.

## Mandatory Output Format
1. **Scope check**
   - State whether task is MVP-sized.
   - If oversized, split into smaller steps and stop at step 1.
2. **Plan**
   - Bullet list of implementation tasks.
3. **Changes**
   - Small, incremental edits only.
4. **Review**
   - Self-review for correctness, maintainability, and performance.
5. **Next steps**
   - 2–5 concrete options with tradeoffs toward final product.

## Oversized Task Detector
Mark task as oversized if any true:
- Requires broad cross-cutting changes.
- Introduces more than one subsystem at once.
- Cannot be validated with focused tests.
- Ambiguous acceptance criteria.

## Coding Guidelines
- Prioritize readability and deterministic behavior.
- Keep methods small and side effects explicit.
- Prefer composition over inheritance.
- Add comments only where intent is non-obvious.
- Write tests first for bug fixes and critical rules.

## Performance Guidelines
- Avoid N+1 data access patterns.
- Keep payloads small (snapshot + delta/event patterns).
- Use pagination for logs/history endpoints.
- Use indexes for frequent turn/game queries.

## Security Guidelines
- Server-authoritative validation of all orders.
- Enforce authentication + authorization per game.
- Audit admin actions.
- Avoid exposing hidden-map data in API responses.
