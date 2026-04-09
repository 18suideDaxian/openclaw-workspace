---
date: 2026-04-09
topic: 去AI腔、Skills配置、Excel实操
tags: [润色, skills, excel, 首次对话]
---

## 摘要

首次对话，主要三块内容：文本润色去AI腔、OpenClaw skills配置与启用、Excel文件创建与编辑。

## 要点

### 去AI腔
- 用户对中英文文本润色很感兴趣，测试了多种场景（邮件、营销、合同、技术文档）
- 英文偏好：砍套话、去buzzword、少用连接词
- 中文偏好：消灭公文体（首先/其次/综上所述）、正式场合可出双版本
- 合同条款用户要求了正式+口语双版本

### Skills配置
- 从 ClawhHub 启用了5个skill：de-ai-polish、de-ai-ify、ai-text-humanizer、excel-xlsx、memory-pkm
- 配置写入 openclaw.json skills.entries
- gateway重启遇到进程锁问题（pid 24杀不掉），skills.watcher应自动生效

### Excel实操
- 用 Node.js + xlsx 包创建Excel（python没有openpyxl）
- 创建了销售数据+成绩单两个sheet
- 用户发了两个文件让我合并（六月的数据.xlsx → 测试.xlsx）

### 其他
- 查了海口天气（38°C，晴）
- 介绍了 excel-xlsx 和 memory-pkm 两个skill

## 待办
- [ ] gateway重启问题待解决
- [ ] skills是否正确加载需验证
