---
applyTo: "kadai-d/**"
---

**Problem statement:** Research which system calls `pthread` uses internally to create threads,
then write a program that creates threads using those system calls directly — without using
`pthread`. Document the findings in `report-d.md`.

*For the report, don't review the content — just check that `report-d.md` has been created and
that something is written.*

**Requirements:**

- A `Makefile` must be present
- The program's structure and output format are free — just demonstrate that threads are created
  via the underlying system call(s) directly
