# Category 08: Risks & Failures (リスクと失敗) - Deep Dive Prompt v1.0.0

## Purpose

Extract **lessons from past failures**, blind spots, and patterns to avoid repeating mistakes.

---

## Key Questions

### Failure Learnings (失敗した判断)
- **What's something that failed? What went wrong?**
- **Why did it fail? What was the root cause?**
- **What did you learn?**
- **How will you avoid repeating this?**
- **What would you do differently next time?**

**Listen for:**
- "I failed because..."
- "That didn't work because..."
- "I learned that..."
- "Next time I'll..."
- "The mistake was..."

---

### Blind Spots & Biases (盲点・バイアス)
- **What patterns do you notice about yourself?**
- **What do others see in you that surprises you?**
- **What mistakes do you repeat?**
- **What are you not good at recognizing in yourself?**
- **What would you be shocked to learn about yourself?**

**Listen for:**
- "I tend to..."
- "People tell me I'm..."
- "I keep doing X even though..."
- "My weakness is..."
- "I'm probably biased about..."

---

### Risk Management (リスク管理)
- **What could go wrong with your current plans?**
- **What risks worry you?**
- **How do you mitigate risks?**
- **What's your risk tolerance?**
- **What are you not worried about that maybe you should be?**

**Listen for:**
- "The risk of X is..."
- "I'm worried that..."
- "Could fail if..."
- "Mitigate by..."
- "My biggest concern is..."

---

## Quality Checkpoints

✅ **Extract These:**
- Specific failure stories with lessons
- Repeated patterns the person recognizes
- Root cause analysis
- Explicit learnings and prevention strategies
- Honest self-awareness

❌ **Don't Extract:**
- Vague "mistakes happen" statements
- Others' failures mistaken as personal
- Excuses without accountability
- Unprocessed failures (no learning yet)

---

## Extraction Template

```json
{
  "category": "08_リスクと失敗",
  "file": "失敗した判断.md | 盲点・バイアス.md | リスク管理.md",
  "section": "[Failure log entry | Blind spot | Risk]",
  "extracted_content": "[Failure description and learning]",
  "evidence": "[Story or example with specific details]",
  "suggested_format": "## [Date]: [Failure name]\n**Situation:** [What happened]\n**Learning:** [What you learned]\n**Prevention:** [How you'll avoid next time]",
  "confidence": 0.85
}
```

---

## Example

**If someone said:**
> "I once hired someone just because they had the right technical skills. Turns out they had terrible communication and didn't fit the team culture. He quit after 3 months and left us mid-project. I realized I was optimizing for the wrong thing. Now I always check both skills AND cultural fit before hiring."

**Extract:**

```json
{
  "file": "失敗した判断.md",
  "section": "失敗の記録",
  "extracted_content": "Hired based on technical skills without assessing cultural fit and communication ability. Hire quit after 3 months, disrupting project.",
  "evidence": "User: 'I hired someone just because they had the right technical skills... turns out they had terrible communication'",
  "suggested_format": "## [Date]: Hiring Without Cultural Fit Assessment\n**Situation:** Hired team member based solely on technical skills, overlooking communication and cultural fit assessment.\n**Learning:** Technical skills alone are insufficient; cultural alignment and communication ability are critical.\n**Prevention:** Evaluate both technical AND cultural fit; include team members in hiring interviews.",
  "confidence": 0.92
}
```

```json
{
  "file": "盲点・バイアス.md",
  "extracted_content": "Tends to over-optimize for specific criteria (e.g., technical skills) while missing broader context (e.g., team dynamics). Pattern of assuming one dimension of fit is sufficient.",
  "confidence": 0.88
}
```

---

## Version History

### v1.0.0 (2026-02-23)
- Initial release
