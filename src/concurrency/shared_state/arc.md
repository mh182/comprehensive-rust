# `Arc`

[`Arc<T>`][1] allows shared read-only access via `Arc::clone`:

```rust,editable
use std::thread;
use std::sync::Arc;

fn main() {
    let v = Arc::new(vec![10, 20, 30]);

    let handles = (0..5).map(|_| {
        let v = Arc::clone(&v);

        thread::spawn(move || {
            let thread_id = thread::current().id();
            println!("{thread_id:?}: {v:?}");
        })
    }).collect::<Vec<_>>();

    for handle in handles {
        handle.join().unwrap();
    }

    println!("v: {v:?}");
}
```

[1]: https://doc.rust-lang.org/std/sync/struct.Arc.html

<details>

- `Arc` stands for "Atomic Reference Counted", a thread safe version of `Rc` that uses _atomic
  operations_.
- `Arc<T>` implements `Clone` whether or not `T` does. It implements `Send` and `Sync` if
  and only if `T` implements them both.
- `Arc::clone()` has the cost of atomic operations that get executed, but after that the use of the
  `T` is free.
- Beware of reference cycles, `Arc` does not use a garbage collector to detect them.

</details>
