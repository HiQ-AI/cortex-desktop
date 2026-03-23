## v0.0.31 — 蜗牛接受投喂了 📦

市场里的技能不够用？自己做一个喂给它。

Skills 页面底部多了**导入区**——选一个 `.skill` 或 `.zip` 文件，蜗牛自己拆包、检查、安装。格式不对会告诉你哪里错了，不会闷声吞下去。

### 📦 自定义技能导入
- 支持 `.skill` 和 `.zip` 格式
- 自动校验：SKILL.md 存在、frontmatter 完整、文件安全
- 校验失败有具体错误提示
- 导入后立刻出现在已安装列表，带"自定义"标签

### 🔒 安全校验
- 不含符号链接、不含 `..` 路径
- 单文件 ≤ 10MB，总计 ≤ 50MB
- 任何一项不通过都不写入

蜗牛接受投喂了。但挑食。🐌

### 平台
- **macOS** — arm64 | **Windows** — x64 | **Linux** — x64

---

Not enough skills in the marketplace? Make one and feed it to the snail.

New **import section** at the bottom of Skills — pick a `.skill` or `.zip` file. The snail unpacks, validates, and installs. Bad format? It tells you exactly what's wrong.

### 📦 Custom Skill Import
- `.skill` and `.zip` formats
- Auto-validates: SKILL.md exists, frontmatter complete, files safe
- Specific error messages on failure
- Appears in installed list with "Custom" badge

### 🔒 Security Checks
- No symlinks or path traversal
- Max 10MB per file, 50MB total
- Nothing written until all checks pass

The snail accepts offerings now. But it's picky. 🐌

### Platforms
- **macOS** — arm64 | **Windows** — x64 | **Linux** — x64
