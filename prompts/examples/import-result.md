# Import Result Example

This file shows what a Personal OS file looks like after importing extracted data.

---

## Example: 01_コア・原則/アイデンティティ.md

### Before Import

```markdown
# Identity - 自分は何者か

## 核となるアイデンティティ

### 自分の立ち位置
* Placeholder content...

### 視点・スタンス
* Placeholder content...
```

### After Import

```markdown
# Identity - 自分は何者か

## 核となるアイデンティティ

### 自分の立ち位置
* Placeholder content...
* **Technical-Business Bridge** - Translates between engineering and business perspectives to align teams around shared goals

### 視点・スタンス
* Placeholder content...

---

## [2026-02-23]: ChatGPT Auto-Extraction

**信頼度:** 0.92
**根拠:** User stated: 'I see myself as a translator between engineers and business people. I bridge the gap so both sides understand each other.'

**Technical-Business Bridge** - Translates between engineering and business perspectives to align teams around shared goals

---
```

---

## Example: 03_目標/ビジョン.md

### After Import

```markdown
# Vision - 10年後の将来像

## 10年ビジョン

Founding a purpose-driven company with a culture of deep collaboration and creative freedom

---

## [2026-02-23]: ChatGPT Auto-Extraction

**信頼度:** 0.90
**根拠:** User: 'In 10 years, I want to have founded something meaningful. A place where people genuinely enjoy coming to work, not just for money but because the work matters.'

Founding a purpose-driven company with a culture of deep collaboration and creative freedom. A place where people are attracted by meaningful work and maintained through genuine relationships.

---
```

---

## Example: 08_リスクと失敗/失敗した判断.md

### After Import

```markdown
# Failure Log - 失敗の記録

## 2024-XX: Overcommitment Without Capacity Planning

* **状況:** Committed team to ambitious project without assessing capacity. Everyone burned out, deadlines missed, client unhappy.
* **何が起きたか:** Signed up for impactful project that sounded great in the moment, but didn't have team resources to execute.
* **原因:** Overvalued excitement and impact potential without tempering with realistic assessment of team bandwidth.
* **学び（再発防止）:**
  * Always assess team readiness before committing to new projects
  * Impact potential must be balanced against realistic team capacity
  * "No" to exciting things is better than "yes" that leads to burnout

---

## [2026-02-23]: ChatGPT Auto-Extraction

**信頼度:** 0.89

#### Overcommitment Without Capacity Planning
- **Situation:** Committed team to ambitious project without assessing team capacity
- **Learning:** Impact potential must be balanced against realistic team capacity
- **Prevention:** Assess team readiness before committing to new projects

---
```

---

## Key Observations

### 1. Append-Only Pattern
- Original content is preserved
- New data is added with timestamp
- No existing content is overwritten

### 2. Metadata Included
- **信頼度 (Confidence):** Shows certainty level (0.70-1.0)
- **根拠 (Evidence):** Shows where the data came from
- **日付 (Date):** When it was extracted
- **Source:** Which prompt was used

### 3. Formatting Consistency
- Uses markdown format consistent with Personal OS
- Bullet points for lists
- Clear section headers
- Links between related concepts

### 4. Spacing and Readability
- Clear visual separation between dated entries
- Horizontal dividers `---` for clarity
- Multiple entries can coexist in same file

---

## Git Diff Example

When you commit imported data, `git diff` will show:

```diff
--- a/01_コア・原則/アイデンティティ.md
+++ b/01_コア・原則/アイデンティティ.md
@@ -5,6 +5,7 @@
 ### 自分の立ち位置
 * Placeholder content...
+* **Technical-Business Bridge** - Translates between engineering and business perspectives

@@ -15,3 +16,15 @@
 ### 視点・スタンス
 * Placeholder content...
+
+---
+
+## [2026-02-23]: ChatGPT Auto-Extraction
+
+**信頼度:** 0.92
+**根拠:** User stated: 'I see myself as a translator between engineers and business people...'
+
+**Technical-Business Bridge** - Translates between engineering...
```

---

## Import Statistics

From the sample extraction JSON above:

| Metric | Value |
|--------|-------|
| Total Extractions | 8 |
| High Confidence (≥0.85) | 6 |
| Medium Confidence (0.75-0.84) | 2 |
| Low Confidence (< 0.75) | 0 |
| Categories Covered | 7 / 12 |
| Files Modified | 7 |
| Conflict Flags | 0 |
| Approval Required | 0 |

---

## Next Steps After Import

1. **Review Changes**
   ```bash
   git diff
   # Review all changes before committing
   ```

2. **Commit**
   ```bash
   git add .
   git commit -m "Personal OS: ChatGPT extraction from 2026-02-23"
   ```

3. **Continuous Integration**
   - GitHub Actions automatically runs validation
   - Checks JSON schema compliance
   - Validates file paths and formatting

4. **Track Trends**
   - Use git log to see evolution over time
   - `git log --oneline` shows all extraction dates
   - `git show <commit>` shows what was extracted when

---

## This is What Good Import Looks Like

✅ **What This Example Demonstrates:**

- Data is properly appended (not overwritten)
- Metadata (confidence, evidence) is included
- Formatting matches Personal OS style
- Multiple entries can coexist
- Git history is clean and traceable
- No duplicate data
- Sensible categorization

❌ **Common Mistakes to Avoid:**

- Overwriting existing sections
- Missing timestamps
- Forgetting confidence scores
- No evidence/source attribution
- Formatting inconsistencies
- Contradicting previous entries without flagging

---

## Summary

This example shows the typical workflow:

1. **Raw Conversation** → ChatGPT with prompt
2. **Extracted JSON** → Claude Code receives this
3. **Imported Data** → Appended to Personal OS files
4. **Committed Changes** → git history tracks evolution

Each import adds a new timestamped section while preserving all historical data.

**Result:** A growing, time-series record of your Personal OS that reflects your evolution while maintaining full audit trail.

---

Generated: 2026-02-23
