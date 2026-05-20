# Software

[English](./README.md) | [简体中文](./README.zh-CN.md) | [繁體中文](./README.zh-TW.md)

這個目錄用來存放 OpenJugglePlate 的 Linux SBC 側軟體。

預期職責包括：

- 相機擷取
- 影像預處理
- 球偵測與追蹤
- 狀態估計
- 模式邏輯
- 高層控制
- 日誌與調參支援

目前的基線軟體堆疊是 `C++ + OpenCV`，在線感知路徑是單一頂視相機。
具體板卡後續可能會在 `Orange Pi`、`Raspberry Pi` 或其他合適的 Linux SBC 之間調整。
