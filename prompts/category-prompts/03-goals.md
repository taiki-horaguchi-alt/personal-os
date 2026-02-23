# Category 03: Goals (目標) - Deep Dive Prompt v1.0.0

## Purpose

Extract your **vision and aspirations** at different time horizons: where you're heading in 10 years, 3-5 years, 1 year, and next 1-3 months.

---

## Key Questions

### 10-Year Vision (ビジョン)
- **If you're wildly successful in 10 years, what does your life look like?**
- **What do you want to create or accomplish?**
- **What legacy do you want to leave?**
- **Who do you want to become?**
- **Where will you be living, what will you be doing?**

**Listen for:**
- "In 10 years, I hope to..."
- "My dream is..."
- "I want to build..."
- "I envision myself..."

---

### 3-5 Year Goals (長期目標)
- **What are your major goals for the next 3-5 years?**
- **What milestones matter in this timeframe?**
- **Career progression? Skill development? Life changes?**
- **What would feel like success?**

**Listen for:**
- "By year 3, I want to..."
- "In 5 years, I'll have..."
- "Next major step is..."

---

### 1-Year Goals (中期目標)
- **What are you working toward in the next 12 months?**
- **What would you be proud to accomplish?**
- **Key projects or milestones?**
- **Personal growth targets?**

**Listen for:**
- "This year I want to..."
- "By end of year, I need to..."
- "12-month goal is..."

---

### 1-3 Month Goals (短期目標)
- **What's your next immediate focus?**
- **What are you working on right now?**
- **Quick wins you want to achieve?**
- **What's blocking progress on larger goals?**

**Listen for:**
- "Next thing I'm doing is..."
- "Right now I'm focused on..."
- "This week/month I want to..."

---

## Quality Checkpoints

✅ **High Confidence:**
- Specific, measurable goals
- Timeline clearly stated
- Multiple mentions across conversation
- Emotional commitment evident
- Concrete examples

❌ **Low Confidence:**
- Vague aspirations ("be successful")
- Hypothetical ("I could maybe...")
- Someone else's goal mistaken as personal
- Wishful thinking without commitment

---

## Extraction Template

```json
{
  "category": "03_目標",
  "file": "ビジョン.md | 長期目標.md | 中期目標.md | 短期目標.md",
  "section": "[10-year vision | 3-5 year goals | 1 year | 1-3 months]",
  "extracted_content": "[Specific goal or vision statement]",
  "evidence": "[Quote(s) showing goal commitment]",
  "confidence": 0.85,
  "suggested_format": "[How to phrase this in Personal OS]"
}
```

---

## Example

**If someone said:**
> "My dream is to start my own AI consultancy focused on helping nonprofits. Over the next 5 years, I need to build expertise in ML and develop a network of nonprofit leaders. This year, I'm learning advanced ML techniques and attending nonprofit conferences. Right now I'm taking Andrew Ng's deep learning course."

**Extract:**

```json
{
  "file": "ビジョン.md",
  "extracted_content": "Founding an AI consultancy that serves nonprofits",
  "confidence": 0.93
}
```

```json
{
  "file": "長期目標.md",
  "extracted_content": "Build ML expertise and develop network of nonprofit leaders within 5 years",
  "confidence": 0.90
}
```

```json
{
  "file": "中期目標.md",
  "extracted_content": "Develop advanced ML skills and attend nonprofit conferences",
  "confidence": 0.88
}
```

```json
{
  "file": "短期目標.md",
  "extracted_content": "Complete Andrew Ng's deep learning course",
  "confidence": 0.95
}
```

---

## Version History

### v1.0.0 (2026-02-23)
- Initial release
