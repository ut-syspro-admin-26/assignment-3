---
applyTo: "kadai-c/**"
---

**Problem statement:** Implement a thread-safe Bounded Buffer in `bb.c` and write a test in
`main.c` that verifies it works correctly under concurrent access.

**General requirements:**

- The command `make bb` produces the executable.

**Bounded buffer requirements (`bb.c`):**

- Internal buffer holds up to 10 elements.
- Interface:
  - `void bb_put(int i)` — appends to the tail; if the buffer is full, blocks until space is
    available.
  - `int bb_get(void)` — removes and returns from the head; if the buffer is empty, blocks until
    another thread calls `bb_put()`
- The implementation of these two functions must be thread-safe.

**Test code requirements (`main.c`):**

- Perform single-threaded test: verify that multiple elements put via `bb_put()` can all be
  retrieved in insertion order.
- Perform multi-threaded test: insert 10000 elements via `bb_put()` and retrieve 10000 elements via
  `bb_get()`, using multiple threads for both (e.g. 4 producer threads, 4 consumer threads); print
  each retrieved value to stdout. Output must be exactly 10000 lines.
- Use `assert(3)` to verify correctness.
