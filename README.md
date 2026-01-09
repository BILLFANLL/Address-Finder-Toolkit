# 📍 Address Finder Toolkit / 地址查找工具

一个**零构建、零后端**的地址投影与反向查找工具，提供 **Google Maps** 与 **OpenStreetMap** 两种实现，支持 **中 / 英文切换**，适合本地使用或直接部署到静态站点（GitHub Pages、Netlify 等）。

---

## ✨ 特性一览

- 🌐 **双引擎**：Google Maps（高精度、低延迟）与 OpenStreetMap（完全免费、免密钥）
- 🌍 **双语言 UI**：中文 / English 一键切换，偏好自动保存（LocalStorage）
- 🧭 **地址投影**：根据方位角与距离计算目标坐标
- 📌 **最近地址查找**：自动反向地理编码并高亮误差距离
- 🗺️ **实时预览**：小地图即时显示投影点，支持点击反算距离与角度
- 📋 **自动复制**：最近地址自动复制到剪贴板（Clipboard API + 兼容回退）
- 🧩 **纯静态**：单文件 HTML，无需构建流程或后端服务

---

## 🧠 两个版本的区别

| 对比项 | Google Maps 版本 | OpenStreetMap 版本 |
|---|---|---|
| 是否免费 | ❌（需 API Key，可能产生费用） | ✅ 完全免费 |
| 精度与速度 | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ |
| 门牌号覆盖 | 高 | 许多国家/地区缺失 |
| 依赖 | Google Maps JS + Geocoding API | Leaflet + Nominatim |
| 使用门槛 | 需要配置 API Key | 即开即用 |

---

## 🚀 快速开始

### 本地使用

1. 克隆或下载本仓库
2. 使用现代浏览器（Chrome / Edge / Firefox）直接打开：
   - **Google 版本**：`address_googlemap_api.html`
   - **OpenStreetMap 版本**：`address_OpenStreetMap_api.html`

### Google Maps 版本额外步骤

- 首次打开后，在**左上角控制面板**输入并保存你的 **Google API Key**
- API Key 会安全地存储在浏览器 **LocalStorage** 中

> 需要启用的 API：
> - Maps JavaScript API
> - Geocoding API

---

## 🧭 使用流程

1. **输入起始地址**，点击查询进行地理编码
2. **选择方向**（或输入自定义方位角）与 **距离**
3. 小地图实时显示投影点位置，可点击地图反算参数
4. 点击 **“查找地址”** 后，系统将自动：
   - 计算投影坐标
   - 查询最近可识别地址
   - 显示并高亮误差距离（> 30 米时给出提示）
   - 自动复制最近地址到剪贴板
5. 右侧结果区展示完整信息，主地图同步显示起点与目标点

---

## ⚙️ 技术实现

- **Google Maps 版本**
  - 动态加载 Maps JavaScript SDK
  - API Key 本地持久化
  - 原生 Geocoding / Reverse Geocoding

- **OpenStreetMap 版本**
  - Leaflet 地图库
  - Nominatim 地理编码服务
  - 无需 Token 或账号

---

## ⚠️ 注意事项

- **Google Maps**
  - 请留意 API 配额与可能产生的费用
  - 建议为 Key 设置域名或 IP 限制

- **OpenStreetMap / Nominatim**
  - 存在访问频率限制，不适合高频或批量请求
  - 在部分国家/地区无法返回精确门牌号

## 📄 许可证

本项目为前端工具示例，可自由用于学习与个人项目。商业使用请自行确认 Google Maps 与 OpenStreetMap / Nominatim 的相关条款。

---


