<p align="center">
  <img src="icon.png" width="80" alt="HiQ Cortex" />
</p>

<h1 align="center">HiQ Cortex</h1>

<p align="center">
  <strong>AI-Powered LCA Data Workbench</strong><br/>
  Search carbon footprint datasets · Match BOM background data · Analyze locally with full privacy
</p>

<p align="center">
  <a href="https://github.com/HiQ-AI/cortex-desktop/releases/latest"><img src="https://img.shields.io/github/v/release/HiQ-AI/cortex-desktop?style=flat-square&label=Download" alt="Latest Release" /></a>
  <a href="https://www.hiqlcd.com"><img src="https://img.shields.io/badge/HiQLCD-Platform-orange?style=flat-square" alt="HiQLCD" /></a>
  <img src="https://img.shields.io/badge/platform-macOS%20%7C%20Windows%20%7C%20Linux-lightgrey?style=flat-square" alt="Platform" />
</p>

<p align="center">
  <a href="./README_CN.md">中文</a> · English
</p>

---

## What is HiQ Cortex?

HiQ Cortex is a desktop AI assistant for Life Cycle Assessment (LCA) professionals. It connects to **12 major LCA databases** with **1,000,000+ emission factor records** and helps you find the right carbon footprint data, match background datasets for your BOM, and analyze data — all through natural language.

