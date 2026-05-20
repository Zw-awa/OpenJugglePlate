# Firmware

[English](./README.md) | [简体中文](./README.zh-CN.md) | [繁體中文](./README.zh-TW.md)

這個目錄用來存放 OpenJugglePlate 的 `STM32` 即時控制部分。

預期職責包括：

- 歸零
- 限位處理
- 多軸同步步進輸出
- 接收來自高層 Linux SBC 的命令
- 致動器狀態管理
- 輕量級診斷

目前的基線目標是 `STM32F407`，如果後續性能分析證明有需要，也可以升級到 `STM32H7`。
