# 第四幕 · 设计（Design）——用户会怎样走完这段路？信息怎么组织？

> **本幕目标**：把第三幕选定的功能从"清单"变成"用户能流畅走完的产品"。本幕调度理论的总原则——**先时间后空间，再容器**：用 Journey Map / Story Mapping 把时间维度的"用户怎么走"画出来，再用 IA / Wireframe 把空间维度的"信息怎么放"组织起来，最后用 Service Blueprint 检查"前台后台是否对得上"。**没有时间维度先行的设计都是"功能墓地"**。

---

## 用户旅程地图 / Customer Journey Map

**一句话定义**：把用户从"产生需求"到"完成任务"的全过程按时间轴展开，每个阶段标注"行为/想法/情感/痛点/机会"。

**出处**：起源于 1980s 服务设计领域（Lynn Shostack 的 Service Blueprint 启发），后被 Forrester / Adaptive Path 等公司推广为 UX 核心工具。Kim Flaherty / Nielsen Norman Group 2018 年的《Journey Mapping 101》是当前权威指南。

**适用情境（默认场景）**：
- 跨触点产品（App + 网页 + 客服 + 线下）需要看到全貌
- 现有体验有"断点"但说不清在哪——Journey Map 让断点可见
- 跨团队对齐"用户视角"（设计/产品/运营/客服各画一段，拼起来看差异）
- 改版前的现状诊断 + 改版后的目标态对比

**核心步骤**：
1. **定 Persona / Actor**：基于真实数据的角色，不是想象
2. **定 Scenario（场景）和 Time Frame**：哪个具体任务、覆盖多长时间（一次会话 / 一周 / 一个月）
3. **画时间轴 + 切阶段**：通常 4-7 个阶段（Awareness → Consideration → Onboarding → First Use → Habit → Advocacy）
4. **每阶段填 5 行**：Action（行为）/ Touchpoint（触点）/ Thought（想法）/ Emotion（情感曲线）/ Pain & Opportunity（痛点机会）
5. **标注 Moment of Truth**：哪 1-2 个关键节点决定整体体验——后续设计重投这里

**局限与不适用**：
- **不适用于多角色高度交织的场景**：B2B2C 中"决策人/购买人/使用人"是不同人，单线 Journey 强行合并会扭曲，应用 Service Blueprint 或多 Persona 多 Journey 并列
- **缺少真实数据时退化为团队想象**：必须基于访谈/客服记录/行为数据，不然就是"我们以为的旅程"
- **不会自动告诉你"该改什么"**：Journey Map 是诊断工具不是方案工具，需要配合 HMW 转换成设计挑战
- **常见误用**：把功能流程画成 Journey Map——Journey 是用户视角（"我在比较 3 个产品"），不是功能视角（"用户点击对比按钮"）
- **过度精美陷阱**：很多团队花 2 周画一张超精美 Journey Map 然后挂墙——产物美不美不重要，**洞察导出来了没**才重要

**与其他理论的配合**：
- **上游配合**：JTBD 的 Job Map → 提供 Journey 的阶段骨架；Empathy Map → 喂给每阶段的 Thought/Emotion；用户访谈原话 → 喂给每阶段的 Pain
- **下游配合**：Journey 的 Pain → 喂给 HMW；Moment of Truth → 喂给 Wireframe 重投设计；Journey 阶段 → 喂给 Service Blueprint 的纵向轴
- **互替**：Experience Map 不绑定 Persona 更宏观；Service Blueprint 增加了"前台/后台/支撑系统"维度；User Flow 更细更工程化

**判断要点（融会贯通信号）**：
- 当团队对"用户为什么在 X 步流失"猜不出来——Journey Map 能定位断点
- 当跨触点设计开始"各管各的"——立即用 Journey Map 强制端到端视角

