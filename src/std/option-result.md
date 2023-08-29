# `Option` and `Result`

Two simple yet very powerful enums!

[`Option`](https://doc.rust-lang.org/stable/std/option/enum.Option.html):

```rust,noplayground
enum Option<T> {
    Some(T),
    None
}
```

No `Null`, no [magic numbers](https://en.wikipedia.org/wiki/Magic_number_(programming)), no extra boolean, just an enum that tells you if you get something (`Some`) or nothing (`None`).

[`Result`](https://doc.rust-lang.org/stable/std/result/enum.Result.html):

```rust,noplayground
enum Result<T, E> {
    Ok(T),
    Err(E)
}
```

Here too: No `Null`, no magic numbers, no extra `err` variable, no uncaught exceptions, just an enum that forces you to handle the case where something goes wrong (`Err`).

Example:

```rust,editable
use std::{fs::File, io};

fn main() {
    let numbers = vec![10, 20, 30];
    let first: Option<&i8> = numbers.first();
    println!("first: {first:?}");

    let file: Result<File, io::Error> = File::open("does_not_exist.txt");
    println!("file: {file:?}");
}
```

<details>

- `Option` and `Result` are widely used not just in the standard library.
- `Option<&T>` has zero space overhead compared to `&T`.
- `Result` is the standard type to implement error handling as we will see on Day 3.

</details>
