# Summary

<!-- Keep first page as index.md to avoid giving it two names. -->

[Welcome to Comprehensive Rust 🦀](index.md)

- [Using Cargo](cargo.md)
  - [Rust Ecosystem](cargo/rust-ecosystem.md)
  - [Running Cargo Locally](cargo/running-locally.md)
  - [Code Samples](cargo/code-samples.md)

# Day 1: Morning

---

- [What is Rust?](what-is-rust.md)
- [Hello World!](hello-world.md)
  - [Small Example](hello-world/small-example.md)
- [Why Rust?](why-rust.md)
  - [Compile Time Guarantees](why-rust/compile-time.md)
  - [Runtime Guarantees](why-rust/runtime.md)
  - [Modern Features](why-rust/modern.md)
- [Scalar Types](scalar-types.md)
- [Compound Types](compound-types.md)
- [References](references.md)
  - [Shared References](references/shared-references.md)
  - [Exclusive References](references/exclusive-references.md)
  - [Dangling References](references/references-dangling.md)
- [Slices](slices.md)
  - [String vs str](slices/string-slices.md)
- [Control Flow](control-flow.md)
  - [Blocks](control-flow/blocks.md)
  - [if expressions](control-flow/if-expressions.md)
  - [for expressions](control-flow/for-expressions.md)
  - [while expressions](control-flow/while-expressions.md)
  - [break & continue](control-flow/break-continue.md)
  - [loop expressions](control-flow/loop-expressions.md)
- [Exercises](exercises/day-1/morning.md)

# Day 1: Afternoon

- [Functions](functions.md)
  - [Early return](functions/early-return.md)
  - [Rustdoc](functions/rustdoc.md)
  - [Methods](functions/methods.md)
  - [Overloading](functions/functions-interlude.md)
- [Variables](variables.md)
  - [Type Inference](variables/type-inference.md)
  - [static & const](variables/static-and-const.md))
  - [Scopes and Shadowing](variables/scopes-shadowing.md)
- [Memory Management](memory-management.md)
  - [Stack vs Heap](memory-management/stack-vs-heap.md)
  - [Stack Memory](memory-management/stack.md)
  - [Manual Memory Management](memory-management/manual.md)
  - [Scope-Based Memory Management](memory-management/scope-based.md)
  - [Garbage Collection](memory-management/garbage-collection.md)
  - [Rust Memory Management](memory-management/rust.md)
  - [Comparison](memory-management/comparison.md)
- [Exercises](exercises/day-1/afternoon.md)

# Day 2: Morning

---

- [Ownership](ownership.md)
  - [Move Semantics](ownership/move-semantics.md)
  - [Moved Strings in Rust](ownership/moved-strings-rust.md)
    - [Double Frees in Modern C++](ownership/double-free-modern-cpp.md)
  - [Moves in Function Calls](ownership/moves-function-calls.md)
  - [Copying and Cloning](ownership/copy-clone.md)
  - [Borrowing](ownership/borrowing.md)
    - [Shared and Unique Borrows](ownership/shared-unique-borrows.md)
  - [Lifetimes](ownership/lifetimes.md)
  - [Lifetimes in Function Calls](ownership/lifetimes-function-calls.md)
  - [Lifetimes in Data Structures](ownership/lifetimes-data-structures.md)
- [Exercises](exercises/day-2/morning.md)

# Day 2: Afternoon

- [Structs](structs.md)
  - [Tuple Structs](structs/tuple-structs.md)
  - [Constructors](structs/constructors.md)
- [Enums](enums.md)
  - [Variant Payloads](enums/variant-payloads.md)
  - [Option and Result](enums/option-result.md)
- [Methods](methods.md)
  - [Method Receiver](methods/receiver.md)
  - [Example](methods/example.md)
- [Pattern Matching](pattern-matching.md)
  - [Destructuring Enums](pattern-matching/destructuring-enums.md)
  - [Destructuring Structs](pattern-matching/destructuring-structs.md)
  - [Destructuring Arrays](pattern-matching/destructuring-arrays.md)
  - [Match Guards](pattern-matching/match-guards.md)
  - [if let expressions](pattern-matching/if-let-expressions.md)
  - [while let expressions](pattern-matching/while-let-expressions.md)
- [Exercises](exercises/day-2/afternoon.md)

# Day 3: Morning

---

