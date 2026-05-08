---
description: 自动搜寻并筛选与 NAS（网络存储）品类高度相关、可用于 EDM 邮件营销的热点选题。
---

# NAS 营销选题挖掘助手 (NAS Topic Selector for EDM)

这个 Skill 用于从全网挖掘 **NAS（Network Attached Storage / 网络存储）** 品类下的高潜力营销选题，专门服务于 **EDM（电子邮件营销）** 场景。

## 目标 (Goal)
找到当下 NAS 目标用户最关心、最焦虑、最兴奋的话题，转化为可以推动 **打开率 / 点击率 / 转化率** 的 EDM 选题。

> [!IMPORTANT]
> **CRITICAL RULE 1（相关性）**：选题必须能 **自然过渡到 NAS 价值主张**。允许两类来源：
>
> **A. NAS 直接相关**：数据存储、备份、私有云、家庭影音、数据安全、隐私、Plex/Jellyfin、Docker/虚拟化、监控录像、照片管理、订阅服务涨价/跑路、网盘替代、远程访问、RAID/硬盘、能耗。
>
> **B. AI 相关但能挂接到 NAS**（强烈鼓励，NAS 正在进入 AI 时代）：
>   - 本地大模型部署（Ollama / LM Studio / llama.cpp 在 NAS / Homelab 跑模型）
>   - 本地 AI 照片管理（Immich AI 人脸/物体识别、PhotoPrism、自托管 Stable Diffusion）
>   - 数据隐私 vs 云端 AI（ChatGPT/Claude 训练数据、企业数据合规）
>   - AI 工作流的存储需求（向量数据库、RAG 知识库自托管、模型权重存储）
>   - 创作者 AI 素材管理（生成式 AI 输出海量素材的归档备份）
>   - 厂商 AI 功能（Synology AI Console、QNAP QuMagie AI、绿联 AI 相册等）
>
> **纯 AI 话题不挂钩 NAS 价值则淘汰**（例如 GPT-5 评测、AI 商业新闻、纯 SaaS AI 工具）。判断标准：能否在邮件正文中自然引出"所以你需要一台 NAS"。
>
> **CRITICAL RULE 2（时效性）**：新闻类选题严格限制 **7天内**（行业动态/产品发布 72小时内更佳）。常青痛点类选题（如"如何替代 Google Photos"）不受时间限制，但必须有近期热度信号。

## 核心目标受众 (Target Audience for NAS EDM)

EDM 选题必须围绕以下细分人群的痛点设计，每个选题需明确标记主攻人群：

| 人群代号 | 画像 | 核心痛点 |
| :--- | :--- | :--- |
| **P1 摄影爱好者 / 家庭用户** | 照片视频海量增长 | iCloud/Google Photos 涨价、隐私、备份恐惧 |
| **P2 影音发烧友** | Plex/Jellyfin/4K 蓝光原盘玩家 | 串流性能、转码、硬解、片库管理 |
| **P3 SOHO / 中小企业主** | 小团队协作、客户资料 | 数据安全、勒索病毒、多人共享、合规 |
| **P4 极客 / 自托管玩家** | Self-hosted、Docker、Homelab | 折腾乐趣、订阅服务替代、数据主权 |
| **P5 内容创作者 / YouTuber** | 大体积素材、剪辑协作 | 容量、读写速度、异地备份 |

## 搜索源 (Data Gathering)

### 1. 行业新闻与厂商动态
*   `Synology OR QNAP OR Asustor OR TerraMaster OR UGREEN NAS news`
*   `Synology DSM update / new model release`
*   `QNAP QTS security advisory`
*   `"NAS" "ransomware" OR "vulnerability" when:7d`
*   `WD OR Seagate OR Toshiba HDD news`（硬盘新品/降价/故障率）

### 2. 替代订阅 / 痛点驱动选题
*   `Google Photos alternative self-hosted`
*   `Dropbox / iCloud / OneDrive price increase`
*   `Plex price hike OR policy change`
*   `Immich / Nextcloud / PhotoPrism release`

### 3. AI × NAS 交叉选题（重要！）
*   `Ollama on NAS / Synology / QNAP`
*   `local LLM home server / homelab`
*   `Immich smart search AI release`
*   `Synology AI Console / QNAP QuMagie / UGREEN AI`
*   `self-hosted RAG / vector database`
*   `Stable Diffusion home server`
*   `"AI" "privacy" "local" when:7d`
*   `site:reddit.com (r/LocalLLaMA OR r/selfhosted) "NAS" OR "home server" when:7d`

### 4. 社区热度信号（核心 EDM 灵感来源）
*   `site:reddit.com (r/synology OR r/qnap OR r/HomeServer OR r/selfhosted OR r/DataHoarder OR r/Plex OR r/jellyfin OR r/LocalLLaMA OR r/homelab) when:7d`
*   排名靠前、评论数 >100 的帖子优先（社区共鸣即 EDM 共鸣）。
*   r/LocalLLaMA 中讨论"硬件 / 存储 / 部署"的帖子优先于纯模型评测帖。

### 5. SEO 与搜索趋势
*   Google Trends：`NAS` / `home server` / `自建网盘` / `Plex 替代` / `本地大模型` / `Ollama` 上升关键词
*   `"how to" NAS` / `"run AI locally"` 长尾词

## EDM 营销价值评分 (EDM Marketing Index)

对所有候选选题打分 (0-100)：

