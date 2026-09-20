## Tony Slosar

**TODOMODO.IO AGENCY LLC** &nbsp;·&nbsp; [slosars.me](https://slosars.me) &nbsp;·&nbsp; [t.me/toneron2](https://t.me/toneron2)

One architecture, tested in several places, converging on one product line: devices at the
edge, one portal, services behind it. The other repositories are standalone projects that
share the account and, where noted, the pattern.

### The problem

An AI agent can act. It usually cannot show why the action was permitted. In healthcare that
question has a legal answer, and a confidence score is not one.

### TODOMODO

```
 device ──▶ WebTransport / HTTP/3 ──▶ igent.me (portal) ──▶ BROAD (service #1)
                                       URGE gates every call:
                                       ALLOW / DENY + reasoning trace
```

| | Repository | What it is | Status |
|---|---|---|---|
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/physicalized-agent.png" width="64" alt="physicalized‑agent"> | **[physicalized‑agent](https://github.com/toneron2/physicalized-agent)** | A low-cost healthcare sensor head: stereo cameras, two MEMS microphones in acoustic horns, one ESP32-P4. Deterministic signal processing produces bearings and ranges; a local state machine handles safety; telemetry streams to the portal over WebTransport. | The sensor head is specified and not yet built. |
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/urge.png" width="64" alt="URGE"> | **[URGE](https://github.com/toneron2/URGE)** | The governance engine, in Rust. Evaluates a policy expression across seven formal logics, cross-validates the results, returns a verdict with its derivation. [Demo](https://toneron2.github.io/URGE/demo/) runs in the browser. | Published: six crates on crates.io, docs on docs.rs, the demo runs in the browser. |
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/broad.png" width="64" alt="broad"> | **[broad](https://github.com/toneron2/broad)** | The first service behind the portal: a healthcare agentic ERP design (ERPNext, n8n, FHIR R4) where every agent action passes a formal check first. Holds the 2025 specifications and the shell logic engine URGE grew from. | Specification and partial implementation. |

### Standalone

| | Repository | What it is | Status |
|---|---|---|---|
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/sfh-os.png" width="64" alt="SFH-OS"> | **[SFH-OS](https://github.com/toneron2/SFH-OS)** | Fractal acoustic horns, from geometry through acoustic simulation to L-PBF build preparation. Six Claude Code skills, four MCP servers. | Geometry, acoustic simulation and build preparation are implemented; no horn has been machined. |
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/rws.png" width="64" alt="RWS"> | **[RWS](https://github.com/toneron2/RWS)** | Air-handling-unit design and estimation as seven cooperating agents over psychrometric, component, sizing and cost calculators. | Specification, four MCP servers and a scripted demonstration, December 2025. |
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/agent-world.png" width="64" alt="agent-world"> | **[agent-world](https://github.com/toneron2/agent-world)** | Agent activity rendered as a game world. The README is the postmortem. | A failed experiment, kept public. |
| | **[agentic-platform](https://github.com/toneron2/agentic-platform)** | Project scaffolding for long-running work: thought capture, dependency-aware tasks, an agent that files both. | v1.0, January 2026. A test, kept public, no further work. |
| | **[robosnomo](https://github.com/toneron2/robosnomo)** | A 1976 Polaris Colt snowmobile made autonomous: perception, engine control and actuation as three layers on a CAN bus. | Architecture documented, one of eight hardware components acquired, nothing built. |
| | **[hum2hendrix](https://github.com/toneron2/hum2hendrix)** | Hummed melodies to rendered guitar: pitch detection, scale and grid quantization, amp simulation. | The audio-to-MIDI stage is in progress and rendering is not built. |

### Reading this account

Working implementations, specifications and research prototypes; not products. Each README
states what runs and what does not. Written with AI tooling, which is also the subject.
