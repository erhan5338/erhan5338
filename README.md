# erhan5338

Welcome to my GitHub profile!

## About Me

- Developer passionate about building great software
- Open to collaboration and new ideas

## Setup: everything-claude-code

This repo documents the local setup of [everything-claude-code](https://github.com/affaan-m/everything-claude-code) — a comprehensive Claude Code plugin system.

### Installation Steps

```bash
# 1. Clone the repo
git clone https://github.com/affaan-m/everything-claude-code.git ~/everything-claude-code

# 2. Install dependencies (Node.js >=18 required)
cd ~/everything-claude-code
npm install

# 3. Run the ECC installer (installs to ~/.claude/)
node scripts/install-apply.js --target claude --profile full

# 4. Verify installation
node tests/run-all.js
```

### Results

- **1674/1678 tests passed** (4 failures are environment-specific, not ECC bugs)
- **597 files** installed to `~/.claude/` (rules, agents, skills, commands, hooks)
- Skills available: `/tdd`, `/plan`, `/code-review`, `/security-scan`, and 60+ more

## Connect

Feel free to explore my repositories and reach out!
