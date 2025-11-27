### 📂 File: `01-getting-started/hello-world.md`
*(Explaining Cargo vs Rustc)*

```markdown
# 🌍 Hello World: The Cargo Way

In other languages, you might start by creating a single file. In Rust, we use **Cargo**.

## 📦 What is Cargo?
Cargo is Rust's **Package Manager** and **Build System** wrapped in one. It handles:
1.  Downloading libraries (dependencies).
2.  Compiling your code.
3.  Linking libraries.
4.  Running tests.

> **Rule #1:** Never invoke `rustc` manually unless you are building a compiler. Always use `cargo`.

## 🚀 Creating Your First Project

Open your terminal and navigate to your coding folder.

```bash
cargo new hello_rust
cd hello_rust
The Folder Structure
Cargo created this for you:

Plaintext

hello_rust/
├── Cargo.toml    <-- The configuration file (like package.json)
├── src/
│   └── main.rs   <-- Your code lives here
└── .gitignore    <-- Git is initialized automatically
Analyzing src/main.rs
Open src/main.rs. You will see:

Rust

fn main() {
    println!("Hello, world!");
}
fn: Keyword to define a function.

main(): The entry point of every Rust program.

println!: This is a Macro (noticed the !). Macros write code for you. Regular functions do not have !.

▶️ Running the Code
Run this command:

Bash

cargo run
Output:

Plaintext

   Compiling hello_rust v0.1.0 (...)
    Finished dev [unoptimized + debuginfo] target(s) in 0.42s
     Running `target/debug/hello_rust`
Hello, world!
🔍 Deep Dive: What just happened?
Compiling: Cargo translated your Rust code into Machine Code (0s and 1s specific to your CPU).

Linking: It wrapped it into an executable binary.

Running: It executed the binary file located at ./target/debug/hello_rust.

⚡ Speed Mode: Release Builds
By default, cargo run builds a Debug version. It is slow but compiles fast and has extra info for debugging.

When you want to ship your app, run:

Bash

cargo run --release