# How to Use - 詳細ガイド

Personal OS Extraction Prompts を使ってあなたの会話から Personal OS データを抽出する方法を、ステップバイステップで説明します。

---

## 準備するもの

- ✅ ChatGPT（無料版でOK）
- ✅ あなたの会話履歴（テキスト形式）
- ✅ Claude Code（インポート用）
- ✅ このプロンプト集から任意のプロンプト

---

## 方法 1: Master Prompt で全体分析（推奨：初回）

### 用途
- Personal OS を初期セットアップする
- 大きな転機や人生の節目に全体を分析したい
- 全 12 カテゴリを一度に確認したい

### ステップ

#### Step 1: Master Prompt を準備

```
1. このリポジトリの [master-prompt.md](../master-prompt.md) を開く
2. 全文をコピー（Ctrl+A → Ctrl+C）
```

#### Step 2: ChatGPT で新規チャットを開く

```
1. https://chatgpt.com を開く
2. 「新規チャット」をクリック
3. ChatGPT 4o または ChatGPT o1 を選択（o1推奨、より精密）
```

#### Step 3: Master Prompt を貼り付けて実行

```
1. ChatGPT のメッセージボックスに Master Prompt を貼り付け
2. 「送信」をクリック
3. 「Understood」などの返答を待つ
```

**例:**
```
[Master Prompt の全文がここに貼り付けられる]
```

#### Step 4: あなたの会話履歴を追加

Master Prompt に対して、以下のメッセージを送信：

```
Please analyze this conversation and extract Personal OS data.

---
[ここにあなたの会話履歴を貼り付け]
---

Output the structured JSON as specified in the prompt.
```

**会話履歴の形式:**
```
User: 「私は何者か」を考える際、最も大事なのは「本来の自分」を見つけることです。
User: 私の核となる価値観は、「人を喜ばせること」と「自分の成長」のバランスです。
User: 最近気づいたのは、短期的には利益を優先してしまうバイアスがあるということ。
User: でも長期的には、本当にやりたいのは AI を使って社会課題を解決することです。
```

#### Step 5: JSON 出力を確認

ChatGPT が構造化された JSON を出力します：

```json
{
  "extraction_metadata": { ... },
  "extractions": [ ... ],
  "summary": { ... }
}
```

**チェックポイント:**
- ✅ JSON は有効か？（`{` で始まり `}` で終わる）
- ✅ `extractions` 配列に複数のアイテムがあるか？
- ✅ `confidence` スコアが 0.70 以上か？
- ✅ `evidence` に根拠が記載されているか？

#### Step 6: JSON をコピー

```
1. JSON 全体を選択（ChatGPT のコピーボタンを使用）
2. コピー（Ctrl+C）
```

#### Step 7: Claude Code にインポート

Claude Code を開いて：

```
Import this Personal OS data: [JSONをここに貼り付け]
```

Claude Code が以下を自動実行：
- JSON をバリデート
- 低信頼度アイテムを確認
- コア原則変更を承認要求
- Personal OS ファイルに追記

---

## 方法 2: Category-Specific Prompt で深掘り分析

### 用途
- 特定カテゴリをより詳しく分析
- 月次・週次更新（例：毎月末に目標進捗を確認）
- マスタープロンプトより短い会話で分析

### ステップ

#### Step 1: カテゴリを選択

12 個のカテゴリから 1 つを選択：

```
例: 目標について深掘りしたい
→ [03-goals.md](../category-prompts/03-goals.md) を使用
```

#### Step 2: Category-Specific Prompt をコピー

```
1. 該当ファイルを開く
2. 全文をコピー
```

#### Step 3: ChatGPT に貼り付けて実行

```
1. 新規チャットを開く
2. Category-Specific Prompt を貼り付け
3. 「送信」をクリック
```

#### Step 4: あなたの会話を追加

```
[Category-Specific Prompt の後に]

Please analyze this conversation focusing on [Category Name].

---
[会話履歴]
---

Output structured JSON as specified.
```

#### Step 5～7: Master Prompt と同じプロセス

JSON を取得 → Claude Code でインポート

---

## 方法 3: 定期的な更新ワークフロー

### 毎日 (Daily)

**時間:** 5分

```
1. その日の会話を簡潔に記録
2. [06-life-log.md](../category-prompts/06-life-log.md) で分析
3. 新しい経験や学びを Personal OS に追加
```

**例：今日のメモ**
```
User: 今日はチームメンバーと新しいプロジェクトについて議論した。
User: 意見の対立があったが、相手の視点を理解しようと努めた。
User: その結果、予想外の良いアイデアが生まれた。
User: このプロセスから学んだのは「対立も創造的になることがある」ということ。
```

### 毎週 (Weekly)

**時間:** 20分

```
1. その週の会話・経験をまとめる
2. [08-risks-failures.md](../category-prompts/08-risks-failures.md) で失敗と学びを分析
3. [07-skills.md](../category-prompts/07-skills.md) で新しいスキル獲得を記録
```

### 毎月 (Monthly)

**時間:** 1時間

