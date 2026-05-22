# product-designer · Claude Code Skill

> 把一个粗糙的产品想法蒸馏成大师级 0→1 产品设计稿。

一个 [Claude Code](https://claude.com/claude-code) skill——给 Claude 装上**十年经验产品设计师的思维内核**。

输入：你脑中的一个想法（明确 / 半模糊 / 完全模糊 都行）。
输出：一份**典雅风单文件 HTML 产品设计稿**（≈ 1500-3000 行，可离线/可打印/可发同事/可放飞书&Notion）。

---

## 🧬 为什么不是又一个"AI 帮你写 PRD"的工具

主流"AI 帮写 PRD"的问题是 —— **机械堆理论 + 没有产品本身**。

我们做了三件不一样的事：

1. **24 种理论融会贯通，而非生搬硬套** —— JTBD/Lean Canvas/Kano/RICE/HEART/北极星/AARRR/用户旅程地图/服务蓝图... 不是清单堆砌，而是根据想法情境**调度 2-3 个最合适的**，并在附录里诚实解释「为什么用它们，不用其他」。

2. **产品本身是核心交付物** —— 不是只有思考过程。**产品形态决策 + 功能清单详表 + 至少 1 个核心界面 wireframe + 用户流程图** 是 4 件套硬约束。读者看完应能在脑里复现「这个产品长什么样、第一屏是什么、3 个核心功能是什么、用户怎么从触发走到完成」。

3. **敢做减法** —— 完全模糊型想法不强行填满 5 幕；明确型不画用不到的 Kano 矩阵。**一份只把 2-3 幕做深的设计稿，胜过 5 幕都浅尝辄止的稿子。**

---

## 🚀 安装

### 方式 1：git clone（推荐，方便后续 pull 更新）

```bash
git clone https://github.com/daizhouchen/claude-product-designer.git ~/.claude/skills/product-designer
```

### 方式 2：直接下载 .skill 包

下载 [Releases](https://github.com/daizhouchen/claude-product-designer/releases) 里的 `product-designer-v2.skill` 文件，按 Claude Code skill 安装方式装入。

安装后，在 Claude Code 任意 session 里直接说话即可自动触发，**不需要 import 也不需要手动启用**。

---

## 💬 触发场景

只要你说类似的话，skill 就会自动触发：

| 触发关键词 | 例子 |
|------------|------|
| "我想做个 XX" | 我想做个帮独立开发者验证 idea 的工具 |
| "帮我设计一个 XX" | 帮我设计一个 B 端客户健康度仪表盘 |
| "做个 PRD" / "产品立项" | 给我做份《晚归陪伴 app》的 PRD |
| "0→1 产品" / "MVP" | 我有个 0→1 的产品想法想立项 |
| "做个 app / 小工具" | 我想做个小工具帮上班族下班放松 |
| "产品概念" / "新产品想法" | 这个产品概念你帮我做份设计稿 |

**没有触发？** 直接说 `用 product-designer skill 帮我做...` 即可显式调用。

---

## 🎬 五幕视角（不是流程，是工具箱）

```
┌──────┬──────────────────┬────────────────────────────────────┐
│ 一幕 │ 探索 Discover    │ 这是个什么问题？用户真的需要吗？   │
│ 二幕 │ 定义 Define      │ 我们到底要解决什么？怎么定义价值？ │
│ 三幕 │ 决策 Decide      │ MVP 边界划在哪？v1 功能清单是什么？│
│ 四幕 │ 产品 + 旅程       │ 产品长什么样？用户怎么走到价值？   │
│      │ Design           │ （产品形态 + wireframe + 用户流程）│
│ 五幕 │ 度量 Deliver     │ 怎么知道做对了？指标怎么定？       │
└──────┴──────────────────┴────────────────────────────────────┘
```

skill 会根据你想法的清晰度自动决定**重点做哪 2-3 幕**：
- 🔴 **完全模糊** → 重一幕、二幕（挖真实任务，定义清楚机会）
- 🟡 **半模糊** → 重一幕、三幕、五幕（补全用户、果断划 MVP、定指标）
- 🟢 **明确** → 重三幕、四幕、五幕（直接划范围、画产品、定指标）

---

## 📊 Benchmark（v2.0）

3 个梯度场景（B 端明确 / 独立开发者半模糊 / 上班族晚睡完全模糊），对比 with-skill vs baseline：

| 指标 | With Skill | Without Skill | Delta |
|------|-----------|---------------|-------|
| **Pass Rate** | **100%** ± 0% | 40% ± 9% | **+60%** |
| 产物厚度 | 1062-2166 行 | 397-761 行 | +2.7× |
| SVG 可视化 | 2-8 个 inline | 0-3 个 | 含 8 种预制模板 |
| 4 件套覆盖 | 11/12 | 0/12 | 痛点核心治愈 |

---

## 📦 内含的资产

```
product-designer/
├── SKILL.md                        ← 230 行主文档（五幕原则 + 调度器 + 反 slop 12 条）
├── references/theories/            ← 24 张理论卡片（5 个 md / 1204 行）
│   ├── discover.md                 ← JTBD / 5 Why / 反向假设 / Empathy Map / 访谈剧本
│   ├── define.md                   ← Lean Canvas / VPC / HMW / 问题陈述
│   ├── decide.md                   ← Kano / RICE / MoSCoW / 北极星 / ICE
│   ├── design.md                   ← 用户旅程 / 服务蓝图 / IA / 线框 / 故事地图
│   └── deliver.md                  ← HEART / AARRR / 反指标 / 假设矩阵 / 风险登记
├── assets/
│   ├── template.html               ← 1928 行典雅风 HTML 模板（362 个 {{占位符}}）
│   └── svg/                        ← 8 个预制 SVG（含字数硬约束防 overlap）
│       ├── journey-map.svg
│       ├── kano-matrix.svg
│       ├── aarrr-funnel.svg
│       ├── ia-tree.svg
│       ├── north-star-card.svg
│       ├── mobile-wireframe.svg    ← 手机端 3 屏并排线框
│       ├── user-flow-diagram.svg   ← 用户核心流程图
│       └── feature-matrix.svg      ← 功能 v1/v1.1/v1.2 矩阵
└── evals/evals.json                ← 3 个梯度测试场景 + 12 assertions
```

---

## 🎨 设计哲学

- **视觉**：典雅风（米黄底 #F5F0E8 / 深棕墨字 #3A2E26 / 朱砂 #8B3A3A / 松针绿 / 淡金 / 天青）。绝对不用渐变、毛玻璃、emoji 满天飞。
- **字体**：思源宋体 + 楷体 + Crimson Pro 三轨字体系统。
- **章节**：每幕用「剧场幕」标识（Act I-V），上下横线包夹，西文 eyebrow + 中文楷体标题 + 灰字提要。
- **可信度**：三层信任标注 ✅ VERIFIED / 🟡 INFERRED / 🔴 CRITICAL —— 推测必须明确标注，不可冒充事实。

---

## 🤝 致谢

- 受 [Claude Code skill 系统](https://docs.claude.com/en/docs/claude-code/skills) 启发
- 视觉风格借鉴 [book-distiller](https://github.com/zhouwong/book-distiller) 的典雅风范式
- 理论组合参考 Marty Cagan / 俞军 / Julie Zhuo / Ash Maurya / Christensen 的产品设计思想

---

## 📄 License

MIT —— 拿去用，改了 PR 欢迎。
