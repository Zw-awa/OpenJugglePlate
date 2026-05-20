# OpenJugglePlate

[English](./README.md) | [简体中文](./README.zh-CN.md) | [繁體中文](./README.zh-TW.md)

[![状态](https://img.shields.io/badge/status-planning%20%2F%20prototyping-4c8bf5)](#当前状态)
[![许可证](https://img.shields.io/badge/license-Apache--2.0-1976d2)](./LICENSE)
![视觉](https://img.shields.io/badge/vision-top--view%20camera-2e7d32?logo=opencv&logoColor=white)
![控制](https://img.shields.io/badge/control-Linux%20SBC%20%2B%20STM32-8e24aa)
![执行器](https://img.shields.io/badge/actuation-stepper%20motors-f57c00)

这是一个开源、可独立运行的乒乓球平衡与连续颠球机器人，采用顶视视觉、`Linux SBC` 高层控制，以及 `STM32` 实时运动控制。

## 目录

- [OpenJugglePlate](#openjuggleplate)
  - [目录](#目录)
  - [这个项目是什么](#这个项目是什么)
  - [它想做到什么](#它想做到什么)
  - [第一版重点聚焦什么](#第一版重点聚焦什么)
  - [当前状态](#当前状态)
  - [项目目录结构](#项目目录结构)
  - [快速开始](#快速开始)
    - [1. 克隆仓库](#1-克隆仓库)
    - [2. 先阅读总览文档](#2-先阅读总览文档)
    - [3. 选择一个工作方向](#3-选择一个工作方向)
    - [4. 如果想参与贡献](#4-如果想参与贡献)
    - [5. 如果你想提前跟着搭建](#5-如果你想提前跟着搭建)
  - [贡献](#贡献)
  - [安全提示](#安全提示)
  - [许可证](#许可证)

## 这个项目是什么

这个仓库是 `OpenJugglePlate` 的公开主页。
它最终会成为一个完整的开源机器人仓库，包含：

- 项目文档
- 硬件设计文件
- `STM32` 固件
- 面向 `Orange Pi`、`Raspberry Pi`、`RK3588` 这类 `Linux SBC` 的软件
- 可复现的 BOM 与装配说明

它现在还不是一个“已经完成的整机发布仓库”。
当前阶段更准确地说，是一个公开的项目骨架和持续建设中的开发记录。

## 它想做到什么

OpenJugglePlate 只聚焦一个对象：标准 `40 mm` 乒乓球。

第一版希望逐步做到：

- 把球拉回平台中心
- 让球在平台上稳定住
- 从板上平衡过渡到受控弹跳
- 实现连续颠球

为了让第一代机器更现实、也更容易复现，V1 会刻意收得比较窄：

- 感知方式：`single top-view vision`
- 高层计算：`Linux SBC`
- 实时执行控制：`STM32`
- 平台拓扑：`3-actuator parallel platform`
- 主执行器：`stepper motors`

## 第一版重点聚焦什么

第一版目前主要聚焦这些事情：

- 只围绕标准 `40 mm` 乒乓球构建
- 先把顶视视觉这条路线跑通
- 先把 `Linux SBC + STM32` 这条控制分工做稳
- 先把三执行器平台做成可复现样机

这也意味着，第一版暂时不打算同时覆盖下面这些方向：

- 多种球类或任意物体泛化
- 自动捡球或自动补球
- `brushless` 主执行方案
- 把强化学习作为基线控制器

## 当前状态

`规划中 / 原型开发中`

当前仓库的重点是：

- 公开项目结构
- 项目文档
- 参考资料整理
- 协作与贡献流程
- 子系统占位

具体的硬件、固件和 `Linux SBC` 侧软件会随着原型推进逐步补进来。

## 项目目录结构

```text
.
|-- .github/                  # Issue 模板、PR 模板、CI 与 Pages 工作流
|-- firmware/                 # STM32 实时控制侧
|-- hardware/                 # CAD、机械、BOM 与装配侧
|-- software/                 # Linux SBC 视觉与高层控制侧
|-- README.md                 # 英文总览
|-- README.zh-CN.md           # 简体中文总览
|-- README.zh-TW.md           # 繁體中文总览
|-- CONTRIBUTING.md
|-- CODE_OF_CONDUCT.md
|-- SECURITY.md
|-- LICENSE
`-- NOTICE
```

补充说明：

- 公开仓库会尽量让机械、固件、软件三条线可以并行推进。
- 某些本地规划材料会保留在私有区域，不会作为公开内容发布。

## 快速开始

### 1. 克隆仓库

```bash
git clone https://github.com/Zw-awa/OpenJugglePlate.git
cd OpenJugglePlate
```

### 2. 先阅读总览文档

建议先看：

- [`README.md`](./README.md)
- [`hardware/README.md`](./hardware/README.md)
- [`firmware/README.md`](./firmware/README.md)
- [`software/README.md`](./software/README.md)

### 3. 选择一个工作方向

- 对机械/CAD 更感兴趣：从 [`hardware/`](./hardware/README.md) 开始
- 对嵌入式控制更感兴趣：从 [`firmware/`](./firmware/README.md) 开始
- 对视觉/高层控制更感兴趣：从 [`software/`](./software/README.md) 开始

### 4. 如果想参与贡献

先阅读：

- [`CONTRIBUTING.md`](./CONTRIBUTING.md)
- [`Issue 模板`](./.github/ISSUE_TEMPLATE/)
- [`SUPPORT.md`](./SUPPORT.md)

### 5. 如果你想提前跟着搭建

请注意，这个仓库还处于规划/原型期。
接口、BOM 和子系统细节会继续演进。

## 贡献

欢迎围绕机械、电控、视觉、控制、文档和复现性展开贡献。
请先阅读 [`CONTRIBUTING.md`](./CONTRIBUTING.md)。

如果改动较大，建议先开 issue 讨论，避免硬件与软件假设互相冲突。

## 安全提示

这个仓库面向的是一台会运动的机电原型机。
即使是低成本样机，只要超出安全包络，也可能打飞球、夹手或损坏零件。
请把运动调试、电源接线和机械测试都当成硬件安全工作来对待。

## 许可证

本项目采用 [Apache License 2.0](./LICENSE)。
版权归属：`2026` `Zw-awa`。
补充归属信息见 [`NOTICE`](./NOTICE)。
