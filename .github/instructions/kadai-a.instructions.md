---
applyTo: "kadai-a/**"
---

**Problem statement:** Implement a binary tree without any locking in `btree.c`, then in `main.c`
concurrently insert a total of 10000 nodes using multiple threads. At the end, call `btree_dump()`
and confirm that some inserted nodes are lost due to the lack of synchronization.

**Requirements:**

- The command `make unsafe_btree` produces the executable.
- `btree.h` must declare (and `btree.c` must implement) the following interface: 
  - `tnode * btree_create()`
  - `void btree_insert(int v, tnode * t)` — duplicate values should be allowed
  - `void btree_destroy(tnode * t)` — frees all memory
  - `void btree_dump(tnode * t)` — prints all values in ascending order to stdout, one per line,
    formatted as `"%d\n"`.
- Internal implementation details of `btree.c` are left to the implementer.
- The expected behavior is that concurrent unsynchronized access causes some nodes to be missing,
  resulting in fewer than 10000 lines of output
