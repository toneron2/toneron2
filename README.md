## Tony Slosar

Most of what follows is one architecture
tested in different places, and it is now converging on a single product line, **TODOMODO**:
devices at the edge, one portal, and services behind it. The rest are standalone projects
that share the account and, where the table says so, the pattern.

**TODOMODO.IO AGENCY LLC** &nbsp;·&nbsp; [slosars.me](https://slosars.me)

### The problem

An AI agent can act. It usually cannot prove why the action was permitted. That gap is
tolerable in ordinary software and unacceptable in healthcare, where "who accessed this
record, under what authority, and show me the reasoning" is a question with a legal answer.
Probabilistic systems answer it with a confidence score. That is not an answer.

### The system

**[The Physicalized Agent](https://github.com/toneron2/physicalized-agent) is the first
device.** A low-cost sensor head — stereo cameras, binaural MEMS microphones in tuned
acoustic horns, one ESP32-P4 — that computes *vectors* rather than guesses. Deterministic
signal processing instead of black-box inference is what makes it cheap, and cheap is the
point: the goal is a device you give to the patient, not one you sell to the building. It
runs a local governance state machine for safety overrides and streams logical telemetry to
the portal over **WebTransport on HTTP/3** — Chromium's QUIC, bidirectional, with the
governance heartbeat holding priority on stream 0 and video yielding to it. Connected, the
head works as the patient's advocate rather than the building's camera.

**[URGE](https://github.com/toneron2/URGE) is the reasoning core.** A deterministic policy
engine in Rust that evaluates a decision across seven kinds of formal logic, cross-validates
the results, and returns a full audit trace. The same input gives the same verdict every
time. **[Try it](https://toneron2.github.io/URGE/demo/)** — it runs in the browser.

**igent.me is the portal**: the one cloud-side thing every device talks to, where URGE gates
every capability call before a service sees it. **[BROAD](https://github.com/toneron2/broad)
is the first service behind it.** Business Resource Observability and Automation Deployment:
a healthcare agentic ERP built on FHIR R4 and clinical pathway standards, where every agent
action passes a formal access check before it executes and every decision is logged with its
reasoning.

The standalone projects test the same pattern against unrelated disciplines on purpose,
because that is the only honest way to find out whether it generalizes.

### The repositories

**TODOMODO**

| | | |
|---|---|---|
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/physicalized-agent.png" width="72" alt="physicalized‑agent"> | **[physicalized‑agent](https://github.com/toneron2/physicalized-agent)** | The design system for the sensor head — six Claude skills, three MCP servers, three schemas. Hardware referenced, not vendored. |
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/urge.png" width="72" alt="URGE"> | **[URGE](https://github.com/toneron2/URGE)** | The governance engine. Rust, seven logic paradigms, cross-paradigm validation, runs without an operating system. [Live demo](https://toneron2.github.io/URGE/demo/) |
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/broad.png" width="72" alt="broad"> | **[broad](https://github.com/toneron2/broad)** | The healthcare platform: workflow library, clinical pathways, and the access layer that fronts them. Specification and partial implementation. |

**Standalone**

| | | |
|---|---|---|
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/sfh-os.png" width="72" alt="SFH-OS"> | **[SFH-OS](https://github.com/toneron2/SFH-OS)** | Fractal acoustic horns, geometry through toolpaths. The pattern against manufacturing. Geometry, acoustic simulation and build preparation are implemented; no horn has been machined. |
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/rws.png" width="72" alt="RWS"> | **[RWS](https://github.com/toneron2/RWS)** | Six agents doing real ASHRAE calculations to design and estimate air handling units. The pattern against a regulated engineering discipline. Specification, four MCP servers and a scripted demonstration, December 2025. |
| <img src="https://raw.githubusercontent.com/toneron2/toneron2/main/icons/agent-world.png" width="72" alt="agent-world"> | **[agent-world](https://github.com/toneron2/agent-world)** | A failed experiment, kept public. Agent activity rendered as a game world. The README explains why that was the wrong answer. |
|  | **[agentic-platform](https://github.com/toneron2/agentic-platform)** | Project scaffolding for long-running work: idea capture, dependency-aware tasks, an agent that maintains both. v1.0, January 2026. A test, kept public, no further work. |
|  | **[robosnomo](https://github.com/toneron2/robosnomo)** | A 1976 Polaris Colt snowmobile made autonomous: brain, engine control and actuation as three layers on a CAN bus. Architecture documented, one of eight hardware components acquired, nothing built. |
|  | **[hum2hendrix](https://github.com/toneron2/hum2hendrix)** | Hummed melodies to rendered guitar solos: pitch detection, quantization, amp simulation. The audio-to-MIDI stage is in progress and rendering is not built. |

### How to read this account

These are working implementations, specifications and research prototypes, not commercial
products. The sensor head is specified and not yet built. Where something does not work, the
repository says so. I would rather publish an accurate account of a dead end than a polished
description of a project nobody can run.

Written with heavy use of AI tooling, which is also the subject.
