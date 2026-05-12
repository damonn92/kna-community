# KNA 社区 / Community

> 中国大陆开发者的 Claude API 中转服务 · 用人民币驱动 Claude
>
> A community hub for KNA users — discuss integrations, share workflows, get help.

## 🪄 KNA 是什么

KNA（[wearekna.com](https://wearekna.com)）是一家独立运营的 Claude API 中转服务，专为中国大陆开发者打造：

- **免海外信用卡**，微信、支付宝直接充值
- **引流期官方价 1.5 折** — 同样的 token 只付 Anthropic 官方价的 15%，余额永不过期。先充先享，之后会涨价
- **3 分钟拿到 API Key**，5 分钟接入 Claude Code / Cursor / Cline / Hermes / 任何 Anthropic SDK 工具
- **网页直接聊**：[chat.wearekna.com](https://chat.wearekna.com)，注册即送 100 万 Sonnet token（1.5 折后等于约 666 万官方 token）

## 🗺️ 找到你需要的

| 我想… | 去这里 |
|---|---|
| 直接聊天试试 | [chat.wearekna.com](https://chat.wearekna.com) |
| 注册 / 拿 API Key | [code.wearekna.com/register](https://code.wearekna.com/register) |
| 看完整接入文档 | [wearekna.com/docs](https://wearekna.com/docs) |
| Claude Code 配置 | [code.wearekna.com/integrations/claude-code](https://code.wearekna.com/integrations/claude-code) |
| Hermes Agent 配置 | [code.wearekna.com/integrations/hermes-agent](https://code.wearekna.com/integrations/hermes-agent) |
| OpenClaw 配置 | [code.wearekna.com/integrations/openclaw](https://code.wearekna.com/integrations/openclaw) |
| 提问 / 讨论 / 反馈 | [GitHub Discussions](../../discussions) ← 就在本仓库 |
| 用 Shopify 卖货？看 Shopify 实战 skills | [shopify-merchant-skills](https://github.com/damonn92/shopify-merchant-skills) |
| 中转选型对比（KNA vs others） | [china-claude-api-relays](https://github.com/damonn92/china-claude-api-relays) |

## 💬 进社区

- **GitHub Discussions** — 在这个仓库里直接发帖：[➜ Discussions tab](../../discussions)
 - `Q&A` 板块：接入卡住、报错排查
 - `Show & tell` 板块：分享你的 workflow（Cursor + KNA、Claude Code 项目案例等）
 - `Ideas` 板块：想看的功能、新模型支持
- **WeChat 客服群** — 扫码加群，技术答疑 + 重大公告同步
 - 入口：[code.wearekna.com](https://code.wearekna.com) → 页脚二维码

## 🛠️ 仓库 / Repos

| 仓库 | 说明 |
|---|---|
| [`shopify-merchant-skills`](https://github.com/damonn92/shopify-merchant-skills) | 11 个生产级 Shopify 操作 skill（cache 调试 / dropshipping / CPQ / 自动化 blog 等） |
| [`china-claude-api-relays`](https://github.com/damonn92/china-claude-api-relays) | 2026 国内 Claude API 中转选型指南，客观对比 + 验证方法 |
| `kna-community`（本仓库） | 社区入口、Discussions、WeChat 二维码 |

## ❓ 常见问题速答

<details>
<summary>KNA 长期运营吗？数据安全吗？</summary>

KNA 独立运营，与 Anthropic 无隶属关系。我们做了几件可以公开验证的事：

- **协议透明**：100% byte-for-byte 透传 Anthropic 官方 API，不缓存、不读取 prompt、不二次微调。响应头里能看到 `x-upstream: api.anthropic.com`，自己拿 `curl` 就能验
- **数据不落盘**：只记录 metadata（model、tokens、latency）用于计费与排障，prompt 与 completion 全程不持久化（详见 [wearekna.com/privacy](https://wearekna.com/privacy)）
- **基础设施可查**：服务器在 Vultr Tokyo 节点，开放众测仪表盘 [code.wearekna.com/_kna/dashboard](https://code.wearekna.com/_kna/dashboard)，大陆访问质量 + 上游 dated model ID 真实状态实时公开
- **充值即时到账，余额永不过期**，不强制订阅、不预扣
- **完整退款政策**：7 天内未消费部分原路退回（[wearekna.com/refund](https://wearekna.com/refund)）
- **行业对比也公开**：[china-claude-api-relays](https://github.com/damonn92/china-claude-api-relays) 把 KNA 和别家放一起做客观对比

</details>

<details>
<summary>价格怎么算？</summary>

**引流期按 Anthropic 官方 token 价 1.5 折计费** — 实付仅官方 15%，无月费、无最低消费。属于限时引流活动，之后会涨价，先充先享。

**当前 KNA 价格（官方价 → KNA 引流价 per MTok）：**
- Opus 4.7: $15/$75 → **$2.25/$11.25**
- Sonnet 4.6: $3/$15 → **$0.45/$2.25**
- Haiku 4.5: $1/$5 → **$0.15/$0.75**

**充值档位（按 1.5 折引流价跑量）：**
- 充 ¥30 ≈ $5 USD 余额，约 **1100 万** Sonnet 4.6 输入 token（或 3300 万 Haiku 输入 token）
- 充 ¥200 ≈ $33 USD 余额（含 20% 赠送），约 **7400 万** Sonnet 输入 token
- 充 ¥1000 含 30% 赠送 + 1v1 客服 + 可申请发票
- 充 ¥5000 含 50% 赠送 + 团队子账号 + SLA

> ⚠️ 1.5 折是引流期限时价格。我们会在官方提价或活动结束时调价，但已充值余额按当时锁定价格使用，不追溯。

</details>

<details>
<summary>支持哪些 Claude 模型？</summary>

**当前推荐**（2026-05 起，alias 形式最稳定）：
- `claude-sonnet-4-6` — 主力，性价比最佳
- `claude-opus-4-7` — 复杂 reasoning
- `claude-haiku-4-5` — 辅助任务、速度优先

dated ID 在上游会被 Anthropic 不定期下线，KNA 内部有 model rewriter 把过时 dated ID 透明重写成当代 alias，**客户的老 hermes/openclaw 配置不用动**。

</details>

<details>
<summary>Claude Code 接入要注意什么？</summary>

两个常见坑：

1. **KNA Key 格式**：`sk-` + 64 位 hex 字符（开头不带 `kna-` 中段，直接 `sk-...`）。配置时把 `ANTHROPIC_BASE_URL=https://code.wearekna.com` + `ANTHROPIC_AUTH_TOKEN=sk-xxxx` 一起设就行。
2. **Claude Code 自带 OAuth 凭据** 会优先于环境变量。如果你之前用 Anthropic 官方账号登录过 Claude Code，先跑 `claude /logout` 清掉本地 OAuth session，再设 KNA 环境变量才会生效。

完整排查指南：[wearekna.com/docs](https://wearekna.com/docs)

</details>

## 🤝 贡献

欢迎：
- 在 Discussions 分享你的接入方案、踩坑笔记
- 提 PR 改 README 错字 / 补充 FAQ
- 在 [`shopify-merchant-skills`](https://github.com/damonn92/shopify-merchant-skills) 仓库贡献新的 skill（要求：来自真实生产问题）

## 📬 联系

- 邮箱：[info@wearekna.com](mailto:info@wearekna.com)
- 商务合作：同上

---

🥃 _KNA — 独立运营，与 Anthropic 无隶属关系。Built by developers, for developers._
