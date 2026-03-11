---
title: "从零开始：青龙面板部署与网易云、B站、夸克自动化脚本实战"
date: 2026-03-11T21:30:00+08:00
draft: false
author: "Yudi"
categories: ["自动化", "生产力"]
tags: ["青龙面板", "Docker", "脚本", "签到", "网易云"]
---

在云服务器（VPS）的日常使用中，如何最大化利用闲置资源？**青龙面板**（Qinglong）给出了完美的答案。它是一个支持 Python、JavaScript、Shell 等多种语言的定时任务管理平台。今天记录我在服务器上部署青龙面板，并挂载网易云音乐、B站、夸克网盘等自动化脚本的实战过程。

### 环境准备

考虑到服务器内存资源（1G-2G）的珍贵，我采用了最精简的 Docker 部署方案。为了防止多任务并发导致系统 OOM（内存溢出），我特意在宿主机上开启了 2GB 的 Swap 交换分区。

### 部署步骤

在控制台输入以下指令即可快速拉起青龙环境：

```bash
docker run -dit \
  -v ./ql/data:/ql/data \
  -p 5700:5700 \
  --name qinglong \
  --restart unless-stopped \
  whyour/qinglong:latest
