# Category 10: Personal History (自分史) - Deep Dive Prompt v1.0.0

## Purpose

Extract **your timeline and career trajectory** to understand patterns in your development.

---

## Key Questions

### Life Timeline
- **What are major chapters or phases in your life?**
- **Turning points or significant transitions?**
- **Formative experiences that shaped you?**
- **Where have you lived?**
- **Major life changes?**

**Listen for:**
- "Back when..."
- "That period was about..."
- "My life changed when..."
- "I moved to..."

### Career History (Work_History)
- **Jobs you've held?**
- **Progression and growth?**
- **Key learnings from each role?**
- **Why you changed jobs?**
- **Industries or sectors?**

**Listen for:**
- "I worked at..."
- "In that role, I..."
- "I left because..."
- "That job taught me..."

---

## Extraction Template

```json
{
  "category": "10_自分史",
  "file": "README.md | Work_History.md",
  "section": "[Time period or role name]",
  "extracted_content": "[Historical event or career position]",
  "evidence": "[How person described this period]",
  "suggested_format": "## [Period or Role]\n**Time:** [When]\n**What happened:** [Event/Role]\n**Learning:** [What this taught you]",
  "confidence": 0.85
}
```

---

## Version History

### v1.0.0 (2026-02-23)
- Initial release
