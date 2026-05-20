# Software

[English](./README.md) | [简体中文](./README.zh-CN.md) | [繁體中文](./README.zh-TW.md)

这个目录用于存放 OpenJugglePlate 的 Linux SBC 侧软件。

预期职责包括：

- 相机采集
- 图像预处理
- 球检测与跟踪
- 状态估计
- 模式逻辑
- 高层控制
- 日志与调参支持

当前的基线软件栈是 `C++ + OpenCV`，在线感知路径是单个顶视相机。
具体板卡后续可能会在 `Orange Pi`、`Raspberry Pi` 或其他合适的 Linux SBC 之间调整。
