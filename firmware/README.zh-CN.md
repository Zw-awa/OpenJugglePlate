# Firmware

[English](./README.md) | [简体中文](./README.zh-CN.md) | [繁體中文](./README.zh-TW.md)

这个目录用于存放 OpenJugglePlate 的 `STM32` 实时控制部分。

预期职责包括：

- 归零
- 限位处理
- 多轴同步步进输出
- 接收来自高层 Linux SBC 的命令
- 执行器状态管理
- 轻量级诊断

当前的基线目标是 `STM32F407`，如果后续性能分析证明需要，也可以升级到 `STM32H7`。
