# Functions

An example of a simple function:

```rust,editable
/// R = U / I
fn resistance(voltage: f64, current: f64) -> f64 {
    voltage / current
}

fn main() {
    let U = 5.0; // V
    let I = 2.0; // mA
    let R = resistance(U, I); // kΩ
    println!("R = {R} kΩ");
}
```

<details>

- Declaration parameters are followed by a type, then a return type.
- The last expression in a function body (or any block) becomes the return value. Simply omit the `;` at the end of the expression.
- Some functions have no return value, and return the 'unit type', `()`. The compiler will infer this if the `-> ()` return type is omitted. The `main` function above is such a function.

</details>
