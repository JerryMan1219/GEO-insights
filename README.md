# GEO 洞察 / GEO Insights

艾瑞咨询 **2026 GEO 系列** 双报告 + 品牌级 AI 可见度诊断框架蒸馏。

## 📚 子 Skill

本仓库包含 **2 个独立 skill**：

### 1. `geo-insights/` — GEO 行业理论与方法论
合并自艾瑞咨询 2026 两份 GEO 报告：
- **Part 1** — 消费决策场景 AI 搜索洞察（2026.08，N=1000，44 页）
- **Part 2** — 2026 年 GEO 生成式引擎优化行业研究报告（41 页）

包含：11 章详尽内容 / 80+ 术语表 / 16 种实施模式 / 决策规则 cheatsheet。

### 2. `geo-visibility-report/` — 品牌 AI 可见度诊断报告框架（NEW）
蒸馏自两份实战 AI 可见度分析报告：
- **联想 AI 可见度分析报告**（2026.07，30 问题 × 6 模型 = 180 对话）
- **专业版立白 AI 可见度分析报告**（200 竞品，2033 引用源）

**核心架构**：**10 维度 × 3 阶段 × 6 模型**
- 10 大分析维度：可见度 / 提及率 / 排序 / 竞品对比 / 竞品排序 / 情感倾向 / 高引用源 / 关联引用源 / 共用引用源 / 优化建议
- 3 阶段决策：正面评估期 / 负面质疑期 / 品牌决策期
- 6 模型覆盖：豆包 / DeepSeek / 千问 / 元宝 / 文心 / Kimi

包含：8 章方法论 + 报告模板（直接套用）+ 提问词库（按阶段分类）。

**未来用法**：用本 skill 的报告模板 + `geo-insights` 的 GEO 理论，可以为任何品牌生成对标联想/立白格式的 AI 可见度诊断报告。

---

## 🚀 使用方式

### 作为 Skill 调用
两个 skill 都已部署到 `~/.workbuddy/skills/`：

```bash
~/.workbuddy/skills/geo-insights/          # 行业理论
~/.workbuddy/skills/geo-visibility-report/ # 诊断框架
```

调用时配合使用：
- 报告正文 → 用 `geo-visibility-report` 的章节与模板
- GEO 理论与方法论 → 调用 `geo-insights` skill
- 行业数据 → 调用 `geo-insights` 的 ch01/ch07

### 作为参考阅读
直接浏览 `geo-insights/chapters/` 与 `geo-visibility-report/chapters/` 的 Markdown 文件。

---

## 📂 仓库结构

```
GEO-insights/
├── README.md
├── geo-insights/                 # Skill 1: 行业理论
│   ├── SKILL.md
│   ├── chapters/  (11 章)
│   ├── glossary.md  (80+ 术语)
│   ├── patterns.md  (16 模式)
│   └── cheatsheet.md
└── geo-visibility-report/        # Skill 2: 诊断框架
    ├── SKILL.md
    ├── chapters/  (8 章)
    ├── glossary.md
    ├── patterns.md  (16 报告模式)
    ├── cheatsheet.md
    └── references/
        ├── report-template.md   # 完整报告模板
        └── question-bank.md     # 提问词库
```

---

## 🔗 两个 Skill 的协作流

```
用户输入：品牌 + 产品 + 竞品 + （可选）原始数据
        ↓
geo-visibility-report ──── 提供：报告结构 / 10 维度 / 3 阶段 / 6 模型
        ↓
geo-insights ──────────── 提供：GEO 理论 / 5 特征论 / DRRR / DSS / 3H 方法论
        ↓
输出：对标联想/立白格式的《XX 品牌 AI 可见度分析报告》
```
