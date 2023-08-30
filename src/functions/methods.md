# Methods

Methods are functions associated with a type. The `self` argument of a method is
an instance of the type it is associated with:

```rust,editable
struct Rectangle {
    width: u32,
    height: u32,
}

impl Rectangle {
    fn area(&self) -> u32 {
        self.width * self.height
    }

    fn inc_width(&mut self, delta: u32) {
        self.width += delta;
    }
}

fn main() {
    let mut rect = Rectangle { width: 10, height: 5 };
    println!("old area: {}", rect.area());

    rect.inc_width(5);
    println!("new area: {}", rect.area());
}
```

We will learn more about structs and methods later.
