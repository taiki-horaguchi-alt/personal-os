# Troubleshooting Guide - よくある問題と解決策

このガイドでは、Personal OS Extraction Prompts 使用時に発生しやすい問題と解決方法を説明します。

---

## ChatGPT での問題

### 1. プロンプトが認識されない

**症状:** ChatGPT がプロンプトを無視したり、無関係の応答をする

**原因:**
- プロンプトが不完全にコピーされた
- Chat のコンテキストが混乱している

**解決:**
```
1. ChatGPT を再読み込み（F5キー）
2. 新規チャットを開く
3. Master Prompt をもう一度全文コピー&ペースト
4. 「Thank you for this prompt. I understand my role as a Personal OS data extractor.」などの確認応答を待つ
```

---

### 2. JSON が出力されない

**症状:** ChatGPT がテキスト形式で回答し、JSON を出力しない

**原因:**
- プロンプトが最後まで貼り付けられていない
- モデルの推論が長すぎて打ち切られた

**解決:**
```
1. Message を再送信：
   "Output only valid JSON. No explanations. Start with { and end with }"

2. もう一度会話を送信:
   "Please analyze this and output JSON"

3. それでもダメな場合、ChatGPT を再起動
```

---

### 3. JSON が途中で切れている

**症状:**
```json
{
  "extraction_metadata": { ... },
  "extractions": [
    { "id": "extraction_001", ... },
    ...
  ]
}
```
の最後が不完全

**原因:** Token 上限に達した

**解決:**
```
1. ChatGPT に「JSON の残りを出力してください」と言う
2. 前のメッセージを参照させる：
   "Please continue from extraction_XXX:"

3. 会話を短くして再度チャレンジ（5-10ターンまで）
```

---

### 4. 信頼度スコアが0.70未満ばかり

**症状:** ほとんどの抽出が `"confidence": 0.65` などで、Claude Code が確認を要求する

**原因:**
- 会話が曖昧
- 推測に頼りすぎ
- 具体例がない

**改善:**
```
会話例（改善前）:
User: 「仕事は大事です」

会話例（改善後）:
User: 「私にとって仕事は、人生で最も大事な3つ（家族、成長、仕事）のうちの1つです」
User: 「その理由は、仕事を通じて自分のスキルを磨き、チームに貢献できるから」
User: 「具体的には、毎日『誰かの役に立てたか』を基準に評価しています」
```

**チェックリスト:**
- [ ] 直接的な発言を含めているか？（「私は...」）
- [ ] 具体的な例を含めているか？
- [ ] 同じアイデアが複数回言及されているか？
- [ ] 感情的な言語を使っているか？

---

## Claude Code でのインポート問題

### 5. 「Invalid JSON」エラー

**症状:**
```
Error: Invalid JSON
Expected { at position 0
```

**原因:**
- JSON が `{` で始まっていない
- ChatGPT の前置きテキストが含まれている
- エスケープ文字の問題

**解決:**
```
1. JSON バリデータを使用：https://jsonlint.com
2. エラー位置を確認
3. エディタで修正
4. ChatGPT に「Please output only valid JSON, no explanation」

修正例：
❌ 「Here's the extraction:
{...}」

✅ 「{...}」（JSONだけ）
```

---

### 6. 「ファイルが見つからない」エラー

**症状:**
```
Error: File not found at
c:\Users\steam\Dev\Projects\personal-os\01_コア・原則\アイデンティティ.md
```

**原因:**
- Personal OS テンプレートが未初期化
- ファイル名が日本語で文字化けしている
- パスが間違っている

**解決:**
```
PowerShell で実行:
cd c:\Users\steam\Dev\Projects\personal-os
.\create_templates_1.ps1

または手動で確認:
dir "c:\Users\steam\Dev\Projects\personal-os" /s
```

---

### 7. 既存データが上書きされた

**症状:**
```
git diff ファイル名
- [古いデータ]
+ [新しいデータだけ]
```

**原因:** Claude Code が追記モードの代わりに上書きした

**復旧:**
```bash
# 1. 直前のコミットに戻す
git log --oneline

# 2. ハッシュを確認してリセット
git reset --hard <commit-hash>

# 3. またはファイルだけを復旧
git checkout HEAD~1 -- "01_コア・原則/ファイル名.md"

# 4. Claude Code に「追記モード（Append mode）」で再実行をリクエスト
```

---

### 8. 「Core Changes Require Approval」で止まった

**症状:** インポートが実行されず、ユーザー承認を待っている

**原因:** `01_コア・原則/` ファイルへの変更が検出された

