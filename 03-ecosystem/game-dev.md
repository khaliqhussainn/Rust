# 🎮 Game Development

Rust is becoming a favorite for Game Devs because of the **Entity Component System (ECS)** pattern, which fits Rust's ownership model perfectly.

## 🕹️ Bevy Engine
**The Big Player.** Bevy is a data-driven game engine built in Rust, for Rust.
* **ECS First:** Everything is a system. It is incredibly parallel. Bevy automatically runs logic on different CPU cores without you asking.
* **State:** Still in 0.x (rapid changes), but capable of 2D and 3D.

## 🤖 Godot-Rust (Gdext)
Love the Godot Editor but hate GDScript's performance?
* **Use Godot-Rust.** You build your UI and scenes in Godot, but write the logic in Rust.
* **Pros:** Best of both worlds—visual editor + fast logic.

## 🦀 WGPU
This is the low-level graphics library (based on WebGPU). It is what powers Bevy and many other tools. It allows you to write graphics code that runs on Vulkan, Metal, DX12, and the Web seamlessly.