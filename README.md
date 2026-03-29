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

## Setup: awesome-claude-code

[hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code) — Claude Code ekosistemi için küratörlüğü yapılmış kaynak kataloğu (930+ kaynak, Python araç seti).

### Installation Steps

```bash
git clone https://github.com/hesreallyhim/awesome-claude-code.git ~/awesome-claude-code
cd ~/awesome-claude-code
pip install -e ".[dev]"

# Verify
python3 -m pytest tests/
```

### Results

- **314/314 tests passed**
- `make generate` ile README otomatik üretilir
- `make validate` ile tüm kaynak URL'leri doğrulanır

---

## Setup: paperclip

[paperclipai/paperclip](https://github.com/paperclipai/paperclip) — AI agent orkestrasyonu için full-stack web uygulaması (TypeScript monorepo, Node.js 20+).

### Installation Steps

```bash
git clone https://github.com/paperclipai/paperclip.git ~/paperclip
cd ~/paperclip
pnpm install
pnpm build

# Development server (UI: http://localhost:3100)
pnpm dev
```

### Results

- **Build:** Tüm paketler başarıyla derlendi (server, ui, cli)
- **Typecheck:** Tüm TypeScript kontrolleri geçti (hata yok)
- **Çalıştırma:** `pnpm dev` → `http://localhost:3100`

---

## Setup: n8n-mcp

[czlonkowski/n8n-mcp](https://github.com/czlonkowski/n8n-mcp) — Claude Code / Claude Desktop için n8n workflow otomasyonu MCP sunucusu (TypeScript, 1.396 node, 2.709 şablon).

### Installation Steps

```bash
git clone https://github.com/czlonkowski/n8n-mcp.git ~/n8n-mcp
cd ~/n8n-mcp

# xlsx SheetJS CDN engellenirse npm registry override ekle:
# package.json → overrides → "xlsx": "0.18.5"

npm install
npm run build   # TypeScript → dist/
```

### MCP Configuration (`.mcp.json`)

```json
{
  "mcpServers": {
    "n8n-mcp": {
      "command": "node",
      "args": ["/home/user/n8n-mcp/dist/mcp/index.js"],
      "env": {
        "MCP_MODE": "stdio",
        "LOG_LEVEL": "error",
        "DISABLE_CONSOLE_OUTPUT": "true",
        "N8N_MCP_TELEMETRY_DISABLED": "true"
      }
    }
  }
}
```

### Results

- **Build:** `dist/mcp/index.js` başarıyla derlendi
- **Smoke test:** MCP server stdio modunda başlatılabiliyor
- **Kapsam:** 1.396 n8n node, 2.709 workflow şablonu, 7 doc aracı + 13 yönetim aracı

---

## Connect

Feel free to explore my repositories and reach out!
