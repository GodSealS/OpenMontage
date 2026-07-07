---

name: manim-composer
description: 触发条件：(1) 用户想创建教育/讲解视频，(2) 用户有模糊概念想要可视化，(3) 用户提到「3b1b 风格」或「像 3Blue1Brown 那样讲解」，(4) 用户想规划 Manim 视频或动画序列，(5) 用户要求「编排」或「规划」数学/科学可视化。将模糊的视频创意转化为详细的逐场景规划（scenes.md）。进行研究、询问关于受众/范围/焦点的澄清问题，并输出全面的场景规格，可用于 ManimCE 或 ManimGL 实现。在编写任何 Manim 代码前使用此技能。本技能规划视频；实现部分请使用 manimce-best-practices 或 manimgl-best-practices。
---

## Workflow

### Phase 1: Understand the Concept

1. **Research the topic** deeply before asking questions
   - Use web search to understand the core concepts
   - Identify the key insights that make this topic interesting
   - Find the "aha moment" - what makes this click for learners
   - Note common misconceptions to address

2. **Identify the narrative hook**
   - What question does this video answer?
   - Why should the viewer care?
   - What's the surprising or counterintuitive element?

### Phase 2: Clarify with User

Ask targeted questions (not all at once - adapt based on responses):

**Audience & Scope**
- What math/science background should I assume? (e.g., "knows calculus" or "high school algebra")
- Target video length? (short: 5-10min, medium: 15-20min, long: 30min+)
- Should this be self-contained or part of a series?

**Focus & Depth**
- Any specific aspects to emphasize or skip?
- Proof-heavy or intuition-focused?
- Real-world applications to include?

**Style Preferences**
- Color scheme preferences?
- Narration style? (casual, formal, playful)
- Any specific visual metaphors you have in mind?

### Phase 3: Create scenes.md

Output a comprehensive `scenes.md` file with this structure:

```markdown
# [Video Title]

## Overview
- **Topic**: [Core concept]
- **Hook**: [Opening question/mystery]
- **Target Audience**: [Prerequisites]
- **Estimated Length**: [X minutes]
- **Key Insight**: [The "aha moment"]

## Narrative Arc
[2-3 sentences describing the journey from confusion to understanding]

---

## Scene 1: [Scene Name]
**Duration**: ~X seconds
**Purpose**: [What this scene accomplishes]

### Visual Elements
- [List of mobjects needed]
- [Animations to use]
- [Camera movements]

### Content
[Detailed description of what happens, what's shown, what's explained]

### Narration Notes
[Key points to convey, tone, pacing notes]

### Technical Notes
- [Specific Manim classes/methods to use]
- [Any tricky implementations to note]

---

## Scene 2: [Scene Name]
...

---

## Transitions & Flow
[Notes on how scenes connect, recurring visual motifs]

## Color Palette
- Primary: [color] - used for [purpose]
- Secondary: [color] - used for [purpose]
- Accent: [color] - used for [purpose]
- Background: [color]

## Mathematical Content
[List of equations, formulas, or mathematical objects that need to be rendered]

## Implementation Order
[Suggested order for implementing scenes, noting dependencies]
```

## 3b1b Style Principles

Apply these principles when composing scenes:

### Visual Storytelling
- **Show, don't just tell** - Every concept needs a visual representation
- **Progressive revelation** - Build complexity gradually, don't show everything at once
- **Visual continuity** - Transform objects rather than replacing them when possible

### Pacing & Rhythm
- **Pause for insight** - Give viewers time to absorb key moments
- **Vary the pace** - Mix quick sequences with slower explanations
- **End scenes with resolution** - Each scene should feel complete

### Mathematical Beauty
- **Emphasize elegance** - Highlight when math is surprisingly simple or beautiful
- **Connect representations** - Show the same concept multiple ways (algebraic, geometric, intuitive)
- **Embrace abstraction gradually** - Start concrete, then generalize

### Engagement Techniques
- **Pose questions** - Make viewers curious before revealing answers
- **Acknowledge difficulty** - "This might seem confusing at first..."
- **Celebrate insight** - Make the "aha moment" feel earned

## References

- [references/narrative-patterns.md](references/narrative-patterns.md) - Common 3b1b narrative structures
- [references/visual-techniques.md](references/visual-techniques.md) - Effective visualization patterns
- [references/scene-examples.md](references/scene-examples.md) - Example scenes.md excerpts

## Templates

- [templates/scenes-template.md](templates/scenes-template.md) - Blank scenes.md template
