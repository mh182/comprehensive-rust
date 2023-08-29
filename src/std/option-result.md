# `Option` and `Result`

```rust,editable
use std::{fs::File, io};

fn main() {
    let numbers = vec![10, 20, 30];
    let first: Option<&i8> = numbers.first();
    println!("first: {first:?}");

    let result: Result<File, io::Error> = File::open("does_not_exist.txt");
    println!("result: {result:?}");
}
```

<details>

- [`Option`](https://doc.rust-lang.org/stable/std/option/enum.Option.html) and [`Result`](https://doc.rust-lang.org/stable/std/result/enum.Result.html) are widely used not just in the standard library.
- `Option<&T>` has zero space overhead compared to `&T`.
- `Result` is the standard type to implement error handling as we will see on Day 3.

</details>
