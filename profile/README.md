# LabWired

**Every AI can write firmware now. LabWired is the layer that proves it runs** — the same binary in
sim, on the bench, and in CI, byte-exact. Our client isn't human anymore; it's an agent.

Generation is commoditizing; trustworthy **verification** is the bottleneck. LabWired is the
deterministic gate every firmware agent passes through: the agent **proposes** a build, the oracle
**disposes** — a pass/fail verdict it cannot fake. No "the AI says it works."

Run embedded firmware against deterministic, register-level silicon twins — no board on the desk.
Same input, same result every run, so an agent can debug, write drivers, and trust its own
build → run → **verify** loop without a HIL rig or flashing delays. Humans step in through Studio and
VS Code to check the work.

**Bring your own agent** — Claude Code / Codex over MCP — **or use ours**, the LabWired agent
(opencode wired to the oracle; local-model & air-gap ready).

[labwired.com](https://labwired.com) · [app.labwired.com](https://app.labwired.com)

## Built for agents

- **Deterministic execution** — bit-accurate, identical `result.json` and `trace.vcd` every run. No flakes to reason around.
- **The oracle gates it** — a "verified" verdict is server-side and deterministic, never an LLM self-report. Only a real pass counts.
- **Structured observability** — memory maps, pin state, and traces as JSON and VCD, not screens to scrape.
- **Real-board parity** — the same binary runs in the sim and, via WebUSB-JTAG, on the bench.

## Repos

| Repo | What it is |
|------|------------|
| [agent](https://github.com/LabWired/agent) | The LabWired firmware agent — opencode wired to the oracle; local-model & air-gap ready |
| [skills](https://github.com/LabWired/skills) | Agent Skills for firmware — starting with `firmware-verification`, the oracle gate |
| [firmware-test](https://github.com/LabWired/firmware-test) | Run LabWired firmware simulation tests in GitHub Actions — no hardware, no toolchain |
| [firmware-ci-starter](https://github.com/LabWired/firmware-ci-starter) | Template repo — firmware, test script, and CI; a passing simulation run on your first push |
