# Shared References

A reference provides a way to access another value without taking responsibility for the value, and is also called “borrowing”. Shared references are read-only, and the referenced data cannot change.

```rust,editable
fn main() {
    let a = 'A';
    let b = 'B';
    let mut r: &char = &a;  // mutable shared reference, value can't change
    println!("r: {}", *r);
    r = &b;                 // re-bind, so it refers to something else
    println!("r: {}", *r);
    println!("Is '{}' alphabetic: {}", *r, r.is_alphabetic());
}
```

A shared reference to a type `T` has type `&T`. A reference value is made with the `&` operator. The `*` operator “dereferences” a reference, yielding its value.

<details>
This slide should take about 10 minutes.

- A reference is said to “borrow” the value it refers to, and this is a good model for students not familiar with pointers: code can use the reference to access the value, but is still “owned” by the original variable. The course will get into more detail on ownership in day 3.

- References are implemented as pointers, and a key advantage is that they can be much smaller than the thing they point to. Students familiar with C or C++ will recognize references as pointers. Later parts of the course will cover how Rust prevents the memory-safety bugs that come from using raw pointers.

- Rust does not automatically create references for you - the `&` is always required.

- Rust will auto-dereference in some cases, in particular when invoking methods (try `r.is_alphabetic()`). There is no need for an `->` operator like in C++.

- In this example, `r` is mutable so that it can be reassigned (`r = &b`). Note that this re-binds `r`, so that it refers to something else. This is different from C++, where assignment to a reference changes the referenced value.

- A shared reference does not allow modifying the value it refers to, even if that value was mutable. Try `*r = 'X'`.

</details>

