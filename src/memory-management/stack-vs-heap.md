# The Stack vs The Heap

- Stack: Continuous area of memory for local variables.
  - Values have **fixed sizes** known at compile time.
  - Extremely fast: just move a stack pointer.
  - Easy to manage: follows function calls.

- Heap: Storage of values outside of function calls.
  - Values have **dynamic sizes** determined at runtime.
  - Slower than the stack: some book-keeping needed.
