# Development Workflow (MVP)

## Branching
- `main`: stable trunk.
- Short-lived feature branches.

## Definition of Ready (DoR)
A task is ready when it has:
- Problem statement.
- Acceptance criteria.
- Scope limits.
- File/component touch estimate.

## Definition of Done (DoD)
A task is done when it includes:
- Working code.
- Tests for behavior change.
- Updated documentation.
- Migration notes (if schema changed).
- Risks + next-step suggestions.

## Pull Request Checklist
- Small and reviewable.
- SOLID and separation-of-concerns respected.
- No dead code.
- Public API and data contracts documented.
- Performance impact noted.

## MVC / SOLID Guardrails
- Keep business rules in domain/application layers, not controllers.
- Prefer interfaces at boundaries (DIP).
- Keep classes narrowly focused (SRP).
- Extend behavior through new types/policies, avoid fragile conditionals (OCP).
- Avoid fat interfaces; split by use-case (ISP).
