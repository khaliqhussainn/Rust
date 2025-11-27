### 📂 File: `02-why-rust/use-cases.md`
*(Validating the language with big tech examples.)*

```markdown
# 🚀 Who is using Rust & Why?

Rust is no longer a "niche" academic language. It is powering the infrastructure of the internet.

## 1. Discord (Performance)
**The Problem:** Discord used Go for their "Read States" service. Go uses a Garbage Collector. Every few minutes, the GC would run, freezing the service for milliseconds. This caused "lag spikes" for millions of users.
**The Fix:** They rewrote the service in Rust.
**The Result:** Rust has no Garbage Collector. The lag spikes disappeared completely. The service became faster and used less RAM.

## 2. Microsoft & Windows (Security)
**The Problem:** 70% of all security vulnerabilities (hacks) in Windows were caused by memory safety issues (using C++).
**The Fix:** Microsoft is now rewriting core parts of the Windows Kernel in Rust.
**The Result:** Rust mathematically guarantees memory safety, making those classes of bugs impossible.

## 3. The Linux Kernel
**The Milestone:** As of version 6.1, Rust is officially supported in the Linux Kernel alongside C. It is the first language *ever* to join C in the kernel. This allows for writing safer drivers that won't crash the whole OS.

## 4. Cloudflare (WebAssembly)
Cloudflare Workers allow you to run code on the edge. Because Rust has a tiny runtime (no heavy virtual machine), it starts up instantly, making it perfect for serverless computing.

## Summary: When to use Rust?
* ✅ **System Programming:** Operating systems, drivers, game engines.
* ✅ **CLI Tools:** Fast, single-binary tools (like `ripgrep`).
* ✅ **Web Services:** High-performance APIs (backend).
* ✅ **WebAssembly:** Running heavy code in the browser.
* ❌ **Quick Prototyping:** Python/JS is faster to write if performance doesn't matter.