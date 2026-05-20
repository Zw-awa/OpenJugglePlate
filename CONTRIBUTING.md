# Contributing To OpenJugglePlate

[English](./CONTRIBUTING.md) | [简体中文](./CONTRIBUTING.zh-CN.md) | [繁體中文](./CONTRIBUTING.zh-TW.md)

Thanks for considering a contribution.
This project is an open hardware robot, so good contributions are not limited to source code.

We welcome improvements in:

- mechanics and CAD
- firmware
- Linux SBC software
- control design
- calibration and test procedures
- BOM and sourcing notes
- documentation and reproducibility

## Before You Start

For large changes, please open an issue first.
This helps avoid drifting away from the current hardware assumptions, roadmap, or safety envelope.

Useful starting points:

- [`README.md`](./README.md)

## Contribution Principles

Contributions should try to improve at least one of these dimensions:

- system clarity
- reproducibility
- safety
- maintainability
- performance backed by evidence

Please avoid changes that only add complexity without making the build easier to understand, validate, or extend.

## Expected Pull Request Quality

### Documentation Changes

For docs-focused changes, explain:

- what was unclear or missing
- what was changed
- whether screenshots, diagrams, or links were updated

### Hardware Changes

For mechanical, electrical, or BOM changes, include:

- the design intent
- the affected subsystem
- any dimensions, interfaces, or assumptions that changed
- whether assembly steps or sourcing guidance also need updates

### Firmware Or Software Changes

For code changes, include:

- what behavior changed
- how it was validated
- what assumptions were made about hardware or environment
- whether logging, docs, or tests should also change

## Safety And Scope

This project involves moving hardware.
If your change affects motion limits, power, homing, actuation, or safety behavior, call that out explicitly in the pull request.

Do not silently change:

- operating assumptions
- target object
- safety-related defaults
- architecture ownership boundaries between the Linux SBC and STM32

## Style Expectations

- Prefer clear, direct writing over marketing language.
- Keep public docs understandable to contributors who are strong in only one area.
- Favor incremental changes over large speculative rewrites.
- Add rationale when a decision is not obvious from the diff itself.

## Questions And Support

If you are not sure where to start, open a support/question issue and describe:

- which part you want to help with
- what context you already have
- what is blocking you

## License

By contributing to this repository, you agree that your contributions will be licensed under the Apache License 2.0 included in this repository.
