# Tender Intelligence Extraction Skill

## 1. Purpose｜目标

快速从城市共享微出行招标（e-bike / e-scooter / bike-sharing）中抓取关键信息与核心结构，用于：

- 快速判断项目价值与类型
- 为后续深度分析做输入
- 构建城市/国家 tender 数据库

---

## 2. Input｜输入

优先输入：

- 官方招标链接（URL）
- PDF（Bando / Disciplinare / Capitolato / SVO）
- 城市 + 时间 + 关键词（如 “Bologna bike-sharing tender 2026”）

---

## 3. Output Structure｜输出结构（必须按此格式）

### 1️⃣ 基本信息

| 字段 | 内容 |
|---|---|
| 城市 / 国家 |  |
| 招标方 |  |
| 原文名称 |  |
| 中文翻译 |  |
| Tender 类型 | concession / permit / procurement / pilot |
| 服务类型 | e-bike / e-scooter / bike-sharing |
| 投标截止日期 |  |
| 合同期限 |  |
| 估算金额 |  |
| Lot 数量 |  |
| 可入选运营商数量 |  |

---

### 2️⃣ 车辆与规模

| 项目 | 内容 |
|---|---|
| 车辆类型 | e-bike / scooter / mixed |
| 最低车辆数 |  |
| 最高车辆数 |  |
| 每个 Lot 规模 |  |
| 上线节奏 |  |
| 是否允许扩容 |  |

---

### 3️⃣ 评分结构

| 维度 | 分值 | 说明 |
|---|---:|---|
| 技术分 |  |  |
| 经济分 |  |  |
| 是否有门槛 |  |  |
| 经济评分方式 | 价格 / 车队规模 / 混合 |  |

---

### 4️⃣ 关键评分项（Top 5）

提取最重要的 3–5 个评分项：

| 原文名称 | 中文 | 分值 | 类型（SOG/CN/SN） |
|---|---|---:|---|
|  |  |  |  |
