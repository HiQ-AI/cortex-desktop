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

## HiQ Cortex 是什么？

HiQ Cortex 是一款面向生命周期评估（LCA）专业人士的桌面 AI 助手。它接入了 **12 个主流 LCA 数据库**，覆盖 **100 万+ 条排放因子数据**，帮你快速检索碳足迹数据、匹配 BOM 背景数据、分析和导出报告——全部通过自然语言完成。

由 [海科数据 (HiQ)](https://www.hiqlcd.com) 开发，一家总部在上海的 LCA 数据服务公司，服务于汽车、电子、包装、建筑、化工等行业的 100+ 家企业客户。

---

## 两种模式，一个应用

### Chat — 随时提问，即时解答
和一位专业的 AI 碳咨询师对话。跨库搜索、对比数据源、解释方法论差异——就像身边随时有一位资深 LCA 分析师。

### Cowork — AI 操作你的本地文件
让 Cortex 访问你电脑上的文件，处理复杂的多步骤任务：解析 BOM 表、匹配排放因子、执行计算、生成图表、导出报告。

**简单说：Chat 是问同事一个问题，Cowork 是和同事坐下来一起出活儿。**

---

## 隐私架构：云端思考，本地执行

Cortex Cowork 将 AI 推理和数据处理严格分离：

|  | 云端 | 你的电脑 |
|---|---|---|
| AI 推理与规划 | ✅ | |
| 文件读取 / 写入 / 搜索 | | ✅ |
| Python / Shell 执行 | | ✅ |
| LCA 数据库搜索 | ✅ | |
| 工作目录与文件存储 | | ✅ |
| Cowork 对话记录 | | ✅ |

**你的文件始终不离开你的设备。** AI 通过运行在你电脑上的本地 Agent 访问文件，文件内容不会上传到任何服务器。Cowork 的对话记录存储在本地数据库中，不在云端。

> AI 来找你的数据，而不是把数据送给 AI。

---

## 核心能力

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

> 总计：**100 万+** 条 LCA 数据记录

### AI 碳咨询师
- 理解你的产品，拆解为材料清单
- 没有精确匹配时，推荐合适的替代数据集
- 解释数据质量、地区代表性、系统模型差异

### 本地文件分析（Cowork）
- 上传或选择本地 BOM 文件（Excel、CSV、PDF、Word）
- AI 在本地读取文件内容，规划分析步骤并执行
- 内置 Python 环境，支持数据处理、可视化、格式转换
- 每个任务拥有独立的隔离工作目录

### 人机协作（HITL）
当 AI 需要你的判断时——搜索条件模糊、多个候选数据集、缺少参数——它会停下来直接问你，而不是瞎猜。

### 全程透明
每一次工具调用、搜索关键词、中间步骤都实时可见。你始终知道 AI 在做什么、为什么这样做。

---

## 下载

| 平台 | 下载 |
|---|---|
| **macOS** (Intel + Apple Silicon) | [Cortex.dmg](https://github.com/HiQ-AI/cortex-desktop/releases/latest) |
| **Windows** (x64) | [Cortex-Setup.exe](https://github.com/HiQ-AI/cortex-desktop/releases/latest) |
| **Windows** (ARM64) | [Cortex-Setup-arm64.exe](https://github.com/HiQ-AI/cortex-desktop/releases/latest) |
| **Linux** (x64 / ARM64) | [Cortex.AppImage](https://github.com/HiQ-AI/cortex-desktop/releases/latest) |

内置自动更新——有新版本时会自动通知。

> **注意**：HiQ Cortex 目前处于内测阶段，暂未开放公开注册。如需试用，请[发送邮件](mailto:info@hiqlcd.com)或[提交 Issue](https://github.com/HiQ-AI/cortex-desktop/issues/new)。

---

## 使用场景

### LCA 分析师
- 「查 304 不锈钢在 Ecoinvent 3.12 里的排放因子」→ 指定数据库精准搜索
- 「帮我把这份 BOM 匹配背景数据」→ 上传 Excel，自动逐行匹配排放因子
- 「对比 PET 在 HiQLCD 和 Ecoinvent 里的 GWP 数据」→ 跨库对比

### ESG 与可持续发展团队
- 批量匹配 BOM 材料的排放因子，用于 Scope 3 报告
- 查找特定地区（中国、全球、欧洲）的数据，用于供应链评估
- 导出结构化结果，导入 LCA 软件继续分析

### 供应链管理者
- 用真实数据评估供应商材料的环境影响
- 上传供应商 BOM 获取排放因子推荐
- 生成跨材料、跨地区的对比报告

---

## 产品路线图

### 已上线
- [x] 多数据库搜索（12 个数据库，100 万+ 条记录）
- [x] AI 材料分析与数据集推荐
- [x] 数据源选择与版本管理
- [x] BOM 上传与自动材料匹配
- [x] 本地文件分析与 Python 执行环境
- [x] 人机协作式交互确认
- [x] 多轮对话与上下文记忆
- [x] 数据集详情查看（完整元数据）
- [x] 导出 CSV / Excel
- [x] 跨平台：macOS、Windows、Linux
- [x] 自动更新
- [x] 中英文双语界面
- [x] 本地优先的隐私架构

### 即将推出
- [ ] 项目管理（按产品/客户组织工作）
- [ ] BOM 批量匹配与并发搜索
- [ ] 数据可视化与对比图表
- [ ] PDF 报告生成（ISO 14067 格式）
- [ ] 团队协作与共享工作空间
- [ ] 离线模式与本地数据缓存

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
