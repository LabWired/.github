# LabWired

**A deterministic firmware simulator — the hardware oracle for AI agents.**

Build, run, and verify embedded firmware against real, register-level silicon models — no board on the desk required. Deterministic by construction, so an agent (or your CI) gets the same answer every time.

→ [labwired.com](https://labwired.com) · [app.labwired.com](https://app.labwired.com)

## Projects

| Repo | What it is |
|------|------------|
| [labwired-core](https://github.com/w1ne/labwired-core) | Deterministic firmware simulator for ARM Cortex-M and RISC-V |
| [labwired-action](https://github.com/w1ne/labwired-action) | Run LabWired simulation tests in GitHub Actions |
| [labwired-lab-template](https://github.com/w1ne/labwired-lab-template) | Template repo that gates merges on the LabWired oracle |
| [labwired-zephyr](https://github.com/w1ne/labwired-zephyr) | Run Zephyr applications in the LabWired simulator |
| [labwired-vscode](https://github.com/w1ne/labwired-vscode) | VS Code extension |
| [labwired-flasher](https://github.com/w1ne/labwired-flasher) | Linux-native CLI for reflashing NUCLEO / Discovery boards |

## Why deterministic?

Real silicon is faithful but flaky in a loop; pure mocks are stable but lie. LabWired models the peripheral surface at the register level so results are both **repeatable** and **true to hardware** — the property an autonomous agent needs to trust its own build → run → verify loop.
