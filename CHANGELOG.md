# 2026-10-03 规则优化

- Adobe 提至最前，组仅允许 REJECT；删除误归入 Adobe 的 Windows Update / DigiCert 补充。
- AI 收紧为 36 条服务域名及精确依赖，移除广泛平台、ASN、单 IP 和关键词匹配。
- Apple / Adobe 主名单改为在线维护源，本地只保留必要补充，移除 Apple 的重复 IP 版本。
- 美国地区匹配避免 AUS；亚洲组不再含广美，欧洲组不再含智利。
- 地区组与自动组加入显式 REJECT，避免空组变为 COMPATIBLE 直连。
- 补充来源说明。本次设备端先实施家中 R5S，其他路由器暂不同步。

# Changelog

All notable changes to this repository are documented here.

## 2026-10-03

- 原日本 VPS 迁至洛杉矶后，节点统一为 USCN2 / USCN2-Reality，沿用自选美国组。
- 移除 CF-M、CF-A 和独立 USCN2 组及所有组引用，去重美国组引用。
- 其余分类与规则内容暂保持原样，优化建议另行审计后由用户决定。

## 2026-05-19

### Changed

- Kept only the active `Clash-MG.ini` workflow in the repository.
- Removed old ini/list files and router-side leftovers that were no longer referenced.
- Normalized `Clash-MG.ini` raw links to the shorter `main` path format.
- Fixed a few obvious regex issues without changing the strategy layout.
- Trimmed the four local rule files to remove empty lines and duplicate entries.
- Added a concise README focused on current usage and maintenance.

### Added

- `CHANGELOG.md` to track future repository changes.

## 2026-05-10

### Changed

- Refreshed the local AI, Apple, Adobe, and Proxy rule providers.
- Kept personal supplement rules separate from upstream blackmatrix7 sources.
