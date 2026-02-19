# 🛠️ CLI AI Tools - Overview & Comparison

## Why CLI over Web?

| Aspecto | Web (ChatGPT, Claude.ai) | CLI (Claude Code, aider) |
|---------|--------------------------|--------------------------|
| **Acceso a archivos** | ❌ Copy-paste manual | ✅ Lee directo del disco |
| **Tamaño de contexto** | Limitado por ventana | Puede leer proyectos enteros |
| **Automatización** | ❌ No scripteable | ✅ Integrable en pipelines |
| **Edición de código** | Copy-paste de vuelta | ✅ Edita archivos directo |
| **Historial de Git** | ❌ Manual | ✅ Commits automáticos |
| **Privacidad** | Datos van a la nube | Algunas opciones locales |
| **Velocidad** | Overhead del browser | Más directo |

---

## 🔍 Comparison Matrix

| Tool | Provider | Pricing | Best For | Difficulty |
|------|----------|---------|----------|------------|
| **Claude Code** | Anthropic | API ($) | Coding, file editing | ⭐ Easy |
| **OpenClaw** | Open Source | API ($) | Automation, integrations | ⭐⭐ Medium |
| **GitHub Copilot CLI** | GitHub | $10-19/mo | Shell commands, Git | ⭐ Easy |
| **aider** | Open Source | API ($) | Pair programming | ⭐⭐ Medium |
| **Gemini CLI** | Google | 🆓 FREE tier! | General, budget-friendly | ⭐ Easy |
| **Cursor** | Cursor Inc | $20/mo | Full IDE experience | ⭐ Easy |
| **Continue** | Open Source | API ($) | VS Code integration | ⭐ Easy |

---

## 1️⃣ Claude Code (Anthropic)

### Web vs CLI

| Claude.ai (Web) | Claude Code (CLI) |
|-----------------|-------------------|
| Chat interface | Terminal interface |
| Upload files one by one | Read entire directories |
| Copy-paste code back | Edits files directly |
| Limited context | Extended context |
| No shell access | Can run commands |

### Getting Started

```bash
# Install
npm install -g @anthropic-ai/claude-code

# Set API key
export ANTHROPIC_API_KEY="sk-ant-..."

# Run
claude
```

### Pricing
- Pay per token (API usage)
- ~$3 per 1M input tokens (Claude 3.5 Sonnet)
- ~$15 per 1M output tokens

### Best For
- Refactoring code
- Explaining complex codebases
- Writing documentation

---

## 2️⃣ Gemini CLI (Google) 🆓 FREE TIER!

### Why Gemini?
- **Free tier:** 15 requests/minute, 1M tokens/day
- Good for learning without spending money
- Competitive quality with GPT-4

### Getting Started

```bash
# Install
npm install -g @anthropic-ai/claude-code

# Or use Google's official approach
pip install google-generativeai

# Get FREE API key at:
# https://aistudio.google.com/app/apikey

# Set key
export GOOGLE_API_KEY="AIza..."
```

### Using with aider (Free!)

```bash
# Install aider
pip install aider-chat

# Use with Gemini (free!)
aider --model gemini/gemini-1.5-flash
```

### Pricing
| Tier | Cost | Limits |
|------|------|--------|
| Free | $0 | 15 RPM, 1M tokens/day |
| Pay-as-you-go | ~$0.075/1M tokens | Higher limits |

### Best For
- Learning CLI AI tools without cost
- Quick tasks and experiments
- Budget-conscious teams

---

## 3️⃣ GitHub Copilot CLI

### What It Does
- Suggests shell commands from natural language
- Explains complex commands
- Integrated with `gh` CLI

### Getting Started

```bash
# Requires GitHub Copilot subscription ($10/mo individual, $19/mo business)

# Install extension
gh extension install github/gh-copilot

# Suggest a command
gh copilot suggest "find all files larger than 100MB"

# Explain a command
gh copilot explain "tar -xzvf archive.tar.gz"
```

### Pricing
- Individual: $10/month
- Business: $19/month
- Free for students & open source maintainers

### Best For
- DevOps tasks
- Learning shell commands
- Git operations

---

## 4️⃣ aider (Open Source)

### What Makes It Special
- Git-aware: auto-commits changes
- Multi-file editing
- Works with ANY model (OpenAI, Anthropic, Gemini, local)

### Getting Started

