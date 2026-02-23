# Personal OS Extraction Prompts

自分の会話からPersonal OSのデータを自動抽出するためのプロンプト集です。

## 🎯 このプロンプト集でできること

- **ChatGPT で会話を分析** - あなたの会話履歴から Personal OS に入れるべき情報を自動検出
- **構造化データを生成** - JSON形式で整理されたデータを出力
- **Claude Code で簡単インポート** - JSONを貼り付けるだけで Personal OS ファイルに追記

---

## 🚀 推奨される使い方：12 回に分けて実行

**各カテゴリを 1 つずつ深掘りして、計 12 回実行します。**

### なぜ 12 回に分ける？

| 方式 | メリット | デメリット |
|------|---------|---------|
| Master Prompt（1回） | 時間が短い | 各カテゴリが浅くなりやすい |
| **Category Prompts（12回）⭐推奨** | **各カテゴリを深掘りできる** | 時間がかかる |

**深さの比較：**
```
❌ Master Prompt での「目標」（1回で全カテゴリ）
「10年ビジョン：AI 企業を立ち上げたい」（短い）

✅ Category Prompt 03-goals での「目標」（1 回で 1 カテゴリ）
「10年ビジョン：AI を民主化する企業を立ち上げたい。
 理由：『技術は一部の専門家だけのものではない』という信念
 成功指標：『非技術者でも使えること』
 現在の課題：資金調達、初期チーム構築
 今年のマイルストーン：MVP 完成
 実現への障害：開発リソース不足」（詳しい、背景がある）
```

---

## 📅 実行スケジュール（推奨例）

```
【Week 1】  01_Core Principles
【Week 2】  02_Values
【Week 3】  03_Goals
【Week 4】  04_Decision Logic
【Week 5】  05_Constraints
【Week 6】  06_Life Log
【Week 7】  07_Skills & Assets
【Week 8】  08_Risks & Failures
【Week 9】  09_Reflection
【Week 10】 10_Personal History
【Week 11】 11_Personality Profile
【Week 12】 12_Influences

完了！ Personal OS が 12 カテゴリすべて蓄積される ✅
```

---

## 1 回の実行フロー（例：Week 1 - Core Principles）

### Step 1: プロンプトをコピー

```
[category-prompts/01-core-principles.md] を開く
→ 全文をコピー（Ctrl+A, Ctrl+C）
```

### Step 2: ChatGPT で実行

```
1. ChatGPT で新規チャット
2. [01-core-principles.md のプロンプト] を貼り付け
3. 「---以下、あなたの会話です---」の下に、
   あなたのアイデンティティについての会話を貼り付け
4. 送信 → ChatGPT が JSON を出力
```

### Step 3: Claude Code でインポート

```
Claude Code に以下をコピー&ペースト：

Import this Personal OS data: [ChatGPT から取得した JSON]
```

Claude Code が自動的に `01_コア・原則/` ファイルに追記 ✅

---

## 📚 プロンプト一覧

### 12 カテゴリの Category-Specific Prompts

| # | ファイル | 説明 | 実行タイミング |
|---|---------|------|---------------|
| 01 | [01-core-principles.md](./category-prompts/01-core-principles.md) | アイデンティティ、信念、美学 | Week 1 |
| 02 | [02-values.md](./category-prompts/02-values.md) | 価値観階層、人生で大事なもの | Week 2 |
| 03 | [03-goals.md](./category-prompts/03-goals.md) | ビジョン、目標、夢 | Week 3 |
| 04 | [04-decision-logic.md](./category-prompts/04-decision-logic.md) | 判断フレームワーク | Week 4 |
| 05 | [05-constraints.md](./category-prompts/05-constraints.md) | 制約条件、限界 | Week 5 |
| 06 | [06-life-log.md](./category-prompts/06-life-log.md) | 最近の出来事、学び | Week 6 |
| 07 | [07-skills.md](./category-prompts/07-skills.md) | スキル、強み、人脈 | Week 7 |
| 08 | [08-risks-failures.md](./category-prompts/08-risks-failures.md) | 失敗、盲点、教訓 | Week 8 |
| 09 | [09-reflection.md](./category-prompts/09-reflection.md) | 振り返り、パターン認識 | Week 9 |
| 10 | [10-personal-history.md](./category-prompts/10-personal-history.md) | 自分史、キャリア | Week 10 |
| 11 | [11-personality.md](./category-prompts/11-personality.md) | 性格、気質 | Week 11 |
| 12 | [12-influences.md](./category-prompts/12-influences.md) | 影響を受けた人、本、アイデア | Week 12 |

