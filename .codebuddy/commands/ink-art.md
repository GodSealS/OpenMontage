---
description: 手绘墨水涂鸦动画 — 角色自己画出自己然后走路/跳舞/挥手，或冷面机械装置说明动画。矢量、确定性，通过 HyperFrames 渲染为 MP4
argument-hint: [要动画化的内容描述]
---

阅读 `skills/creative/ink-theater.md`（隐喻方法、颜色语法、挖掘出的原型）和 `ink-theater/README.md`（引擎 API、确定性、SVG-text 字体陷阱），然后构建下面描述的作品。

- 使用 **Ink Theater** 引擎（`ink-theater/ink-theater.js`）：可变宽度墨线笔触、seek-safe 抖动、闭合弹簧缓动、FABRIK IK、机械装置语法
- 对于**走路 / 跳舞 / 挥手 / 跳跃的角色**，使用 **Ink Puppet** 动捕系统：`InkPuppet.create(...)` → `p.drawIn(tl, ...)` 用于自绘揭示 → `InkPuppet.choreograph(tl, p, [{clip:'wave'},{clip:'twist'},{clip:'walk'},...])`。片段名称来自 `ink-theater/mocap/catalog.json`（12 个 CMU 来源动作）。**永远不要手动调动画** — 用 `node ink-theater/mocap/add-motion.mjs <name> <cmu-id> …` 添加动作（免费 CMU 动捕库有 walk/run/dance/…）
- 字幕 = **HTML 覆盖层 `<div>`**（HyperFrames 不会将网络字体应用于 SVG `<text>`）
- 用 `npx hyperframes lint` + `snapshot` 验证（目视检查缩略图），然后渲染

在 OpenMontage 中，这运行在 `animation` 管道（插画）或 `character-animation` 管道（动捕木偶）上 — 它是一种风格 + 引擎，不是独立管道。

请求：$ARGUMENTS