```bash
# Install
pip install aider-chat

# Use with OpenAI (default)
export OPENAI_API_KEY="sk-..."
aider

# Use with Claude
export ANTHROPIC_API_KEY="sk-ant-..."
aider --model claude-3-5-sonnet-20241022

# Use with Gemini (FREE!)
export GOOGLE_API_KEY="AIza..."
aider --model gemini/gemini-1.5-flash

# Specify files to edit
aider app.py utils.py tests/
```

### Key Commands (inside aider)
```
/add file.py      # Add file to context
/drop file.py     # Remove from context
/diff             # Show pending changes
/commit           # Commit changes
/undo             # Undo last change
/help             # All commands
```

### Pricing
- Tool is free & open source
- You pay for the API of your chosen model

### Best For
- Refactoring with Git history
- Multi-file changes
- Developers who want control

---

## 5️⃣ OpenClaw (Self-hosted Gateway)

### What Makes It Special
- Connects to WhatsApp, Telegram, Discord, Slack
- Persistent memory across sessions
- Full system access (files, shell, browser)
- Runs 24/7 as a service

### Getting Started

```bash
# Install
npm install -g openclaw

# Setup wizard
openclaw onboard --install-daemon

# Open chat interface
openclaw tui
```

### Architecture
```
┌─────────────────────────────────────────┐
│              Your Machine               │
│  ┌─────────┐    ┌──────────────────┐   │
│  │OpenClaw │───▶│ Claude/GPT API   │   │
│  │ Gateway │    └──────────────────┘   │
│  └────┬────┘                           │
│       │                                │
│  ┌────┴────────────────────────────┐   │
│  │  WhatsApp  Telegram  Discord    │   │
│  └─────────────────────────────────┘   │
└─────────────────────────────────────────┘
```

### Best For
- Personal AI assistant
- Automation workflows
- Multi-platform presence

---

## 6️⃣ Cursor / Continue (IDE-based)

### For Those Who Prefer GUI

| Tool | Type | Price | Best For |
|------|------|-------|----------|
| **Cursor** | Full IDE (VS Code fork) | $20/mo | All-in-one experience |
| **Continue** | VS Code extension | Free (you pay API) | Keep your existing setup |

### Cursor Getting Started
```bash
# Download from cursor.com
# It's a full IDE, not CLI

# Features:
# - Chat with codebase
# - Auto-complete
# - Multi-file edits
```

### Continue Getting Started
```bash
# Install from VS Code marketplace
# Search: "Continue"

# Configure API keys in extension settings
# Works with any model
```

---

## 🎯 Quick Decision Guide

### "I want to try for FREE"
→ **Gemini CLI** with aider
```bash
pip install aider-chat
export GOOGLE_API_KEY="your-free-key"
aider --model gemini/gemini-1.5-flash
```

### "I want the best quality"
→ **Claude Code** or **aider with Claude**
```bash
npm install -g @anthropic-ai/claude-code
claude
```

### "I just want shell command help"
→ **GitHub Copilot CLI**
```bash
gh copilot suggest "your task"
```

### "I want a personal AI assistant"
→ **OpenClaw**
```bash
openclaw onboard --install-daemon
```

### "I don't want to leave my IDE"
→ **Cursor** or **Continue**

---

## 💰 Cost Comparison (Typical Usage)

| Tool | Light Use (1hr/day) | Heavy Use (8hr/day) |
|------|---------------------|---------------------|
| Gemini | 🆓 Free | 🆓 Free |
| Claude Code | ~$5-10/mo | ~$30-50/mo |
| aider + GPT-4 | ~$10-20/mo | ~$50-100/mo |
| GitHub Copilot | $10/mo flat | $10/mo flat |
| Cursor | $20/mo flat | $20/mo flat |

---

## 🚀 Demo Commands for Workshop

### Quick Demo 1: Gemini (Free)
```bash
# Show it's free and works
aider --model gemini/gemini-1.5-flash
# Then: "Create a hello world in Python"
```

### Quick Demo 2: Claude Code
```bash
claude
# Then: "Read this directory and explain the project structure"
```

### Quick Demo 3: Copilot CLI
```bash
gh copilot suggest "compress all png files in this folder"
# Shows the command without running it
```

---

## 📚 Resources

| Tool | Docs | API Keys |
|------|------|----------|
| Claude Code | anthropic.com/claude-code | console.anthropic.com |
| Gemini | ai.google.dev | aistudio.google.com/app/apikey |
| aider | aider.chat | (uses other providers) |
| Copilot CLI | docs.github.com/copilot | github.com/settings/copilot |
| OpenClaw | docs.openclaw.ai | (uses other providers) |

---

*Workshop by Juan Torres - Symphony Solutions 2026*
