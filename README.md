# OpenJugglePlate

[English](./README.md) | [简体中文](./README.zh-CN.md) | [繁體中文](./README.zh-TW.md)

[![Status](https://img.shields.io/badge/status-planning%20%2F%20prototyping-4c8bf5)](#current-status)
[![License](https://img.shields.io/badge/license-Apache--2.0-1976d2)](./LICENSE)
![Vision](https://img.shields.io/badge/vision-top--view%20camera-2e7d32?logo=opencv&logoColor=white)
![Control](https://img.shields.io/badge/control-Linux%20SBC%20%2B%20STM32-8e24aa)
![Actuation](https://img.shields.io/badge/actuation-stepper%20motors-f57c00)

An open-source standalone ping-pong ball balancing and juggling robot with top-view vision, Linux SBC high-level control, and STM32 real-time motion control.

## Table of Contents

- [OpenJugglePlate](#openjuggleplate)
  - [Table of Contents](#table-of-contents)
  - [What This Project Is](#what-this-project-is)
  - [What It Tries To Do](#what-it-tries-to-do)
  - [What This First Version Focuses On](#what-this-first-version-focuses-on)
  - [Current Status](#current-status)
  - [Repository Structure](#repository-structure)
  - [Quick Start](#quick-start)
    - [1. Clone The Repository](#1-clone-the-repository)
    - [2. Read The Project Overview](#2-read-the-project-overview)
    - [3. Pick A Workstream](#3-pick-a-workstream)
    - [4. If You Want To Contribute](#4-if-you-want-to-contribute)
    - [5. If You Want To Build Along Early](#5-if-you-want-to-build-along-early)
  - [Contributing](#contributing)
  - [Safety Note](#safety-note)
  - [License](#license)

## What This Project Is

This repository is the public home of the `OpenJugglePlate` project.
The long-term goal is to make it a complete open-source robotics repository with:

- project documentation
- hardware design files
- firmware for `STM32`
- software for a Linux SBC such as `Orange Pi`, `Raspberry Pi`, or an `RK3588`-class board
- reproducible BOM and assembly guidance

At the moment, this is still an early-stage public build log and project skeleton rather than a finished machine release.

## What It Tries To Do

OpenJugglePlate is focused on one object only: a standard `40 mm` ping-pong ball.

The first practical version aims to:

- bring the ball back to the center of the plate
- keep it stable on the plate
- transition from plate balancing into controlled bouncing
- sustain continuous juggling

The implementation is intentionally narrow so the first public machine can be realistic and reproducible.
That means V1 is built around:

- `single top-view vision`
- `Linux SBC + STM32`
- a `3-actuator parallel platform`
- `stepper motors`

## What This First Version Focuses On

The first public version is mainly focused on:

- one target object: a standard `40 mm` ping-pong ball
- one practical sensing path: `single top-view vision`
- one pragmatic compute split: `Linux SBC + STM32`
- one reproducible motion platform: `3-actuator parallel platform`

That also means V1 is intentionally not trying to do everything at once.
For now, it does not aim to cover:

- multiple ball types or arbitrary objects
- automatic ball pickup or reload
- brushless primary actuation
- reinforcement learning as the baseline controller

## Current Status

`Planning / prototyping`

Right now the repository is focused on:

- public project structure
- documentation
- reference collection
- contribution workflow
- early subsystem placeholders

The actual hardware, firmware, and Linux SBC software will be added incrementally as the prototype moves forward.

## Repository Structure

```text
.
|-- .github/                  # Issue templates, PR template, CI, Pages workflows
|-- firmware/                 # STM32 real-time control side
|-- hardware/                 # CAD, mechanics, BOM, assembly side
|-- software/                 # Linux SBC vision and high-level control side
|-- README.md                 # English project overview
|-- README.zh-CN.md           # Simplified Chinese overview
|-- README.zh-TW.md           # Traditional Chinese overview
|-- CONTRIBUTING.md
|-- CODE_OF_CONDUCT.md
|-- SECURITY.md
|-- LICENSE
`-- NOTICE
```

Notes:

- The public repository is organized so hardware, firmware, and software can evolve in parallel.
- Some local planning material is intentionally kept private and is not part of the public repository.

## Quick Start

### 1. Clone The Repository

```bash
git clone https://github.com/Zw-awa/OpenJugglePlate.git
cd OpenJugglePlate
```

### 2. Read The Project Overview

Start with:

- [`README.md`](./README.md)
- [`hardware/README.md`](./hardware/README.md)
- [`firmware/README.md`](./firmware/README.md)
- [`software/README.md`](./software/README.md)

### 3. Pick A Workstream

- Interested in mechanics: start in [`hardware/`](./hardware/README.md)
- Interested in embedded control: start in [`firmware/`](./firmware/README.md)
- Interested in vision and high-level control: start in [`software/`](./software/README.md)

### 4. If You Want To Contribute

Read:

- [`CONTRIBUTING.md`](./CONTRIBUTING.md)
- [`Issue templates`](./.github/ISSUE_TEMPLATE/)
- [`SUPPORT.md`](./SUPPORT.md)

### 5. If You Want To Build Along Early

Be aware that this repository is still in planning/prototyping mode.
Expect subsystem details and BOM choices to evolve as the first machine is built.

## Contributing

Contributions across mechanics, firmware, vision, controls, docs, and reproducibility are welcome.
Start with [`CONTRIBUTING.md`](./CONTRIBUTING.md).

For large changes, open an issue first so the project can keep the hardware and software assumptions coherent.

## Safety Note

This repository targets a moving electromechanical prototype.
Even low-cost prototypes can throw balls, pinch fingers, or damage parts if driven outside their safe envelope.
Treat all motion, power, and tuning work as hardware safety work.

## License

This project is licensed under the [Apache License 2.0](./LICENSE).
Copyright `2026` `Zw-awa`.
Additional attribution details are recorded in [`NOTICE`](./NOTICE).
