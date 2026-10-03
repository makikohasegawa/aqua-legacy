# Architecture

技術スタックは2026-07-13時点で未定です。
このドキュメントは、決定事項と検討中の選択肢を分けて記録していく場所です。

## 決定事項

現状を簡潔に示す一覧です。決定の背景・理由・検討した選択肢・根拠とした原則は
[docs/decisions.md](decisions.md) を参照してください。

| 項目 | 決定内容 | 詳細 |
|------|----------|------|
| Beingという中核データモデル | Beingを永続エンティティとして導入し、最初の型をfishとする | [DEC-0006](decisions.md#dec-0006-beingを中核エンティティとして導入し最初の型をfishとする) |
| Beingのnature（fishスキーマ） | Being生成時にid・type・birth・nameと同時にnatureを確定し、Beingレコードに埋め込む。fishのnatureフィールドと選択肢を定義 | [DEC-0007](decisions.md#dec-0007-being生成時にnatureを同時確定しfishの最初のnatureスキーマを定める) |
| HopeFragment | 「希望のカケラ」を導入し、Being LogとGardenを最小の橋でつなぐ | [DEC-0011](decisions.md#dec-0011-希望のカケラhopefragmentを導入しbeing-logとgardenを最小の橋でつなぐ) |
| recordNumber | Being Logの記録に、生涯変わらないシリアルナンバーを持たせる | [DEC-0012](decisions.md#dec-0012-being-logの記録に生涯変わらないrecordnumberを持たせる) |
| recordNumberのカウンター管理 | カウンターの保存場所、バックアップ復元時の扱い、複数端末同時利用の限界 | [DEC-0013](decisions.md#dec-0013-recordnumberというシリアルナンバーを現在の技術構成の中でどう守るか) |
| MemoryCompanionship | Being LogとAqua（Being）の間に「記憶を共に持つ」関係を置く | [DEC-0014](decisions.md#dec-0014-memorycompanionshipを導入しbeing-logの記録とaquabeingの間に記憶を共に持つ関係を置く) |

## 検討中

| 領域 | 選択肢 | 状況 |
|------|--------|------|
| 言語・ランタイム | 未定 | 検討前 |
| フロントエンド | 未定 | 検討前 |
| バックエンド | 未定 | 検討前 |
| データストレージ | 未定 | 検討前 |
| ホスティング/インフラ | 未定 | 検討前 |

言語・ランタイム/フロントエンド/データストレージについては、これまでに実装された5つのプロトタイプ
（Being Log, Aquarium, Garden, MemoryCompanionship, Atmosphere）すべてが、単一HTMLファイル + Vanilla JS +
localStorageという構成を一貫して採用している。ただし、これはプロトタイプごとの実装上の選択の積み重ねであり、
プロジェクト全体の技術スタックとして正式にDECで決定されたことはまだない。上の表のステータスは、この区別を
保つためにあえて変更していない。
バックエンド/ホスティング・インフラは、実践上も何も試されていない。

## 決定時の記録ルール

技術選定を行う際は、以下の手順で記録する。

1. [docs/decisions.md](decisions.md) に DEC-XXXX として、背景・決定・検討した選択肢・根拠とした原則・影響を記録する
2. 上の「決定事項」表に一行追加し、「詳細」列から該当のDEC-XXXXへリンクする

例:

| 項目 | 決定内容 | 詳細 |
|------|----------|------|
| 言語・ランタイム | TypeScript | [DEC-0002](decisions.md#dec-0002-言語にtypescriptを採用) |

## 更新履歴

- 2026-07-13: 雛形作成（技術スタック未定）
- 2026-07-14: decisions.mdとの連携方法を追加（決定事項表に「詳細」列、記録ルールを2段階に変更）
- 2026-07-28: 決定事項表にBeing / Nature（fishスキーマ）を追加（DEC-0006, DEC-0007。実装・動作確認まで完了したタイミングで記録）
- 2026-10-03: 決定事項表にHopeFragment・recordNumber・MemoryCompanionshipを追加（DEC-0011〜0014。実装・動作確認まで完了したタイミングで記録）。検討中の表に、実践上の構成と正式決定の違いを分ける注記を追加
