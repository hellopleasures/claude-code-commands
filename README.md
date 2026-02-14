# Claude Code Commands

Structured slash commands for **iterative agentic development** with [Claude Code](https://docs.anthropic.com/en/docs/claude-code).

> "AI doesn't write bad code because it's bad at coding; it writes bad code because we give it permission to."

These commands enforce a disciplined development workflow where every phase — planning, implementation, testing, review, and deployment — has explicit rules and quality gates. No stubs. No placeholders. No TODOs. Just real, production-ready code.

## The Problem

AI coding assistants are eager to please. They'll write code that *looks* right but isn't — stubbed functions, hardcoded values, mocked-away logic, silent error swallowing. The code compiles. It even passes tests (that mock the thing being tested). But it doesn't actually work.

These commands fix that by giving the AI explicit constraints at each phase of development.

## The Workflow

```
/plan  -->  /implement  -->  /test  -->  /quality  -->  /review  -->  /production
                ^                                           |
                |                                           |
                +----------  /keepgoing  -------------------+
                             /larp (anytime)
```

| Command | Phase | What It Does |
|---------|-------|-------------|
| `/plan` | Research | Analyze the problem before writing code. Clarify goals, constraints, risks. Produce a written plan. Wait for approval. |
| `/implement` | Build | Execute the plan step-by-step. Real code only — no stubs, no TODOs, no simplified versions. |
| `/keepgoing` | Continue | Work through remaining tasks without stopping for permission between items. |
| `/test` | Test | Expand test coverage beyond the happy path. Boundary conditions, error handling, integration points. |
| `/quality` | Refine | Code quality pass — Compact, Concise, Clean, Capable. Remove dead code, simplify verbose logic. |
| `/review` | Audit | Honest assessment of what was built. What works, what doesn't, what could break in production. |
| `/production` | Ship | Final deployment checklist. Every item verified with evidence, not assertions. |
| `/larp` | Check | Detect performative code. Find and fix stubs, hardcodes, mocked logic, and validation theater. |

## Installation

Copy the `commands/` folder into your project's `.claude/` directory:

```bash
# From your project root
mkdir -p .claude/commands
curl -sL https://github.com/hellopleasures/claude-code-commands/archive/main.tar.gz | tar xz --strip-components=2 -C .claude/commands "claude-code-commands-main/commands/"
```

Or clone and copy:

```bash
git clone https://github.com/hellopleasures/claude-code-commands.git
cp -r claude-code-commands/commands/ your-project/.claude/commands/
```

Your project structure should look like:

```
your-project/
├── .claude/
│   └── commands/
│       ├── implement.md
│       ├── keepgoing.md
│       ├── larp.md
│       ├── planning.md
│       ├── production.md
│       ├── quality.md
│       ├── review.md
│       └── test.md
├── src/
└── ...
```

## Usage

Once installed, use the commands as slash commands in Claude Code:

```
> /plan I need to add user authentication with JWT

> /implement

> /test

> /quality

> /review

> /production
```

### When Things Smell Off

Run `/larp` anytime you suspect the AI is writing performative code:

```
> /larp
```

It will scan for:
- Stubbed functions returning fake data
- Hardcoded values pretending to be dynamic
- Tests that mock away the logic being tested
- Error handling that silently swallows failures
- Async code that doesn't actually await
- Validation that always returns true

## Customization

Each command is a standalone Markdown file. Edit them to match your project's standards:

- Add your framework-specific rules to `/implement`
- Add your test runner commands to `/test`
- Add your deployment checklist items to `/production`
- Adjust the quality criteria in `/quality`

## Philosophy

This isn't about making AI write more code faster. It's about making AI write **real code** that actually works in production. The commands create guardrails that prevent the most common failure modes of AI-assisted development:

1. **Planning before coding** — prevents building the wrong thing
2. **No stubs or TODOs** — prevents incomplete implementations
3. **Testing beyond happy path** — prevents fragile code
4. **Honest review** — prevents false confidence
5. **Evidence-based deployment** — prevents "it works on my machine"

## License

MIT
