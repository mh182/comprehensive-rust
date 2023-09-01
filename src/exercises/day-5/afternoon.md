# Day 5: Afternoon Exercises

You should do the following Rustlings exercises:

- `clippy1`
- `clippy2`
- `clippy3`

---

## Web server

Now that we gone through [the blog post about Axum](https://mo8it.com/blog/getting-started-with-rust-backends/), create a new Rust project and reproduce the server presented in that blog post.

_Don't just copy paste!_ Type it yourself to get a better understanding of what the code snippets are doing.

**If you have time left**, extend the functionality of the server:

- Instead of just printing the submitted form, append its content to a log file.
- Create a route to `/submissions` that returns the content of that form log file (as a `String` for simplicity, not HTML).
