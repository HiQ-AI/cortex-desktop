## v0.0.39 — 蜗牛换脑了 🧠

### 事情的起因

老板昨天给客户演示 Chat 模式。

"帮我查碳钢的碳足迹。"

蜗牛想了 8 秒钟，先把任务委派给一个叫 siphon 的小弟，小弟又想了 5 秒，搜了个"碳酸钙"回来，蜗牛拿到结果再加工了 6 秒——

**总共 19 秒，查了个寂寞。**

老板的脸色当场就不对了。

更绝的是第二个问题："帮我查钢的碳足迹。" 蜗牛先问了一嘴"什么钢"，等用户选了碳钢——**然后就不动了。** HITL 流程炸了。

### 我们干了什么

**把 Chat 模式的引擎拆了。**

旧架构是 Team 模式：用户 → Leader（Claude Sonnet 4.6）→ 委派 → Siphon（Claude Haiku）→ 返回 → Leader 再加工。两层 LLM 串联，每层都可能幻觉，延迟叠加。

新架构是单 Agent 模式：用户 → Agent（Claude Sonnet 4.6，直接搜）→ 出结果。砍掉中间人，砍掉委派，砍掉幻觉。

然后发现——**Web 端也炸了。**

因为 Chat Agent 从 Team 变成了 Agent，SSE 事件格式变了（`TeamRunContent` → `RunContent`），HITL 的 continue 端点变了（JSON body → Form data），session_id 传递方式变了……

**不得不把 Web 端的 SSE 解析器、HITL 流程、消息渲染全部重写。**

### 现在怎么样

**快了。** 从 19 秒降到 3 秒。没有委派开销，没有中间人加工。

**准了。** 走 Anthropic 原生 `/v1/messages` 格式（跟 Cowork 一条链路），tool_use 不再经过 OpenAI 格式翻译。碳钢就是碳钢，不是碳酸钙。

**稳了。** HITL 用 Agno 原生 continue 端点（Form data + ToolExecution），不再用自定义 hack。

### 具体改了什么

#### 🧠 Chat 引擎重写
- Team coordinate 模式 → 单 Agent 模式
- Leader + Siphon 两层 LLM → 单 Agent 直搜
- OpenAI 兼容格式 → Anthropic 原生 `/v1/messages`
- 技能注入：只加载 lca-search（不再加载 7 个无关技能）

#### 🔗 HITL 流程修复
- continue 端点适配 AgentOS 原生格式（Form data）
- session_id 从 SSE 事件正确传递
- user_input_schema 值正确回传

#### 🎨 消息渲染升级
- Chat 模式支持 interleaved rendering（文本和工具卡片交错显示）
- SSE 解析器兼容 Team 和 Agent 两种事件格式

#### ⚙️ LiteLLM 最佳实践
- Anthropic 原生 `/v1/messages` 链路（同 Cowork，不经 OpenAI 格式翻译）
- Budget ID 分级（free/pro/enterprise），改 tier 不用改代码
- Per-user RPM/TPM 限速
- Spend tracking 修复（显式 cost per token，之前全是 $0）
- Plan 从 SSO roles 推断

#### 🌐 平台感知引导
- 桌面端复杂任务 → "切换到 Cowork 模式"
- Web 端复杂任务 → "下载 Cortex Desktop" + 链接
- 欢迎页按钮改为引导式 HITL（不再直接查具体材料）

### 还差什么

换了引擎不代表万事大吉。目前还缺：

- **Chat 和 Cowork 的记忆没打通** — 两个模式各记各的，Chat 里聊过的材料 Cowork 不知道
- **没有用量面板** — 花了多少钱、搜了多少次，用户看不到，只有管理员能在后台查
- **Web 端 HITL 界面简陋** — 能用，但按钮样式和交互体验还需要打磨
- **没有搜索历史** — 上周查过什么材料，找不回来

但这些都是「好不好用」的问题，不是「能不能用」的问题。先把引擎换对，再一个个补。

蜗牛换了脑子。这次老板应该能演示完了。🐌

### 平台
- **macOS** — arm64 | **Windows** — x64 | **Linux** — x64

---

### What happened

The boss demoed Chat mode to a client yesterday.

"Search carbon steel carbon footprint."

The snail thought for 8 seconds, delegated to a helper called "siphon," siphon thought for 5 more seconds, came back with "calcium carbonate," the snail reprocessed for 6 seconds—

**19 seconds total. Wrong material.**

The boss was not amused.

Second query: "Search steel carbon footprint." Snail asked "what kind?" User picked carbon steel — **then it froze.** HITL was broken.

### What we did

**Ripped out the Chat engine.**

Old: Team mode (Leader → delegate → Siphon → return → Leader reprocesses). Two LLM layers, each can hallucinate, latency stacks.

New: Single Agent mode (Agent searches directly). No middleman, no delegation, no hallucination.

Then **the web client broke too.** SSE events changed, HITL endpoint changed, session_id handling changed. Had to rewrite the SSE parser, HITL flow, and message rendering.

### Now

**Fast.** 19s → 3s. No delegation overhead.

**Accurate.** Native Anthropic `/v1/messages` format (same pipeline as Cowork). Carbon steel stays carbon steel.

**Stable.** HITL uses AgentOS native continue endpoint.

### Changes

- Chat engine: Team → single Agent, Anthropic native format
- HITL: AgentOS native continue (Form data + ToolExecution)
- Rendering: interleaved content + tool cards
- LiteLLM: Anthropic native format, Budget ID tiers, RPM/TPM limits, spend tracking fix
- Platform-aware: desktop → "switch to Cowork", web → "download Desktop"
- Welcome buttons: guided HITL prompts

### What's still missing

New engine doesn't mean everything's done. Still need:

- **Chat and Cowork memory not connected** — two modes, two separate histories
- **No usage dashboard** — users can't see their spend or search count
- **Web HITL UI is rough** — functional but needs polish
- **No search history** — can't recall what you searched last week

These are "how nice" problems, not "does it work" problems. Engine first, polish next.

The snail got a brain transplant. The demo should work this time. 🐌

### Platforms
- **macOS** — arm64 | **Windows** — x64 | **Linux** — x64
