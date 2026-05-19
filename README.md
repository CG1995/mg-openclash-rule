# mg-openclash-rule

这个仓库只维护我当前正在使用的 OpenClash / Subconverter 配置：

- `Clash-MG.ini`

它依赖的本地规则文件只有 4 个：

- `AI.list`
- `Apple.list`
- `Proxy.list`
- `Adobe.list`

其他分类规则都直接引用 `blackmatrix7/ios_rule_script` 的外链，不再搬运到本地。

## 仓库内容

| File | Purpose |
| --- | --- |
| `Clash-MG.ini` | 主配置，定义 ruleset 和策略组 |
| `AI.list` | 本地 AI 补充规则 |
| `Apple.list` | 本地 Apple 补充规则 |
| `Proxy.list` | 本地个人补充规则 |
| `Adobe.list` | 本地 Adobe 补充规则 |
| `README.md` | 仓库说明 |
| `CHANGELOG.md` | 变更记录 |

## 使用方式

1. 在 OpenClash / Subconverter 中把 `Clash-MG.ini` 作为模板或规则配置使用。
2. 本地规则通过 GitHub Raw 链接加载：
   - `https://raw.githubusercontent.com/CG1995/mg-openclash-rule/main/AI.list`
   - `https://raw.githubusercontent.com/CG1995/mg-openclash-rule/main/Apple.list`
   - `https://raw.githubusercontent.com/CG1995/mg-openclash-rule/main/Proxy.list`
   - `https://raw.githubusercontent.com/CG1995/mg-openclash-rule/main/Adobe.list`
3. 其余规则继续沿用 `blackmatrix7/ios_rule_script` 的在线来源。

## 维护原则

- 只保留当前实际使用的文件
- 不把外部维护良好的规则源搬运成本地
- `.list` 文件只保留必要的个人补充规则
- 仓库保持小而清晰，避免旧配置和历史文件混入

## 变更记录

参见 [CHANGELOG.md](./CHANGELOG.md)。
