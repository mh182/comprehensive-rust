# Constructors

You can have multiple constructors:

```rust,editable
#[derive(Debug)]
struct Person {
    name: String,
    age: u8,
}

impl Person {
    fn new(name: String, age: u8) -> Person {
        // You could do some input processing and validation here.

        Person { name, age }
    }

    fn bot(name: String) -> Person {
        Person { name, age: 0 }
    }
}

fn main() {
    let peter = Person::new(String::from("Peter"), 27);

    println!("{peter:?}");
}
```

<details>

- The functions `new` and `bot` could be written using `Self` as a type, as it is interchangeable with the struct type name

  ```rust,editable
  #[derive(Debug)]
  struct Person {
      name: String,
      age: u8,
  }

  impl Person {
      fn new(name: String, age: u8) -> Self {
          Self { name, age }
      }
  }
  ```
- Implement the `Default` trait for the struct.

  ```rust,editable
  #[derive(Debug)]
  struct Person {
      name: String,
      age: u8,
  }

  impl Default for Person {
      fn default() -> Self {
          Self {
              name: "Bot".to_string(),
              age: 0,
          }
      }
  }
  ```

- Use `{:#?}` when printing structs to request the **pretty-printed** `Debug` representation.

</details>
