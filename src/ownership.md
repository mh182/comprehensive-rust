# Ownership

All variable bindings have a _scope_ where they are valid and it is an error to
use a variable outside its scope:

```rust,editable,compile_fail
fn main() {
    {
        let x = 42;
        println!("x: {x}");
    }

    println!("x: {x}");
}
```

- At the end of the scope, the variable is _dropped_ and the data is freed.
- A destructor can run here to free up resources.
- We say that the variable _owns_ the value.