| Metric | Weight | Points | Description |
| :--- | :--- | :--- | :--- |
| **Relevance (NAS相关度)** | 25% | 0-25 | **一票否决项**。低于 18 分直接淘汰。是否能自然过渡到 NAS 产品/解决方案？ |
| **Pain Resonance (痛点共鸣)** | 30% | 0-30 | 是否击中 P1-P5 任一人群的真实痛点/焦虑/兴奋点？社区讨论是否激烈？ |
| **Open-Rate Potential (打开率潜力)** | 20% | 0-20 | 能否提炼出有冲击力的邮件主题行（subject line）？是否带反差/数字/紧迫感？ |
| **CTA Conversion (转化潜力)** | 15% | 0-15 | 是否能自然导向产品页/教程/促销/试用注册？ |
| **Timeliness (时效性)** | 10% | 0-10 | 行业新闻当天>72h>7d；常青痛点取近期热度信号。 |

**筛选门槛**:
*   `Total = Relevance + Pain Resonance + Open-Rate + CTA + Timeliness`
*   只有 **Total >= 75** 且 **Relevance >= 18** 的选题才能进入 Top 10。

## 选题类型分类 (Topic Buckets)

每条选题须打上一个类型标签，便于 EDM 节奏规划：

*   `[News]` 行业新闻 / 厂商发布（蹭热度）
*   `[Pain]` 痛点教育（用户焦虑 → 解决方案）
*   `[Tutorial]` 实操教程（高打开率，建立专业感）
*   `[Compare]` 对比测评（决策期用户）
*   `[Trend]` 趋势洞察（高端用户/B 端）
*   `[Promo-Hook]` 促销钩子（可绑定优惠/新品）
*   `[AI×NAS]` AI 与 NAS 结合的新场景（本地大模型、AI 相册、隐私 AI）

## 输出格式 (Output Format)

```markdown
# 📬 今日 NAS EDM 选题 Top 10 (YYYY-MM-DD)

### 1. [Pain] Google Photos 又涨价了，老用户彻底坐不住 - EDM指数: 92
- **来源**: [9to5Google](https://...) / r/DataHoarder 热帖 (2.3k upvotes)
- **目标人群**: P1 摄影爱好者 / P4 极客
- **关键词**: #GooglePhotos #照片备份 #私有云 #Immich
- **评分理由**:
  - 🎯 NAS相关度 (24/25): 完美引出"用 NAS + Immich 一劳永逸"。
  - 💢 痛点共鸣 (28/30): 订阅疲劳是 2026 年最大共识。
  - 📧 打开率 (18/20): 主题行可写"你的照片，又要被'加价'一次了"。
  - 🛒 转化 (14/15): 直接挂照片备份方案落地页。
- **EDM 角度建议**: 焦虑开场 → 数据主权升华 → 引导查看"NAS 照片管理终极方案"。
- **推荐主题行 (Subject Line)**:
  1. "你的回忆，凭什么每年涨价 20%？"
  2. "Google 又把照片当人质了"
  3. "10 万张照片，5 分钟搬回自己家"

### 2. ...
```

## 示例选题（参考库）

*   `[News]` 群晖发布 DS925+ / DSM 7.3 重大更新
*   `[Pain]` Plex 又改订阅政策，老玩家集体迁移 Jellyfin
*   `[Tutorial]` 用 NAS 5 分钟搭建全家共享相册（替代 iCloud）
*   `[Compare]` 2026 年 4 盘位 NAS 横评：群晖 vs 极空间 vs 绿联
*   `[Trend]` 勒索病毒 2026 年攻击 NAS 同比 +180%，3-2-1 备份还够吗？
*   `[Promo-Hook]` 双11 前瞻：硬盘价格走势 + NAS 选购避坑
*   `[AI×NAS]` Ollama + 你的 NAS：在家跑 Llama 4 完全教程
*   `[AI×NAS]` Immich 上线本地 AI 搜索：自然语言找十年前的照片
*   `[AI×NAS]` ChatGPT 用你的聊天记录训练？把知识库搬回 NAS 自托管 RAG
*   `[AI×NAS]` Synology / QNAP 新一代型号集成 NPU，本地 AI 推理实测
*   `[AI×NAS]` AI 视频生成时代来了，4K 素材一周吃掉 2TB，你的存储还够吗？

## 严禁选题 (Hard Filter)
*   **纯 AI 话题挂不上 NAS 的**（如 GPT-5 商业模式分析、纯 API 工具评测、AI 创业新闻）。
*   纯消费数码（手机/笔电）发布会，与存储/数据无关联。
*   政治、宗教、争议性社会话题。
*   竞品负面攻击（合规风险）。

## AI 选题挂钩 NAS 的标准角度（写邮件时套用）

当选题来自 AI 领域时，邮件正文必须用以下任一角度收口到 NAS：

1.  **隐私角度**："你的对话/照片/代码，不该成为别人的训练数据" → 本地部署
2.  **成本角度**："OpenAI/Claude API 月费 vs 一次性 NAS + 本地模型"
3.  **存储角度**："AI 生成内容（图/视频/音频）爆炸式增长，云盘装不下"
4.  **性能角度**："新一代 NAS 集成 NPU/GPU，AI 任务不再卡顿"
5.  **数据主权**："RAG 知识库放别人服务器？不如自己掌握"
6.  **能力扩展**："你的 NAS 不只是存储，还能跑 LLM / Stable Diffusion / 语音转写"
