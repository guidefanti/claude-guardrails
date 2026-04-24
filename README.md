# Claude Guardrails

Universal cognitive guardrails for Claude Code. Shield any new project against predictable LLM mistakes from day one — zero manual setup after install.

## What this is

Three files that make Claude Code more disciplined across any type of project:

1. **Global CLAUDE.md** — universal cognitive rules (anti-hallucination, verification before "done", clarity before execution). Automatically applies to every project.

2. **Skill `universal-thinking`** — quality protocols for non-code tasks: research, analysis, strategy, marketing, planning. Loaded on demand.

3. **Skill `new-project`** — automatic bootstrap. Generates a guardrailed CLAUDE.md for any new project. Just type `/new-project`.

## Install

```bash
# Clone
git clone https://github.com/guidefanti/claude-guardrails.git /tmp/claude-guardrails

# Append global rules (preserves existing content)
echo "" >> ~/.claude/CLAUDE.md
cat /tmp/claude-guardrails/CLAUDE.md >> ~/.claude/CLAUDE.md

# Copy skills
cp -r /tmp/claude-guardrails/skills/universal-thinking ~/.claude/skills/
cp -r /tmp/claude-guardrails/skills/new-project ~/.claude/skills/

# Clean up
rm -rf /tmp/claude-guardrails
```

> **Note:** Review `~/.claude/CLAUDE.md` after install to remove duplicates if you already had content there.

## Usage

### New project

Open Claude Code in your project and type:

```
/new-project
```

Claude analyzes the project and generates an adapted CLAUDE.md with guardrails.

For specific project types:

```
/new-project dev
/new-project marketing
/new-project automation
/new-project research
/new-project content
```

### Existing project

The global CLAUDE.md adds to your project existing CLAUDE.md — it does not replace it. To add guardrails to a project that already has a CLAUDE.md:

```
/new-project
```

Claude analyzes the existing CLAUDE.md and suggests only additions, never removes anything.

### Daily workflow

Work normally. Cognitive rules are always active. When you correct a Claude mistake, it automatically logs the pattern in the project Known failures section.

## Structure

```
claude-guardrails/
├── CLAUDE.md                           # Global rules (~35 lines)
├── skills/
│   ├── universal-thinking/
│   │   └── SKILL.md                    # Protocols for non-code tasks
│   └── new-project/
│       └── SKILL.md                    # Project CLAUDE.md bootstrap
└── README.md
```

## Recommended companions

These are NOT bundled but pair well with this framework:

| Resource | What it does | Install |
|---|---|---|
| [Karpathy Guidelines](https://github.com/forrestchang/andrej-karpathy-skills) | Behavioral rules for LLM coding mistakes (81k stars) | `claude plugin install forrestchang/andrej-karpathy-skills` |
| [LLM Wiki pattern](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) | Build persistent knowledge bases with LLMs (research-heavy projects) | Copy gist to your LLM agent |
| [UltraPlan](https://github.com/6missedcalls/ultraplan) | Deep multi-phase planning before implementation | `cp -r ultraplan ~/.claude/skills/` |

## Compatibility

- Works with any existing skills or hooks
- Does not conflict with project-level CLAUDE.md files
- Does not conflict with Claude Code auto-memory
- Tested with Claude Code v2.1+

## Philosophy

- **Less is more.** Global file is ~35 lines. Skills load on demand.
- **Advisory, not deterministic.** These are cognitive instructions. For guaranteed mechanical rules, use hooks.
- **Self-improving.** Corrected mistakes become permanent lessons in the project CLAUDE.md.
- **Universal.** Works for code, marketing, automation, research, strategy.

## Language

All files are in English for maximum LLM adherence and global shareability.
To get responses in your preferred language, add a language instruction to your
project CLAUDE.md or `~/.claude/CLAUDE.local.md`.

## License

MIT
