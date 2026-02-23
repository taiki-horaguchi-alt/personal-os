# Category 01: Core Principles - Deep Dive Prompt v1.0.0

## Purpose

Extract deep insights about **who you are** at your core: your identity, values, beliefs, communication style, aesthetics, and emotional triggers.

---

## Key Questions to Answer - 深掘り版

### Identity & Positioning (アイデンティティ)

**Q1: How do you describe yourself in one sentence?**
- Follow-up: 「なぜそう思う？」「誰がそう見ている？」「いつからそう考えている？」

**Q2: What roles or titles matter most to you?** (Professional, personal, social roles)
- Follow-up: 「なぜそのロール？」「やらされているのか、やりたいのか？」「それをやることで何を成し遂げたい？」「今、それにどのくらい時間を使っている？」

**Q3: What do you want to be known for?** (Legacy, impact)
- Follow-up: 「具体的には？」「人生の終わりに振り返って何を達成したい？」「今の行動はそれに向かっている？」「邪魔になっているものは？」

**Q4: What's your unique perspective or angle?** (What do you see that others don't?)
- Follow-up: 「なぜそう見える？」「経験は？」「誰がそれに気づいた？」「それが活きた場面は？」

**Q5: How do you want to be remembered?** (Character traits, impact)
- Follow-up: 「どういう場面で？」「誰に覚えていてほしい？」「今、それに向かっている？」「完全には達成していない理由は？」

**Listen for patterns:**
- "I'm the person who..." → 「その根拠？実例？何回そう言われた？」
- "I'm known for..." → 「誰に知られている？いつからそう見られている？意図的か自然か？」
- "My brand is..." → 「ブランドをどう構築した？その構築過程は？失敗は？」
- Identity metaphors ("I'm a bridge...", "I'm the glue...") → 「なぜそのメタファー？具体的には何と何をつなぐ？その役割でどう成功したか？」
- **最小要件:** 各セクションで 150 文字以上、背景と根拠を含める

---

### Values & Aesthetics (美学・価値観)

**Q1: What feels beautiful or elegant to you?** (In code, design, nature, relationships, work)
- Follow-up: 「なぜそれが美しい？」「誰も同意する？」「醜いものの対比は？」「その美学がないと何が起きる？」

