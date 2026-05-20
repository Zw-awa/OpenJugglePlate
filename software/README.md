# Software

[English](./README.md) | [简体中文](./README.zh-CN.md) | [繁體中文](./README.zh-TW.md)

This directory will hold the Linux SBC side of OpenJugglePlate.

Expected responsibilities:

- camera acquisition
- image preprocessing
- ball detection and tracking
- state estimation
- mode logic
- high-level control
- logging and tuning support

The current baseline stack is `C++ + OpenCV`, with a single top-view camera as the V1 online sensing path.
The exact board may change between `Orange Pi`, `Raspberry Pi`, or another suitable Linux SBC.
