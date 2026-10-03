# mg-openclash-rule

个人 OpenClash / Subconverter 模板：Clash-MG.ini。共享模板保持 23 个策略组。

## 当前策略

- USCN2 / USCN2-Reality 进入现有「🐱自选-美国」与「美国-自动」。没有独立 USCN2、CF-M 或 CF-A 组。
- Adobe 分类在所有业务分类与 FINAL 前，Adobe 组仅可选 REJECT，按用户要求全部拦截。
- AI 只使用审核过的服务域名及精确依赖主机，不使用整个 ASN、IP 网段、通用关键词或共享平台根域名。
- 地区组和自动组明确包含 REJECT，空地区拒绝连接，不依赖 empty-fallback。
- 真正的日本机场节点仍进入「日本-自动」。美国匹配支持 USCN2/USA/边界清晰的 US，不把 AUS 当成美国。

## 名单维护

Apple、Adobe 主名单直接引用 blackmatrix7 在线分类源，更新时无需手工复制；其余分类继续用在线源。

| 文件 | 用途 |
|---|---|
| AI.list | 严格 AI 分流政策，36 条服务域名/精确主机，按需求审核维护 |
| Apple.list | 仅 3 条既有 CDN 补充，没有重复 IP 网段 |
| Adobe.list | 全部 Adobe 拦截的关键词补充，完整主名单在线提供 |
| Proxy.list | 50 条个人分流需求，与在线 Global 主名单分开 |
| SOURCES.md | 来源、删改理由和适用范围 |

本地文件是明确的个人政策补充，已移除旧厂商快照。在线社区名单不等于厂商官方域名全集。客户端沿用现有规则源更新机制，本次未添加路由器自动重启或订阅任务。

## 使用与验证

模板地址：`https://raw.githubusercontent.com/CG1995/mg-openclash-rule/refs/heads/main/Clash-MG.ini`。

转换器须保留显式 []REJECT。OpenClash 运行配置和自定义规则必须同步，否则旧分组或自定义顺序仍可改变结果。每次检查生成配置、实际匹配日志和空组行为；下载成功不等于所有规则生效。

R5S 另有固定美国 Claude-USA-Only / Claude-USA-Pinned，保留其最高优先级保护。不要用共享组替换它。账号 ID 与流量历史不因节点改名而改变。

变更记录：[CHANGELOG.md](./CHANGELOG.md)。来源：[SOURCES.md](./SOURCES.md)。
