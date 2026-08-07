[![LabWired — build and test embedded systems without waiting on hardware](https://raw.githubusercontent.com/LabWired/.github/main/profile/banner.png)](https://labwired.com)

**We make hardware easy.**

LabWired lets you build and test embedded systems without waiting on hardware. Lay out a board and
its parts in the browser, write and compile the firmware, and run it on a register-accurate
simulation of the chip. The simulation is deterministic, so the same firmware behaves the same way
every time — a result is a real pass or fail, not a guess from reading the code.

[labwired.com](https://labwired.com) &nbsp;·&nbsp; [Playground](https://app.labwired.com) &nbsp;·&nbsp; [Start a repo with CI wired up](https://github.com/LabWired/firmware-ci-starter/generate) &nbsp;·&nbsp; contact@labwired.com

## Who it's for

**Makers.** Design a board in the Playground, drop in parts, wire it up, and watch the firmware run
in your browser. Free to try, nothing to buy first.

**Teams.** Gate CI and real hardware on register-accurate behaviour, catch firmware bugs before a
board is on the desk, and drive the whole thing from your own agent or ours, on-prem if you need it.

Both run on the same simulation underneath. When you're ready, the same binary runs on a real board
over WebUSB-JTAG.

## What you can do

| | |
|---|---|
| **Design** | Lay out boards, parts, and wiring in the browser Playground. |
| **Build** | Write firmware in Studio or VS Code and compile it hosted (PlatformIO, Zephyr). |
| **Run and verify** | Run on the deterministic simulator and check behaviour against what you specified. |
| **CI and hardware** | Gate merges on a simulation run, then run the same binary on a real board. |
| **Agents** | An MCP interface, ready-made skills, and a preconfigured agent. |

Silicon we model: STM32 · ESP32 (Xtensa and RISC-V) · nRF52 / nRF54 · RP2040 · Cortex-M.

## Works with agents

People use the Playground and the Studio IDE, plus a VS Code extension. Agents drive the same tools
over MCP: connect Claude Code or Codex, or use the LabWired agent, which comes preconfigured and can
run on a local model with no internet.

## Repositories

| Repo | What it is |
|------|------------|
| [**agent**](https://github.com/LabWired/agent) | The LabWired agent — opencode preconfigured for firmware, runs on a local model offline |
| [**firmware-test**](https://github.com/LabWired/firmware-test) | Run LabWired simulation tests in GitHub Actions — no hardware, no toolchain |
| [**firmware-ci-starter**](https://github.com/LabWired/firmware-ci-starter) | Template repo — firmware, a test script, and CI wired up on your first push |
| [**skills**](https://github.com/LabWired/skills) | Agent skills for firmware work, starting with `firmware-verification` |
| [**labwired-cra-evidence**](https://github.com/LabWired/labwired-cra-evidence) | CRA-style secure-boot / signed-OTA evidence pack, regenerated in CI on a virtual nRF52840 |
