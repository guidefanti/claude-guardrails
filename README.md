# Claude Guardrails

Universal cognitive guardrails for Claude Code. Shield any new project against predictable LLM mistakes from day one.

## What this is

Three skills that make Claude Code more disciplined across any type of project:

1. **guardrails** — core cognitive rules (anti-hallucination, verification before "done", clarity before execution, scope discipline). Loaded automatically when relevant.

2. **universal-thinking** — quality protocols for non-code tasks: research, analysis, strategy, marketing, planning. Loaded on demand.

3. **new-project** — automatic bootstrap. Generates a guardrailed CLAUDE.md for any new project. Just type `/new-project`.

## Install

One line:

```bash
git clone https://github.com/guidefanti/claude-guardrails.git /tmp/cg && cp -r /tmp/cg/skills/* ~/.claude/skills/ && rm -rf /tmp/cg
```

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

To add guardrails to a project that already has a CLAUDE.md:

```
/new-project
```

Claude analyzes the existing CLAUDE.md and suggests only additions, never removes anything.

### Daily workflow

Work normally. Cognitive rules are active. When you correct a Claude mistake, it automatically logs the pattern in the project Known failures section.

## Structure

```
claude-guardrails/
├── CLAUDE.md                           # Global rules (optional manual install)
├── skills/
│   ├── guardrails/
│   │   └── SKILL.md                    # Core cognitive guardrails
│   ├── universal-thinking/
│   │   └── SKILL.md                    # Protocols for non-code tasks
│   └── new-project/
│       └── SKILL.md                    # Project CLAUDE.md bootstrap
└── README.md
```

## Recommended companions

These are NOT bundled but pair well with this framework:

| Resource | What it does |
|---|---|
| [Karpathy Guidelines](https://github.com/forrestchang/andrej-karpathy-skills) | Behavioral rules for LLM coding mistakes (81k stars) |
| [LLM Wiki pattern](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f) | Build persistent knowledge bases with LLMs |
| [UltraPlan](https://github.com/6missedcalls/ultraplan) | Deep multi-phase planning before implementation |

## Philosophy

- **Less is more.** Skills load on demand, not every session.
- **Advisory, not deterministic.** These are cognitive instructions. For guaranteed mechanical rules, use hooks.
- **Self-improving.** Corrected mistakes become permanent lessons in the project CLAUDE.md.
- **Universal.** Works for code, marketing, automation, research, strategy.

## Language

All files are in English for maximum LLM adherence and global shareability.
To get responses in your preferred language, add a language instruction to your project CLAUDE.md or `~/.claude/CLAUDE.local.md`.

## License

MIT
