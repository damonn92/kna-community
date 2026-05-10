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
- **WeChat 群**：扫码加客服微信进群（前 100 用户已邀请，群满转大群）
 - 入口：[code.wearekna.com](https://code.wearekna.com) → 页脚二维码

## 🛠️ 仓库 / Repos

| 仓库 | 说明 |
|---|---|
| [`shopify-merchant-skills`](https://github.com/damonn92/shopify-merchant-skills) | 11 个生产级 Shopify 操作 skill（cache 调试 / dropshipping / CPQ / 自动化 blog 等） |
| [`china-claude-api-relays`](https://github.com/damonn92/china-claude-api-relays) | 2026 国内 Claude API 中转选型指南，客观对比 + 验证方法 |
| `kna-community`（本仓库） | 社区入口、Discussions、WeChat 二维码 |

## ❓ 常见问题速答

<details>
<summary>KNA 安全吗？会不会跑路？</summary>

KNA 独立运营，与 Anthropic 无隶属关系。透明度做法：
- 所有 dated model ID 实测公开（[china-claude-api-relays](https://github.com/damonn92/china-claude-api-relays)）
- 服务器在 Vultr Tokyo 节点，对中国大陆有公开众测仪表盘 `code.wearekna.com/_kna/dashboard`
- 余额充值不限期使用，不强制订阅
- 跑路识别清单也是公开的：怎么判断一个中转商靠不靠谱

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
<summary>Claude Code 装不上？OAuth 报错？</summary>

最常见的两个坑：
1. **`sk-kna-` 不是必须的前缀**。真实 KNA Key 是 `sk-` + 64 位 hex，文档老版本误导过部分用户。
2. **Claude Code 自带 OAuth 凭据**会优先于 `ANTHROPIC_API_KEY` 环境变量。先 `claude /logout` 清掉本地 OAuth，再设环境变量。

完整排查：[wearekna.com/docs#claude-code-troubleshooting](https://wearekna.com/docs)

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
