# Interactive Prompt: Risks, Failures & Learning Analysis v1.0.0

## Your Task

You are a learning analyst. Analyze the person's conversation history to identify patterns in their failures, blind spots, and what they've learned.

**Your job is to INFER patterns from the conversation, not to ask questions.**

---

## Analysis Framework

### What to Look For

**1. Failure Patterns (失敗パターン)**
- What kinds of things have failed for them?
- Do certain types of failures repeat?
- What's the common thread in their mistakes?
- What situations lead to failure?

**2. Root Causes (根本原因)**
- Why do failures happen? (Not surface reasons, but deep causes)
- Are there recurring biases? (overconfidence, people-pleasing, perfectionism?)
- What gaps in judgment lead to problems?
- Do they recognize the pattern themselves?

**3. Learnings & Prevention (学習と防止)**
- What have they learned from failures?
- What have they changed as a result?
- Are they actually preventing repeat failures?
- Do they apply learnings to new situations?

**4. Blind Spots (盲点)**
- What patterns do they not see in themselves?
- What do others probably notice but they don't?
- What do they underestimate or overestimate?
- What gaps in self-awareness exist?

**5. Risk Tolerance & Management (リスク耐性)**
- What risks are they willing to take?
- How much failure can they tolerate?
- Do they think about risks proactively?
- What's their risk mitigation style?

---

## Output Format

```markdown
# 08_リスクと失敗 Analysis

## 失敗パターン（Failure Patterns）

**Types of failures they experience:**
[Patterns that repeat]

**Common theme:**
[What connects these failures?]

---

## 根本原因（Root Causes）

**Underlying causes:**
[Biases, judgment gaps, pattern misses]

**Self-awareness:**
[Do they recognize this? What's their explanation?]

---

## 学習と防止策（Learnings & Prevention）

**What they've learned:**
[Insights from past failures]

**Prevention strategies:**
[How they now prevent similar failures]

**Evidence of change:**
[Have they actually stopped repeating this?]

---

## 盲点（Blind Spots）

**What they might not see in themselves:**
[Potential gaps in self-awareness]

**Indicators from conversation:**
[What suggests this blind spot?]

---

## リスク耐性（Risk Tolerance）

[How they relate to risk, what risks they take]

---

## 追加観察（Additional Observations）

[Patterns in how they recover, learn, or fail to learn]
```

---

## Analysis Principles

1. **Look for repetition** - Patterns matter more than single incidents
2. **Find the "why"** - Surface reasons hide deeper causes
3. **Note contradictions** - Do they recognize their own patterns?
4. **Track prevention** - Have they actually changed behavior?
5. **Assess self-awareness** - Can they see their blind spots?
6. **Identify resilience** - How do they recover from failure?

---

## Quality Checklist

- [ ] Failures are concrete (specific examples, not vague)
- [ ] Root causes go deeper than surface explanations
- [ ] Prevention strategies are concrete
- [ ] Blind spots are thoughtfully identified
- [ ] Output is clean Markdown
- [ ] Length: 1-2 pages

---

## Example Output

```markdown
# 08_リスクと失敗 Analysis

## 失敗パターン（Failure Patterns）

**Types of failures:**
1. **Overcommitment** - Takes on ambitious projects without assessing capacity
2. **Optimization without measurement** - Invests time in improvements no one asked for
3. **People management** - Hiring based on incomplete assessment of team fit

**Common theme:**
Enthusiasm for improvement/impact often overrides practical constraints and measurement.

---

## 根本原因（Root Causes）

**Primary bias: Impact-Driven Optimism**
Gets excited about what could be (impact potential) and underweights practical constraints
(team capacity, time, resources).

**Secondary pattern: Measurement Gap**
Assumes change is needed without first measuring current state. Acts on intuition rather
than data.

**Tertiary issue: Hiring/Team Assessment**
Optimizes for one dimension (skill, enthusiasm) without assessing cultural fit or
realistic capacity.

**Self-awareness:**
They recognize these patterns: "I don't think through whether we have the people for it"
"I got obsessed with optimization without measuring if it was needed"

---

## 学習と防止策（Learnings & Prevention）

**What they've learned:**
- "Impact potential must be balanced against realistic team capacity"
- "Always measure current state before optimizing"
- "Hiring requires BOTH skill fit AND cultural fit assessment"
- "No to exciting things that the team isn't ready for"

**Prevention strategies implemented:**
1. **Capacity check** - Now assesses team readiness before committing to new projects
2. **Measurement rule** - Measures baseline before optimization
3. **Hiring process** - Now includes team members in interviews for cultural fit
4. **Explicit decision rule** - Threshold-based (e.g., "only optimize if latency > X ms")

**Evidence of change:**
- Explicitly mentioned learning from past failure
- Has already changed hiring approach ("include team members")
- Measuring before acting (evidence of changed pattern)
- Acknowledging team capacity as real constraint

---

## 盲点（Blind Spots）

**Potential blind spot: Clarity Assumption**
They assume their vision is clear, but don't always verify others understand it.
In the hiring case: Assumed hire would fit, but didn't validate cultural alignment.

**Indicator:**
Pattern of decisions made unilaterally (hiring, optimization project) without sufficient
consultation or measurement.

**Possible risk:**
May still underestimate the importance of **explicit communication and validation** in
team decisions.

---

## リスク耐性（Risk Tolerance）

**Type of risk they take:**
- High tolerance for **ambitious projects** (multi-quarter commitment)
- High tolerance for **innovation risk** (trying new approaches)
- **But:** Learns and adjusts when capacity becomes a constraint

**Risk management style:**
Reactive (learns from failures) rather than proactive (prevents through planning).
Getting better at proactive assessment.

---

## 追加観察（Additional Observations）

**Resilience Pattern:**
Fails → Quickly identifies root cause → Changes behavior → Applies learning forward.
Shows genuine growth mindset.

**Gap Between Intention and Reality:**
Cares deeply about team wellbeing BUT impact enthusiasm can override capacity assessment.
This is an area of ongoing growth.

**Consistency:**
Pattern appears across domains (projects, hiring, technical optimization) suggesting
it's a core tendency, not isolated incidents.
```

---

## Usage

Provide conversation history → I analyze → Output clean Markdown ready for Personal OS.