Built by [HiQ](https://www.hiqlcd.com), a Shanghai-based LCA data company serving 100+ enterprise clients across automotive, electronics, packaging, construction, and chemical industries.

---

## Two Modes, One App

### Chat — Ask Anything About LCA
Quick Q&A with a professional AI carbon consultant. Search across all databases, compare data sources, get explanations on methodology — like having a senior LCA analyst on standby.

### Cowork — AI Works With Your Local Files
Give Cortex access to your local files and let it handle complex multi-step tasks: parse BOMs, match emission factors, run calculations, generate charts, export reports.

**Think of it as the difference between asking a colleague a question (Chat) versus sitting down and working together on a deliverable (Cowork).**

---

## Privacy Architecture: Think in the Cloud, Act Locally

Cortex Cowork is designed with a clear separation between AI reasoning and data handling:

|  | Cloud | Your Computer |
|---|---|---|
| AI Reasoning & Planning | ✅ | |
| File Read / Write / Search | | ✅ |
| Python / Shell Execution | | ✅ |
| LCA Database Search | ✅ | |
| Workspace & Files Storage | | ✅ |
| Conversation History (Cowork) | | ✅ |

**Your files never leave your device.** AI accesses them through a local Agent running on your machine. File contents are not uploaded to any server. Cowork conversation history is stored in a local database on your computer, not in the cloud.

> AI comes to your data. Your data doesn't go to AI.

---

## Key Features

### Search Across 12 Databases

| Database | Coverage |
|---|---|
| HiQLCD | China-focused, 25+ industries |
| Ecoinvent | Global, most comprehensive |
| EF | EU Product Environmental Footprint |
| TianGong | Chinese national LCA database |
| CarbonMinds | Chemicals & plastics |
| Agri-footprint | Agriculture & food |
| WorldSteel | Steel industry |
| + 5 more | USDA, EXIOBASE, OZLCI, NEEDS, ELCD |

> Total: **1,000,000+** LCA data records across all databases

### AI-Powered LCA Consultant
- Understands your product and breaks it down into materials
- Recommends appropriate proxy datasets when exact matches aren't available
- Explains data quality, regional representativeness, and system model differences

### Local File Analysis (Cowork)
- Upload or select local BOM files (Excel, CSV, PDF, Word)
- AI reads file contents locally, plans analysis steps, and executes
- Built-in Python environment for data processing, visualization, and export
- Each task gets its own isolated workspace directory

### Human-in-the-Loop
When the AI needs your judgment — ambiguous search terms, multiple matching datasets, missing parameters — it pauses and asks you directly instead of guessing.

### Full Transparency
Every tool call, search query, and intermediate step is visible in real-time. You always know what the AI is doing and why.

---

## Download

| Platform | Download |
|---|---|
| **macOS** (Intel + Apple Silicon) | [Cortex.dmg](https://github.com/HiQ-AI/cortex-desktop/releases/latest) |
| **Windows** (x64) | [Cortex-Setup.exe](https://github.com/HiQ-AI/cortex-desktop/releases/latest) |
| **Windows** (ARM64) | [Cortex-Setup-arm64.exe](https://github.com/HiQ-AI/cortex-desktop/releases/latest) |
| **Linux** (x64 / ARM64) | [Cortex.AppImage](https://github.com/HiQ-AI/cortex-desktop/releases/latest) |

Auto-update is built in — you'll be notified when new versions are available.

> **Note**: HiQ Cortex is currently in closed beta. To request access, please [email us](mailto:info@hiqlcd.com) or [open an issue](https://github.com/HiQ-AI/cortex-desktop/issues/new).

---

## Use Cases

### For LCA Analysts
- "Find emission factor for 304 stainless steel in Ecoinvent 3.12" → Precision search with data source control
- "Match my BOM with background datasets" → Upload Excel, auto-match materials to emission factors
- "Compare GWP data for PET across HiQLCD and Ecoinvent" → Cross-database comparison

### For ESG & Sustainability Teams
- Batch-match BOM materials to emission factors for Scope 3 reporting
- Find region-specific data (China, Global, Europe) for supply chain assessments
- Export structured results for integration with LCA software

### For Supply Chain Managers
- Evaluate supplier materials' environmental impact with real data
- Upload supplier BOMs and get emission factor recommendations
- Generate comparison reports across materials and regions

---

## Roadmap

### Available Now
- [x] Multi-database search (12 databases, 1M+ records)
- [x] AI material analysis and dataset recommendations
- [x] Data source selection and version management
- [x] BOM upload and automated material matching
- [x] Local file analysis with Python environment
- [x] Human-in-the-loop interactive clarification
- [x] Multi-turn conversation with context memory
- [x] Dataset detail view with full metadata
- [x] Export to CSV / Excel
- [x] Cross-platform: macOS, Windows, Linux
- [x] Auto-update
- [x] Chinese + English bilingual interface
- [x] Local-first privacy architecture

### Coming Soon
- [ ] Project management (organize work by product/client)
- [ ] BOM batch matching with concurrent search
- [ ] Data visualization and comparison charts
- [ ] PDF report generation (ISO 14067 format)
- [ ] Team collaboration and shared workspaces
- [ ] Offline mode with local data cache

---

## About HiQ

[HiQ (海科数据)](https://www.hiqlcd.com) is a Shanghai-based company specializing in Life Cycle Assessment data and services. Founded by a team of LCA experts and engineers, HiQ addresses the critical need for high-quality, region-specific environmental data in China — the world's largest manufacturing economy.

- **100+** enterprise clients
- **18+** strategic partners (Tsinghua, Tongji, Fudan, and more)
- **ISO 14040 / 14044 / 14067** compliant data
- **30+** team members

---

## Feedback

- **Bug reports & feature requests** — [Open an issue](https://github.com/HiQ-AI/cortex-desktop/issues/new)
- **Questions & discussions** — [Join the discussion](https://github.com/HiQ-AI/cortex-desktop/discussions)
- **Business inquiries** — [info@hiqlcd.com](mailto:info@hiqlcd.com)

---

## License

Copyright © 2026 HiQ (Shanghai) Data Technology Co., Ltd. All rights reserved.

This software is proprietary. Unauthorized copying, modification, distribution, or use is strictly prohibited.

---

<p align="center">
  <sub>Built with ❤️ by <a href="https://www.hiqlcd.com">HiQ AI</a> in Shanghai</sub>
</p>
