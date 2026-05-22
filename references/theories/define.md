# 第二幕 · 定义（Define）——我们到底要解决什么？怎么定义价值？

> **本幕目标**：把第一幕捞上来的洞察凝成"一个可以被反驳、被验证、被砍掉的命题"。本幕调度理论的总原则——**先聚焦再展开**：用 Problem Statement 把命题钉死（converge），再用 HMW 把命题撬开成可设计空间（diverge），最后用 Lean Canvas / VPC 把整个商业逻辑串起来验真。**定义阶段的核心产物是"一句话"，不是"一份文档"**。

---

## Lean Canvas / 精益画布

**一句话定义**：用 9 个格子在一张 A4 纸上画清楚"问题-客户-价值-方案-渠道-成本-收入-指标-不公平优势"的完整商业逻辑。

**出处**：Ash Maurya《Running Lean》(2010, 2nd ed 2012)，改编自 Alex Osterwalder 的 Business Model Canvas，针对初创和 0→1 场景把 Key Partners 换成 Problem，Key Activities 换成 Solution，Customer Relationships 换成 Unfair Advantage。

**适用情境（默认场景）**：
- 0→1 立项前的"一张纸说清楚"——给老板、给投资人、给团队对齐
- Pivot 决策时——前后两版 Lean Canvas 对比，看到底变了什么
- 多个产品方向竞争时——每个方向画一张 Canvas 横向对比
- 早期产品的周度/月度健康检查——哪格还是假设没验证？

**核心步骤**：
1. **从右上角的 Customer Segments 开始填**（不是从问题）——客户决定一切
2. **顺时针 → Problem（前 3 大问题）→ UVP（独特价值主张，一句话）→ Solution（每个 Problem 对应一个最小方案）**
3. **左下：Key Metrics（北极星指标 + 关键漏斗指标）+ Cost Structure**
4. **右下：Channels（怎么触达）+ Revenue Streams（怎么收钱）**
5. **中间：Unfair Advantage（不公平优势）——别人无法 copy 的东西**——填不出来不是问题，意识到没有更重要

**局限与不适用**：
- **不适用于成熟产品**：成熟产品的"问题-客户-渠道"早已稳定，画 Lean Canvas 是文字游戏，应用 BMC 或 Value Stream Map
- **不适用于 B2B2C / 平台型产品**：多方价值需要画多张 Canvas（供给侧一张、需求侧一张），单张 Canvas 会强行简化
- **容易变成"我们想做的"而非"市场需要的"**：所有格子都是假设，没区分"已验证"和"待验证"就是空想图
- **Unfair Advantage 是最被滥用的格**：填"团队执行力强""技术好"都是废话，真正的不公平优势是"内部数据 / 网络效应 / 独家牌照 / 创始人独有的资源"
- **不应"画完即定稿"**：Canvas 是活文档，每周更新被证伪/证实的部分

**与其他理论的配合**：
- **上游配合**：JTBD → 喂给 Problem 格；Empathy Map → 喂给 Customer Segments；反向假设 → 标注每格的致命假设
- **下游配合**：Lean Canvas 的"待验证假设"→ 喂给假设验证矩阵（第五幕）；Key Metrics → 喂给北极星指标 / AARRR；Solution → 喂给 MoSCoW 优先级（第三幕）
- **互替**：BMC（Business Model Canvas）适合成熟业务；Mission Model Canvas 适合公益/政府项目；Value Proposition Canvas 是 Lean Canvas 中 UVP+Customer+Problem 三格的放大版

**判断要点（融会贯通信号）**：
- 当团队 PRD 写到第 30 页还说不清"我们到底卖什么给谁"——立即停手画 Lean Canvas
- 当 Lean Canvas 里 3 个以上格子是"我们觉得…"——这是要去做用户访谈/验证的信号

