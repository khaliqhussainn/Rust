# 🔌 Embedded Rust (IoT)

Rust is fantastic for hardware because it produces tiny binaries and needs no OS.

## `no_std`
Standard Rust (`std`) relies on an Operating System (for files, threads, time). On a microcontroller (like an Arduino), there is no OS.
Rust allows you to turn off the standard library with `#![no_std]`.

## ⚡ The HAL (Hardware Abstraction Layer)
Rust has a genius system called `embedded-hal`.
It defines generic traits for hardware pins (GPIO, UART, I2C).
This means a driver written for a specific sensor (like a thermometer) will work on **any** microcontroller that implements the HAL traits (ESP32, STM32, Arduino, Raspberry Pi Pico).

## 🚀 Embassy
The new hotness. **Async Rust on Embedded.**
Usually, async/await is for web servers. Embassy brings it to chips. You can run multiple tasks (blink LED, read sensor, send WiFi) efficiently on a tiny chip without a Real-Time Operating System (RTOS).