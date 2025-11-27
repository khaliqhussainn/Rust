# 🛠️ Rust Installation Guide

Installing Rust is usually easy, but if you skip a step (especially on Windows), nothing will work. We use **Rustup**, the official toolchain installer.

## 🪟 Windows Users (Read Carefully!)

Before installing Rust, you **MUST** have the C++ Build Tools. Rust compiles to native code, so it needs a linker.

1.  **Download Visual Studio Build Tools** (Not VS Code, but the Build Tools).
2.  Run the installer and check the box: **"Desktop development with C++"**.
3.  Ensure the Windows SDK is selected on the right sidebar.
4.  Install and **Restart your computer**.

**Now, install Rust:**
1.  Go to [rustup.rs](https://rustup.rs/).
2.  Download `rustup-init.exe`.
3.  Run it. Press `1` and Enter for standard installation.

---

## 🍎 macOS & 🐧 Linux Users

Open your terminal and run this magic command:

```bash
curl --proto '=https' --tlsv1.2 -sSf [https://sh.rustup.rs](https://sh.rustup.rs) | sh
Follow the on-screen instructions (usually just press 1). Once it finishes, run:

Bash

source $HOME/.cargo/env
✅ Verification
Close your terminal and open a new one. Type:

Bash

rustc --version
If you see something like rustc 1.75.0 (82e1608df 2023-12-21), congratulations! You are a Rustacean. 🦀

🔄 Lifecycle Commands
Rust updates frequently (every 6 weeks). Here is how you manage it:

Update Rust: rustup update

Uninstall Rust: rustup self uninstall

Check Documentation locally: rustup doc (Opens the offline book in your browser).