**示例输出片段**：
> **Lean Canvas（B 端 AI 报表工具）**
> Customer Segment：50-500 人企业的财务主管（决策人）+ 财务专员（使用人）
> Problem：①月度报表手工耗时 30+ 小时 ②数据散落在 4+ 系统 ③老板要新视角时改报表周期 3 天起
> UVP：让财务专员"30 分钟出一份老板满意的新报表"
> Solution：自然语言生成 SQL + 一键关联多源数据 + 模板库
> Unfair Advantage：3 家头部 ERP 的官方 API 合作（待验证 ⚠️）
> Key Metrics：周活财务专员数 / 平均报表生成时长 / 模板复用率
> **待验证假设**：UVP 中"老板满意"的定义；API 合作能否拿下

---

## 价值主张画布（Value Proposition Canvas, VPC）

**一句话定义**：用"客户档案（Pain/Gain/Job）"和"价值地图（Pain Reliever/Gain Creator/Product）"两个三角拼图，把价值主张和客户需求严格对齐。

**出处**：Alexander Osterwalder, Yves Pigneur 等《Value Proposition Design》(2014)，作为 Business Model Canvas 中"Value Proposition + Customer Segment"两格的放大工具。

**适用情境（默认场景）**：
- 团队对"我们到底创造什么价值"有分歧时
- 写 UVP（独特价值主张）前的素材整理
- 现有功能集要重新对齐用户需求时（"我们做了 100 个功能但留存还是低"）
- B 端销售话术开发——把价值地图直接翻译成销售卖点

**核心步骤**：
1. **先填右边客户档案（Customer Profile）**：Customer Job（要完成的任务，来自 JTBD）+ Pain（任务过程中的痛苦）+ Gain（期望达成的收益）
2. **按重要性排序 Pain 和 Gain**——必须有 top 3，不能并列
3. **再填左边价值地图（Value Map）**：Product/Service（你提供的东西）+ Pain Reliever（如何缓解每个 Pain）+ Gain Creator（如何创造每个 Gain）
4. **画 Fit 连接线**：每个 Pain Reliever 必须连到一个 Pain，每个 Gain Creator 连到一个 Gain——孤儿格说明价值错配
5. **检查 Problem-Solution Fit**：连接最密集且对应 top Pain/Gain 的就是你的核心价值

**局限与不适用**：
- **不适用于早期还没有 Solution 时**：左边价值地图填不出来就先别画，先回到第一幕做 JTBD
- **不适用于多边市场**：双边平台需要两张 VPC（卖家端 + 买家端），强行单张会顾此失彼
- **Gain 和 Pain 容易写得太抽象**：写"提高效率""降低成本"是废话，必须量化或具象（"减少周报耗时 50%"）
- **常见误用**：把"功能"塞到 Pain Reliever 格里——Pain Reliever 是"如何缓解 Pain"的机制描述，不是功能名
- **PSF 不等于 PMF**：Problem-Solution Fit 只说明价值匹配，Product-Market Fit 还需要市场规模和愿付价格验证

**与其他理论的配合**：
- **上游配合**：JTBD → 喂给 Customer Job 格；Empathy Map 的 Pain/Gain → 直接 1:1 喂给 VPC
- **下游配合**：VPC 的核心价值 → 喂给 Lean Canvas 的 UVP 格；Fit 连接图 → 喂给 HMW 转换为设计挑战；Pain Reliever 描述 → 喂给销售话术 / 落地页文案
- **互替**：JTBD 的 Outcome-Driven Innovation 框架在"价值识别"功能上几乎等价；Empathy Map 是更轻量的客户档案版本

**判断要点（融会贯通信号）**：
- 当 UVP 起草卡住或写出来后没人能复述——VPC 是底层素材表
- 当用户访谈说"这功能我用不到"——直接画 VPC 看哪个 Pain/Gain 没对上

**示例输出片段**：
> **客户档案（财务专员）**：
> Job：每月给老板出 3-5 份"角度不同的"经营分析报表 | Pain：①跨系统取数 70% 工时 ②老板临时改需求 ③Excel 公式易错 | Gain：①周末不加班 ②被老板表扬"反应快" ③同事问她要模板
> **价值地图（我们的产品）**：
> Pain Reliever：①自然语言一句话取数（对 Pain ①） ②2 分钟生成新视角（对 Pain ②） ③数据校验内置（对 Pain ③） | Gain Creator：①把 30 小时压缩到 2 小时（对 Gain ①） ②内置"老板风格"模板（对 Gain ②）
> **未对齐**：Gain ③（同事认可）没有对应——可以加入"模板分享"功能强化社交价值

