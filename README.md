# PDCA Task Workflow · PDCA 铁律工作流

> **让 AI agent 先计划再动手、用真实结果验证、收尾四阶段闭环。**
> An iron-rule PDCA workflow skill for AI agents — [OpenClaw](https://openclaw.ai) `SKILL.md` format, also usable with any system that supports Agent Skills.

---

## 这是什么？

一份给 AI 代理的**"工作纪律"技能**：规定 agent 接到任务后必须走完整的
**计划 (Plan) → 执行 (Do) → 检查 (Check) → 处置 (Act)** 循环：

| 阶段 | 要求 |
|---|---|
| **P 计划** | 动手前先给计划（做什么 / 为什么 / 怎么做），不裸奔开始 |
| **D 执行** | 按计划执行，有改动先小样试点再铺开 |
| **C 检查** | 用真实结果验证输出，绝不凭空说"完成" |
| **A 处置** | 沉淀经验、总结教训、遗留问题进入下一轮 |

还有一批从实战里打磨出来的纪律：

- 结论先行（先给结论 + 方案，再给证据）
- 长任务中途汇报进度（别让用户对着转圈等）
- 不以"我将去做 X"结束回合——说了就当场做
- 收尾用 **P ✅ / D ✅ / C ✅ / A ✅** 把结果映射回四阶段
- 结尾有歧义时只问**一个**带选项的问题

> 它来自一个真实生产环境：一个 **7 agent 的内容创作流水线**每天靠它运转。

## 安装

### OpenClaw（推荐）

```bash
openclaw skills install git:hanyu880530-lang/pdca-task-workflow --global
```

### 手动安装

把 `SKILL.md` 放到技能库目录：

```
~/.openclaw/skills/pdca-task-workflow/SKILL.md
```

### 其他框架

`SKILL.md` 是通用 Agent Skill 格式（YAML frontmatter + Markdown），接入你的系统提示或技能系统即可。

## 适配建议

- **"知识沉淀"一节请按自己的目录习惯修改**——路径写对，沉淀才会真正发生。
- frontmatter 里的 `description` 决定技能何时被 AI 触发，可按你的使用场景改写。
- 如果你的 agent 支持斜杠命令，它也会自动注册为命令。

## 文件结构

```
.
├── SKILL.md    # 技能本体
├── README.md   # 本文件
└── LICENSE     # MIT
```

## License

MIT © 2026 hanyu880530-lang
