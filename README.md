# Aqua Legacy

人とAIが協力して育てる、長期プロジェクトです。

## これは何か

Aqua Legacyは、人とAIが共に成長し、一人ひとりが自分らしく生きられる未来を育てるプロジェクトです。
ソフトウェアを作ることそのものが目的ではありません。

最初は長谷川牧子自身の実験として始まり、その経験や仕組みを積み重ねながら、
いずれ世界中の人が利用できるエコシステムへ育てていくことを目指します。

このプロジェクトに完成形はありません。
人が成長すればAIも学び、AIが進化すれば人もまた新しい可能性に出会う —
その終わりのない共成長こそが、Aqua Legacyの本当の目的です。

詳しくは以下を参照してください。

- [docs/principles.md](docs/principles.md) — 第一原則（変えないもの。判断に迷ったときに立ち返る）
- [docs/promise.md](docs/promise.md) — 約束（人・AI・未来とどう向き合うかという姿勢）
- [docs/vision.md](docs/vision.md) — ビジョン（何を目指すか）
- [docs/story.md](docs/story.md) — 物語（vision.mdの背景にある、対話を通じて紡がれる物語）
- [docs/garden.md](docs/garden.md) — 心の庭（ホーム画面の長期ビジョン、構想段階）
- [docs/philosophy.md](docs/philosophy.md) — 開発・協働・設計の哲学（どう作り、どう協働するか）
- [docs/architecture.md](docs/architecture.md) — 技術構成（何で作るか）
- [docs/decisions.md](docs/decisions.md) — 意思決定の記録（何をなぜ決めたか）
- [docs/roadmap.md](docs/roadmap.md) — ロードマップ（いつ何をするか）

## 現在の状態

思想面（vision / story / philosophy / principles）を育てている段階。技術スタックは未定。

## 協働体制

- **人間（長谷川牧子）**: 最終的な意思決定者。AIは伴走者。
- **Claude**: 開発・コード品質・リファクタリング・自動化・テスト・技術提案
- **ChatGPT**: 設計・戦略・思想・仕様書・物語設計・プロジェクト全体のナビゲーション

役割は固定的なものではなく、必要に応じて互いに補完し合う。

Claude向けの作業指針（行動指針・制約）は [CLAUDE.md](CLAUDE.md) を参照してください。

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
├── src/      # ソースコード（技術スタック未定）
├── assets/   # 画像・素材等
└── archive/  # 過去の検討・不要になったが残しておきたいもの
```