---

## HMW / How Might We

**一句话定义**：把一个问题/洞察转换成"我们可能怎样…"句式的开放性设计挑战，打开方案空间。

**出处**：Min Basadur 1970s 在宝洁提出，后被 IDEO 系统化推广，Tim Brown《Change by Design》(2009) 和 Stanford d.school 设计思维教程收录为标准工具。

**适用情境（默认场景）**：
- 把模糊洞察转成可设计的挑战（JTBD/5 Why 输出 → HMW 输入）
- Workshop 中的头脑风暴启动——HMW 是发散环节的官方触发器
- Pain Point 列表过长，需要选出"最值得设计"的 3-5 个
- 产品评审中重新框定问题（评审说"用户体验差"→ 拆成 5 个 HMW）

**核心步骤**：
1. **从一个具体的 Insight 出发**——不是从功能或解决方案
2. **写第一版 HMW**：套用 "How might we [verb] [user] to [outcome] [in context]?"
3. **做三种变体测试**——参考 IDEO 的 5 种变体：
   - 放大正面（"How might we amplify…"）
   - 移除负面（"How might we remove…"）
   - 探索反向（"How might we do the opposite of…"）
   - 类比邻域（"How might we make X like Y?"）
   - 改变前提（"How might we make it so users don't need to…"）
4. **检查 HMW 的开放度**：太宽（"HMW 改善用户体验"=无效）/ 太窄（"HMW 把按钮变成红色"=已隐含方案）
5. **选 3-5 个最有撬动力的 HMW 进入发散环节**——其他可以归档

**局限与不适用**：
- **不适用于已经确定方案要执行时**：HMW 是发散工具，方案已定还用 HMW 是浪费
- **不适用于强约束工程问题**：技术决定型问题（"内存只有 100MB 怎么放下 1GB 数据"）HMW 形式上空，应该用工程权衡
- **极易被写成伪 HMW**：①"HMW 做一个 X 功能"（已含方案）②"HMW 提升用户满意度"（无具体洞察）——必须严格审查
- **HMW 不能脱离 Insight 独立存在**：脱离洞察就退化成头脑风暴的废话生成器

**与其他理论的配合**：
- **上游配合**：5 Why 根因 → 喂给 HMW（"How might we 解决根因 X"）；JTBD 的 Underserved 维度 → 喂给 HMW；VPC 的未对齐 Pain → 喂给 HMW
- **下游配合**：HMW → 喂给 Brainstorming / Crazy 8s 等发散方法；优选 HMW → 喂给 Problem Statement 作为定义；多个 HMW → 喂给 Story Mapping 串成产品愿景
- **互替**：Design Challenge 句式（"Design a way to…"）几乎等价但更命令式；Problem Statement 是 HMW 的"已收敛版"

**判断要点（融会贯通信号）**：
- 当 Insight 已经被反复讨论但没人能提出"那我们做什么"——HMW 是桥梁
- 当头脑风暴会议开 30 分钟还在原地——大概率因为没有先做 HMW，方案散乱无主题

**示例输出片段**：
> **Insight**（来自 JTBD + 访谈）：财务专员花 70% 工时跨系统取数，但她真正想要的是"看上去专业的洞察"而非"数据本身"。
> **HMW 三变体**：
> ①（移除负面）How might we remove cross-system data fetching from the financial analyst's workflow entirely?
> ②（改变前提）How might we make it so the analyst presents insights without ever opening Excel?
> ③（类比）How might we make report-building feel like Tinder—swipe through pre-built insights?
> **选 ②** 进入发散环节——撬动力最大，因为它挑战了"分析必须用 Excel"的隐含假设。

---

## 北极星问题陈述（Problem Statement）

**一句话定义**：用一句话钉死"为谁、解决什么、在什么情境、获得什么、为什么现在没解决"的产品命题。

