## Tony Slosar

**TODOMODO.IO AGENCY LLC** &nbsp;·&nbsp; [slosars.me](https://slosars.me) &nbsp;·&nbsp; [t.me/toneron2](https://t.me/toneron2)

**An AI agent can act. It usually cannot show why the action was permitted.** In healthcare that
question has a legal answer, and a confidence score is not one.

Working implementations, specifications and research prototypes, not products. Each README states
what runs and what does not. For collaboration on the devices, healthcare pilots, or agency work on
governed agent systems: [t.me/toneron2](https://t.me/toneron2) or anthonyslosar@gmail.com.

### Run it

**[URGE](https://github.com/toneron2/URGE)**, the governance engine, evaluates a policy expression
across seven formal logics and returns a verdict with its derivation.
[Run the demo in the browser](https://toneron2.github.io/URGE/demo/) &nbsp;·&nbsp;
[source](https://github.com/toneron2/URGE) &nbsp;·&nbsp; [docs](https://docs.rs/urge)

### TODOMODO

One architecture converging on one product line: devices at the edge, one portal, services behind it.

```
 device ──▶ WebTransport / HTTP/3 ──▶ igent.me (portal) ──▶ BROAD (service #1)
                                       URGE gates every call:
                                       ALLOW / DENY + reasoning trace
```

| | Repository | What it is | Status |
|---|---|---|---|
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/physicalized-agent.png" width="80" alt="physicalized‑agent"> | **[physicalized‑agent](https://github.com/toneron2/physicalized-agent)** | A healthcare sensor head: cameras, microphones and local safety checks on a Raspberry Pi 5. | Procurement in process. |
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/urge.png" width="80" alt="URGE"> | **[URGE](https://github.com/toneron2/URGE)** | The governance engine, in Rust: a verdict with its derivation for every call. | Published: six crates on crates.io, docs on docs.rs, the demo runs in the browser. |
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/broad.png" width="80" alt="broad"> | **[broad](https://github.com/toneron2/broad)** | The first service: a healthcare agentic ERP design where every agent action passes a formal check. | Specification and partial implementation. |
| | **[igent](https://github.com/toneron2/igent)** · **[identities](https://github.com/toneron2/identities)** · **[bolt-buddy](https://github.com/toneron2/bolt-buddy)** · **[silent-drone](https://github.com/toneron2/silent-drone)** | The device-to-portal contract, the six agent identities, and two further igents: a vehicle ride-along and a drone. | Procurement in process. |

### Standalone

| | Repository | What it is | Status |
|---|---|---|---|
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/sfh-os.png" width="80" alt="SFH-OS"> | **[SFH-OS](https://github.com/toneron2/SFH-OS)** | Fractal acoustic horns, from geometry through acoustic simulation to L-PBF build preparation. | Geometry and acoustic simulation are implemented; fabrication and visualization are interface stubs, and no horn has been machined. |
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/rws.png" width="80" alt="RWS"> | **[RWS](https://github.com/toneron2/RWS)** | Air-handling-unit design and estimation by seven agents over ASHRAE calculators. | Specification, four MCP servers and a scripted demonstration, December 2025. |
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/hum2hendrix.png" width="80" alt="hum2hendrix"> | **[hum2hendrix](https://github.com/toneron2/hum2hendrix)** | Hummed melodies to MIDI, quantized to a scale and a grid, for rendering as guitar. | Audio to MIDI, quantization and piano-roll views run, with 68 tests; rendering is not built. |

<details>
<summary>Other repositories</summary>

| | Repository | What it is | Status |
|---|---|---|---|
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/agent-world.png" width="80" alt="agent-world"> | **[agent-world](https://github.com/toneron2/agent-world)** | Agent activity rendered as a game world. The README is the postmortem. | A failed experiment, kept public. |
| | **[agentic-platform](https://github.com/toneron2/agentic-platform)** | Project scaffolding for long-running work: thought capture and dependency-aware tasks. | v1.0, January 2026. A test, kept public, no further work. |
| | **[robosnomo](https://github.com/toneron2/robosnomo)** | A 1976 Polaris Colt snowmobile made autonomous, in three layers on a CAN bus. | Architecture documented, one of eight hardware components acquired, nothing built. |

</details>

Written with AI tooling, which is also the subject.