**対処:**
```
1. 提案内容を確認
2. 同意なら：「Approve」と応答
3. 修正が必要なら：「Reject and suggest...」

重要：コア原則の変更は慎重に。
新しいデータが本当に古い信念と異なるか確認してから承認。
```

---

## データ品質の問題

### 9. 矛盾する抽出データ

**症状:**
```
"extracted_content": "仕事を最優先にする"
（別の抽出）
"extracted_content": "人生の質が最優先"
```

**原因:** 実際の会話で矛盾している、または ChatGPT が誤解した

**解決:**
```
1. 元の会話を確認
2. Claude Code に矛盾を報告：
   "These two extractions conflict. Please review and comment."

3. 必要に応じて、1つを削除または修正
```

---

### 10. 重要なデータが抽出されない

**症状:** 明らかに Personal OS に入るべき情報が抽出リストにない

**原因:**
- 信頼度判定が厳しすぎた
- 検出パターンに該当しなかった
- 文脈が曖昧だった

**解決:**
```
1. 該当する Category-Specific Prompt を使用
2. 明示的に「この情報を抽出してください」と指示
3. 会話をもう一度、より詳しく述べる

例:
User: 「以前の失敗について。2024年、新機能のスケジュール見積が大幅に外れて...」
（ここで詳しく説明）
```

---

## パフォーマンスの問題

### 11. ChatGPT の応答が遅い

**症状:** 通常より 2-3 倍遅い、またはタイムアウト

**原因:**
- ChatGPT が混雑している（時間帯による）
- 会話履歴が長すぎる
- モデルの推論が複雑

**解決:**
```
1. 時間を変える（深夜よりも昼間が早い傾向）
2. 会話を短くする（最大 5-10 ターン）
3. Master Prompt ではなく Category-Specific Prompt を使用
4. ChatGPT Plus に升格（必要に応じて）
```

---

### 12. Token 上限に達した

**症状:** ChatGPT が「Token limit exceeded」エラーを返す

**原因:** 長い会話 + Master Prompt で合計 Token が多すぎる

**解決:**
```
1. 会話を分割（例：3つの会話に分けて実行）
2. 不要なテキストを削除
3. Category-Specific Prompt で1カテゴリずつ分析
```

---

## ワークフロー上の問題

### 13. ファイルが git で競合している

**症状:**
```
CONFLICT (content merge): ...
Merge conflict in ...
```

**原因:** 複数の機器や人物が同時に Personal OS ファイルを編集

**解決:**
```bash
# 競合の確認
git status

# 手動で解決するか、マージツールを使用
git mergetool

# または一方を選択
git checkout --ours <file>  # ローカル版を採用
git checkout --theirs <file> # リモート版を採用

# その後コミット
git add .
git commit -m "Resolve merge conflict"
```

---

### 14. データが重複している

**症状:** 同じ情報が複数回、ファイルに記載されている

**原因:** 複数回のインポートで同じデータが追加された

**解決:**
```
1. 重複を検出：
   git diff HEAD~1 | grep -A5 -B5 [内容]

2. 手動で削除
3. git commit -m "Remove duplicate entries"

予防:
- 同じ会話を複数回インポートしない
- インポート前に git diff で確認
```

---

## 一般的なヒント

### デバッグの基本フロー

```
1. エラーメッセージを読む
   → 正確に何が問題なのか？

2. 最小限のテストケースを試す
   → 短い会話で単一 Category-Specific Prompt を実行

3. ステップバイステップで確認
   → JSON は有効？ ファイルは存在？ 権限は？

4. Git でロールバック
   → 何か壊れたら、git reset で復旧可能
```

---

### サポートを求める場合

問題を報告する際は、以下を含めてください：

1. **症状の説明** - 何が起こったか？
2. **エラーメッセージ** - 正確なテキスト
3. **使用したプロンプト** - どのプロンプト？
4. **会話例** - 最小限の再現例
5. **環境情報** - Windows/Mac、ChatGPT バージョン
6. **既に試した解決策** - 何を試した？

---

## チェックリスト：問題が発生したら

- [ ] ChatGPT を再読み込みした？
- [ ] 新規チャットで試した？
- [ ] JSON バリデータを使用した？
- [ ] Personal OS ファイルが存在する？
- [ ] Git ステータスは clean？
- [ ] 会話をもっと短くして試す？
- [ ] 別の Category-Specific Prompt を試す？
- [ ] エラーメッセージを全文コピーした？

---

## 更新履歴

### v1.0.0 (2026-02-23)
- 初版公開
- 14 個の一般的な問題をカバー

---

**問題が解決しない場合は、GitHub Issue で報告してください。**

Happy troubleshooting! 🔧
