---
title: "装备与技术栈 (/uses)"
date: 2026-03-15
layout: "single"
---

这里列出了我在构建数字实验室、日常办公以及网络折腾中使用的核心硬件与软件。本清单长期保持更新（Set it and forget it）。

### 💻 基础设施 (Infrastructure)
* **核心路由：** ASUS AX6600 (承担 PPPoE 拨号与 DHCP 分发)
* **内网骨干：** 全千兆无管理交换机
* **数据中心：** 自建 NAS 存储池，承载私有云与媒体库，采用 ZFS/Btrfs 保证数据完整性。
* **网络提供商：** 中国联通 (China Unicom) 宽带网络。

### 🌐 云端计算节点 (Cloud & VPS)
不在于多，而在于精细化管理与线路互补。
* **Oracle Cloud (甲骨文云)：** ARM 架构实例，主要用于跑长期的自动化脚本与 Docker 容器。
* **RackNerd：** 极具性价比的洛杉矶节点，承担部分测试业务与前端反代。
* **BandwagonHost (搬瓦工)：** 顶级 CN2 GIA 线路，作为关键时刻的保障网络出口。
* **边缘计算：** Cloudflare Pages (静态托管) & CF Workers (无服务器 API)。

### 🛠️ 生产力与运维工具 (Tools & DevOps)
* **网络接管：** Surge (macOS / iOS) - 永远的神，不可替代的精细化分流网关。
* **容器化：** Docker & Docker Compose - 所有后端服务一律容器化，拒绝宿主机环境污染。
* **运维面板：** 1Panel - 现代化的 Linux 服务器运维管理面板。
* **监控告警：** Uptime Kuma 实时监控所有服务连通性，配合 Bark 实现 iOS 端秒级异常推送。
* **代理内核：** V2RayN, Clash, Xray-core。
