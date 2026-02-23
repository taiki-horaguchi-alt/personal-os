# Personal OS Extraction Prompts

自分の会話からPersonal OSのデータを自動抽出するためのプロンプト集です。

## 🎯 このプロンプト集でできること

- **ChatGPT で会話を分析** - あなたの会話履歴から Personal OS に入れるべき情報を自動検出
- **構造化データを生成** - JSON形式で整理されたデータを出力
- **Claude Code で簡単インポート** - JSONを貼り付けるだけで Personal OS ファイルに追記

## 🚀 クイックスタート（3ステップ）

### Step 1: ChatGPT でプロンプトを実行
1. [master-prompt.md](./master-prompt.md) をコピー
2. ChatGPT に貼り付け
3. あなたの会話履歴を追加
   ```
   [マスタープロンプトをここに貼り付け]

   ---以下、あなたの会話です---

   [会話履歴をここに貼り付け]
   ```

### Step 2: JSON 出力を取得
ChatGPT が構造化された JSON を出力します（このフォーマット）：
```json
{
  "extraction_metadata": { ... },
  "extractions": [ ... ],
  "summary": { ... }
}
```

### Step 3: Claude Code でインポート
Claude Code に JSON を貼り付けて実行：
```
Import this Personal OS data: [JSONをここに貼り付け]
```

Claude Code がファイルに自動追記します。

---

## 📚 プロンプトの種類

### Master Prompt
**ファイル:** [master-prompt.md](./master-prompt.md)

全 12 カテゴリに対応した統合プロンプト。1 つのプロンプトで全体を分析したいときに使用。

**特徴:**
- 12 カテゴリの全検出パターンを含む
- JSON スキーマ準拠の出力
- 信頼度スコア付き
- 根拠（エビデンス）の自動記載

---

### Category-Specific Prompts
**フォルダ:** [category-prompts/](./category-prompts/)

各カテゴリに特化した深掘りプロンプト。特定のカテゴリをより詳しく分析したいときに使用。

#### 12 カテゴリ

1. **[01-core-principles.md](./category-prompts/01-core-principles.md)** - あなたのアイデンティティ、信念、美学
2. **[02-values.md](./category-prompts/02-values.md)** - 価値観階層、人生で大事なもの
3. **[03-goals.md](./category-prompts/03-goals.md)** - ビジョン、目標、夢
4. **[04-decision-logic.md](./category-prompts/04-decision-logic.md)** - 判断フレームワーク
5. **[05-constraints.md](./category-prompts/05-constraints.md)** - 制約条件、限界
6. **[06-life-log.md](./category-prompts/06-life-log.md)** - 最近の出来事、学び
7. **[07-skills.md](./category-prompts/07-skills.md)** - スキル、強み、人脈
8. **[08-risks-failures.md](./category-prompts/08-risks-failures.md)** - 失敗、盲点、教訓
9. **[09-reflection.md](./category-prompts/09-reflection.md)** - 振り返り、パターン認識
10. **[10-personal-history.md](./category-prompts/10-personal-history.md)** - 自分史、キャリア
11. **[11-personality.md](./category-prompts/11-personality.md)** - 性格、気質
12. **[12-influences.md](./category-prompts/12-influences.md)** - 影響を受けた人、本、アイデア

---

## 💡 使い方ガイド

### パターン 1: 全体分析（Master Prompt を使う場合）

**推奨:** 初期セットアップ時や大きな転機のとき

```
1. [master-prompt.md](./master-prompt.md) をコピー
2. ChatGPT に貼り付けて実行
3. 全 12 カテゴリの JSON を取得
4. Claude Code でインポート
```

### パターン 2: 深掘り分析（Category-Specific Prompt を使う場合）

**推奨:** 特定の分野をより詳しく掘り下げたいとき

```
1. 特定カテゴリの Prompt をコピー
   例: [03-goals.md](./category-prompts/03-goals.md)
2. ChatGPT に貼り付けて実行
3. そのカテゴリに特化した JSON を取得
4. Claude Code でインポート
```

### パターン 3: 連続分析（複数の Prompt を組み合わせる場合）

**推奨:** 毎週・毎月、特定の Prompt を定期的に実行

例えば毎月：
- 月初: [03-goals.md](./category-prompts/03-goals.md) で目標進捗を確認
- 月中: [08-risks-failures.md](./category-prompts/08-risks-failures.md) で学びを記録
- 月末: [09-reflection.md](./category-prompts/09-reflection.md) で振り返り

---

## 📊 出力フォーマット

すべてのプロンプトは以下の JSON フォーマットで出力します：

