---
description: 用动捕动画化用户提供的角色绘图/照片（Meta AnimatedDrawings）→ 光栅 GIF/MP4。如需从零创建矢量涂鸦，使用 /ink-art
argument-hint: [绘图文件路径] [动作：dance|walk|jump|wave]
---

阅读 `skills/creative/animated-drawing.md`，然后设置并运行 Meta 的开源 **AnimatedDrawings**，用指定动作动画化提供的绘图。

- 仅在用户**已有**类人形绘图/照片需要动画化时使用。如需从零创建自绘矢量涂鸦 → 使用 `/ink-art`
- 输出为**光栅**（原始绘图变形） — 无矢量，无绘制揭示。确认输入是浅色纯背景上的单个人形角色
- 优先使用打包角色路径；自动骨骼绑定路径需要 Docker + ~670 MB 模型

绘图 + 动作：$ARGUMENTS
