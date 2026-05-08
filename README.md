# NAS Hot Spot EDM Writer (NAS 营销热点 EDM 邮件助手)

把全网 NAS 圈的最新热点和老痛点，自动转化成可直接投递的 **EDM 营销邮件**。

## 🎯 定位

*   **品类**：NAS（Network Attached Storage / 网络存储）
*   **场景**：EDM 电子邮件营销（内容营销 / 用户唤醒 / 转化引流）
*   **核心人群**：摄影家庭用户、影音发烧友、SOHO 中小企业、自托管极客、内容创作者

## 🚀 核心能力

### 1. NAS 选题挖掘 (`topic_selector/`)
*   **数据源**：Synology / QNAP / 绿联 / 极空间 等厂商动态、Reddit（r/synology, r/DataHoarder, r/selfhosted, r/Plex, r/jellyfin, r/homelab）、Google Trends、订阅服务（iCloud / Google Photos / Plex）涨价跑路事件。
*   **EDM 营销指数**：从 **NAS 相关度 / 痛点共鸣 / 打开率潜力 / 转化潜力 / 时效性** 五个维度打分。
*   **选题类型**：News / Pain / Tutorial / Compare / Trend / Promo-Hook。

### 2. EDM 邮件文案 (`script_writer/`)
*   **完整邮件结构**：Hook → Problem → Solution → Proof → CTA → P.S.
*   **5 条主题行候选**（5 种风格：痛点提问 / 数字冲击 / 悬念 / 反差 / 利益直给）+ 5 条预览文本。
*   **合规校验**：避开 SPAM 触发词、不绝对化宣传、不贬低竞品、保留退订占位。
*   **A/B 测试建议**：自动给出测试方案与假设。

### 3. 自动化工作流 (`.agent/workflows/`)
一键串联：挖掘 → 选择 → 生成 → 润色 → 归档。

## 🛠 使用方法

在 Copilot Chat 输入：

> "**开始写今天的 NAS 邮件**"
> 或 "**/nas_edm_workflow**"

工作流会：
1. 输出 NAS 营销选题 Top 10
2. 询问你：选哪个 / 转化目标 / 主推产品 / 落地页
3. 生成完整 EDM 邮件交付包（主题行 + 预览 + 正文 + A/B 测试）
4. 支持继续润色、缩短、出英文版、切换人群

## 📂 项目结构

*   `topic_selector/SKILL.md` — NAS 选题挖掘规则与评分模型
*   `script_writer/SKILL.md` — EDM 邮件文案撰写规范
*   `.agent/workflows/tech_news_workflow.md` — 自动化工作流定义
*   `scripts/` — 历史生成的邮件归档
*   `xhs_topics.json` — 选题缓存（可选）

---
*Customized for NAS category EDM marketing.*
