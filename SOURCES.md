# 规则来源与政策边界

审核：2026-10-03。规则语法以 [Mihomo 官方文档](https://wiki.metacubex.one/config/rules/) 为准，类别与厂商归属另行审核。

## 在线分类源

Apple 和 Adobe 主名单直接读取 [blackmatrix7/ios_rule_script](https://github.com/blackmatrix7/ios_rule_script) 的 `rule/Clash/Apple/Apple.list`、`rule/Clash/Adobe/Adobe.list`。GitHub、TikTok、Telegram、YouTube、Disney、Netflix、Spotify、Global 继续读取同项目在线名单。

这些是社区分类源，不宣称由服务商维护。Apple 当前主名单的 10 个 IPv4 网段统一为带 no-resolve 的形式；旧个人快照中不带 no-resolve 的重复版本已移除。保留的三个 CDN 补充来自此前配置，其余旧补充已被主名单后缀覆盖。主名单含进程规则，当前 domain/ipcidr 转换模式只承载网络规则，不宣称进程规则也已导出。

Adobe 旧快照额外包含 Windows Update 证书吊销及 DigiCert 整域；它们是共享基础服务，已从 Adobe 补充移除。Adobe 主名单及关键词补充全部执行 REJECT。社区名单中的共享分析域仍按该分类拦截，可能涉及同平台其他客户；不把此行为说成逐域名厂商归属认证。

## AI 严格分流

AI.list 是个人分流政策，不是上游副本。仅保留服务本身的后缀或精确主机；新增服务要单独审核。原 ASN 两条、两个无稳定服务归属的旧单 IP、通用关键词，以及 auth0.com / stripe.com / sentry.io / algolia.net / intercom.io / livekit.cloud 等整个平台匹配已删除。

OpenAI 服务域名和两条精确 Sentry 主机参考 [OpenAI 网络要求](https://help.openai.com/en/articles/9247338-network-recommendations-for-chatgpt-errors-on-web-and-apps)。该文档是放行需求，不能把其中所有共享平台域名直接作为 AI 专属分类。本策略保留服务专属域名与已经明确列出的精确依赖，不将支付、验证码或客服整个平台都划为 AI。

Gemini API 精确主机参考 [Google API 文档](https://ai.google.dev/api)。Copilot 精确服务域参考 [Microsoft 网络要求](https://learn.microsoft.com/en-us/microsoft-365/copilot/microsoft-copilot-requirements)。这些资料不意味着泛 Microsoft 365、Google API、Bing 或网页静态资源都应该进入 AI 组。

GitHub Copilot 的专属 githubcopilot.com 后缀参考 [GitHub 官方允许列表](https://docs.github.com/en/copilot/reference/copilot-allowlist-reference)。GitHub 网站本身仍由 GitHub 分类处理。

既有 Claude、Meta AI、Perplexity、Poe、Character AI 服务域保留；Claude 另补 claude.com / claudeusercontent.com。R5S 的既有六条 Claude 专用规则继续优先，不受本次严格名单替换影响。

严格分类后，共享支付/验证码/登录依赖可由 Global 或其余规则处理。网站请求成功仍需实际登录验证，不能仅以域名分类或 HTTP 200 保证完整业务流程。

## 个人覆盖与兜底

Proxy.list 保留原有 50 条用户分流需求，不冒称是厂商权威列表。完整 Global 分类仍在线维护，FINAL 保持最后。

地区名按节点显示名称筛选，不是地理位置证明；明确 REJECT 保证空组拒绝连接。无可用节点时拒绝与网络故障直连是不同政策；R5S Claude 必须继续采用固定节点与客户端保护。
