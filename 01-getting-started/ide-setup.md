### 📂 File: `01-getting-started/ide-setup.md`
*(The most important file. A bad IDE setup makes Rust feel impossible.)*

```markdown
# 💻 The Perfect Rust IDE Setup

Rust is a static, strongly-typed language. This means the tooling can be **incredible**. If set up correctly, the IDE will write half the code for you, show types inline, and catch errors before you save.

## 🥇 The Gold Standard: VS Code

Visual Studio Code is the most popular editor for Rust. Here is the optimized configuration.

### 1. Essential Extensions

Do **NOT** install the extension named "Rust" (it is deprecated). Install these specific ones:

| Extension | Why? |
| :--- | :--- |
| **rust-analyzer** | The brain. It provides auto-complete, go-to-definition, and type hints. |
| **CodeLLDB** | The debugger. Allows you to set breakpoints and inspect variables. |
| **Even Better TOML** | Syntax highlighting for `Cargo.toml` files. |
| **Error Lens** | Shows compilation errors *inline* next to your code line (Game Changer). |
| **Crates** | Helps manage dependencies versions in `Cargo.toml`. |

### 2. Critical `settings.json` Config

To make the experience smooth, we want Rust to format our code every time we save, and run "Clippy" (the advanced linter) to check for issues.

Open VS Code Settings (JSON) and add:

```json
"[rust]": {
    "editor.defaultFormatter": "rust-lang.rust-analyzer",
    "editor.formatOnSave": true
},
"rust-analyzer.check.command": "clippy",
"rust-analyzer.inlayHints.typeHints.enable": true,
"rust-analyzer.inlayHints.parameterHints.enable": true
3. Understanding Inlay Hints
Once rust-analyzer is running, you will see gray text appearing in your code that you didn't type. These are Inlay Hints. They show you the inferred types of variables.

Don't try to delete them! They are virtual helpers.

🥈 The Premium Option: RustRover (JetBrains)
If you come from Java/Kotlin/Python and love IntelliJ:

RustRover is a dedicated Rust IDE by JetBrains.

Pros: Incredible refactoring tools, deep database integration.

Cons: Paid product (free for non-commercial use sometimes), heavier on RAM.

🥉 The Vim/Neovim Route
For the terminal warriors:

Install LazyVim or AstroNvim (they have pre-configured Rust packs).

Ensure rust-analyzer binary is in your path.