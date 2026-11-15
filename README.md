# ShipSnag Skills: Prove It Works (free)

**Your AI coding agent says "done". This makes it prove it.**

Prove It Works is a free agent skill from [ShipSnag](https://shipsnag.com). Before your agent says a task is done, it runs your project's real tests, build, typecheck and lint, shows the real output, and checks the change for the quiet ways "done" is not done: skipped or weakened tests, test commands that cannot fail, swallowed errors, hardcoded results, files changed outside the task, broken project rules, debug leftovers, secrets, and dependency or migration mistakes.

Works with Claude Code, Claude.ai, Cursor, Codex and any agent that reads `SKILL.md` files. Needs only Python 3 and git.

## Install

**Any agent (skills CLI):**

```
npx skills add shashwat14m/shipsnag-skills --skill prove-it-works
```

**Claude Code plugin:**

```
/plugin marketplace add shashwat14m/shipsnag-skills
/plugin install prove-it-works@shipsnag
```

**Manual:** copy `skills/prove-it-works/` into `~/.claude/skills/` (or `.claude/skills/` in your project, or your agent's skills folder). In Claude.ai, zip the folder and upload it under Settings > Capabilities > Skills.

Start a new session. Then finish a task, or ask "prove it works".

## What you get

The first line of every proof is one of four verdicts:

- `PROVEN: all 3 checks passed, no problems in the change`
- `CHECKS PASS (task not verified): ...`
- `NOT VERIFIED: 2 checks could not run (...)`
- `NOT DONE: 1 failing check, 2 problems in the change`

Below it: the real output of every check, and a finding for each problem with the file and line. Say "don't do that again" after correcting a mistake and it becomes a rule checked on every later proof.

Full details: [skills/prove-it-works/README.md](skills/prove-it-works/README.md)

## More from ShipSnag

Small paid skills that catch what AI-built code breaks, leaks or costs after you ship:

- **Broke After Deploy**: works on your laptop, breaks in production
- **Key Leaked**: API keys and secrets exposed in your code or bundle
- **Bill Spiked**: code that quietly runs up your cloud or API bill
- **Ship Check**: all three in one scan

Get them at [shipsnag.com](https://shipsnag.com). Support: support@shipsnag.com