**Q2: What feels ugly or offensive?** (What's the opposite of beautiful?)
- Follow-up: 「なぜそれが許せない？」「その相手にどう対応する？」「我慢したことは？」「結果は？」

**Q3: What would you never compromise on?** (Non-negotiables)
- Follow-up: 「理由は？」「例外はあるか？」「それを守るために何を失ったことがある？」「後悔していないか？」

**Q4: What do you stand for?** (Principles, causes)
- Follow-up: 「なぜそこまで？」「行動に移しているか？」「周囲の反対は？」「今のキャリアはそれに向かっているか？」

**Q5: If you could change one thing about the world, what would it be?**
- Follow-up: 「なぜそれ？」「その問題を見たことは？」「自分は何ができる？」「今、それをしているか？」

**Listen for patterns (最小 200 文字以上):**
- "Beautiful to me is..." → 「具体例？場面は？その美しさが損なわれたらどう？」
- "I absolutely can't stand..." → 「実例？その時どうした？今は？」
- "Elegance means..." → 「そこに至るまでの経験？」
- "Aesthetic preference is..." → 「いつからそう？影響？活かしている場面？」

---

### Core Beliefs (信念・前提)
- **What fundamental truths do you believe in?**
- **How do you see human nature?** (Optimistic? Realistic? Cynical?)
- **What assumptions guide your worldview?**
- **What do you believe is possible/impossible?**
- **Is the world ultimately fair/unfair, predictable/random?**

**Listen for:**
- "I believe that..."
- "In my experience, people are..."
- "The world works like..."
- "I assume..."

---

### Ethics & Non-Negotiables (倫理・やらないこと)
- **What would you never do, no matter the reward?**
- **Where are your ethical lines?**
- **What behaviors do you find unacceptable in others?**
- **What principles would you fight for?**
- **What's your code of conduct?**

**Listen for:**
- "I would never..."
- "That crosses a line for me"
- "Unethical would be..."
- "I refuse to..."

---

### Emotional Triggers (感情トリガー)
- **What gets you excited/energized?**
- **What drains or demotivates you?**
- **What makes you angry or frustrated?**
- **What creates a sense of meaning or fulfillment?**
- **What situations bring out your best self?**

**Listen for:**
- "I get excited when..."
- "Nothing is worse than..."
- "I thrive in environments where..."
- Emotional language: "love", "hate", "can't stand", "energized by"

---

### Communication Style (コミュニケーションスタイル)
- **How do you prefer to receive information?** (Detailed vs. summaries, written vs. verbal)
- **How do you like to give feedback or receive it?**
- **What's your communication preference?** (Direct vs. diplomatic, formal vs. casual)
- **How do you build trust with others?**
- **What communication styles rub you the wrong way?**

**Listen for:**
- "I prefer when people..."
- "I work best with..."
- "I hate when..."
- "My communication style is..."

---

### Decision-Making Style (認知・学習スタイル)
- **How do you process information?** (Big picture vs. details, visual vs. analytical)
- **How do you learn best?** (Reading, doing, watching, discussing)
- **What's your learning style?** (Fast learner? Methodical? Experimental?)
- **Do you prefer data or intuition?**
- **How do you handle ambiguity?**

**Listen for:**
- "I learn best by..."
- "I process information by..."
- "I like to understand the big picture first..."
- "I jump into details..."

---

## Quality Checkpoints

✅ **Strong Indicators (High Confidence):**
- Direct, specific self-descriptions
- Examples or stories illustrating values
- Multiple confirmations of same principle
- Clear emotional language
- Explicit "would never" statements

⚠️ **Medium Confidence:**
- General statements about preferences
- Inferred values from actions
- Statements with caveats or exceptions

❌ **Do Not Extract:**
- Speculative statements ("I might be...")
- Statements about others ("most people...")
- Hypothetical scenarios without clear values
- Vague or ambiguous language

---

## Extraction Template

For each item you extract, use this format in your JSON:

```json
{
  "id": "extraction_NNN",
  "category": "01_コア・原則",
  "file": "アイデンティティ.md | 美学・価値観.md | 信念・前提.md | etc.",
  "section": "核となるアイデンティティ | 視点・スタンス | etc.",
  "extracted_content": "[Clear, specific statement about identity/value]",
  "evidence": "[Quote(s) from conversation with surrounding context]",
  "confidence": 0.85,
  "suggested_format": "[How to phrase this in Personal OS format]",
  "requires_approval": false
}
```

---

## Example Deep Dive

**If someone said:**
> "I always choose elegance over expedience. Even when I'm under time pressure, I can't bring myself to write quick hacks. I spend those extra hours making code beautiful. People sometimes think I'm inefficient, but I know the investment pays off in maintainability. I just can't do ugly code."

**You would extract multiple items:**

```json
{
  "id": "extraction_001",
  "category": "01_コア・原則",
  "file": "美学・価値観.md",
  "extracted_content": "Elegance and maintainability are non-negotiable values, even under time pressure",
  "evidence": "User: 'I always choose elegance over expedience' and 'I just can't do ugly code'",
  "confidence": 0.95
}
```

```json
{
  "id": "extraction_002",
  "category": "01_コア・原則",
  "file": "倫理・やらないこと.md",
  "section": "やらないこと",
  "extracted_content": "Will not compromise on code quality or aesthetics, even under deadline pressure",
  "evidence": "User: 'Even when I'm under time pressure, I can't bring myself to write quick hacks'",
  "confidence": 0.93
}
```

```json
{
  "id": "extraction_003",
  "category": "01_コア・原則",
  "file": "アイデンティティ.md",
  "section": "核となるアイデンティティ",
  "extracted_content": "Code aesthete who prioritizes long-term maintainability over short-term speed",
  "evidence": "Pattern of emphasis on elegance and quality; willing to invest time despite pressure",
  "confidence": 0.88
}
```

---

## Follow-Up Questions

If someone has shared insights from this category, these follow-ups deepen extraction:

- "Can you give me a specific example of when you stood by this principle?"
- "Has anyone ever challenged this belief? How did you respond?"
- "How would your ideal colleague/friend embody this?"
- "What would someone who doesn't share this value do differently?"
- "When was the last time this value was tested?"

---

## Version History

### v1.0.0 (2026-02-23)
- Initial release
- 7 subcategories with detailed questions
- Quality checkpoints
- Extraction template
- Example deep dive
