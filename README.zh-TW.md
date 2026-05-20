# OpenJugglePlate

[English](./README.md) | [简体中文](./README.zh-CN.md) | [繁體中文](./README.zh-TW.md)

[![狀態](https://img.shields.io/badge/status-planning%20%2F%20prototyping-4c8bf5)](#目前狀態)
[![授權](https://img.shields.io/badge/license-Apache--2.0-1976d2)](./LICENSE)
![視覺](https://img.shields.io/badge/vision-top--view%20camera-2e7d32?logo=opencv&logoColor=white)
![控制](https://img.shields.io/badge/control-Linux%20SBC%20%2B%20STM32-8e24aa)
![致動器](https://img.shields.io/badge/actuation-stepper%20motors-f57c00)

這是一個開源、可獨立運行的乒乓球平衡與連續顛球機器人，採用頂視覺、`Linux SBC` 高層控制，以及 `STM32` 即時運動控制。

## 目錄

- [OpenJugglePlate](#openjuggleplate)
  - [目錄](#目錄)
  - [這個專案是什麼](#這個專案是什麼)
  - [它想做到什麼](#它想做到什麼)
  - [第一版重點聚焦什麼](#第一版重點聚焦什麼)
  - [目前狀態](#目前狀態)
  - [專案目錄結構](#專案目錄結構)
  - [快速開始](#快速開始)
    - [1. 複製倉庫](#1-複製倉庫)
    - [2. 先閱讀總覽文件](#2-先閱讀總覽文件)
    - [3. 選擇一個工作方向](#3-選擇一個工作方向)
    - [4. 如果想參與貢獻](#4-如果想參與貢獻)
    - [5. 如果你想提早跟著搭建](#5-如果你想提早跟著搭建)
  - [貢獻](#貢獻)
  - [安全提醒](#安全提醒)
  - [授權](#授權)

## 這個專案是什麼

這個倉庫是 `OpenJugglePlate` 的公開首頁。
它最終會成為一個完整的開源機器人倉庫，包含：

- 專案文件
- 硬體設計檔
- `STM32` 韌體
- 面向 `Orange Pi`、`Raspberry Pi`、`RK3588` 這類 `Linux SBC` 的軟體
- 可重現的 BOM 與裝配說明

它現在還不是一個「已經完成的整機發佈倉庫」。
更準確地說，它目前是一個公開的專案骨架與持續建設中的開發記錄。

## 它想做到什麼

OpenJugglePlate 只聚焦一個物件：標準 `40 mm` 乒乓球。

第一版希望逐步做到：

- 把球拉回平台中心
- 讓球在平台上穩定住
- 從板上平衡過渡到受控彈跳
- 實現連續顛球

為了讓第一代機器更現實，也更容易重現，V1 會刻意收斂：

- 感知方式：`single top-view vision`
- 高層運算：`Linux SBC`
- 即時執行控制：`STM32`
- 平台拓撲：`3-actuator parallel platform`
- 主要致動器：`stepper motors`

## 第一版重點聚焦什麼

第一版目前主要聚焦這些事情：

- 只圍繞標準 `40 mm` 乒乓球構建
- 先把頂視覺這條路線跑通
- 先把 `Linux SBC + STM32` 這條控制分工做穩
- 先把三執行器平台做成可重現樣機

這也代表第一版暫時不打算同時覆蓋下面這些方向：

- 多種球類或任意物件泛化
- 自動撿球或自動補球
- `brushless` 主執行方案
- 把強化學習當作基線控制器

## 目前狀態

`規劃中 / 原型開發中`

目前倉庫的重點是：

- 公開專案結構
- 專案文件
- 參考資料整理
- 協作與貢獻流程
- 子系統占位

具體的硬體、韌體與 `Linux SBC` 側軟體會隨著原型推進逐步補進來。

## 專案目錄結構

```text
.
|-- .github/                  # Issue 模板、PR 模板、CI 與 Pages workflow
|-- firmware/                 # STM32 即時控制側
|-- hardware/                 # CAD、機械、BOM 與裝配側
|-- software/                 # Linux SBC 視覺與高層控制側
|-- README.md                 # 英文總覽
|-- README.zh-CN.md           # 簡體中文總覽
|-- README.zh-TW.md           # 繁體中文總覽
|-- CONTRIBUTING.md
|-- CODE_OF_CONDUCT.md
|-- SECURITY.md
|-- LICENSE
`-- NOTICE
```

補充說明：

- 公開倉庫會盡量讓機械、韌體、軟體三條線可以並行推進。
- 某些本地規劃材料會保留在私有區域，不會作為公開內容發佈。

## 快速開始

### 1. 複製倉庫

```bash
git clone https://github.com/Zw-awa/OpenJugglePlate.git
cd OpenJugglePlate
```

### 2. 先閱讀總覽文件

建議先看：

- [`README.md`](./README.md)
- [`hardware/README.md`](./hardware/README.md)
- [`firmware/README.md`](./firmware/README.md)
- [`software/README.md`](./software/README.md)

### 3. 選擇一個工作方向

- 對機械/CAD 更有興趣：從 [`hardware/`](./hardware/README.md) 開始
- 對嵌入式控制更有興趣：從 [`firmware/`](./firmware/README.md) 開始
- 對視覺/高層控制更有興趣：從 [`software/`](./software/README.md) 開始

### 4. 如果想參與貢獻

先閱讀：

- [`CONTRIBUTING.md`](./CONTRIBUTING.md)
- [`Issue 模板`](./.github/ISSUE_TEMPLATE/)
- [`SUPPORT.md`](./SUPPORT.md)

### 5. 如果你想提早跟著搭建

請注意，這個倉庫仍處於規劃/原型期。
介面、BOM 與子系統細節會持續演進。

## 貢獻

歡迎圍繞機械、電控、視覺、控制、文件與重現性展開貢獻。
請先閱讀 [`CONTRIBUTING.md`](./CONTRIBUTING.md)。

如果改動較大，建議先開 issue 討論，避免硬體與軟體假設互相衝突。

## 安全提醒

這個倉庫面向的是一台會運動的機電原型機。
即使是低成本樣機，只要超出安全包絡，也可能把球打飛、夾手或損壞零件。
請把運動調試、電源接線與機械測試都當成硬體安全工作來對待。

## 授權

本專案採用 [Apache License 2.0](./LICENSE)。
版權歸屬：`2026` `Zw-awa`。
補充歸屬資訊見 [`NOTICE`](./NOTICE)。
