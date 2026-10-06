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

思想面（vision / story / philosophy / principles / promise）は、対話を通じて育ってきています。
実装面では、5つの独立したプロトタイプ（Being Log / Aquarium / Garden / MemoryCompanionship / Atmosphere）が動いています。

いずれも単一HTMLファイル + CSS + Vanilla JS + localStorageという構成で実装されていますが、
これはプロトタイプごとに繰り返されてきた実践であり、プロジェクト全体の技術スタックとして
正式に決定されたものではありません（検討中の項目については[docs/architecture.md](docs/architecture.md)を参照）。

## 現在のプロトタイプ

いずれもビルドツールを使わず、ブラウザで直接HTMLファイルを開くだけで動きます。
各設計判断の背景・理由は[docs/decisions.md](docs/decisions.md)を参照してください。

### Being Log（在ることの記録）

日々の小さな気づきを記録する、最初の実装プロダクト。OpenAI Build Weekで最初のプロトタイプとして作られました。
記録の保存・バックアップと復元・継続日数表示・過去の記憶の振り返りに対応しています。
さらに、記憶に本人が自由に付け外しできる「目印」を付けて、後から眺めることができます。
目印は記録とは別に保存され、並び順や重要度を自動で変えることはありません（[DEC-0015](docs/decisions.md#dec-0015-ラベル目印をbeing-logの記録を書き換えない橋として別保管し何も自動で変えない)）。

`src/being-log/index.html` を開いて動かせます。

### Aquarium（水槽）

Being（魚）が生きる水槽。起源となる3匹（Something Great, Adam, Eve）から始まり、
壁への反応や魚同士の出会いなど、最小のWill/Experienceの仕組みを持っています。

`src/aquarium/index.html` を開いて動かせます。

### Garden（心の庭）

Being Logの記録から「希望のカケラ」(HopeFragment)を見つけ、庭の好きな場所に置く実験。

`src/prototypes/garden/index.html` を開いて動かせます。

### MemoryCompanionship

Being Logの1つの記録と、水槽の中の1匹のAquaの間に、「この記憶をこのAquaと共に持つ」関係を結ぶ実験。

`src/prototypes/memory-companionship/index.html` を開いて動かせます。

### Atmosphere

水槽の世界観・視覚表現だけを探る、他の4つとは独立したプロトタイプ。

`src/prototypes/atmosphere/index.html` を開いて動かせます。

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
├── .claude/
│   └── launch.json      # ローカル開発用の起動設定
├── docs/
│   ├── principles.md    # 第一原則（変えないもの）
│   ├── promise.md       # 約束（人・AI・未来と向き合う姿勢）
│   ├── vision.md        # ビジョン
│   ├── story.md         # 物語
│   ├── garden.md        # 心の庭（長期ビジョン、構想段階）
│   ├── philosophy.md    # 開発・協働・設計の哲学
│   ├── architecture.md  # 技術構成
│   ├── decisions.md     # 意思決定の記録（背景・理由・選択肢）
│   └── roadmap.md       # ロードマップ
├── src/      # ソースコード（技術スタック未定）
│   ├── being-log/        # Being Log（在ることの記録）
│   ├── aquarium/         # Aquarium（水槽）
│   └── prototypes/
│       ├── garden/               # Garden（心の庭）
│       ├── memory-companionship/ # MemoryCompanionship
│       └── atmosphere/           # Atmosphere（世界観・視覚表現）
├── assets/   # 画像・素材等
└── archive/  # 過去の検討・不要になったが残しておきたいもの
```
