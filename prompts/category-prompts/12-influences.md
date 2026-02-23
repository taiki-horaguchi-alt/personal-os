# Category 12: Influences (影響を受けたもの) - Deep Dive Prompt v1.0.0

## Purpose

Extract **people, books, ideas, and media that shaped your thinking** and continue to influence you.

---

## Key Questions

### People (People)
- **Who has influenced you most?**
- **Mentors, role models, or inspiring people?**
- **What did they teach you?**
- **People you admire and why?**

**Listen for:**
- "I was influenced by..."
- "X taught me..."
- "I look up to..."
- "My mentor was..."

### Books & Media (Books_Media)
- **Books that changed how you think?**
- **Movies, podcasts, articles that resonated?**
- **Ideas or philosophies you follow?**
- **What do you read/listen to?**

**Listen for:**
- "This book changed my..."
- "I'm inspired by..."
- "Reading/listening to..."
- "Philosophy I follow..."

### Philosophies & Ideas
- **What ideas guide your life?**
- **Frameworks or concepts you believe in?**
- **Values you adopted from others?**

**Listen for:**
- "I believe in the concept of..."
- "X's philosophy influences me..."
- "I live by..."

---

## Extraction Template

```json
{
  "category": "12_影響を受けたもの",
  "file": "README.md | [Specific influence file]",
  "influence_type": "person | book | idea | media",
  "extracted_content": "[Who/what influenced you and how]",
  "evidence": "[How they influenced your thinking]",
  "suggested_format": "**[Name/Title]** - [How it influenced you]",
  "confidence": 0.85
}
```

---

## Version History

### v1.0.0 (2026-02-23)
- Initial release
