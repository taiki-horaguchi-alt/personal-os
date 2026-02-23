# Category 04: Decision Logic (判断ロジック) - Deep Dive Prompt v1.0.0

## Purpose

Extract **how you make decisions**: your frameworks, criteria, and problem-solving approach.

---

## Key Questions

- **How do you decide between important options?**
- **What's your decision-making process?**
- **What factors do you consider? In what order?**
- **Do you trust your gut or prefer data?**
- **What's a recent important decision? Walk me through how you made it.**
- **How do you handle uncertainty or missing information?**
- **Do you gather more information or decide quickly?**

**Listen for:**
- "I decide by..."
- "My process is..."
- "I consider X, then Y, then Z"
- "I trust my intuition when..."
- "I need data when..."

---

## Extraction Template

```json
{
  "category": "04_判断ロジック",
  "file": "基本判断フレームワーク.md",
  "extracted_content": "[Decision framework or criteria]",
  "evidence": "[Example decision with explanation]",
  "suggested_format": "## [Framework Name]\n1. [Step 1]\n2. [Step 2]\n3. [Step 3]",
  "confidence": 0.85
}
```

---

## Example

**If someone said:**
> "I always start by getting the facts straight. Then I brainstorm all possible options without judging. Then I evaluate each option against my core values - does it align? Then I look at practical factors like cost and timeline. Finally, I go with my gut feeling to pick the best one."

**Extract:**
```json
{
  "file": "基本判断フレームワーク.md",
  "extracted_content": "Decision Framework: (1) Facts/Context, (2) Generate Options, (3) Values Alignment Check, (4) Practical Factors, (5) Gut Feel",
  "confidence": 0.90
}
```

---

## Version History

### v1.0.0 (2026-02-23)
- Initial release
