[简体中文](README.md) | **English**

# PDCA Task Workflow

> **Make your AI agent plan before acting, verify with real results, and close the loop after every task.**
> An iron-rule PDCA workflow skill for AI agents — in the open **Agent Skills** (`SKILL.md`) format, compatible with **Claude Code, Codex, Cursor, Gemini CLI, Copilot, OpenClaw** and 30+ other agents.

---

## What is this?

A **"work discipline" skill** for AI agents: it requires the agent to run the full **Plan → Do → Check → Act** cycle on every task:

| Phase | Requirement |
|---|---|
| **P — Plan** | Present a plan (what / why / how) *before* acting — never start blind |
| **D — Do** | Execute the plan; pilot small changes before scaling up |
| **C — Check** | Verify results with real tool output — never claim "done" without checking |
| **A — Act** | Capture what worked, summarize what failed, carry open issues into the next loop |

Plus a set of battle-tested disciplines:

- Lead with the conclusion (finding + fix first, evidence after)
- Post interim progress on long tasks — don't leave the user staring at a spinner
- Never end a turn with "I will do X" — do it in the same turn
- Close with **P ✅ / D ✅ / C ✅ / A ✅** mapped back to the phases
- Ask exactly **one** question (with options) if a genuine ambiguity remains

> It comes from a real production environment: a **7-agent content-production pipeline** runs on it every day.

## Install

### OpenClaw (recommended)

```bash
openclaw skills install git:hanyu880530-lang/pdca-task-workflow --global
```

### Manual

Drop `SKILL.md` into your skills directory:

```
~/.openclaw/skills/pdca-task-workflow/SKILL.md
```

### Other frameworks

`SKILL.md` is the open Agent Skills format (YAML frontmatter + Markdown). Wire it into your system prompt or skill system as-is.

## Compatibility

This skill uses the **open Agent Skills standard** (`SKILL.md`: only `name` + `description` frontmatter plus a Markdown body — no scripts, no dependencies), natively supported by 30+ agents:

| Tool | Install location |
|---|---|
| **OpenClaw** | `~/.openclaw/skills/` (or the command above) |
| **Claude Code / Claude** | `.claude/skills/<name>/` or `~/.claude/skills/<name>/` |
| **OpenAI Codex CLI** | `.agents/skills/` or `~/.codex/skills/` |
| **Cursor** (2.4+) | `.cursor/skills/<name>/` or `.agents/skills/` |
| **Gemini CLI / Copilot CLI / Cline / Windsurf, etc.** | their own skills directories (`SKILL.md` supported) |

Universal install (skills.sh ecosystem — installs into `.agents/skills/` and symlinks Claude Code, Codex, Cursor and more):

```bash
npx skills add hanyu880530-lang/pdca-task-workflow
```

**Any AI can use it**: if a tool has no skills directory, paste the contents of `SKILL.md` into its custom instructions / system prompt — it's just a one-page Markdown work discipline.

## Customization

- **Adapt the "Knowledge Capture" section to your own directory conventions** — real paths make capture actually happen.
- The `description` in the frontmatter decides when the AI activates the skill; rewrite it for your use case.
- If your agent supports slash commands, the skill will also be registered as one.

## Files

```
.
├── SKILL.md      # The skill itself (bilingual 中文 / English)
├── README.md     # 中文说明 (Chinese)
├── README.en.md  # This file
└── LICENSE       # MIT
```

## License

MIT © 2026 hanyu880530-lang
