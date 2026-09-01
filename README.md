# Architecting PostgreSQL with an LLM

This repository supports a single Advanced Databases class session. Students
architect a small university course-registration database, then use an LLM as
an implementation partner for the SQL.

The student remains responsible for the important decisions: data boundaries,
invariants, transaction behavior, and indexes. The LLM can draft SQL, tests,
and revisions after those decisions are explicit.

## Start here

Read [`students/README.md`](students/README.md), then complete the one exercise
under `students/exercises/`.

## Core scope

- Model students, courses, offerings, and registrations.
- Prevent duplicate registrations and enrollment beyond capacity.
- Place overflow requests on a waitlist.
- Add one useful roster index and inspect its query plan.

Auditing, prerequisite graphs, temporal history, and row-level security are
optional stretch directions, not requirements for the session.

Instructor notes and reference material live in a local, gitignored
`instructor/` directory and are not included when students clone the repo.
