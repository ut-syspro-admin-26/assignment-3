---
applyTo: "kadai-b/**"
---

**Problem statement:** Add synchronization inside `btree_insert()` from kadai-a so that concurrent
insertions work correctly.

**Requirements:**

- The command `make safe_btree` produces the executable.
- Locking must be inside `btree_insert()` — serializing calls from the caller side is not
  acceptable. In other words, `main.c` and `btree.h` must be identical to kadai-a; only `btree.c`
  should change.
- Lock only the minimum necessary section.
- `btree_dump()` output must be exactly 10000 lines.
