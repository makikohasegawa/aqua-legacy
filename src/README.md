# src/

ソースコード用ディレクトリ。

プロジェクト全体の技術スタックはまだ未定。プロダクトごとに、必要最小限の技術を選び、
選定理由は [docs/decisions.md](../docs/decisions.md) に記録する。
現時点ではどのプロトタイプも単一HTML/CSS/JavaScript、localStorage保存という構成を採用している
（これはプロダクトごとに繰り返されてきた実践であり、プロジェクト全体として正式に決定したものではない。
[docs/architecture.md](../docs/architecture.md)を参照）。

- `being-log/` — 在ることの記録（Being Log）。日々の小さな気づきを記録する、最初の実装プロダクト。記憶に本人が付け外しできる「目印」と、それを含むバックアップ（version 3）を持つ。[DEC-0003](../docs/decisions.md#dec-0003-最初の実装プロダクトとしてbeing-logを採用)、[DEC-0015](../docs/decisions.md#dec-0015-ラベル目印をbeing-logの記録を書き換えない橋として別保管し何も自動で変えない)
- `aquarium/` — Aquarium（水槽）。Being（魚）が生きる場所。最初の3匹（Something Great, Adam, Eve）と、最小のWill/Experienceの仕組みを持つ。[DEC-0006](../docs/decisions.md#dec-0006-beingを中核エンティティとして導入し最初の型をfishとする)
- `prototypes/garden/` — Garden（心の庭）。Being Logの記録から「希望のカケラ」(HopeFragment)を見つけ、庭の好きな場所に置く実験。[DEC-0011](../docs/decisions.md#dec-0011-希望のカケラhopefragmentを導入しbeing-logとgardenを最小の橋でつなぐ)
- `prototypes/memory-companionship/` — Being Logの1つの記録と、水槽の中の1匹のAquaの間に、「この記憶をこのAquaと共に持つ」関係を結ぶ実験。[DEC-0014](../docs/decisions.md#dec-0014-memorycompanionshipを導入しbeing-logの記録とaquabeingの間に記憶を共に持つ関係を置く)
- `prototypes/atmosphere/` — 水槽の世界観・視覚表現だけを探る実験。他の4つから独立しているが、Aquaの色などのデータは読み込んで（書き換えずに）反映している。現時点ではこのプロトタイプ単独のDECはまだ無い。
