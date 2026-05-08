---
description: 一键启动：自动挖掘今日 NAS 营销热点 → 用户选题 → 自动生成 EDM 营销邮件。
---

# NAS EDM 营销自动化工作流 (NAS EDM Auto Flow)

这个工作流将 **NAS 热点选题挖掘** 与 **EDM 邮件文案撰写** 串联，输出可直接投放的营销邮件。

## 步骤详解

1.  **NAS 热点挖掘 (Scout)**
    *   Agent 调用 `search_web`，按 `topic_selector` 中定义的搜索源（厂商动态、Reddit r/synology r/DataHoarder r/selfhosted、订阅替代痛点、SEO 关键词）执行搜索。
    *   严格执行 **NAS 相关度 ≥18** 的硬性过滤。
    *   输出 **Top 10 候选选题**（含目标人群、选题类型、EDM 指数、推荐主题行）。

2.  **人工决策与上下文投喂 (Human Selection)**
    *   Agent 展示 Top 10，并主动询问 EDM 必要参数：
        > "选哪个？回复序号即可。同时请告诉我：
        > 1. 这封邮件的转化目标？（产品页 / 教程下载 / 直播报名 / 优惠券）
        > 2. 主推哪款产品或 SKU？（可选）
        > 3. 是否绑定促销活动？（可选）
        > 4. 落地页 URL？（没有可用占位）"

3.  **EDM 邮件撰写 (Drafting)**
    *   调用 `script_writer` 生成完整邮件交付包：
        *   5 条候选主题行（5 种风格）
        *   5 条候选预览文本
        *   完整邮件正文（Hook → Problem → Solution → Proof → CTA → P.S.）
        *   A/B 测试建议

4.  **润色与变体 (Polish & Variants)**
    *   Agent 询问："这版方向对吗？需要哪种调整？
        *   🎯 更聚焦痛点 / 更专业理性 / 更轻松活泼
        *   ✂️ 更短（手机端 15 秒读完）
        *   🌐 输出英文版（出海 EDM）
        *   👥 切换目标人群（P1-P5）"

5.  **归档 (Archive)**
    *   最终稿默认保存到 `scripts/EDM-{{YYYYMMDD}}-{{选题slug}}.md`。

## 启动指令

在对话框输入以下任意一句即可触发：

*   "**开始写今天的 NAS 邮件**"
*   "**跑一下 NAS EDM 工作流**"
*   "**/nas_edm_workflow**"

## 默认参数（可在调用时覆盖）

| 参数 | 默认值 |
| :--- | :--- |
| `brand` | `{{brand}}`（待用户配置） |
| `audience_priority` | P1 > P4 > P2 > P3 > P5 |
| `language` | 中文（输出英文版需明确指定） |
| `email_length` | ≤350 字 |
| `cta_count` | 1 主 CTA + 1 P.S. 次级信息 |
