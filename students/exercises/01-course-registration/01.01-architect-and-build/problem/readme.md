# Architect and Build Course Registration

## Scenario

A university publishes course offerings for a term. Each offering has a fixed
capacity. A student requests a place in an offering: if a seat is available,
the student is enrolled; otherwise, the student is waitlisted.

## Your five architecture decisions

Record these in `students/work/architecture.md` before generating SQL:

1. Which tables exist, and what does each table own?
2. Which primary and foreign keys connect them?
3. Which database constraints enforce valid state?
4. What must one registration transaction lock so concurrent requests cannot
   exceed capacity?
5. Which index supports the common roster lookup?

## Deliverables

- `architecture.md`: your five decisions and brief reasons.
- `schema.sql`: tables, constraints, index, and registration operation.
- `demo.sql`: small seed data and checks showing the behavior.

## Required behavior

- A student cannot register twice for the same offering.
- Enrolled registrations never exceed the offering capacity.
- Requests beyond capacity become waitlisted.
- An unknown student or offering is rejected.
- The roster query filters by offering and registration status.
- `EXPLAIN` is used to inspect the roster query.

## A useful first prompt

> We are architecting a PostgreSQL course-registration database. I will provide
> five architecture decisions. Challenge missing invariants and concurrency
> risks, but do not write SQL until I approve the design.

## Stretch only if the core works

Choose at most one: prerequisites, an audit trail, temporal registration
history, or row-level security. Do not sacrifice the required behavior for a
stretch feature.
