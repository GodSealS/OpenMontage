---
description: 打开 Backlot 实时故事板 — 浏览器面板，实时显示管道阶段、脚本、场景计划和生成的资源
argument-hint: [project-id（可选，默认最新项目）]
---

打开指定项目的 Backlot 面板：

```bash
python -m backlot open $ARGUMENTS
```

- 无参数 → 打开项目库视图（所有项目）：`python -m backlot open`
- 命令是幂等的：如果 Backlot 服务器未运行则启动，然后打开浏览器
- 如果命令失败，报告错误并继续用户的请求 — 面板是观察者，不是阻断器
- 面板从磁盘读取所有数据（`projects/<id>/` 检查点、资源、事件）。无需手动更新 UI；保持检查点和产出物符合 `skills/meta/checkpoint-protocol.md` 的规范，面板会自动同步