**出处**：Stanford d.school 设计思维框架的 Define 阶段产物；常见模板包括 POV（Point of View, "[user] needs to [need] because [insight]"）和 Atlassian 的 5W Problem Statement Template。Marty Cagan《INSPIRED》(2017) 也把 Problem Statement 列为产品发现的核心产物。

**适用情境（默认场景）**：
- 任何 PRD/Spec 文档的第一页——没有 Problem Statement 的 PRD 是无主之书
- 团队对齐"我们到底在做什么"的最简工具
- 评审/老板提问时的回答骨架（"我们解决的是 X 用户在 Y 情境下的 Z 问题"）
- 用作"反 scope creep 的护栏"——任何不在陈述范围内的功能都该被质疑

**核心步骤**：
1. **明确格式**：选 POV 模板或 5W 模板，团队统一
2. **填 5 个槽位**：①目标用户（具体到角色而非"用户"） ②当下情境（什么场景下） ③核心需求/任务（要完成什么） ④期望结果（怎样算成功） ⑤当下痛点（为什么现有方案不行）
3. **压缩到一句话**——超过 3 行就是没想清楚
4. **三方反驳测试**：销售、客服、技术各看一眼能不能复述
5. **打印贴墙 / 钉文档头部**：所有后续决策的对齐锚点

**局限与不适用**：
- **不适用于多产品组合策略**：组合策略需要的是 Vision Statement / Mission，不是单一 Problem Statement
- **不适用于探索期还没收敛时**：一句话写不出来 = 还没想清楚，应该回到第一幕
- **容易写成"流量话术"**：写"帮助用户更高效地工作"= 废话；必须有具体角色、具体情境、具体痛点
- **不能替代 Vision**：Problem Statement 是"现在解决的"，Vision 是"长期要去哪"，两个不能互相替代

**与其他理论的配合**：
- **上游配合**：JTBD + VPC + 5 Why 共同蒸馏出问题陈述；HMW 最终收敛到 Problem Statement
- **下游配合**：Problem Statement → 喂给 Lean Canvas 的 Problem 格；喂给 MoSCoW 优先级作为"Must"的判定标准；喂给北极星指标定义
- **互替**：POV Statement / 5W Statement / "Mom Test" 风格的 Problem Statement 都是同一物的不同模板；OKR 的 O（Objective）部分常常就是 Problem Statement 的另一种表达

**判断要点（融会贯通信号）**：
- 当团队两个人对"产品要解决什么"的描述差异 > 30%——这是必写 Problem Statement 的信号
- 当 PRD 改到第 5 版还在加功能——回看 Problem Statement，大概率定义太宽

**示例输出片段**：
> **Problem Statement（B 端 AI 报表工具）**：
> 50-500 人企业的财务专员，在每月被老板临时要求做"新视角经营分析"时，需要在 1 小时内输出一份既准确又可发出的报表，目前因为数据跨 4+ 系统、Excel 公式易错、缺老板风格模板，平均要 1-2 天且经常返工，导致她周末加班且无法被同事/老板视为"反应快的专业人才"。
> **反 scope 护栏**：任何不服务于"1 小时出一份老板满意报表"的功能都先打问号——比如"高级数据建模""跨企业基准对比"都是后续而非 MVP。

---

## 第二幕末决策提示

- **如果情境是"早期立项、需要对齐"**：先写 Problem Statement → 再画 Lean Canvas（Problem Statement 喂 Problem 格）→ 用 VPC 验真 UVP。
- **如果情境是"已有洞察但不知怎么做"**：5 Why 根因 → HMW 转换 → 收敛到 Problem Statement → 进入第三幕决策。
- **如果情境是"现有产品 PMF 没找到、要 Pivot"**：旧版 Lean Canvas vs 新版 Lean Canvas 对比 → 用 VPC 验证新 UVP → 重写 Problem Statement。
- **如果情境是"团队评审分歧大"**：直接逼出一句话 Problem Statement——能不能写出来本身就是诊断信号。
- **本幕产物的硬指标**：①一句话 Problem Statement ②一张 Lean Canvas ③一组 3-5 个 HMW ④一张 VPC。少任何一个进入第三幕都会带来无效决策。
