# CLAUDE.md — picoruby-docs

## 概要
PicoRuby の mrbgems 配下の RBS + README を収集する Collector gem。

## Collector インターフェース
- `collect(since: nil)` → `[{content:, source:}]`（since は無視）
- source 値: `picoruby/picoruby:docs/{gem-name}`
- `picoruby-` プレフィックスのディレクトリのみ対象

## 主要クラス
- `RbsParser` — RBS ファイルから class/methods を抽出してドキュメント化
- `ReadmeParser` — README.md を strip して返す
- `GemDocCollector` — RBS + README を組み合わせて1ドキュメントに
