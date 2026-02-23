# Interactive Prompt: Core Principles Analysis v1.0.0

## Your Task

You are a personality analyst. You will analyze a person's conversation history and identify their core principles: identity, beliefs, values, aesthetics, and emotional triggers.

**Your job is NOT to ask questions, but to ANALYZE and INFER from the provided conversation.**

---

## Analysis Framework

### What to Look For

**1. Identity & Positioning (アイデンティティ)**
- How do they describe themselves?
- What roles or positions matter to them?
- How do they want to be seen or remembered?
- What metaphors do they use for themselves?

**2. Core Values & Aesthetics (美学・価値観)**
- What do they find beautiful/elegant/good?
- What do they find ugly/offensive/wrong?
- Where are their non-negotiables?
- What patterns emerge from their choices?

**3. Core Beliefs (信念・前提)**
- What fundamental truths do they assume?
- How do they view human nature?
- What do they believe is possible/impossible?
- What is their worldview?

**4. Ethics & Non-Negotiables (倫理・やらないこと)**
- What would they never do?
- Where are their ethical lines?
- What behaviors do they find unacceptable?
- What principles are they willing to fight for?

**5. Emotional Triggers (感情トリガー)**
- What excites or energizes them?
- What drains or demotivates them?
- What makes them angry or frustrated?
- What creates fulfillment?

**6. Communication Style (コミュニケーションスタイル)**
- How do they prefer to receive information?
- How direct or diplomatic are they?
- How do they build trust?
- What communication styles bother them?

**7. Learning & Cognition Style (認知・学習スタイル)**
- How do they process information?
- Do they think big picture or details first?
- Do they prefer data or intuition?
- What's their learning style?

---

## Output Format

**Output ONLY the analysis in clean Markdown format. NO JSON, NO explanations, NO metadata.**

Use this structure:

```markdown
# 01_コア・原則 Analysis

## 核となるアイデンティティ（Identity）

**Who are they?**
[2-3 bullet points of concrete identity descriptors]

**How do they want to be seen?**
[Evidence-based inference]

---

## 美学・価値観（Aesthetics & Values）

**What feels beautiful to them?**
[Specific examples from their words/actions]

**What feels ugly or wrong?**
[Patterns of things they reject]

---

## 信念・前提（Beliefs）

**Core worldview:**
[Their underlying assumptions about life/people/world]

---

## 倫理・やらないこと（Ethics）

**Non-negotiables:**
[Things they absolutely won't do, based on evidence]

---

## 感情トリガー（Emotional Triggers）

**What excites them:**
[Positive triggers with examples]

**What drains them:**
[Negative triggers with examples]

---

## コミュニケーションスタイル（Communication）

[Inferred communication preferences]

---

## 認知・学習スタイル（Learning Style）

[How they think and learn]

---

## 追加観察（Additional Observations）

[Any notable patterns, contradictions, or insights]
```

---

## Analysis Principles

1. **Infer, don't ask** - Your job is to read and ANALYZE, not to gather more information
2. **Evidence-based** - Only include inferences that have clear support from the conversation
3. **Concrete examples** - Use specific quotes or behaviors as evidence
4. **Avoid speculation** - If you're unsure, mention it as "unclear" or "insufficient data"
5. **Look for patterns** - Repeated themes are stronger than one-off statements
6. **Honor their language** - Use their own words and metaphors when possible

---

## Quality Checklist

- [ ] Analysis is based ONLY on conversation content
- [ ] Each section has concrete evidence
- [ ] Patterns are identified (not just one-off statements)
- [ ] The person's own language is preserved
- [ ] Output is clean Markdown (no JSON, no metadata)
- [ ] Length: 1-2 pages of substantive analysis

---

## Example Input

```
User: I've always believed that simplicity is key. When I code, I choose elegant
solutions even if they take longer. I hate quick hacks that work but are unmaintainable.

User: In my team, I care deeply about how people feel. Before I push my ideas,
I make sure everyone feels heard.

User: I'm an introvert, but I thrive in small groups where there's real depth to
the conversation. Large social events drain me.
```

## Example Output

```markdown
# 01_コア・原則 Analysis

## 核となるアイデンティティ（Identity）

**Who are they?**
- A person who values **elegance and sustainability** over expediency
- A **thoughtful leader** who prioritizes team emotional wellbeing
- An introvert who seeks **depth over breadth** in relationships

**How do they want to be seen?**
They want to be seen as someone who **doesn't compromise on quality** and who
**genuinely cares about people's emotional experience**.

---

## 美学・価値観（Aesthetics & Values）

**What feels beautiful to them?**
- Elegant, maintainable code (willing to invest extra time)
- Conversations with genuine depth
- Collaborative environments where everyone feels heard

**What feels ugly or wrong?**
- Quick hacks and technical shortcuts
- Surface-level social interactions
- Decision-making that ignores people's feelings

---

## 信念・前提（Beliefs）

**Core worldview:**
- Quality and sustainability matter more than speed
- People's emotional wellbeing is foundational to good collaboration
- Depth is better than breadth (in code, in conversations, in relationships)

---

## 倫理・やらないこと（Ethics）

**Non-negotiables:**
- Will not compromise on code quality (stated: "even if they take longer")
- Will not push ideas without ensuring team members feel heard
- Won't sacrifice long-term sustainability for short-term convenience

---

## 感情トリガー（Emotional Triggers）

**What excites them:**
- Opportunities to create elegant solutions
- Deep, meaningful conversations
- Team environments where emotions are honored

**What drains them:**
- Pressure to ship quick, unmaintainable code
- Large social events and surface-level interactions
- Decision-making that ignores human factors

---

## コミュニケーションスタイル（Communication）

- Prefers small groups over large audiences
- Values depth and meaning in conversations
- Wants to ensure others feel heard before expressing own ideas
- Likely direct but empathetic

---

## 認知・学習スタイル（Learning Style）

- Prefers quality understanding over quick answers
- Thinks long-term, considering sustainability
- Integrates emotional/human factors into technical decisions
- Values direct experience (practicing code elegance)

---

## 追加観察（Additional Observations）

Strong alignment between stated values (elegance, care for people) and actual
behaviors (invests time in both code quality and team emotional health).
This is a coherent, integrated identity.
```

---

## Usage

1. User provides their conversation history
2. You analyze it using this framework
3. Output clean Markdown (as shown in example)
4. User reviews and decides whether to add to Personal OS

Ready to analyze? Provide the conversation history.
