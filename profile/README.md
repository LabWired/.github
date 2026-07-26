# LabWired

LabWired is a platform for building and testing embedded systems without waiting on hardware. You can
lay out a board and its parts in the browser, write and compile the firmware, and run it on a
register-accurate simulation of the chip. The simulation is deterministic, so the same firmware
behaves the same way every time. You can gate CI on the result, or run the same binary on a real
board over WebUSB-JTAG.

It works for people and for AI agents. People use the Playground and the Studio IDE, plus a VS Code
extension. Agents drive the same tools over MCP: connect Claude Code or Codex, or use the LabWired
agent, which comes preconfigured and can run on a local model with no internet.

The core of it is the oracle. It runs firmware and reports whether it actually worked, so a result is
a real pass or fail instead of a guess from reading the code.

labwired.com · app.labwired.com

## What's here

- **Design** — lay out boards, parts, and wiring in the browser Playground.
- **Build** — write firmware in Studio or VS Code and compile it hosted (PlatformIO, Zephyr).
- **Run and verify** — run on the deterministic simulator and check behaviour against what you specified.
- **CI and hardware** — gate merges on a simulation run, and run the same binary on a real board.
- **Agents** — an MCP interface, ready-made skills, and a preconfigured agent.

## Repos

| Repo | What it is |
|------|------------|
| [agent](https://github.com/LabWired/agent) | The LabWired agent: opencode preconfigured for firmware, runs on a local model offline |
| [skills](https://github.com/LabWired/skills) | Agent skills for firmware work, starting with `firmware-verification` |
| [firmware-test](https://github.com/LabWired/firmware-test) | Run LabWired simulation tests in GitHub Actions, no hardware or toolchain needed |
| [firmware-ci-starter](https://github.com/LabWired/firmware-ci-starter) | Template repo with firmware, a test script, and CI wired up |