**示例输出片段**：
> **Journey Map（B 端财务专员，月度报表场景，时间跨度 3 天）**
> ┌──────┬──────────────┬──────────────┬──────────────┬──────────────┐
> │ 阶段 │ 收到需求     │ 跨系统取数   │ 制作报表     │ 老板审阅     │
> ├──────┼──────────────┼──────────────┼──────────────┼──────────────┤
> │ 行为 │ 老板 IM 发"看│ ERP/CRM/Excel│ Excel 拼接   │ PPT 发出     │
> │      │ 看 X 角度"   │ 切换 10+ 次  │ 改 vlookup   │ 等回复       │
> │ 想法 │"又要临时改"  │"这数对吗？"  │"别错"        │"求不退回"    │
> │ 情感 │ 焦虑 ↓↓      │ 烦躁 ↓↓↓     │ 紧张 ↓↓      │ 忐忑 →       │
> │ 痛点 │ 上下文丢失   │ 数据校验难   │ 公式易错     │ 反馈周期长   │
> │ 机会 │ 模板提示     │ 一键关联     │ 校验内置     │ 即时预览     │
> └──────┴──────────────┴──────────────┴──────────────┴──────────────┘
> **Moment of Truth**：跨系统取数（占总时间 70% + 情感最低点）→ 这是产品要重投的点

---

## 服务蓝图 / Service Blueprint

**一句话定义**：在 Journey Map 上方加"前台动作/可见线/后台动作/支撑系统/失败点"五层，看清"用户体验"和"内部能力"的对应关系。

**出处**：Lynn Shostack 1984 年在《Harvard Business Review》发表 "Designing Services That Deliver" 提出原始版本，后被 Mary Jo Bitner / Amy Ostrom 等扩展为现代五层结构。

**适用情境（默认场景）**：
- 服务型产品（含人工服务的：客服、外卖、酒店、医疗、教育、金融）
- 需要内部多部门协作交付体验时
- 体验问题根源在后端流程（不是 UI）时——Service Blueprint 让后端问题可见
- 设计与运营/客服/技术团队对齐"谁负责哪段"

**核心步骤**：
1. **横轴 = Journey 阶段**（直接复用第一个理论的 Journey 阶段）
2. **第 1 层 Customer Action**：用户在每阶段做什么
3. **第 2 层 Frontstage Action**：用户能看见的服务方动作（客服回复、推送通知、店员动作）——之间是 "Line of Visibility"（可见线）
4. **第 3 层 Backstage Action**：用户看不见但服务方在做的（订单审核、库存调度、内部审批）
5. **第 4 层 Support Processes / Systems**：支撑后台动作的系统（ERP、CRM、AI 模型、外部 API）
6. **标注 Failure Points 和 Wait Times**：失败发生在哪一层？等待发生在哪个交接？

**局限与不适用**：
- **纯数字产品 / 无人工服务**：不需要那么多层，Journey Map + User Flow 就够
- **覆盖整个公司流程过载**：Blueprint 适合一个服务场景，不适合画整个公司
- **不适用于早期还没确定服务流程时**：Blueprint 是"现状/目标态对比"工具，从 0 设计应该先 Journey 再演化到 Blueprint
- **维护成本高**：流程变动后 Blueprint 不更新就成废纸——必须有 owner
- **常见误用**：把 Frontstage 和 Backstage 混在一起——可见线必须严格区分，这是 Blueprint 的灵魂

**与其他理论的配合**：
- **上游配合**：Journey Map → 直接喂给 Blueprint 的横轴；JTBD 的 Job Executor 区分 → 喂给 Backstage 角色定义
- **下游配合**：Blueprint 的 Failure Points → 喂给 HEART 框架的 Task Success 指标；Backstage 流程 → 喂给内部系统需求 / API 定义
- **互替**：Journey Map 是 Blueprint 的"前台精简版"；Process Map / BPMN 在后台流程上更工程化但缺少用户视角；System Map 在跨系统数据流上更细但缺少时间维度

**判断要点（融会贯通信号）**：
- 当用户痛点反复出现但 UI 改了多次没用——根因可能在 Backstage，需要 Blueprint
- 当客服/运营天天救火但产品不知道——Blueprint 让"前台救火"可见

