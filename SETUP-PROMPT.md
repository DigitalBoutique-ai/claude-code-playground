# Setup prompt

Paste this into Claude Code on a new machine to install the playground mods.

```
Set up the claude-code-playground mods on this machine:

1. Clone https://github.com/DigitalBoutique-ai/claude-code-playground.git to ~/Code/claude-code-playground (if it already exists, git pull instead). Then add Anthropic's repo as a second remote: git remote add upstream https://github.com/anthropics/claude-code-playground.git
2. Add the mods folder as a local marketplace (the repo root has no marketplace.json, so don't add the GitHub repo directly):
   claude plugin marketplace add ~/Code/claude-code-playground/claude-code/mods
3. Install all three mods at user scope:
   claude plugin install blast-radius@claude-code-playground-mods --scope user
   claude plugin install replay-theater@claude-code-playground-mods --scope user
   claude plugin install token-weather@claude-code-playground-mods --scope user
4. Check that `claude plugin list` shows all three as enabled, then tell me to run /reload-plugins.
5. Check ~/Code/claude-code-playground/skills for any SKILL.md folders. If there are any, list them and ask me before installing. If there are none, say so.

Note: blast-radius will hold risky Bash commands (rm -rf, git reset --hard, git clean, force push, migrations) for my Proceed/Cancel. That's expected.
```
