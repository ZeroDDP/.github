<div align="center">

<img src="assets/banner.svg" alt="ZeroDDP — student software development team, Tomsk Polytechnic University" width="100%">

<br>

**We build tools for developers and DevOps engineers.**<br>
Student projects, done the grown-up way: pull requests, code review, CI on three operating systems and tests on every commit.

<br>

![Python](https://img.shields.io/badge/Python_3.12-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![Svelte](https://img.shields.io/badge/Svelte_5-FF3E00?style=flat-square&logo=svelte&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

</div>

---

## 🛰️ Synex

**One window for your servers.** Synex is a desktop app that brings together an SSH terminal,
live monitoring, Docker, an SFTP file manager and git deploys — the things you would otherwise
juggle across five different tools.

| | |
|---|---|
| 🔐 **SSH** | Several sessions at once, encrypted key vault, saved connections, host key verification (TOFU) |
| 📈 **Monitoring** | CPU, RAM, disk, network and GPU in real time, streamed over WebSocket |
| 🐳 **Docker** | Containers at a glance: start, stop, restart, live logs |
| 📁 **Files** | Two-pane SFTP manager: whole folders, checksums, cancel at any time |
| 🚀 **Git** | Pull and deploy on the server in one click |

**Under the hood:** a microkernel. The core only provides the platform, the UI shell and a data bus;
every feature is a plugin you can switch on and off while the app is running.

```mermaid
flowchart LR
    UI["🖥️ UI<br/>Svelte 5"] <-- "REST + WebSocket" --> API["⚙️ Backend<br/>FastAPI · plugins"]
    API <-- "IPC · MessagePack" --> W["🦀 Worker<br/>Rust · russh"]
    W <-- "SSH / SFTP" --> S[("☁️ Your servers")]
```

<p align="center"><a href="https://github.com/ZeroDDP/Synex"><b>→ ZeroDDP/Synex</b></a></p>

---

## 👥 Team

<table>
  <tr>
    <td align="center" width="25%">
      <a href="https://github.com/Rinneway"><img src="https://github.com/Rinneway.png?size=120" width="80" alt=""><br><b>Danil Tyustin</b></a><br>
      <sub>Backend & logic</sub>
    </td>
    <td align="center" width="25%">
      <a href="https://github.com/MAGVANCHiK"><img src="https://github.com/MAGVANCHiK.png?size=120" width="80" alt=""><br><b>Ivan Blinnikov</b></a><br>
      <sub>Core (Rust)</sub>
    </td>
    <td align="center" width="25%">
      <a href="https://github.com/Prefifix"><img src="https://github.com/Prefifix.png?size=120" width="80" alt=""><br><b>Ilya Kolesnikov</b></a><br>
      <sub>Frontend</sub>
    </td>
    <td align="center" width="25%">
      <a href="https://github.com/appolsmirnykh-ship-it"><img src="https://github.com/appolsmirnykh-ship-it.png?size=120" width="80" alt=""><br><b>Polina Smirnykh</b></a><br>
      <sub>Design</sub>
    </td>
  </tr>
</table>

## 🛠️ How we work

- **`main` always works.** Changes land only through pull requests with green checks.
- **One task, one branch:** `backend/…`, `core/…`, `frontend/…`, `docs/…`.
- **Small, clear commits** in the imperative mood: *Add IPC client*, *Fix worker startup*.
- **Tests are part of the feature:** unit tests on Linux, Windows and macOS, integration tests against a real SSH server.

---

<div align="center">
<sub>Tomsk Polytechnic University · School of Information Technology and Robotics Engineering (ESITR) · 2026</sub>
</div>