**示例输出片段**：
> **Service Blueprint（财务报表场景，简化版）**
> 阶段：收到需求 | 跨系统取数 | 制作报表 | 老板审阅
> Customer Action：见 Journey
> ─── Line of Visibility ───
> Frontstage：(无) | 数据连接器 UI | 报表编辑器 UI | 报表预览页
> Backstage：(无) | ERP API 拉取 → 字段映射 → 缓存 | 公式校验 → 数据回写 | 通知服务 → 评论通道
> Support：ERP/CRM/Excel API | 字段映射规则库 | 校验引擎 + 模板库 | IM 集成
> **Failure Points**：①字段映射失败（70% 故障源） ②校验引擎漏报（错误数据未拦截）
> **Wait Times**：API 拉取平均 90s（用户已开始焦虑）→ 这是后端性能优先级

---

## 信息架构 / IA（Information Architecture）

**一句话定义**：把内容/功能按用户认知模型组织成"找得到、看得懂、用得对"的结构。

**出处**：Richard Saul Wurman 1976 年提出 "Information Architect" 概念；Peter Morville & Louis Rosenfeld《Information Architecture for the World Wide Web》（1998，三版续到 2015）是经典教材；Abby Covert《How to Make Sense of Any Mess》（2014）是更现代的入门书。

**适用情境（默认场景）**：
- 多页面/多模块产品的导航和层级设计
- 内容型产品（媒体、电商、知识库、文档站）
- 改版前的"现状信息混乱"诊断
- 多语言/多角色场景下的统一信息结构

**核心步骤**：
1. **盘点 Content Inventory**：现有/规划的内容和功能全清单
2. **做 Card Sorting**（卡片分类）：让真实用户把卡片归类——开放式（用户自创类别）/ 封闭式（在预设类别里分）
3. **设计 Sitemap / Taxonomy**：基于 Card Sorting 结果设计 1-3 级导航和分类
4. **定 Navigation Pattern**：全局导航 / 局部导航 / 上下文链接 / 搜索 / 面包屑——多种导航并存
5. **Tree Testing 验证**：让用户在 IA 上找特定任务，测试成功率和路径——成功率 > 80% 才合格

**局限与不适用**：
- **不适用于强搜索驱动产品**：电商搜索 + 推荐为主时，过度 IA 反而限制；应该让 search & filter 主导
- **不适用于强工作流型产品**：用户路径是固定流程（如报税、医疗诊断），需要 User Flow 而非 IA
- **小产品（<10 页面）不需要复杂 IA**：扁平结构就够
- **个人 IA 偏见**：设计师按自己的认知模型设计 → 用户找不到。必须 Card Sorting 验证
- **常见误用**：把 IA 等同于 Sitemap——IA 还包括分类、标签、导航模式、元数据等多维系统
- **改 IA 是高代价行为**：上线后改 IA 用户重新学习成本高，要预留充分时间验证

**与其他理论的配合**：
- **上游配合**：JTBD 的 Job Executor 区分 → 决定是否多角色多 IA；Journey Map → 提供"用户在每阶段需要什么信息"的输入
- **下游配合**：IA → 喂给 Wireframe 的页面结构；IA → 喂给搜索/标签系统设计
- **互替**：Sitemap 是 IA 的可视化产物之一；Mental Model（Indi Young）在认知层面更深但工具化更弱

**判断要点（融会贯通信号）**：
- 当用户反复说"找不到"——立即 Tree Testing 现有 IA
- 当 PM 频繁问"这功能放哪个 tab"——根本问题是 IA 不清，不是单功能位置

**示例输出片段**：
> **IA 诊断（B 端 AI 报表工具 v0.9）**
> Card Sorting 结果（20 位真实用户）：
> - 用户把"模板"放在"开始"附近（频率 17/20），但当前 IA 把"模板"放在"设置"——这是错配
> - "数据源"和"连接器"被用户认知为同一物（频率 14/20）——但当前 IA 分两个 tab
> **重设计**：导航从 [首页 / 编辑器 / 设置] 改为 [模板 / 数据 / 报表 / 协作]
> **Tree Testing**：新 IA 找"创建一份对比上月的报表"成功率 87%（旧 IA 52%）→ 改版合格

---

## 低保真线框 / Lo-fi Wireframe 设计原则

**一句话定义**：用最低的视觉成本把"页面有什么、什么最重要、怎么走"画出来，专注结构和优先级而非美观。

