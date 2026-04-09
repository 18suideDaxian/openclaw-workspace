---
id: k002
title: 用 Node.js + xlsx 处理 Excel
date: 2026-04-09
tags: [excel, node, 工具]
source: 2026-04-09-de-ai-excel-skills
---

## 环境

- python 没有 openpyxl，用 Node.js + xlsx 包
- 安装：npm install xlsx（在 workspace 目录下）
- require 路径：/root/.openclaw/workspace/node_modules/xlsx

## 常用操作

```js
const XLSX = require('xlsx');
// 读取
const wb = XLSX.readFile('file.xlsx');
const data = XLSX.utils.sheet_to_json(wb.Sheets['Sheet1'], {header:1, raw:true});
// 写入
ws['B7'] = { t: 'n', v: 17200 };
ws['E7'] = { t: 'n', f: 'B7+C7+D7' };
XLSX.writeFile(wb, 'out.xlsx');
```

## 注意

- 公式值用 raw:true 读取时为空（xlsx不计算），但公式字符串存在
- 写公式用 { t: 'n', f: 'SUM(A1:A5)' } 格式
- aoa_to_sheet 创建的表需要重新设置 !ref 范围
