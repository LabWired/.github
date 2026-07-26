# LabWired

**We make hardware easy.**

LabWired lets you build and test embedded systems without waiting on hardware. Lay out a board and
its parts in the browser, write and compile the firmware, and run it on a register-accurate
simulation of the chip. The simulation is deterministic, so the same firmware behaves the same way
every time.

## Who it's for

**Makers.** Design a board in the Playground, drop in parts, wire it up, and watch the firmware run
in your browser. Free to try, nothing to buy first.

**Teams.** Gate CI and real hardware on register-accurate behaviour, catch firmware bugs before a
board is on the desk, and drive the whole thing from your own agent or ours, on-prem if you need it.

Both run on the same simulation underneath, so a result is a real pass or fail, not a guess from
reading the code. When you're ready, the same binary runs on a real board over WebUSB-JTAG.

## Works with agents

People use the Playground and the Studio IDE, plus a VS Code extension. Agents drive the same tools
over MCP: connect Claude Code or Codex, or use the LabWired agent, which comes preconfigured and can
run on a local model with no internet.

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
