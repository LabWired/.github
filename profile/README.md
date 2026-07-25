# LabWired

An agent-first hardware oracle. Our main client is not human anymore, it is an agent.

Write, build, run, and verify embedded firmware against deterministic, register-level silicon twins — no board on the desk. The same input gives the same result every run, so an agent can debug, write drivers, and trust its own build-run-verify loop without a HIL rig or flashing delays. Humans step in through Studio and VS Code to check the work.

The whole loop, one place: author firmware in the browser Playground or the Studio IDE, compile it hosted (PlatformIO / Zephyr `west build`), run it against the silicon twin, and gate CI or a real board on the result. Agents drive it over MCP from Claude or Codex.

[labwired.com](https://labwired.com) · [app.labwired.com](https://app.labwired.com)

## Built for agents

- **Deterministic execution** — bit-accurate, identical `result.json` and `trace.vcd` every run. No flakes to reason around.
- **Structured observability** — memory maps, pin state, and traces as JSON and VCD, not screens to scrape.
- **Metered** — simulation minutes tracked, so a fleet can budget an agent's verification spend.
- **Real-board parity** — the same firmware runs in the sim and, via WebUSB-JTAG, on the bench.

## Repos

| Repo | What it is |
|------|------------|
| [labwired-core](https://github.com/w1ne/labwired-core) | The oracle engine — deterministic Cortex-M / RISC-V simulation |
| [labwired-action](https://github.com/w1ne/labwired-action) | Gate CI on a firmware run, no build step |
| [labwired-lab-template](https://github.com/w1ne/labwired-lab-template) | Template repo that gates merges on the oracle |
| [labwired-zephyr](https://github.com/w1ne/labwired-zephyr) | Run Zephyr apps against the oracle |
| [labwired-vscode](https://github.com/w1ne/labwired-vscode) | VS Code extension — a viewer for what the agent produced |
| [labwired-flasher](https://github.com/w1ne/labwired-flasher) | CLI for reflashing NUCLEO / Discovery boards |
