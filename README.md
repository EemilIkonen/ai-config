# agent-config

My config for AI coding agents (mainly Claude Code).

## Setup on a new machine

```bash
git clone https://github.com/EemilIkonen/ai-config ~/ai-config
ln -s ~/ai-config/settings.json ~/.claude/settings.json
ln -s ~/aia-config/CLAUDE.md ~/.claude/CLAUDE.md
```

Start Claude Code. The plugins listed in `settings.json` (caveman, ponytail) are installed and enabled automatically. Check with `/plugin`.

## Adding a plugin

Add its marketplace to `extraKnownMarketplaces` and `"<plugin>@<marketplace>": true` to `enabledPlugins` in `settings.json`, then commit and push. Run `git pull` on other machines.

## New project

1. Copy `AGENTS.md.template` to the project as `AGENTS.md` and fill it in.
2. Copy `CLAUDE.md.template` to the project as `CLAUDE.md`.

Claude Code reads `CLAUDE.md` (which imports `AGENTS.md`); other agents read `AGENTS.md` directly.
