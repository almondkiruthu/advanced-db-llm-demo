# Student lab: Course Registration

## Session goal

By 11:50, produce a small PostgreSQL design that can safely accept concurrent
registration requests. Your value is in the architecture; use the LLM to do
most of the mechanical SQL writing.

## Schedule

| Time | Activity |
| --- | --- |
| 10:00-10:10 | Read the scenario and inspect PostgreSQL |
| 10:10-10:30 | Make five architecture decisions |
| 10:30-10:55 | Ask the LLM to implement the schema |
| 10:55-11:20 | Implement and test registration/waitlisting |
| 11:20-11:35 | Add one index and inspect `EXPLAIN` |
| 11:35-11:45 | Review another design and revise yours |
| 11:45-11:50 | Capture the most important lesson |

## Before you begin

Confirm that PostgreSQL is available:

```powershell
psql --version
pg_isready
```

Create a disposable database using your own PostgreSQL credentials. A common
local setup is:

```powershell
createdb -U postgres course_registration_demo
psql -U postgres -d course_registration_demo
```

## Working agreement with the LLM

1. You decide the entities, keys, invariants, transaction boundary, and index.
2. Ask the LLM to challenge those decisions before it writes SQL.
3. Approve or reject its suggestions explicitly.
4. Ask it to implement your approved architecture in `students/work/schema.sql`.
5. Ask it to create a small demonstration in `students/work/demo.sql`.
6. Run the SQL yourself and give actual PostgreSQL errors back to the LLM.

Do not spend the session building a UI or API. The database behavior is the
product for this exercise.

## Exercise

Open
[`01.01-architect-and-build/problem/readme.md`](exercises/01-course-registration/01.01-architect-and-build/problem/readme.md).