```json
{
  "extraction_metadata": {
    "analyzed_at": "2026-02-23T14:30:00Z",
    "conversation_length_turns": 15,
    "total_extractions": 8,
    "confidence_threshold": 0.70
  },
  "extractions": [
    {
      "id": "extraction_001",
      "category": "01_コア・原則",
      "file": "アイデンティティ.md",
      "section": "核となるアイデンティティ",
      "extracted_content": "...",
      "evidence": "...",
      "confidence": 0.88,
      "suggested_format": "..."
    }
  ],
  "summary": {
    "strongest_themes": [...],
    "missing_data": [...],
    "recommendations": [...]
  }
}
```

---

## ⚙️ Claude Code での自動インポート

JSON を受け取った Claude Code は以下を実行します：

1. **JSON バリデーション** - スキーマ準拠を確認
2. **信頼度フィルタリング** - 低信頼度項目は確認要求
3. **コア原則チェック** - `01_コア・原則/` の変更は承認要求
4. **矛盾検出** - 既存内容と矛盾する場合は警告
5. **追記実行** - ファイルに自動追記（上書きしない）

---

## 📋 ベストプラクティス

### ✅ 良い会話の特徴
- 具体的な例や物語を交える
- 価値観や信念を明示的に述べている
- 同じアイデアが複数回確認されている
- 感情的な言語を使っている（「好き」「嫌い」など）
- 明確な対比がある（「X より Y を優先」など）

### ❌ 避けるべき会話
- 曖昧な仮定法（「もしかしたら...」）
- 他人の話を自分のものと混同
- 純粋な事実情報（文脈なし）
- 矛盾した発言（明確化なし）

### 💡 抽出を改善するためのコツ

**特に効果的な質問:**
- "あなたの核となる価値観は何ですか？"
- "10 年後、あなたはどうなっていたいですか？"
- "最大の失敗は何で、何を学びましたか？"
- "どのようにして重要な決断をしますか？"
- "誇りに思うスキルは何ですか？"

---

## 🔍 信頼度スコアについて

すべての抽出は **0.70 ～ 1.0** の信頼度スコア付きです：

- **0.95** - 直接的で明示的な発言（「私は X を信じている」）
- **0.85** - 明確な言い換え
- **0.75** - 複数の発言からの合理的な推論
- **< 0.70** - 抽出しない（推測に頼りすぎ）

Claude Code がインポートする際：
- **信頼度 ≥ 0.80** - 自動追記
- **0.70 ～ 0.79** - ユーザーに確認要求
- **< 0.70** - 抽出対象外

---

## 📁 ファイル構成

```
prompts/
├── README.md                              # このファイル
├── master-prompt.md                       # 統合抽出プロンプト
├── category-prompts/                      # カテゴリ別プロンプト
│   ├── 01-core-principles.md
│   ├── 02-values.md
│   ├── 03-goals.md
│   ├── 04-decision-logic.md
│   ├── 05-constraints.md
│   ├── 06-life-log.md
│   ├── 07-skills.md
│   ├── 08-risks-failures.md
│   ├── 09-reflection.md
│   ├── 10-personal-history.md
│   ├── 11-personality.md
│   └── 12-influences.md
├── examples/                              # 使用例
│   ├── sample-conversation.txt
│   ├── sample-extraction.json
│   └── import-result.md
└── guides/                                # 詳細ガイド
    ├── how-to-use.md
    └── troubleshooting.md
```

---

## 🆘 よくある質問

### Q: どのプロンプトから始めるべき？
**A:** Master Prompt から始めることをお勧めします。初期セットアップ時には全 12 カテゴリを一度に分析するのが効率的です。その後は Category-Specific Prompts で定期的に更新します。

### Q: ChatGPT と Claude どちらで実行する？
**A:** このプロンプト集は ChatGPT 用です。分析結果を Claude Code に渡してインポートします。

### Q: 自分の会話をどこから取得する？
**A:** ChatGPT の会話履歴をコピー&ペーストしてください。テキスト形式なら何でも対応します。

### Q: 既存の Personal OS データを上書きされない？
**A:** 安心してください。すべて**追記モード**です。既存のデータは保持され、新しい情報が追加されるだけです。

---

## 🔗 関連リソース

- [Personal OS 本体](../README.md) - メインリポジトリ
- [Auto-Learning Guide](../00_Auto_Learning_Guide.md) - 自動学習のフレームワーク
- [Portfolio](https://portfolio1-chi-rouge.vercel.app) - Personal OS の紹介

---

## 📝 Version History

### v1.0.0 (2026-02-23)
- Initial release
- Master Prompt + 12 Category-Specific Prompts
- Complete documentation
- Examples included

---

## 💬 Feedback

問題が発生した場合や改善提案がある場合は、GitHub の Issue で報告してください。

**Happy extracting! 🚀**