**推奨フロー:**
```
1. 月初: [03-goals.md](../category-prompts/03-goals.md)
   → 月の目標を設定

2. 月中: [08-risks-failures.md](../category-prompts/08-risks-failures.md)
   → 今月の失敗と学びを記録

3. 月末: [09-reflection.md](../category-prompts/09-reflection.md)
   → 月全体を振り返り、パターンを抽出
```

### 四半期・年次 (Quarterly/Yearly)

**時間:** 2-3時間

```
すべての Category-Specific Prompt を順番に実行
またはMaster Prompts で全体分析

得られたデータから：
- 新しい自分史を記録 [10-personal-history.md]
- コア原則の変更を検討 [01-core-principles.md]
- 長期目標の見直し [03-goals.md]
```

---

## トラブルシューティング

### Q: ChatGPT が JSON を出力しない

**原因:** プロンプトが不完全、または Chat が長すぎる

**解決:**
1. ChatGPT を再読み込み（F5）
2. 新規チャットで試す
3. Master Prompt を再度貼り付け
4. 会話を短くして試す（3-5ターン程度）

---

### Q: JSON が無効（シンタックスエラー）

**原因:** ChatGPT が JSON の途中で切れた、または形式が間違い

**確認:**
1. JSON が `{` で始まっているか？
2. JSON が `}` で終わっているか？
3. すべてのカンマが適切か？

**修正:**
1. ChatGPT に「JSON の残りを出力してください」と言う
2. それでもダメなら、JSON バリデータ（https://jsonlint.com）を使用

---

### Q: 信頼度スコアが低い（< 0.70）

**原因:** 会話が曖昧、推測が多い

**改善:**
1. より具体的な例を会話に含める
2. 直接的な発言（「私は...」）を増やす
3. 同じアイデアを複数回確認する
4. 感情的な言語を使う

**例（悪い）:**
```
User: 多分、目標があると思います。
User: 成功することが大事かもしれません。
```

**例（良い）:**
```
User: 私の 10 年ビジョンは AI を活用した起業です。
User: これは「人生に意味を作りたい」という核となる価値観から来ています。
User: 私は「やりがい」を「給料」より重視します。
```

---

### Q: Claude Code で「ファイルが見つからない」エラー

**原因:** Personal OS ファイルが正しい場所にない

**確認:**
```
c:\Users\steam\Dev\Projects\personal-os\
├── 01_コア・原則/
├── 02_価値観/
└── ...
```

**解決:**
1. PowerShell スクリプトで再生成：
   ```powershell
   cd c:\Users\steam\Dev\Projects\personal-os
   .\create_templates_1.ps1
   ```
2. または手動で欠けているファイルを作成

---

### Q: 既存の Personal OS データが上書きされた

**原因:** 追記モードが動作していない

**復旧:**
1. `git status` で変更を確認
2. `git diff [file]` で何が変わったか確認
3. `git checkout [file]` で復元
4. Claude Code に「追記モード」での再実行をリクエスト

---

## Tips & Best Practices

### 💡 より良い抽出のための会話テクニック

**具体性を増す**
```
❌ 「成功は大事」
✅ 「私にとって成功とは、自分が作ったものが世の中に良い影響を与えることです」
```

**例を含める**
```
❌ 「スキルがある」
✅ 「React と TypeScript で 5 年の経験があり、本番環境で 10+ プロジェクトをリード」
```

**意図を明示**
```
❌ 「これは大事」
✅ 「これが大事な理由は、自分のコア価値である『成長』に直結するから」
```

---

### 🔄 バージョン管理

毎回インポート後、Git にコミット：

```bash
git add -A
git commit -m "Personal OS: ChatGPT extraction from [date]"
git push origin main
```

このようにすることで：
- 時系列で Personal OS の変化を追跡可能
- 過去のバージョンに戻す際の復旧が容易
- GitHub で公開する場合、コミット履歴がドキュメント

---

### 📊 効果測定

毎月のデータ抽出から以下を測定：

1. **データの充実度**
   - 何個の抽出アイテムが得られたか
   - 各カテゴリのカバー率

2. **信頼度の向上**
   - 高信頼度（≥0.85）の割合
   - 低信頼度（< 0.70）の割合

3. **パターン認識**
   - 繰り返されるテーマ
   - 新しく浮かび上がったニーズ
   - 過去の決定との一貫性

---

## FAQ

### Q: 複数の会話を一度に分析できる？
**A:** はい。複数の会話を区切り文字で分けて一つのテキストにしてください。ただし ChatGPT のトークン上限があるため、推奨は最大 3-5 つの会話です。

### Q: 自分以外の人の Personal OS も作成できる？
**A:** テクニカルには可能ですが、本来は自己分析ツールです。他者のデータを分析する場合は、その人の許可を得てください。

### Q: ChatGPT 4 vs Claude でどちらを使うべき？
**A:** このプロンプト集は ChatGPT 専用です。Claude を使いたい場合は、プロンプトを若干修正（Claude 向けの指示に変更）する必要があります。

### Q: オフラインで実行できる？
**A:** いいえ。ChatGPT とのやり取りはクラウドベースです。ただしプロンプト自体はローカルで管理可能です。

---

## Next Steps

- Personal OS ファイルに追記されたデータを確認
- 月 1 回の定期分析スケジュールを設定
- GitHub リポジトリをスター ⭐ して最新アップデートをフォロー

**Happy analyzing! 🚀**
