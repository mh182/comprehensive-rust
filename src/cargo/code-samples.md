# Code Samples in This Training

For this training, we will mostly explore the Rust language through examples
which can be executed through your browser. This makes the setup much easier and
ensures a consistent experience for everyone.

The code blocks in this course are fully interactive:

```rust,editable
fn main() {
    println!("Edit me!");
}
```

You can use <kbd>Ctrl + Enter</kbd> to execute the code when focus is in the
text box.

## Installing the training course

The course is built using a few tools:

- [mdbook](https://github.com/rust-lang/mdBook)
- [mdbook-svgbob](https://github.com/boozook/mdbook-svgbob)

First clone the the following repository.

```shell
git clone https://github.com/mh182/comprehensive-rust.git 
cd comprehensive-rust
```

Then install these tools with:

```shell
cargo install mdbook
cargo install mdbook-svgbob
```

Run

```shell
mdbook serve
```

to start a web server with the course. You'll find the content on
<http://localhost:3000>. You can use `mdbook build` to create a static version
of the course in the `book/` directory.

<details>

Most code samples are editable like shown above. A few code samples
are not editable for various reasons:

- The embedded playgrounds cannot execute unit tests. Copy-paste the
  code and open it in the real Playground to demonstrate unit tests.

- The embedded playgrounds lose their state the moment you navigate
  away from the page!

</details>
