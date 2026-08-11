# GEO 洞察 / GEO Insights

艾瑞咨询 **2026 GEO 系列** 双报告蒸馏为可复用的 AI Skill。

## 📚 来源

合并自艾瑞咨询 2026 两份 GEO 报告：

- **Part 1** — 消费决策场景 AI 搜索洞察（2026.08，N=1000，44 页）
  - 9 大消费品类 AI 搜索行为数据
  - GEO 六步实施框架
  - B2C vs B2B 差异化策略
- **Part 2** — 2026 年 GEO 生成式引擎优化行业研究报告（2026.08，41 页）
  - GEO 技术原理与 8 大认知误区
  - 行业生态与市场规模预测（2025: 6 亿 → 2030: 518 亿）
  - 内容工程、效果评估、未来趋势
  - 7 大 GEO 服务商案例（智推时代/PureblueAI/悠易/源易/迈富时/万悉/光引）
  - 知乎作为语料源 + 7 位专家观点

## 🧩 Skill 结构

```
geo-insights/
├── SKILL.md           — 16 大核心框架 + 章节索引 + 主题索引
├── chapters/          — 11 章详尽内容（AI 搜索时代 → 未来趋势）
├── glossary.md        — 80+ GEO 关键术语
├── patterns.md        — 16 种 GEO 实施模式
└── cheatsheet.md      — 决策规则 + 阈值 + 速查表
```

## 🔧 使用

将此文件夹复制到 `~/.workbuddy/skills/geo-insights/` 或 `~/.agents/skills/geo-insights/` 后：

- 无参数调用 → 加载核心框架
- 带主题（如 "DRRR"、"B2B"）→ 自动定位章节
- 带章节号（如 "ch04"）→ 加载内容工程章节
- 快速决策 → 用 cheatsheet.md 查表/阈值

详见 [SKILL.md](./SKILL.md)
