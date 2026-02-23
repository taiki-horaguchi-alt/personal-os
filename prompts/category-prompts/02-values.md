# Category 02: Values (価値観) - Deep Dive Prompt v1.0.0

## Purpose

Extract what **truly matters** to you: your value hierarchy, how you balance competing priorities, and what gives your life meaning.

---

## Key Questions

### Value Hierarchy (価値観リスト)
- **What are your top 3 values?** (If you had to choose)
- **How would you rank these: growth, security, freedom, connection, impact, creativity, health, wealth?**
- **What's more important: doing what you love or making money?**
- **What would you sacrifice for your top value?**
- **How have your values changed over time?**

**Listen for:**
- "I value X above all else"
- "Top 3 things are..."
- "Non-negotiable values are..."
- Direct value statements

---

### Time & Money Trade-offs (時間と金銭のトレードオフ)
- **Would you rather have more time or more money?**
- **What's worth your time? What's not?**
- **Are there things you'd pay premium prices for to save time?**
- **What would you never charge for? What do you expect payment for?**
- **How do you allocate your most scarce resource (time/money)?**

**Listen for:**
- "I'd rather invest in..."
- "I'm willing to pay for..."
- "Time is more valuable because..."
- Trade-off language: "vs.", "rather than", "prefer"

---

### Ikigai - Why You Exist (生きがい)
- **What do you love doing?** (Activities that energize you)
- **What are you good at?** (Genuine strengths)
- **What does the world need from you?** (How you could contribute)
- **What could you be paid for?** (Economic viability)
- **Where is the intersection of these four?**

**Listen for:**
- "I'm passionate about..."
- "I'm gifted at..."
- "The world needs..."
- "I could make money by..."

---

### Freedom vs. Stability (自由と安定のトレードオフ)
- **Do you prefer autonomy/flexibility or structure/security?**
- **Would you rather have a guaranteed paycheck or the upside of a startup?**
- **How much risk can you tolerate?**
- **What level of predictability do you need?**
- **What would cause you to sacrifice freedom? Stability?**

**Listen for:**
- "I need stability because..."
- "I crave freedom to..."
- "I can't stand being constrained..."
- "I thrive with structure..."

---

## Quality Checkpoints

✅ **Extract These:**
- Explicit value statements
- Trade-off decisions
- Multiple confirmations
- Strong emotional language
- Real examples of values in action

❌ **Don't Extract:**
- Hypothetical "I probably would..."
- Others' values mistaken for personal values
- Vague aspirational statements

---

## Extraction Template

```json
{
  "category": "02_価値観",
  "file": "価値観リスト.md | 時間と金銭のトレードオフ.md | 生きがい.md | 自由と安定のトレードオフ.md",
  "section": "[Appropriate subsection]",
  "extracted_content": "[Clear value statement or trade-off decision]",
  "evidence": "[Quote(s) showing this value in action]",
  "confidence": 0.85
}
```

---

## Example

**If someone said:**
> "I've realized I value impact over money. I could make more as a consultant, but working on education technology feels more meaningful. Even if the startup fails, I'll have created something that helped kids learn."

**Extract:**
```json
{
  "file": "価値観リスト.md",
  "extracted_content": "Tier 1: Impact and meaning in work (higher priority than income optimization)",
  "confidence": 0.92
}
```

```json
{
  "file": "時間と金銭のトレードオフ.md",
  "extracted_content": "Willing to accept lower income for work that creates meaningful impact",
  "confidence": 0.90
}
```

```json
{
  "file": "生きがい.md",
  "extracted_content": "What I love: building educational technology. What I'm good at: software engineering. What the world needs: better learning tools. What I could make money from: EdTech products.",
  "confidence": 0.85
}
```

---

## Version History

### v1.0.0 (2026-02-23)
- Initial release
