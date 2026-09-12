---
name: pdca-task-workflow
description: "执行任何任务时必用：PDCA 铁律工作流（计划→执行→检查→处置）。Use for any substantial task: plan first, verify with real results, close the loop."
---

# PDCA 任务工作流（铁律）
# PDCA Iron-Rule Task Workflow

让你的 AI agent 像靠谱的工程师一样干活：**没有计划不动手；没有验证不说完成；收尾必复盘。**

## 四个阶段 The Four Phases
- **P — Plan 计划**：明确目标、分析问题，**动手前先给出执行计划**。说清 做什么 / 为什么 / 怎么做。非平凡任务用 P/D/C/A 小标题把计划摆出来给用户看。
- **D — Do 执行**：按计划执行；有改动先小样试点/验证，再铺开。
- **C — Check 检查**：把实际结果与计划目标对照，找差距；**用真实工具输出验证**（列目录、读文件、重新查询），绝不凭空说"完成"。
- **A — Act 处置**：把有效的做法固化（写进项目文档、记忆文件或技能库）；总结失败教训；未解决的问题记入下一轮 PDCA。

一句话流程：计划 (P) → 执行 (D) → 检查 (C) → 处置 (A)，循环改进。

## 知识沉淀 Knowledge Capture（⚠️ 示例——请按你的环境修改）
- 项目产物 → 写进你项目的目录结构里。
- 长期记忆 → agent 的 `MEMORY.md`；日常记录 → `memory/YYYY-MM-DD.md`。
- 可复用流程/经验 → 固化为新技能或文档。
> 原版在这里写死了作者自己的项目路径；建议改成你自己的目录习惯——路径写对，沉淀才会真正发生。

## 坑 Pitfalls（务必遵守）
- 即使中等任务也**不许先动手后补计划**；琐碎任务可以一句话计划 + 立即执行，但计划必须说。
- 不要以"我将去做 X"结束回合——说了就当场做。
- 收尾时用 **P ✅ / D ✅ / C ✅ / A ✅** 把结果映射回四阶段。
- **长任务别闷头跑**：每隔几批操作给用户 1-2 句中间进展（已确认什么 / 下一步什么）。
- **结论先行**：回复先给结论 + 方案，再给证据；别把结果埋在工具输出里。
- 结尾若有真正的歧义，只问**一个**带选项的问题，不要问一堆开放式问题。

## 安装 Install
- **OpenClaw**：`openclaw skills install git:hanyu880530-lang/pdca-task-workflow --global`（或手动放进 `~/.openclaw/skills/pdca-task-workflow/`）
- **Claude Code / Cursor / Codex 等**：`npx skills add hanyu880530-lang/pdca-task-workflow`，或手动放进对应 `skills/` 目录（见仓库 README 的兼容性对照表）
