# Tender Intelligence Extraction Skill v1.1

## Version

- **Skill name:** Tender Intelligence Extraction Skill
- **Version:** v1.1
- **Owner:** Yao
- **Primary domain:** Shared micromobility tender intelligence
- **Primary use cases:** e-bike / e-scooter / bike-sharing tender extraction, city permit analysis, scoring breakdown, supplier opportunity assessment

---

## 1. Trigger｜触发方式

Use this skill when the user says or implies:

- “按 Tender Intelligence Skill 分析”
- “分析这个标书 / 招标 / tender / permit / concession”
- “拆解这个城市共享微出行项目”
- “提取 e-bike / e-scooter / bike-sharing 招标信息”
- “判断这个标书对硬件供应商有什么机会”
- “根据这个招标文件输出结构化表格”

When triggered, the assistant must first identify the official source, read the tender material, then extract information according to this skill’s output structure.

---

## 2. Purpose｜目标

快速从城市共享微出行招标（e-bike / e-scooter / bike-sharing）中抓取关键信息与核心结构，用于：

- 快速判断项目价值与类型
- 为后续深度分析做输入
- 构建城市 / 国家 tender 数据库
- 支持运营商、硬件供应商、产品战略和销售机会判断
- 识别车辆要求、评分结构、合同约束、TCO / ESG / 安全要求

---

## 3. Inputs｜输入

优先输入：

- 官方招标链接（URL）
- PDF 文件（Bando / Disciplinare / Capitolato / SVO / Tender documents）
- 城市 + 国家 + 时间 + 关键词，例如：
  - “Bologna bike-sharing tender 2026”
  - “Milano monopattini sharing bando”
  - “Paris e-bike concession tender”
- 用户上传的截图、表格、招标摘要或网页内容

If only city / country / keywords are provided, search using local-language keywords first, then English keywords.

---

## 4. Source Priority｜来源优先级

Use sources in this order:

1. Official tender portal / procurement portal
2. City government / municipality website
3. Regional procurement platform
4. Official PDF tender documents
5. Operator or city press release
6. Reputable local media
7. Industry media
8. Secondary databases or summaries

Never rely only on a media article if official tender documents are available.

---

## 5. Search Rules｜搜索规则

For tender and permit tasks:

- Must search in the local language of the city / country when possible.
- Must capture exact publication date and deadline date when available.
- Must cite or link original sources.
- Must distinguish confirmed information from inferred information.
- Must not invent contract length, fleet size, lot number, scoring weight, operator count, deadline, or estimated value.
- If information is missing, mark it as “未披露 / not disclosed” instead of guessing.
- For Europe, include relevant terms such as:
  - bando, gara, concessione, appalto, affidamento
  - tender, procurement, concession, permit, framework agreement
  - micromobilità, monopattini, biciclette elettriche, bike-sharing
  - mobilité partagée, trottinettes, vélos électriques
  - Ausschreibung, Genehmigung, Konzession, E-Scooter, Fahrradverleih

---

## 6. Execution Steps｜执行步骤

1. **Identify tender source**
   - Confirm city, country, tender authority, document type, and source reliability.

2. **Classify tender type**
   - concession / permit / procurement / pilot / framework agreement / service contract.

3. **Extract basic commercial structure**
   - deadline, contract duration, estimated value, lots, operator slots, exclusivity.

4. **Extract vehicle and fleet requirements**
   - vehicle type, min / max fleet, phased deployment, expansion rights, technical specs.

5. **Extract scoring model**
   - technical score, economic score, minimum threshold, award logic, scoring formula.

6. **Identify top evaluation criteria**
   - safety, parking compliance, lifecycle / sustainability, operations, data integration, user service, price.

7. **Identify hardware requirements**
   - brakes, lights, IoT, battery, swappable battery, GPS, parking tech, anti-vandalism, durability, LCA.

8. **Assess supplier opportunity**
   - vehicle order potential, replacement cycle, spare parts, serviceability, TCO reduction, product-fit implications.

9. **Assess risk**
   - regulatory risk, operational constraints, low fleet ceiling, strict local sourcing, ESG documentation burden, margin pressure.

10. **Output structured summary**
   - Follow the required output format below.

---

## 7. Output Structure｜输出结构（必须按此格式）

### 1️⃣ 基本信息

| 字段 | 内容 |
|---|---|
| 城市 / 国家 |  |
| 招标方 |  |
| 原文名称 |  |
| 中文翻译 |  |
| Tender 类型 | concession / permit / procurement / pilot / framework agreement |
| 服务类型 | e-bike / e-scooter / bike-sharing / mixed |
| 发布日期 |  |
| 投标截止日期 |  |
| 合同期限 |  |
| 估算金额 |  |
| Lot 数量 |  |
| 可入选运营商数量 |  |
| 官方来源链接 |  |

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
| 是否要求换电 / 固定电池 |  |
| 是否要求 docking / station / parking zone |  |
| 是否要求本地维护能力 |  |

