# Category 11: Personality Profile (性格プロファイル) - Deep Dive Prompt v1.0.0

## Purpose

Extract **personality traits and temperament** that characterize how you naturally operate.

---

## Key Questions

- **Are you introverted or extroverted?**
- **How do you typically respond to stress?**
- **Are you organized/chaotic? Detail-oriented/big-picture?**
- **How do you react to change?**
- **Risk-taking or conservative?**
- **Emotional/logical?**
- **How would friends describe your personality?**

**Listen for:**
- "I'm an introvert..."
- "Under stress I..."
- "I'm naturally..."
- "People describe me as..."
- "My personality is..."

---

## Big Five Framework

Consider extracting if mentioned:
- **Openness:** Curiosity, creativity, imagination
- **Conscientiousness:** Organization, discipline, reliability
- **Extraversion:** Sociability, assertiveness, energy
- **Agreeableness:** Cooperation, empathy, kindness
- **Neuroticism:** Emotional stability, anxiety, stress responses

---

## Extraction Template

```json
{
  "category": "11_性格プロファイル",
  "file": "ビッグファイブ分析.md",
  "trait": "[Personality trait or Big Five dimension]",
  "extracted_content": "[How person describes this trait in themselves]",
  "evidence": "[Examples of how this trait shows up]",
  "confidence": 0.85
}
```

---

## Version History

### v1.0.0 (2026-02-23)
- Initial release
