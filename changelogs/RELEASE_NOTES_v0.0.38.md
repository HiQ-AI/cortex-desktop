## v0.0.38 — 蜗牛打通 openLCA 了 🔗

这是一个里程碑。

以前：Cortex 帮你搜数据，搜完你得自己打开 openLCA，手动导入，手动建模，手动跑计算。

现在：Cortex 搜完数据，直接导入 openLCA，自动建产品系统，选个方法，一键跑 LCIA——结果直接回到对话里。

**搜数据 → 导入 → 建模 → 计算 → 出结果，全在一个对话里完成。**

### 🔗 openLCA Bridge
- 连接本地 openLCA 2.x（通过 IPC）
- 导入 JSON-LD 数据包（从 Cortex 搜索结果直接导入）
- 自动创建产品系统（auto-link 上游流程）
- 运行 LCIA 计算（ReCiPe、CML、EF 3.0、IPCC GWP 等）
- 热点分析（哪个流程贡献最大）
- 所有计算在你本地运行，数据不出电脑

### 前提
- 需要安装 openLCA 2.x
- 需要启动 IPC 服务器（Tools > Developer Tools > IPC Server）

蜗牛打通了 openLCA。从搜数据到出结果，一条路走到底。🐌

### 平台
- **macOS** — arm64 | **Windows** — x64 | **Linux** — x64

---

This is a milestone.

Before: Cortex finds the data, then you manually import into openLCA, manually build models, manually run calculations.

Now: Cortex finds data, imports it into openLCA, builds the product system, runs LCIA — results come back to the conversation.

**Search → Import → Model → Calculate → Results. One conversation.**

### 🔗 openLCA Bridge
- Connects to local openLCA 2.x via IPC
- Imports JSON-LD packages (directly from Cortex search results)
- Auto-creates product systems (auto-links upstream processes)
- Runs LCIA calculations (ReCiPe, CML, EF 3.0, IPCC GWP, etc.)
- Hotspot analysis (which process contributes most)
- All calculations run locally — data never leaves your machine

### Prerequisites
- openLCA 2.x installed
- IPC server running (Tools > Developer Tools > IPC Server)

The snail connected to openLCA. Search to results, one straight line. 🐌

### Platforms
- **macOS** — arm64 | **Windows** — x64 | **Linux** — x64
