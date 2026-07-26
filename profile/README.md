# LabWired

LabWired is a simulator for embedded firmware. You give it a compiled binary, it runs on a
register-accurate model of the chip, and it tells you whether the firmware did what you said it
should. Runs are deterministic, so you get the same result every time, whether you run it locally,
in CI, or against a board on your desk.

It's built to be driven by AI agents. The agent writes firmware and runs it here to find out if it
works, instead of guessing from the source. Connect Claude Code or Codex to it over MCP, or use the
LabWired agent, which comes preconfigured and can run against a local model with no internet.

labwired.com · app.labwired.com

## What it does

- Runs are deterministic: the same binary gives the same result and the same trace every time, so tests don't flake.
- A pass or fail comes from the simulator, not from the model saying it worked.
- Output is structured: register values, pin state, and traces as JSON and VCD.
- The same binary also runs on real hardware over WebUSB-JTAG.

## Repos

| Repo | What it is |
|------|------------|
| [agent](https://github.com/LabWired/agent) | The LabWired agent: opencode preconfigured for firmware, runs on a local model offline |
| [skills](https://github.com/LabWired/skills) | Agent skills for firmware work, starting with `firmware-verification` |
| [firmware-test](https://github.com/LabWired/firmware-test) | Run LabWired simulation tests in GitHub Actions, no hardware or toolchain needed |
| [firmware-ci-starter](https://github.com/LabWired/firmware-ci-starter) | Template repo with firmware, a test script, and CI wired up |
