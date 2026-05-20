# Firmware

[English](./README.md) | [简体中文](./README.zh-CN.md) | [繁體中文](./README.zh-TW.md)

This directory will hold the STM32 real-time control side of OpenJugglePlate.

Expected responsibilities:

- homing
- limit handling
- multi-axis synchronized step generation
- command decoding from Raspberry Pi
- actuator state management
- lightweight diagnostics

The current baseline target is `STM32F407`, with `STM32H7` as an upgrade path if later profiling demands it.
