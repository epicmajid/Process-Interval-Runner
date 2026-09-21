# Process Interval Runner

<div align="center">

![Windows](https://img.shields.io/badge/Platform-Windows-0078D6?style=for-the-badge&logo=windows)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Production--Ready-brightgreen?style=for-the-badge)
![Architecture](https://img.shields.io/badge/Architecture-x64%20%7C%20x86-orange?style=for-the-badge)

<p align="center">
  <b>A lightweight, high-precision background interval execution and lifecycle management engine for Windows.</b>
</p>

---

</div>

## 📌 Overview

**Process Interval Runner** is an enterprise-grade utility designed for reliable, automated execution of applications and scripts at specified time intervals. Built specifically for system administrators, DevOps, and power users, it ensures continuous process lifecycle management, prevents overlapping executions, and provides detailed runtime tracking with minimal resource footprint.

---

## ⚡ Core Highlights

* **⏱️ Micro-Precision Scheduling:** Sub-second accuracy across customizable loop timers.
* **🛡️ Process Isolation & Anti-Collision:** Detects active target instances before execution to prevent memory corruption or duplicate tasks.
* **⚡ Ultra-Low Overhead:** Optimized background thread management utilizing negligible CPU and RAM resources.
* **📊 Comprehensive Audit Logging:** Real-time PID tracking, exit code verification, and timestamped log generation.
* **🛠️ Scripting Engine Support:** Out-of-the-box compatibility with `.exe`, `.bat`, `.cmd`, `.ps1`, and custom CLI binaries.

---

## 🏗️ System Architecture

```
                       +-----------------------------------+
                       |    Process Interval Runner        |
                       +-----------------+-----------------+
                                         |
                                         v
                             +-----------+-----------+
                             |   Interval Timer      |
                             +-----------+-----------+
                                         |
                                         v
                             +-----------+-----------+
                             | Check Active Instance |
                             +-----------+-----------+
                                         |
                       +-----------------+-----------------+
                       |                                   |
            [ Instance Running ]                   [ Instance Idle ]
                       |                                   |
                       v                                   v
             ( Terminate / Wait )                 ( Spawn Target Process )
                       |                                   |
                       +-----------------+-----------------+
                                         |
                                         v
                             +-----------+-----------+
                             |  Log PID & Exit Code  |
                             +-----------------------+
```

---

## ⚙️ Configuration Parameters

| Parameter | Type | Required | Description |
| :--- | :---: | :---: | :--- |
| `Target` | `String` | Yes | Path to executable file (`.exe`, `.bat`, `.ps1`) |
| `Interval` | `Integer` | Yes | Frequency interval in seconds |
| `Arguments` | `String` | No | Additional runtime CLI flags |
| `Overlaps` | `Boolean` | No | Allow or restrict concurrent process execution |

---

## 👨‍💻 Developer & Author

<div align="center">

<a href="https://github.com/epicmajid">
  <img src="https://github.com/epicmajid.png" width="120" height="120" style="border-radius: 50%;" alt="majid avatar" />
</a>

### **majid**
**[@epicmajid](https://github.com/epicmajid)**

[![GitHub Follow](https://img.shields.io/github/followers/epicmajid?label=Follow%20%40epicmajid&style=social)](https://github.com/epicmajid)

</div>

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for more information.
