---
name: geo-visibility-report
description: "Brand AI Visibility Audit Report framework distilled from two reference reports (联想笔记本 + 立白). Use when generating brand-level GEO diagnostic reports, structuring AI visibility analyses across 10 dimensions × 3 decision phases × 6 LLM platforms, or when the user wants a '以联想/立白为对标的 AI 可见度诊断报告'. Works in tandem with the geo-insights skill (theory) — this skill defines the REPORT FORMAT and ANALYSIS DIMENSIONS."
---

<!-- argument-hint: [brand, products, competitor set] -->

# GEO 可见度诊断报告 / AI Visibility Audit Report
**来源**: 联想 AI 可见度分析报告 + 专业版立白 AI 可见度分析报告 | **生成**: 2026-08-11

本 skill 定义 **品牌级 AI 可见度诊断报告的标准框架**，与 `geo-insights`（行业理论）配对使用：
- `geo-insights` = GEO 理论与方法论（GEO 是什么、怎么做、怎么做对）
- **`geo-visibility-report`** = 报告模板与分析维度（如何把诊断结果结构化呈现）

---

## How to Use This Skill

调用本 skill 时，提供以下输入：
- 品牌名 + 产品/品类 + 核心竞品清单
- 原始检测数据（可选；缺数据时按框架模板生成）

输出：一份**对标联想/立白格式**的《XX 品牌 AI 可见度分析报告》。

**调用示例**：
- "用这个框架给[品牌]出一份 AI 可见度诊断报告"
- "按这俩报告的结构，分析我们品牌的 GEO 现状"
- "以这个 skill 的维度生成品牌诊断"

**与其他 skill 协作**：
- 报告正文 → 用本 skill 的 `chapters/` 与 `references/report-template.md`
- GEO 理论与方法论 → 调用 `geo-insights` skill
- 行业数据/品类渗透率 → 调用 `geo-insights` 的 ch01/ch07

---

## Report Architecture（核心架构）

### 1. 三大决策阶段 × 6 个大模型 × 10 个分析维度

**3 个用户决策阶段**（决定了用户提问时的心理状态与意图）：
- **正面评估期**：用户主动了解/比较品牌，关注"是什么、怎么样"
- **负面质疑期**：用户产生疑虑或被竞品/评测影响，关注"缺点、问题、避坑"
- **品牌决策期**：用户准备下单，关注"怎么选、值不值、推荐"

**6 个主流 AI 模型**（检测覆盖面）：
- 豆包（字节）｜ DeepSeek（深度求索）｜ 千问（阿里）｜ 元宝（腾讯）｜ 文心（百度）｜ Kimi（月之暗面）

**10 个分析维度**（每阶段都要回答的 10 个问题）：
1. 品牌 AI 可见度 — 品牌是否被提及
2. 品牌提及率 — 品牌在多少对话中被提及
3. 平均排序 — 品牌在 AI 答案中的平均位置
4. 竞品对比 — 与核心竞品可见度差距
5. 竞品排序 — 竞品在 AI 答案中的位置
6. AI 情感倾向 — 模型回答的品牌态度（正/中/负/无效）
7. 高引用源 — 哪些平台贡献了最多引用
8. 关联引用源 — 哪些内容被多个模型共同引用
9. 模型共用引用源 — 跨模型共用的引用源平台
10. 优化方向建议 — 优先处理什么问题、哪些平台

---

## Chapter Index

| # | 标题 | 内容 |
|---|------|------|
| [ch01](chapters/ch01-report-overview.md) | 报告概述与检测说明 | 检测流程 + 采集说明 + 数据基线 |
| [ch02](chapters/ch02-framework-10dim.md) | 10 大分析维度详解 | 每个维度的定义 + 计算公式 + 解读 |
| [ch03](chapters/ch03-phase-positive-evaluation.md) | 正面评估期 | 用户认知阶段 + 优化方法 |
| [ch04](chapters/ch04-phase-negative-doubt.md) | 负面质疑期 | 用户疑虑阶段 + 负面修复策略 |
| [ch05](chapters/ch05-phase-brand-decision.md) | 品牌决策期 | 用户决策阶段 + 决策内容打造 |
| [ch06](chapters/ch06-llm-platforms.md) | 6 大模型特性与引用偏好 | 模型 MAU + 引用源分布 |
| [ch07](chapters/ch07-methodology.md) | GEO 优化执行方法论 | 先聚焦再扩张 + 负面/决策策略 |
| [ch08](chapters/ch08-value-proposition.md) | GEO 价值与前景 | 被看见→被信任→被定义 |

---

## Topic Index

- **10 大分析维度** → ch02
- **AI 情感倾向** → ch02, ch04, ch05
- **GEO 方法论** → ch07
- **GEO 价值** → ch08
- **引用源分布** → ch02, ch06
- **大模型 MAU** → ch01, ch06
- **正面评估期** → ch03
- **负面质疑期** → ch04
- **品牌决策期** → ch05
- **先聚焦再扩张** → ch07
- **优化优先级** → ch03, ch04, ch05, ch07
- **检测流程** → ch01
- **跨模型引用源** → ch02, ch06
- **被定义** → ch08
- **被信任** → ch08
- **被看见** → ch08
- **重建大模型判断** → ch04

---

## Key Metric Formulas

| 指标 | 公式 | 解读 |
|------|------|------|
| 可见度 % | 品牌提及次数 / 总对话次数 | 品牌被 AI 看到的程度 |
| 引用率 | 引用源总量 / 相关文章总量 | AI 抓取信源的效率 |
| 品牌引用源占比 | 品牌相关引用源 / 总引用源 | 模型是否接触品牌信息 |
| 平均排名 | Σ品牌出现位置 / 总次数 | 品牌在 AI 答案中的排序 |
| 模型共用引用源率 | 共用平台引用数 / 总引用数 | 一篇内容多模型覆盖的效率 |
| 负面情感率 | 负面回答数 / 总回答数 | 品牌舆情健康度 |

---

## Supporting Files

- [chapters/ch01-ch08.md](chapters/) — 8 章详尽内容
- [glossary.md](glossary.md) — 关键术语
- [patterns.md](patterns.md) — 各阶段报告模式
- [cheatsheet.md](cheatsheet.md) — 数据基线 + 阈值表
- [references/report-template.md](references/report-template.md) — 完整报告模板
- [references/question-bank.md](references/question-bank.md) — 提问词库（按阶段分类）

---

## Scope & Limits

本 skill 覆盖：
- ✅ 报告整体框架（10 维度 × 3 阶段 × 6 模型）
- ✅ 每个维度的计算公式与解读标准
- ✅ 各阶段的优化方法论
- ✅ 报告模板（可直接套用）

本 skill **不包含**：
- ❌ 具体品牌的实际检测数据（需用户提供或现场采集）
- ❌ GEO 理论与原理（需配合 `geo-insights`）
- ❌ 行业品类数据（需配合 `geo-insights` 的 ch01/ch07）

---

## Reference Sources

- **联想 AI 可见度分析报告**：2026.07.06，30 问题 × 6 模型 = 180 对话，69 竞品，3089 引用源
- **专业版立白 AI 可见度分析报告**：N 问题 × 5+ 模型，200 竞品，2033 引用源
- 两份报告均采用相同 10 维度 × 3 阶段框架，且来自同一服务商（推断为某 GEO 服务商标准模板）
