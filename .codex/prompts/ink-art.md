---
description: 手绘墨水涂鸦动画 — 角色自己画出自己然后走路/跳舞/挥手，或冷面机械装置说明动画（矢量 → HyperFrames MP4）。
argument-hint: [what to animate]
---

Read `skills/creative/ink-theater.md` and `ink-theater/README.md`, then build the hand-drawn ink animation described below.

- **Ink Theater** engine (`ink-theater/ink-theater.js`): variable-width ink strokes, seek-safe boil, closed-form spring eases, FABRIK IK, contraption grammar.
- For a **character that walks / dances / waves / jumps**, use the **Ink Puppet** mocap system: `InkPuppet.create` → `p.drawIn` (self-drawing reveal) → `InkPuppet.choreograph([{clip:'wave'},{clip:'twist'},…])` (names from `ink-theater/mocap/catalog.json`, 12 CMU-sourced moves). **Never hand-tune motion**; add moves via `node ink-theater/mocap/add-motion.mjs`.
- Captions = **HTML overlay `<div>`s** (HyperFrames doesn't apply webfonts to SVG `<text>`). Validate (`npx hyperframes lint` + `snapshot`) before rendering.

Request: $ARGUMENTS
