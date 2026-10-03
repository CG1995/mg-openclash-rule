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