**出处**：来自 1980s-90s HCI 领域的 "paper prototyping"（Carolyn Snyder《Paper Prototyping》2003 经典教材）；UX 实践中由 Jakob Nielsen 等推广 "Iterative Design" 方法论形成现代 Wireframe 实践。

**适用情境（默认场景）**：
- 任何页面设计的第一步——跳过 wireframe 直接画 hi-fi 是高 risk 高浪费
- 多方案对比阶段（一天画 5 个 wireframe vs 一周画 1 个 hi-fi）
- 与工程/产品对齐"页面要素和优先级"
- 用户测试早期方向（用户能看着粗糙的 wireframe 说出"我会点这里"就达成目的）

**核心步骤（设计原则而非操作流程）**：
1. **F 模式 / Z 模式视线优先**：把最重要的内容放在视线起点（左上）+ 终点（CTA 放右下或底中）
2. **优先级 = 视觉层级**：最重要的元素必须最大、最对比、最居中——一屏只允许 1 个主 CTA
3. **8 秒规则**：用户 8 秒内必须看懂"这是什么页 + 我能做什么 + 主操作在哪"——做不到说明 IA/优先级有问题
4. **减法到底**：每加一个元素都要问"删了它会死吗"——不死就删
5. **Wireframe 不画样式**：用灰阶、占位框、Lorem Ipsum——视觉决策推到后面阶段

**局限与不适用**：
- **不适用于"视觉就是核心价值"的产品**：奢侈品、艺术、品牌站，视觉是核心，Wireframe 跳过得太快会失去判断
- **不适用于复杂交互组件**：动态、状态密集的组件（如富文本编辑器、白板）用 wireframe 表达不完整，需要 storyboard 或 prototype
- **常见误用**：直接用现成的 UI 组件库画 wireframe → 实际是低保真 hi-fi，丢失了"快速对比方案"的价值
- **不能替代可用性测试**：wireframe 能验证结构和优先级，不能验证视觉吸引力或情感反应

**与其他理论的配合**：
- **上游配合**：IA → 喂给 Wireframe 的页面结构和导航；Journey Map 的 Moment of Truth → 喂给 Wireframe 的核心页面优先级；MoSCoW Must → 决定 Wireframe 要包含哪些元素
- **下游配合**：Wireframe → 喂给 Hi-fi Mockup 和 Prototype；Wireframe → 喂给可用性测试脚本
- **互替**：Paper Prototype 是 wireframe 的纸面版本，更便宜更快；Storyboard 在叙事流程上更强；Sketch 是 wireframe 的更粗版本

**判断要点（融会贯通信号）**：
- 当团队开始讨论"用什么色"——立即叫停，先回到 Wireframe 把结构对齐
- 当一屏上有 ≥ 3 个主 CTA 平等竞争——优先级失控

**示例输出片段**：
> **Wireframe 设计原则检查表（财务报表编辑器主页）**
> ✓ 一屏 1 个主 CTA（"开始新报表"按钮，右上）
> ✓ 8 秒规则验证（5 位测试用户都在 8 秒内说出"这是个报表工具，主操作是新建"）
> ✗ 删除决策：原方案在首屏放"教程视频"模块——删除，挪到帮助中心
> ✗ 删除决策：原方案有"近期数据预览"图表——删除，对新用户无意义，对老用户在二级页面
> **结果**：首屏元素从 9 个减到 4 个，可用性测试任务成功率从 71% 升到 92%

---

## 用户故事地图 / User Story Mapping

**一句话定义**：把用户故事按"用户活动→任务→子任务"的二维结构铺开，第三维按 Release 切片，让产品演进路径可视化。

**出处**：Jeff Patton《User Story Mapping》(2014)，作为对"flat backlog（一维 Backlog）丢失叙事性"的反思工具。Patton 提出"地图代替列表"是 Agile/Scrum 中最重要的方法论改进之一。

**适用情境（默认场景）**：
- 把"决策幕"选出的 MoSCoW 列表转成"可发布的 Release 切片"
- 跨团队对齐"我们一起在做什么"——地图比文档可视化效率高 10x
- Sprint Planning 切 Increment 时
- 检查"Walking Skeleton（可演示骨架）"是否完整——MVP 的每个 Activity 必须有至少一个 Task 闭环

