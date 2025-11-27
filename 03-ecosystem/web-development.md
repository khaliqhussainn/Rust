# 🌐 Web Development in Rust

"Is Rust web-ready?" **Yes.**
It is widely used for high-performance backends.

## 🐎 The Backend Frameworks

### 1. Axum (Recommended)
Created by the Tokio team (the asynchronous runtime).
* **Pros:** Very ergonomic, feels like Express (JS) but typed, amazing integration with the async ecosystem.
* **Cons:** Newer than Actix.

### 2. Actix-Web
The veteran speedster.
* **Pros:** consistently tops the "TechEmpower" benchmarks as one of the fastest web frameworks *in the world*.
* **Cons:** Slightly more complex syntax (actors model).

### 3. Rocket
The "Battery Included" framework.
* **Pros:** Beautiful syntax, looks like Python/Django code.
* **Cons:** Historically relied on Nightly Rust (now stable, but compilation is slower).

## 🎨 The Frontend (WASM)

Yes, you can write Frontend code in Rust instead of JavaScript using WebAssembly.

* **Leptos:** The current favorite. Uses signals (like SolidJS) for extreme performance.
* **Yew:** The React-like veteran. Uses a Virtual DOM.

## 🗄️ Database Interaction (ORM)

Don't write raw SQL. Use **SQLx** or **Diesel**.

* **SQLx:** Writes raw SQL, but checks if your SQL is valid *at compile time*. If you make a typo in your SQL query, the code won't compile. (Magic! ✨)
* **Diesel:** A traditional ORM. You write Rust structs, it handles the SQL.