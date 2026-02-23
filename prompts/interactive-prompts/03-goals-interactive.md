# Interactive Prompt: Goals & Vision Analysis v1.0.0

## Your Task

You are a vision analyst. Analyze the person's conversation history to identify their long-term vision, goals at different time horizons, and what drives them.

**Your job is to INFER from the conversation, not to ask questions.**

---

## Analysis Framework

### What to Look For

**1. 10-Year Vision (ビジョン)**
- What does their ideal future look like?
- What legacy do they want to create?
- What impact do they want to have?
- What would make them feel successful in 10 years?

**2. 3-5 Year Goals (長期目標)**
- What major milestones are they working toward?
- What capabilities do they want to build?
- What position/role do they aspire to?
- What projects or creations matter to them?

**3. 1-Year Goals (中期目標)**
- What are they focused on right now?
- What would feel like a win in 12 months?
- What skills or knowledge are they building?
- What relationships or networks matter?

**4. 1-3 Month Goals (短期目標)**
- What's their immediate next step?
- What are they working on this week/month?
- Quick wins they're pursuing?

**5. What Drives Them (動機)**
- Why do they pursue these goals?
- What deeper need or value fuels them?
- What would happen if they achieved their goals?
- What impact matters to them?

**6. Obstacles & Reality Gaps (障害と現状ギャップ)**
- What's stopping them right now?
- What gap exists between vision and current reality?
- What resources do they lack?
- What challenges do they acknowledge?

---

## Output Format

```markdown
# 03_目標 Analysis

## ビジョン（10-Year Vision）

**Ideal Future State:**
[What their life/impact looks like in 10 years]

**Why This Matters:**
[What value or impact drives this vision]

---

## 長期目標（3-5 Year Goals）

[Major milestones and what they're building toward]

---

## 中期目標（1-Year Goals）

[Current priorities and 12-month targets]

---

## 短期目標（1-3 Months）

[Immediate next steps]

---

## 原動力（What Drives Them）

[Core values/needs that fuel these goals]

---

## 現状ギャップと障害（Obstacles）

[Gap between vision and reality, barriers they face]

---

## 追加観察（Additional Observations）

[Patterns, coherence, or insights about their goal structure]
```

---

## Analysis Principles

1. **Find the "why"** - Dig into motivation, not just what they want
2. **Look for patterns** - Do their goals align with their values?
3. **Note the gaps** - What's between their vision and current reality?
4. **Honor their language** - Use their own words when describing vision
5. **Identify obstacles** - Acknowledge what they're struggling with
6. **Assess coherence** - Do their goals make sense together?

---

## Quality Checklist

- [ ] Vision is concrete (not vague "be successful")
- [ ] Goals have evidence from conversation
- [ ] Motivation is clear
- [ ] Obstacles/gaps are acknowledged
- [ ] Output is clean Markdown
- [ ] Length: 1-2 pages

---

## Example Output

```markdown
# 03_目標 Analysis

## ビジョン（10-Year Vision）

**Ideal Future State:**
Founder of an **AI accessibility company** that makes advanced AI tools usable
for **non-technical people** (target: grandmothers can use it). A company that
combines technical excellence with genuine care for user experience.

**Why This Matters:**
Driven by frustration that amazing technology remains locked behind expert-only
barriers. Vision is to **democratize AI**, not just build a successful company.
The success metric is **user accessibility**, not revenue.

---

## 長期目標（3-5 Year Goals）

- **Build initial product** with grandmother-level accessibility
- **Develop team** that shares values of accessibility + quality
- **Validate market** - prove non-technical users will pay for good UX
- **Establish market position** as "AI for everyone" company

---

## 中期目標（1-Year Goals）

- Complete MVP with usability testing from non-technical users
- Build initial founding team (2-3 core people)
- Secure seed funding or bootstrap strategy
- Publish initial case studies showing accessibility impact

---

## 短期目標（1-3 Months）

- Research user personas (who are the "grandmothers"?)
- Design initial feature set prioritizing accessibility
- Begin MVP development
- Network with potential co-founders

---

## 原動力（What Drives Them）

Core belief: **"Technology should be for everyone, not just experts"**

Values that fuel goals:
- **Democratization** - Making powerful tools accessible
- **Pragmatism** - Actually shipping products that work
- **User empathy** - Deep care for non-technical users
- **Quality** - Won't sacrifice elegance for speed

---

## 現状ギャップと障害（Obstacles）

**Current Reality Gap:**
- Vision: Accessibility-first AI company
- Reality: Still working in different role, limited time/resources

**Barriers:**
- Funding constraints (will bootstrap or raise seed)
- Technical team availability
- User research (need to find and test with real non-technical users)
- Competitive pressure (others building AI but not focused on accessibility)

**Acknowledged Challenge:**
Has history of overcommitting resources. Now more careful about capacity
before committing to ambitious projects.

---

## 追加観察（Additional Observations）

**Coherence:** Goals strongly align with core values (elegance, democratization,
caring for people). Vision feels authentic, not aspirational.

**Realism:** Acknowledges barriers and has learned from past overcommitment.
Goals seem grounded in experience.

**Timeframe:** Clear progression: MVP in 1 year → established company in 3-5 years
→ category-defining vision in 10 years. Realistic staging.
```

---

## Usage

Provide conversation history → I analyze → Output clean Markdown ready for Personal OS.