---

### 3️⃣ 评分结构

| 维度 | 分值 | 说明 |
|---|---:|---|
| 技术分 |  |  |
| 经济分 |  |  |
| ESG / sustainability |  |  |
| Safety / parking / governance |  |  |
| 是否有门槛 |  |  |
| 经济评分方式 | price / fleet size / concession fee / mixed |
| 最终中标逻辑 | highest score / lowest price / MEAT / other |

---

### 4️⃣ 关键评分项（Top 5）

Extract the most important 3–5 scoring items:

| 原文名称 | 中文 | 分值 | 类型（SOG/CN/SN/Price/ESG/Safety） | 对供应商含义 |
|---|---|---:|---|---|
|  |  |  |  |  |

Definitions:

- **SOG:** Strategic / Operational Governance
- **CN:** Compliance / Normative requirement
- **SN:** Service / Network requirement
- **Price:** Economic scoring
- **ESG:** Lifecycle, sustainability, climate, recycling
- **Safety:** Braking, parking, lighting, user protection, geofencing

---

### 5️⃣ 硬件与产品要求

| 维度 | 要求 | 对产品 / 供应商影响 |
|---|---|---|
| 车辆耐久性 |  |  |
| 制动系统 |  |  |
| 车灯 / 反光 |  |  |
| IoT / GPS / connectivity |  |  |
| 电池 / 换电 |  |  |
| 停车治理 / docking |  |  |
| LCA / 碳排放 |  |  |
| 维修便利性 |  |  |
| 数据接口 |  |  |
| 防破坏 / 防盗 |  |  |

---

### 6️⃣ 商业机会判断

| 项目 | 判断 |
|---|---|
| 项目吸引力 | 高 / 中 / 低 |
| 潜在车辆订单规模 |  |
| 对 e-bike / scooter 的需求倾向 |  |
| 对 Segway / 硬件供应商的机会 |  |
| 是否有备件 / 服务机会 |  |
| 是否适合进入销售 pipeline | 是 / 否 / 观察 |
| 建议跟进对象 | operator / city / partner / tender consultant |

---

### 7️⃣ 风险与限制

| 风险 | 等级 | 说明 | 应对建议 |
|---|---|---|---|
| 监管限制 | 高 / 中 / 低 |  |  |
| 车队规模过小 | 高 / 中 / 低 |  |  |
| 价格竞争 | 高 / 中 / 低 |  |  |
| ESG 证据链要求 | 高 / 中 / 低 |  |  |
| 本地运营能力要求 | 高 / 中 / 低 |  |  |
| 技术门槛 | 高 / 中 / 低 |  |  |

---

### 8️⃣ 结论与建议动作

Use concise executive wording:

- **结论一句话：**
- **为什么重要：**
- **对运营商意味着什么：**
- **对硬件供应商意味着什么：**
- **建议下一步：**
  1. 
  2. 
  3. 

---

## 8. Quality Bar｜质量标准

The output must meet these standards:

- Use official source first whenever available.
- Cite source links or file evidence.
- Dates must be exact where available.
- Tables must be complete and structured.
- Unknown information must be marked as “未披露 / not disclosed”.
- Do not over-analyze before extracting core facts.
- Separate facts, inference, and recommendations.
- For management-facing output, add clear conclusion and supplier implication.
- For Segway / hardware supplier analysis, always connect tender requirements to product-fit, TCO, lifecycle, serviceability, and fleet replacement potential.

---

## 9. Failure Handling｜失败处理

If official tender documents cannot be accessed:

1. State clearly what could not be accessed.
2. Use city / authority / tender title / keywords to search alternative sources.
3. Mark all non-official information as secondary-source information.
4. Do not fabricate missing tender fields.
5. Provide a “next source to verify” list.

If uploaded PDFs are incomplete or scanned:

1. Extract visible information first.
2. Mark unreadable sections.
3. Ask for the original PDF only if the missing data blocks core analysis.

---

## 10. Recommended File Naming｜推荐文件命名

```text
01_Tender_Intelligence/tender_intelligence_extraction_skill_v1.1.md
```

For GitHub commit message:

```text
Add tender intelligence extraction skill v1.1
```

---

## 11. Change Log

### v1.1

Added:

- Trigger rules
- Source priority
- Search rules
- Execution steps
- Hardware requirement extraction
- Supplier opportunity assessment
- Quality bar
- Failure handling
- Versioning guidance

### v1.0

Initial skill focused on:

- Purpose
- Input
- Basic tender extraction structure
- Output tables for basic information, vehicle scale, scoring structure, and key scoring items
