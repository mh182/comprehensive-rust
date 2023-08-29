# `break` and `continue`

- If you want to exit a loop early, use [`break`](https://doc.rust-lang.org/reference/expressions/loop-expr.html#break-expressions),
- If you want to immediately start
  the next iteration use [`continue`](https://doc.rust-lang.org/reference/expressions/loop-expr.html#continue-expressions).

Both `continue` and `break` can optionally take a label argument which is used
to break out of nested loops:

```rust,editable
fn without_labeled_loops() {
    let mut break_outer_loop = false;

    for i in [1, 2, 3] {
        for j in [11, 22, 33] {
            println!("{i}, {j}");

            if i + j == 24 {
                break_outer_loop = true;
                break;
            }
        }

        if break_outer_loop {
            break;
        }
    }
}

fn with_labeled_loops() {
    'outer: for i in [1, 2, 3] {
        for j in [11, 22, 33] {
            println!("{i}, {j}");

            if i + j == 24 {
                break 'outer;
            }
        }
    }
}

fn main() {
    without_labeled_loops();
    println!("-----");
    with_labeled_loops();
}
```
