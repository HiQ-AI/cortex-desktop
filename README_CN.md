<p align="center">
  <img src="icon.png" width="80" alt="HiQ Cortex" />
</p>

<h1 align="center">HiQ Cortex</h1>

<p align="center">
  <strong>AI 驱动的 LCA 数据工作台</strong><br/>
  搜索碳足迹数据集 · 匹配 BOM 背景数据 · 本地分析，隐私无忧
</p>

<p align="center">
  <a href="https://github.com/HiQ-AI/cortex-desktop/releases/latest"><img src="https://img.shields.io/github/v/release/HiQ-AI/cortex-desktop?style=flat-square&label=下载" alt="Latest Release" /></a>
  <a href="https://www.hiqlcd.com"><img src="https://img.shields.io/badge/HiQLCD-平台-orange?style=flat-square" alt="HiQLCD" /></a>
  <img src="https://img.shields.io/badge/平台-macOS%20%7C%20Windows%20%7C%20Linux-lightgrey?style=flat-square" alt="Platform" />
</p>

<p align="center">
  中文 · <a href="./README.md">English</a>
</p>

---

你有一份 31 种材料的 BOM 表。每个材料都需要碳足迹排放因子。你打开 SimaPro，搜"碳钢"——200 条结果。选哪个？换 openLCA 试试，不同的数据库，不同的命名。翻翻同事去年整理的表格。三个小时过去了，你匹配了 8 个材料。

**Cortex 只要 3 分钟。** 用自然语言告诉它你需要什么。它搜索 12 个数据库，不确定时会问你，验证每个结果，然后递给你一份标好颜色的 Excel，附带专业点评。

---

## 快速上手

1. **下载安装** — 在下方选择你的平台下载
2. **登录** — 使用你的 HiQ 账号（没有的话可以申请试用）
3. **选数据库** — 在输入框底部选择要搜索的 LCA 数据库
4. **开始提问** — 输入"查硅钢的碳足迹数据"或"帮我把这份 BOM 匹配背景数据"

就这么简单。Cortex 会自动加载搜索技能、提出澄清问题、验证搜索结果。

---

## 两种模式，一个应用

### Chat — 随时提问，即时解答
和一位专业的 AI 碳咨询师对话。跨库搜索、对比数据源、解释方法论差异——就像身边随时有一位资深 LCA 分析师。

### Cowork — AI 操作你的本地文件
让 Cortex 访问你电脑上的文件，处理复杂的多步骤任务：解析 BOM 表、匹配排放因子、执行计算、生成图表、导出报告。Cortex 会自主规划任务、分配子任务、并行搜索——像一位带着全套工具的资深顾问，每一步都让你看得到。

**Chat 是问同事一个问题，Cowork 是和同事坐下来一起出活儿。**

---

## Cortex 做什么（不做什么）

Cortex **不是** LCA 建模工具。它不替代 SimaPro、GaBi 或 openLCA——它和这些工具配合使用。

| Cortex 做的事 | LCA 工具做的事 |
|---|---|
| 搜索和匹配背景排放因子 | 产品系统建模 |
| 解析你的 BOM 并推荐数据集 | 碳足迹核算 |
| 生成 LCA 工具可导入的文件 | 影响评价 (LCIA) |
| 分析和解读 LCA 工具的输出结果 | 分配与系统边界设定 |
| 跨 12 个数据库对比数据 | 敏感性与不确定性分析 |

**Cortex 是数据准备助手，让你的 LCA 工具跑得更快。** 它处理最繁琐的部分——找到对的数据——让你专注于分析本身。

---

## 它怎么工作

### 12 个数据库一站式搜索

| 数据库 | 覆盖范围 |
|---|---|
| HiQLCD | 中国本土，25+ 行业 |
| Ecoinvent | 全球最全面 |
| EF | 欧盟产品环境足迹 |
| 天工 (TianGong) | 中国国家级 LCA 数据库 |
| CarbonMinds | 化工与塑料 |
| Agri-footprint | 农业与食品 |
| WorldSteel | 钢铁行业 |
| + 5 个 | USDA, EXIOBASE, OZLCI, NEEDS, ELCD |

> 总计 **100 万+** 条排放因子数据。搜索 1-3 秒返回结果，附带 GWP 值、数据质量评分和数据集详情链接。

### 专业搜索技能
Cortex 不只是关键词搜索。它运用专业的 LCA 搜索策略：
- **材料拆解** — "茶叶包装盒"会被拆成马口铁 + 纸板 + 塑料内衬，分别搜索
- **双语覆盖** — 中英文同义词同时搜索，覆盖更多数据库
- **先问再搜** — "查钢的数据"会触发追问："什么钢？碳钢、不锈钢、硅钢还是合金钢？"
- **两阶段验证** — 先找候选数据集，核实详情后才展示给你
- **专业点评** — 解释每个数据集的工艺适配性、地区代表性和数据质量

### 项目管理
- 创建项目，配置专属文件夹、指令和持久记忆
- AI 记住每个项目中的讨论内容，跨会话延续上下文
- 设置项目级指令（如"这个项目使用 EF 3.1 数据库"或"回复用英文"）

