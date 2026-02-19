# 🎯 AI CLI Workshop - Cheat Sheet

## Quick Reference for the Live Demo

---

## 🛠️ Tools to Show

### 1. Claude Code (Anthropic)
```bash
# Install
npm install -g @anthropic-ai/claude-code

# Use
claude

# Or with a prompt
claude "explain this error log"
```

### 2. OpenClaw (Self-hosted Gateway)
```bash
# Install
npm install -g openclaw

# Setup
openclaw onboard --install-daemon

# Chat interface
openclaw tui
```

### 3. GitHub Copilot CLI
```bash
# Install (requires GitHub Copilot subscription)
gh extension install github/gh-copilot

# Suggest shell commands
gh copilot suggest "find all .log files larger than 100MB"

# Explain a command
gh copilot explain "tar -xzvf archive.tar.gz"
```

### 4. aider (AI Pair Programmer)
```bash
# Install
pip install aider-chat

# Use in a git repo
aider

# Or with specific files
aider app.py utils.py
```

---

## 💬 Demo Flow

### Scenario 1: Developer (Logs)
```bash
cd scenarios/01-developer
cat PROBLEM.md
# Then use Claude/OpenClaw to analyze server-logs.txt
```

### Scenario 2: PM (Sales Data)
```bash
cd scenarios/02-pm-analyst
cat PROBLEM.md
# Then use Claude/OpenClaw to analyze sales-q4-2025.csv
```

### Scenario 3: HR (Interview Notes)
```bash
cd scenarios/03-hr-marketing
cat PROBLEM.md
# Then use Claude/OpenClaw to process interview-notes.md
```

---

## 🎤 Talking Points

### Why CLI over Web?
1. **Direct file access** - No copy-paste needed
2. **Larger context** - Can read entire codebases
3. **Automation** - Script and pipeline integration
4. **Privacy** - Local processing possible
5. **Speed** - No browser overhead

### Who Can Use This?
- ✅ Developers (obviously)
- ✅ PMs analyzing data
- ✅ HR processing documents
- ✅ Marketing generating content
- ✅ Anyone who works with text!

### Best Practices
1. **Be specific** - The more detail, the better output
2. **Iterate** - First response isn't always best
3. **Verify** - AI makes mistakes, always review
4. **Context is king** - Feed it relevant files

---

## ⚡ Quick Prompts That Impress

```
# Analyze any file
"Read [filename] and summarize the key points"

# Find patterns
"What patterns do you see in this data?"

# Generate code
"Write a script that does X"

# Explain complex things
"Explain this like I'm a PM who doesn't code"

# Transform data
"Convert this CSV to a markdown table"

# Write content
"Draft a professional email about X"
```

---

## 🚨 Common Issues

| Problem | Solution |
|---------|----------|
| API key not set | Check `$ANTHROPIC_API_KEY` or provider config |
| File too large | Split it or use `head -1000 file.txt` |
| Wrong output | Be more specific in your prompt |
| Slow response | Large files = more tokens = slower |

---

## 📚 Resources

- Claude Code: https://www.anthropic.com/claude-code
- OpenClaw: https://github.com/openclaw/openclaw
- aider: https://aider.chat
- GitHub Copilot CLI: https://docs.github.com/en/copilot

---

*Workshop by Juan Torres - Symphony Solutions 2026*
