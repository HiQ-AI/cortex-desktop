## v0.0.38 — 蜗牛打通 openLCA 了 🔗

这是一个里程碑。

以前：Cortex 帮你搜数据，搜完你自己打开 openLCA，手动导入，手动建模，手动跑计算。中间断了一刀。

现在：搜完数据，直接导入 openLCA，自动建产品系统，选个 LCIA 方法，一键算——结果回到对话里。

**搜数据 → 导入 → 建模 → 计算 → 出结果，全在一个对话里。**

### 🔗 openLCA Bridge
- 连接本地 openLCA 2.x（通过 IPC）
- 导入 JSON-LD（从 Cortex 搜索结果直接导入）
- 自动创建产品系统
- 运行 LCIA 计算（ReCiPe、CML、EF 3.0、IPCC GWP…）
- 热点分析（哪个流程贡献最大）
- 所有计算在你本地跑，数据不出电脑

### ⚠️ 免责声明

说实话，这个功能我还没来得及亲自测。

从周五晚上开始通宵迭代，三天肝了 20 个版本（0.0.19 → 0.0.38）——本地 AI 引擎重写、项目管理、AI 记忆系统、流式输出优化、技能中心、云端技能市场、自定义技能导入、文件上传、ILCD/JSON-LD 格式互转、openLCA 打通……全是一个人 + 一只蜗牛干的。

所以测试的光荣使命，就交给各位尊贵的内测用户了。我要先洗漱一下继续当牛做马了。

毕竟——**不能我一个人卷，你们也得动起来啊。**

🏆 **现面向全宇宙招募优秀内测用户**

- 找到 3 个 bug 并提 issue → 请你喝杯星巴克 ☕（仅限中杯，大杯另算）
- 找到 1 个让蜗牛原地去世的操作 → 你的名字会出现在下个版本的致谢里 🏅
- 用 Cortex 跑通一次 openLCA 全流程（搜数据→导入→建模→出结果） → 授予「蜗牛驯兽师」称号，通报表扬
- 在群里发一条超过 50 字的走心体验 → 解锁成就「蜗牛的第一个朋友」，优先获得后续新功能内测资格

遇到 bug 请温柔地提 [issue](https://github.com/HiQ-AI/cortex-desktop/issues/new)。遇到惊喜请大声地告诉我。

### 前提
- openLCA 2.x 已安装并运行
- 启动 IPC 服务器：Tools > Developer Tools > IPC Server

蜗牛打通了 openLCA。至于通了之后好不好使——你们来告诉我。🐌

### 平台
- **macOS** — arm64 | **Windows** — x64 | **Linux** — x64

---

This is a milestone.

Before: Cortex finds data, then you manually import, build, calculate in openLCA. Gap in the middle.

Now: search → import → model → calculate → results. One conversation. No tab-switching.

### 🔗 openLCA Bridge
- Connects to local openLCA 2.x via IPC
- Imports JSON-LD packages from Cortex search
- Auto-creates product systems
- Runs LCIA (ReCiPe, CML, EF 3.0, IPCC GWP…)
- Hotspot analysis
- Everything runs locally

### ⚠️ Honest Disclaimer

I haven't actually tested this one myself yet.

Three days since Friday night, 20 versions (0.0.19 → 0.0.38) — AI engine rewrite, project management, AI memory, streaming optimization, Skills Center, Marketplace, custom skill import, file upload, ILCD/JSON-LD conversion, openLCA bridge — it's been just me and a snail.

So the glorious duty of testing falls upon you, our valued beta testers.

**I can't be the only one grinding here. Your turn.**

Found a bug? File an [issue](https://github.com/HiQ-AI/cortex-desktop/issues/new). Found something cool? Let me know.

### Prerequisites
- openLCA 2.x installed and running
- IPC server started: Tools > Developer Tools > IPC Server

The snail connected to openLCA. Whether the connection is any good — that's for you to find out. 🐌

### Platforms
- **macOS** — arm64 | **Windows** — x64 | **Linux** — x64