**核心步骤**：
1. **最上一行 = User Activities**（用户活动）：用户在一段时间内做的大事，按时间顺序左到右——通常 5-9 个
2. **第二行 = User Tasks**（用户任务）：每个 Activity 下的具体任务——用动词短语
3. **第三行起 = Stories / Sub-tasks**（用户故事）：每个 Task 下的具体故事，按重要性上下排序（上面=必要，下面=锦上添花）
4. **画 Release 切片线**：第一刀切下"Walking Skeleton"（每个 Activity 至少一个 Story），第二刀切 v1.1，第三刀切 v1.2…
5. **核心检验**：第一刀切下的故事集必须能让用户**端到端完成一次完整体验**——能不能这样验证决定 MVP 是否真 MVP

**局限与不适用**：
- **不适用于纯探索期还没确定要做什么时**：Story Mapping 是"已知要做什么、要决定怎么切"的工具
- **不适用于无明确用户旅程的产品**：技术中间件 / 平台型产品，"用户活动"难以定义
- **维护成本不低**：需求变化频繁时地图会撕掉重画——但每次撕掉重画都是有价值的对齐
- **Release 切片是最难的**：第一切应该切薄而完整（Walking Skeleton），但团队总倾向切厚（"做完一个 Activity 的全部 Stories 再发"）——这违背 MVP 精神
- **常见误用**：把 Story Mapping 当 Backlog 替代品挂着 → 不更新就退化成静态文档

**与其他理论的配合**：
- **上游配合**：Journey Map → 提供 User Activities 的骨架；MoSCoW 优先级 → 决定每个 Story 的层级位置；JTBD Job Map → 喂给 Activities/Tasks
- **下游配合**：Story Mapping 的 Release 切片 → 喂给 Sprint Planning；Walking Skeleton → 喂给 MVP 定义和北极星指标设定
- **互替**：Backlog（一维列表）丢失叙事性但更轻量；Epic + Story 树形结构在 JIRA 等工具里更原生但缺少"用户视角横轴"

**判断要点（融会贯通信号）**：
- 当 Backlog 项 > 50 且团队对"先做啥"没共识——Story Mapping 立即上
- 当 MVP 被切成"做完一个完整 Activity 再发"——Walking Skeleton 没切对，重切

**示例输出片段**：
> **Story Map（B 端 AI 报表工具 MVP）**
> Activities（横轴）：①接入数据 ②建报表 ③校验 ④分享老板 ⑤复用迭代
> Tasks（每 Activity 下）：①.1 连 ERP / ①.2 连 CRM / ②.1 自然语言生成 / ②.2 选模板 / ③.1 公式校验 / ③.2 数据完整性 / ④.1 PDF 导出 / ④.2 IM 分享 / ⑤.1 保存模板 / ⑤.2 协作评论
> **Release 1（Walking Skeleton, 70w 工作量）**：①.1（仅 1 个 ERP）+ ②.1 + ②.2（5 个模板）+ ③.1 + ④.1 + ⑤.1
> **Release 2**：①.2（CRM）+ ③.2 + ④.2
> **Release 3**：⑤.2（协作） + 更多 ERP
> **核验**：Release 1 能让用户从"接入→建→校验→分享→存模板"端到端走通——✓ 是真 MVP

---

## 第四幕末决策提示

- **如果情境是"复杂跨触点服务"**：Journey Map → Service Blueprint → IA → Wireframe，缺一不可。
- **如果情境是"纯数字产品 / 单一触点"**：JTBD/Journey → IA → Wireframe → Story Mapping 串起 Release。
- **如果情境是"已知功能要快速落地"**：跳过 Journey，直接 IA + Wireframe + Story Mapping 切 Release。
- **如果情境是"现有产品体验差但说不清在哪"**：Journey Map（现状 As-is）+ Service Blueprint（找 Failure Points），改造方案再叠目标态（To-be）。
- **核心警告**：**没有时间维度先行的设计都是"功能墓地"**——直接画 Wireframe 不画 Journey 会得出"功能堆砌的产品"。本幕产物的硬指标是"①一张 Journey Map ②一张 IA Sitemap ③一组关键页 Wireframe ④一张 Story Map 含 Walking Skeleton"。