---

## 📖 参考：Master Prompt について

[master-prompt.md](./master-prompt.md) は全 12 カテゴリに対応した統合プロンプトです。

**用途:**
- 初期セットアップ時に全体を一度に見たい場合
- 時間がない場合の緊急用

**注意:** 1 回で全部やろうとすると、各カテゴリが浅くなりやすいため、通常は Category-Specific Prompts の使用を推奨します。

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
- 「なぜ」が複数回聞かれている

### ❌ 避けるべき会話
- 曖昧な仮定法（「もしかしたら...」）
- 他人の話を自分のものと混同
- 純粋な事実情報（文脈なし）
- 矛盾した発言（明確化なし）
- 1 文で終わる説明

### 💡 抽出を改善するためのコツ

**各カテゴリプロンプトに組み込まれた「Why x3」フレームワーク:**

```
Q: 「あなたの価値観は？」
A: 「成長が大事」

Q: 「なぜ？」（Why 1）
A: 「新しいことを学ぶのが好きだから」

Q: 「なぜ学ぶのが好き？」（Why 2）
A: 「世界がより理解できるようになるから」

Q: 「なぜそれが重要？」（Why 3）
A: 「人生の質が変わるから。具体的には 2023 年に XX に挑戦して...」
```

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
├── master-prompt.md                       # 統合抽出プロンプト（参考）
├── category-prompts/                      # ⭐ カテゴリ別プロンプト（推奨）
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

### Q: Master Prompt と Category Prompts、どっちを使う？
**A:** Category Prompts を推奨します。1 カテゴリ 1 回で深掘りできるため、より詳細で質の高いデータが得られます。12 週間で完成させるイメージです。

### Q: ChatGPT と Claude どちらで実行する？
**A:** このプロンプト集は ChatGPT 用です。分析結果を Claude Code に渡してインポートします。

### Q: 自分の会話をどこから取得する？
**A:** ChatGPT の会話履歴をコピー&ペーストしてください。テキスト形式なら何でも対応します。

### Q: 既存の Personal OS データを上書きされない？
**A:** 安心してください。すべて**追記モード**です。既存のデータは保持され、新しい情報が追加されるだけです。

### Q: 1 週間に複数カテゴリやってもいい？
**A:** もちろんです。スケジュールはガイドなので、好きなペースで進めてください。

---

## 🔗 関連リソース

- [Personal OS 本体](../README.md) - メインリポジトリ
- [how-to-use.md](./guides/how-to-use.md) - 詳細な使い方ガイド
- [Auto-Learning Guide](../00_Auto_Learning_Guide.md) - 自動学習のフレームワーク
- [Portfolio](https://portfolio1-chi-rouge.vercel.app) - Personal OS の紹介

---

## 📝 Version History

### v1.1.0 (2026-02-23)
- **推奨方法を変更**: Master Prompt（1回）→ Category Prompts（12回）に
- 12 週間スケジュールを追加
- 各週での実行フロー を明確化
- 深さの比較表を追加

### v1.0.0 (2026-02-23)
- Initial release
- Master Prompt + 12 Category-Specific Prompts
- Complete documentation
- Examples included

---

## 💬 Feedback

問題が発生した場合や改善提案がある場合は、GitHub の Issue で報告してください。

**12 週間で Personal OS を完成させよう！ 🚀**