- [Standard Library](std.md)
  - [Vec](std/vec.md)
  - [String](std/string.md)
  - [HashMap](std/hashmap.md)
  - [Box](std/box.md)
    - [Recursive Data Types](std/box-recursive.md)
    - [Niche Optimization](std/box-niche.md)
  - [Rc](std/rc.md)
- [Exercises](exercises/day-3/morning.md)

# Day 3: Afternoon

- [Modules](modules.md)
  - [Visibility](modules/visibility.md)
  - [Paths](modules/paths.md)
  - [Filesystem Hierarchy](modules/filesystem.md)
- [Generics](generics.md)
  - [Generic Data Types](generics/data-types.md)
  - [Generic Methods](generics/methods.md)
  - [Monomorphization](generics/monomorphization.md)
- [Exercises](exercises/day-3/afternoon.md)

# Day 4: Morning

---

- [Traits](traits.md)
  - [Trait Objects](traits/trait-objects.md)
  - [Deriving Traits](traits/deriving-traits.md)
  - [Default Methods](traits/default-methods.md)
  - [Trait Bounds](traits/trait-bounds.md)
  - [impl Trait](traits/impl-trait.md)
- [Important Traits](traits/important-traits.md)
  - [Iterator](traits/iterator.md)
  - [FromIterator](traits/from-iterator.md)
  - [From and Into](traits/from-into.md)
  - [Read and Write](traits/read-write.md)
  - [Drop](traits/drop.md)
  - [Default](traits/default.md)
  - [Operators: Add, Mul, ...](traits/operators.md)
  - [Closures: Fn, FnMut, FnOnce](traits/closures.md)
- [Exercises](exercises/day-4/morning.md)

# Day 4: Afternoon

- [Error Handling](error-handling.md)
  - [Panics](error-handling/panics.md)
  - [Structured Error Handling](error-handling/result.md)
  - [Propagating Errors with ?](error-handling/try-operator.md)
    - [Converting Error Types](error-handling/converting-error-types.md)
      - [Example](error-handling/converting-error-types-example.md)
    - [Deriving Error Enums](error-handling/deriving-error-enums.md)
    - [Dynamic Error Types](error-handling/dynamic-errors.md)
    - [Adding Context to Errors](error-handling/error-contexts.md)
- [Testing](testing.md)
  - [Unit Tests](testing/unit-tests.md)
  - [Test Modules](testing/test-modules.md)
  - [Documentation Tests](testing/doc-tests.md)
  - [Integration Tests](testing/integration-tests.md)
- [Unsafe Rust](unsafe.md)
  - [Dereferencing Raw Pointers](unsafe/raw-pointers.md)
  - [Mutable Static Variables](unsafe/mutable-static-variables.md)
  - [Calling Unsafe Functions](unsafe/calling-unsafe-functions.md)
    - [Writing Unsafe Functions](unsafe/writing-unsafe-functions.md)
  - [Implementing Unsafe Traits](unsafe/unsafe-traits.md)
- [Exercises](exercises/day-4/afternoon.md)

# Day 5: Morning

---

- [Concurrency](concurrency.md)
- [Threads](concurrency/threads.md)
  - [Scoped Threads](concurrency/scoped-threads.md)
- [Channels](concurrency/channels.md)
  - [Unbounded Channels](concurrency/channels/unbounded.md)
  - [Bounded Channels](concurrency/channels/bounded.md)
- [Send and Sync](concurrency/send-sync.md)
  - [Send](concurrency/send-sync/send.md)
  - [Sync](concurrency/send-sync/sync.md)
  - [Examples](concurrency/send-sync/examples.md)
- [Shared State](concurrency/shared_state.md)
  - [Arc](concurrency/shared_state/arc.md)
  - [Mutex](concurrency/shared_state/mutex.md)
  - [Example](concurrency/shared_state/example.md)
- [Exercises](exercises/day-5/morning.md)

# Day 5: Afternoon

---

- [Async Basics](async.md)
  - [async/await](async/async-await.md)
  - [Futures](async/futures.md)
  - [Tokio](async/tokio.md)
- [Pitfalls](async/pitfalls.md)
  - [Blocking the Executor](async/pitfalls/blocking-executor.md)
  - [Async Traits](async/pitfalls/async-traits.md)
- [Web Server](web-server.md)
- [Exercises](exercises/day-5/afternoon.md)

# Final Words

---

- [Thanks!](thanks.md)
- [Other Resources](other-resources.md)
- [Credits](credits.md)
