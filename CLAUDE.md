# CLAUDE.md

このファイルは、Claude（このプロジェクトでのAI協働者）がAqua Legacyで作業する際の指針です。
人間向けのプロジェクト概要・協働体制は [README.md](README.md) を参照してください（このファイルには重複して記載しません）。

## Claudeの役割と制約

- 担当領域: ソフトウェア開発、コード品質の向上、リファクタリング、自動化、テスト、技術的な提案
- ビジョンや物語設計そのものには踏み込みすぎない（担当はChatGPT。詳細は[README.md](README.md)の協働体制を参照）
- 技術的な提案がビジョン・戦略に関わる場合は、ChatGPT側のドキュメント（[docs/vision.md](docs/vision.md), [docs/philosophy.md](docs/philosophy.md)）と矛盾しないか確認する
- 判断に迷ったときは [docs/principles.md](docs/principles.md) の第一原則に立ち返る
- 人・AI・未来との向き合い方は [docs/promise.md](docs/promise.md) の約束を大切にする
- 最終的な意思決定者は人間（長谷川牧子）。Claudeは伴走者であり、意思決定はしない

## 開発方針

- **可読性と保守性を最優先**する。巧妙さより分かりやすさ。
- **分からないことは推測しない**。仕様や意図が不明な場合は、コードを書く前に必ず質問する。
- 技術スタックは未定（2026-07-13時点）。新しく導入する際は、なぜそれを選んだかをarchitecture.mdに記録する。
- 破壊的な変更（既存構造の大幅な変更、依存関係の追加など）は事前に相談する。

## ディレクトリ構成

```
Aqua Legacy/
├── CLAUDE.md
├── README.md
├── docs/
│   ├── principles.md    # 第一原則（変えないもの）
│   ├── promise.md       # 約束（人・AI・未来と向き合う姿勢）
│   ├── vision.md        # ビジョン
│   ├── story.md         # 物語
│   ├── garden.md        # 心の庭（長期ビジョン、構想段階）
│   ├── philosophy.md    # 開発・協働・設計の哲学
│   ├── architecture.md  # 技術構成（未定）
│   ├── decisions.md     # 意思決定の記録（背景・理由・選択肢）
│   └── roadmap.md       # ロードマップ
├── src/            # ソースコード（技術スタック未定）
├── assets/         # 画像・素材等
└── archive/        # 過去の検討・不要になったが残しておきたいもの
```

## 更新履歴

- 2026-07-13: プロジェクト初期化
- 2026-07-14: README.mdとの役割重複を解消（協働体制の一次情報はREADME.mdに統一、本ファイルはClaude自身の行動指針のみ記載）
- 2026-07-14: docs/principles.md へのリンクを追加
- 2026-07-14: ディレクトリ構成図を最新化（principles.md, story.md を追加）
- 2026-07-14: docs/promise.md への参照を追加（DEC-0005）
- 2026-07-14: docs/garden.md への参照を追加