### 人机协作
当 AI 需要你的判断时——材料名称模糊、多个候选数据集、缺少参数——它会停下来用可点选的按钮问你，而不是瞎猜。

### 全程透明
每一次工具调用、搜索关键词、中间步骤都以内联卡片的形式实时出现在对话中。你能看到 AI 在搜什么、用了什么参数、每步花了多长时间。

---

## 隐私：AI 来找你的数据

你的文件始终不离开你的设备。AI 在云端推理，但在你的电脑上读写文件。Cowork 的对话记录存储在本地，不在任何服务器上。

> **AI 来找你的数据，而不是把数据送给 AI。**

---

## 下载

| 平台 | 下载 |
|---|---|
| **macOS** (Apple Silicon) | [Cortex.dmg](https://github.com/HiQ-AI/cortex-desktop/releases/latest) |
| **Windows** (x64) | [Cortex-Setup.exe](https://github.com/HiQ-AI/cortex-desktop/releases/latest) |
| **Linux** (x64) | [Cortex.AppImage](https://github.com/HiQ-AI/cortex-desktop/releases/latest) |

内置自动更新——有新版本时会自动通知。

> **macOS 首次打开**：右键点击应用 → 选择「打开」→ 在弹窗中点击「打开」。只需操作一次。

> **注意**：HiQ Cortex 目前处于内测阶段。如需试用，请[发送邮件](mailto:info@hiqlcd.com)或[提交 Issue](https://github.com/HiQ-AI/cortex-desktop/issues/new)。

---

## 使用场景

### LCA 分析师
- "查 304 不锈钢在 Ecoinvent 3.12 里的排放因子" → 3 秒内返回 5 个验证过的数据集，GWP 范围 1.8–3.2 kg CO₂e/kg
- "帮我把这份 BOM 匹配背景数据" → 上传 31 种材料的 Excel，返回标好颜色的结果文件，附带每个改动的原因
- "对比 PET 在 HiQLCD 和 Ecoinvent 里的 GWP" → 逐项对比，附地区适用性分析

### ESG 与可持续发展团队
- 批量匹配 BOM 材料的排放因子，用于 Scope 3 报告——31 种材料在一次对话内完成
- 导出结构化结果，可直接导入 SimaPro、GaBi 或 openLCA
- 生成带数据源选择理由的对比报告

### 供应链管理者
- 上传供应商 BOM，获取排放因子推荐和专业点评
- 在中国、欧洲、全球平均数据之间评估和对比
- 生成非 LCA 专业人员也能看懂的分析报告

---

## 产品路线图

### 已上线
- [x] 多数据库搜索（12 个数据库，100 万+ 条记录）
- [x] AI 材料分析与数据集推荐
- [x] 数据源选择与过滤
- [x] BOM 上传与批量并行匹配
- [x] 本地文件分析与 Python 执行环境
- [x] AI 自主任务规划与子任务分配
- [x] 人机协作式交互确认
- [x] 多轮对话与上下文记忆
- [x] 项目管理（文件夹、指令、持久记忆）
- [x] 会话管理（星标、归档、重命名、搜索）
- [x] 内置 LCA 搜索技能（双语关键词策略）
- [x] 实时工具执行可视化（对话内联展示）
- [x] 代码语法高亮
- [x] 导出 CSV / Excel
- [x] 跨平台：macOS、Windows、Linux
- [x] 自动更新
- [x] 中英文双语界面
- [x] 本地优先的隐私架构

### 即将推出
- [ ] 数据可视化与对比图表
- [ ] PDF 报告生成（ISO 14067 格式）
- [ ] LCA 工具导入文件生成（SimaPro CSV、openLCA JSON-LD）
- [ ] 团队协作与共享工作空间
- [ ] 离线模式与本地数据缓存
- [ ] 图像附件支持（可视化分析）

---

## 关于海科数据

[海科数据 (HiQ)](https://www.hiqlcd.com) 是一家总部位于上海的生命周期评估数据与服务公司。由 LCA 专家和工程师团队创立，致力于为中国——全球最大的制造经济体——提供高质量、区域特异性的环境数据。

- **100+** 家企业客户
- **18+** 家战略合作伙伴（清华大学、同济大学、复旦大学等）
- **ISO 14040 / 14044 / 14067** 合规数据
- **30+** 人团队

---

## 反馈与社区

- **Bug 反馈和功能建议** — [提交 Issue](https://github.com/HiQ-AI/cortex-desktop/issues/new)
- **问题与讨论** — [参与讨论](https://github.com/HiQ-AI/cortex-desktop/discussions)
- **商务合作** — [info@hiqlcd.com](mailto:info@hiqlcd.com)

---

## 许可证

Copyright © 2026 海科（上海）数据科技有限公司。保留所有权利。

本软件为专有软件，未经授权禁止复制、修改、分发或使用。

---

<p align="center">
  <sub>由 <a href="https://www.hiqlcd.com">HiQ AI</a> 在上海用 ❤️ 打造</sub>
</p>
