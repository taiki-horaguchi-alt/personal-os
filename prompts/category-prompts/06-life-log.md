# Category 06: Life Log (人生ログ) - Deep Dive Prompt v1.0.0

## Purpose

Extract **significant events, emotions, and learnings** from your recent experiences.

---

## Key Questions

### Major Events (Major_Events)
- **What significant events happened recently?**
- **Any milestones, achievements, or turning points?**
- **Good news or challenging moments?**
- **Travel, changes, or new experiences?**

**Listen for:**
- "Recently..."
- "Last month..."
- "A big thing that happened..."
- "A turning point was..."

### Emotions & Learnings (人生ログ)
- **How did you feel about these events?**
- **What did you learn?**
- **How did it change your perspective?**
- **What's your next action?**

**Listen for:**
- "I felt..."
- "That taught me..."
- "The lesson was..."
- "Next I'll..."

---

## Extraction Template

```json
{
  "category": "06_人生ログ",
  "file": "Major_Events.md | diary_template.md",
  "section": "[Event date/name]",
  "extracted_content": "[Event description + emotion + learning]",
  "evidence": "[Story as told by person]",
  "suggested_format": "## [Date]: [Event Name]\n**What happened:** [Event]\n**How I felt:** [Emotion]\n**What I learned:** [Learning]\n**Next action:** [What's next]",
  "confidence": 0.85
}
```

---

## Version History

### v1.0.0 (2026-02-23)
- Initial release
