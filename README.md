# 📍 Address Finder Toolkit

> 一个纯前端、零构建的地址投影与反向查找工具，提供 Google Maps 与 OpenStreetMap 两种实现。
> 
> A zero-build, purely front-end address projection & reverse lookup toolkit powered by Google Maps and OpenStreetMap.

---

## 🇨🇳 中文 README

### 项目简介

**Address Finder Toolkit（地址查找工具）** 是一个无需后端、无需构建流程的纯静态 Web 工具，用于：

- 将已知地址按 **方位角 + 距离** 进行坐标投影
- 查找投影点附近 **最近可识别的真实地址**
- 辅助地址推算、位置核对、地理验证等场景

项目提供 **Google Maps** 与 **OpenStreetMap** 两个版本，均为单文件 HTML，支持 **中 / 英文界面切换**。

---

### 核心特性

- 🌐 双地图引擎：Google Maps / OpenStreetMap
- 🌍 中英文 UI 切换（偏好自动保存）
- 🧭 基于方位角与距离的地址投影计算
- 📌 最近地址自动反向地理编码
- 📏 自动计算并高亮误差距离（>30 米提醒）
- 🗺️ 小地图实时预览，支持点击反算参数
- 📋 最近地址自动复制到剪贴板
- 🧩 单文件 HTML，零依赖部署

---

### 版本对比

| 项目 | Google Maps 版本 | OpenStreetMap 版本 |
|---|---|---|
| 是否免费 | ❌（需 API Key） | ✅ 完全免费 |
| 定位精度 | 高 | 中 |
| 响应速度 | 快 | 中 |
| 门牌号覆盖 | 完整 | 许多国家缺失 |
| 使用门槛 | 需要配置 Key | 即开即用 |

---

### 快速开始

1. 克隆或下载本仓库
2. 使用现代浏览器直接打开：
   - `address_googlemap_api.html`
   - `address_OpenStreetMap_api.html`

#### Google Maps 版本说明

- 首次使用需在左上角输入 **Google API Key**
- Key 会保存在浏览器 LocalStorage 中
- 需启用以下 API：
  - Maps JavaScript API
  - Geocoding API

---

### 使用流程

1. 输入起始地址并进行地理编码
2. 设置方向（或自定义方位角）与距离
3. 小地图实时显示投影点位置
4. 点击「查找地址」后自动：
   - 计算投影坐标
   - 查询最近地址
   - 显示误差距离并提示
   - 复制最近地址到剪贴板

---

### 注意事项

- Google Maps API 可能产生费用，请留意配额
- Nominatim 有访问频率限制，不适合高频请求
- 建议通过 HTTPS 部署以确保剪贴板功能正常

---

## 🇬🇧 English README

### Introduction

**Address Finder Toolkit** is a zero-build, purely front-end web utility designed to:

- Project a known address by **bearing and distance**
- Retrieve the **nearest recognizable real-world address** to the projected point
- Assist with location verification, address estimation, and geo-validation tasks

It ships with **two standalone HTML implementations**:

- Google Maps (high accuracy, API key required)
- OpenStreetMap (free, no token required)

Both versions support an in-page **Chinese / English language toggle**.

---

### Features

- 🌐 Dual map engines: Google Maps & OpenStreetMap
- 🌍 Built-in Chinese / English UI toggle
- 🧭 Coordinate projection by bearing & distance
- 📌 Automatic reverse geocoding to nearest address
- 📏 Offset distance calculation with visual warning
- 🗺️ Live mini-map preview with click-based adjustment
- 📋 Auto-copy nearest address to clipboard
- 🧩 Single-file HTML, no backend, no build step

---

### Versions Comparison

| Item | Google Maps | OpenStreetMap |
|---|---|---|
| Cost | API key required | Free |
| Accuracy | High | Medium |
| Speed | Fast | Moderate |
| House numbers | Well covered | Limited in many regions |
| Setup | API key needed | Ready to use |

---

### Quick Start

1. Clone or download this repository
2. Open one of the following files in a modern browser:
   - `address_googlemap_api.html`
   - `address_OpenStreetMap_api.html`

#### Google Maps Notes

- Enter your **Google API Key** on first launch
- The key is stored locally in browser LocalStorage
- Required APIs:
  - Maps JavaScript API
  - Geocoding API

---

### How It Works

1. Geocode the origin address
2. Specify direction (or custom bearing) and distance
3. Preview the projected point on the mini map
4. Click **Find Address** to:
   - Compute projected coordinates
   - Reverse-geocode the nearest address
   - Highlight offset distance (>30 m warning)
   - Copy the nearest address to clipboard

---

### Notes

- Monitor Google Maps API quotas and billing
- Respect OpenStreetMap / Nominatim rate limits
- HTTPS deployment is recommended for full browser capabilities

---

### License

This project is provided as a front-end utility example.

Please review and comply with the terms of service of Google Maps and OpenStreetMap / Nominatim when using it in production or commercial environments.

---

### Contributions

Issues and pull requests are welcome, including:

- UI / UX improvements
- Projection accuracy enhancements
- Additional map provider support (Mapbox, HERE, etc.)

