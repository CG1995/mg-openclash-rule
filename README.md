# clash-rule

Personal OpenClash rule-provider lists.

## Maintenance notes

- `Clash-MG.ini` is intentionally left untouched because it controls the visual node and rule selection used by the router.
- `.list` files are normalized to Clash rule-provider syntax and deduplicated case-insensitively.
- Apple, Adobe and AI lists are refreshed from maintained public rules, then merged with personal rules.
- Router custom rules are split by policy target and appended into the matching regional list or `Direct.list`.
- Reject-only custom rules are not committed because this repository does not currently have a reject provider file.

## Current source mix

| File | Rule count | Notes |
| --- | ---: | --- |
| `Apple.list` | 1744 | blackmatrix7/ios_rule_script Apple.list + personal dedupe |
| `AI.list` | 83 | blackmatrix7 OpenAI/Claude/Gemini/Copilot + personal dedupe |
| `Adobe.list` | 140 | blackmatrix7 Adobe.list + personal dedupe |
| `Direct.list` | 518 | existing local direct rules + router custom direct rules |
| `Proxy.list` | 50 | existing local proxy rules + syntax cleanup |
| `MG-USA.list` | 80 | existing local list + router custom US rules |
| `MG-ja.list` | 27 | existing local list + router custom Japan rules |
| `MG-tw.list` | 3 | existing local list + router custom Taiwan rules |
| `MG-HK.list` | 3 | existing local list + router custom Hong Kong rules |
| `MG-EUR.list` | 6 | existing local Europe list + syntax cleanup |

## Upstream references

- blackmatrix7 ios_rule_script: Apple / Adobe / OpenAI / Claude / Gemini / Copilot Clash rules.
- Personal OpenClash custom rules captured from the router on 2026-05-10.
