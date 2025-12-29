# 🔍 LangSmith Fetch Skill for Claude Code

> **AI observability & debugging skill for Claude!**

Debug LangChain and LangGraph agents by fetching execution traces from LangSmith Studio directly in your terminal using Claude Code.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude-Code-blue)](https://code.claude.com)
[![LangSmith](https://img.shields.io/badge/LangSmith-Fetch-green)](https://github.com/langchain-ai/langsmith-fetch)

---

## 🎯 What It Does

This Claude Code skill teaches Claude how to debug your LangChain and LangGraph agents by automatically fetching and analyzing execution traces from LangSmith Studio.

**Just ask Claude:**
- *"Debug my agent"*
- *"What went wrong?"*
- *"Show me recent traces"*
- *"Why is my agent slow?"*

Claude will automatically fetch traces, analyze execution patterns, identify errors, and provide actionable insights!

---

## ✨ Features

- 🐛 **Automatic Debugging** - Claude fetches and analyzes traces autonomously
- 🔍 **Error Detection** - Identifies failures and root causes
- 📊 **Performance Analysis** - Tracks execution time and token usage
- 💾 **Memory Operations** - Checks LTM recall/store operations
- 🛠️ **Tool Call Analysis** - Reviews which tools were called and why
- 📁 **Session Export** - Saves debugging sessions for later review
- 🤝 **Multi-Agent Support** - Debugs orchestration decisions

---

## 🚀 Quick Start

### 1. Install Prerequisites

```bash
# Install langsmith-fetch CLI
pip install langsmith-fetch
```

### 2. Configure Environment

```bash
# Set your LangSmith credentials
export LANGSMITH_API_KEY="your_langsmith_api_key"
export LANGSMITH_PROJECT="your_project_name"
```

Get your API key from: https://smith.langchain.com/

### 3. Install the Skill

#### Option A: Personal Skill (Just for you)
```bash
mkdir -p ~/.claude/skills/langsmith-fetch
curl -o ~/.claude/skills/langsmith-fetch/SKILL.md https://raw.githubusercontent.com/OthmanAdi/langsmith-fetch-skill/main/SKILL.md
```

#### Option B: Project Skill (Share with team)
```bash
mkdir -p .claude/skills/langsmith-fetch
curl -o .claude/skills/langsmith-fetch/SKILL.md https://raw.githubusercontent.com/OthmanAdi/langsmith-fetch-skill/main/SKILL.md
git add .claude/skills/
git commit -m "Add LangSmith Fetch skill"
git push
```

### 4. Use with Claude

Open Claude Code and ask:
```
Debug my agent - what happened in the last 5 minutes?
```

Claude will automatically use this skill! 🎉

---

## 💡 Usage Examples

### Example 1: Quick Debug
```
You: "Debug my agent"

Claude:
Found 3 traces in the last 5 minutes:

Trace 1: ✅ Success
- Agent: memento
- Tools: recall_memories, create_entities
- Duration: 2.3s
- Tokens: 1,245

Trace 2: ❌ Error
- Agent: cypher
- Error: "Neo4j connection timeout"
- Duration: 15.1s
- Failed at: search_nodes tool

💡 Issue: Neo4j timeout. Check database connection and add retry logic.
```

### Example 2: Error Investigation
```
You: "Why did trace abc123 fail?"

Claude:
Deep Dive Analysis - Trace abc123

Goal: User asked "Find all projects"

Execution Flow:
1. ✅ search_nodes → Found 24 nodes
2. ❌ get_node_details → Error: "Node not found"

Root Cause: Search returned deleted node IDs

Suggested Fix:
1. Add error handling in get_node_details
2. Filter deleted nodes in search results
```

### Example 3: Performance Analysis
```
You: "Why is my agent slow?"

Claude:
Performance Analysis - Last 30 minutes

Average execution time: 8.7s
Slowest operation: search_nodes (6.2s avg)
Token usage: 2,145 tokens/trace

Bottlenecks:
1. Neo4j queries taking 71% of time
2. Large context window (15K tokens)

Recommendations:
1. Add database indexes
2. Implement context trimming
3. Cache frequently accessed nodes
```

---

## 🎓 How It Works

1. **Claude listens** for debugging-related questions
2. **Automatically activates** this skill when appropriate
3. **Runs langsmith-fetch** commands to get trace data
4. **Analyzes** execution patterns, errors, and performance
5. **Presents insights** in human-readable format

---

## 📚 Capabilities

### ✅ What Claude Can Do

- Fetch recent traces (last N minutes)
- Analyze specific trace by ID
- Export debugging sessions to files
- Detect and categorize errors
- Review tool calls and results
- Check memory operations (LTM)
- Track token usage and costs
- Compare agent performance
- Identify bottlenecks
- Suggest optimizations

### 🔧 Supported Commands

The skill uses these `langsmith-fetch` commands:
```bash
langsmith-fetch traces         # Get recent traces
langsmith-fetch trace <id>     # Get specific trace
langsmith-fetch threads        # Get conversations
langsmith-fetch config         # Manage configuration
```

---

## 🛠️ Configuration

### Environment Variables

**Required:**
```bash
LANGSMITH_API_KEY    # Your LangSmith API key
LANGSMITH_PROJECT    # Your project name
```

**Optional:**
```bash
LANGCHAIN_ENDPOINT   # Custom endpoint (default: https://api.smith.langchain.com)
```

### Making Variables Persistent

Add to `~/.bashrc` or `~/.zshrc`:
```bash
echo 'export LANGSMITH_API_KEY="your_key"' >> ~/.bashrc
echo 'export LANGSMITH_PROJECT="your_project"' >> ~/.bashrc
source ~/.bashrc
```

---

## 🔍 Troubleshooting

### "No traces found"

**Cause:** No recent agent activity or tracing disabled

**Fix:**
```bash
# Check environment
echo $LANGSMITH_API_KEY
echo $LANGSMITH_PROJECT

# Try longer timeframe
langsmith-fetch traces --last-n-minutes 1440 --limit 50

# Verify tracing is enabled
# In your code: LANGCHAIN_TRACING_V2=true
```

### Skill not activating

**Fix:**
1. Ensure `SKILL.md` is in `~/.claude/skills/langsmith-fetch/`
2. Restart Claude Code
3. Use specific trigger phrases: "debug my agent", "show traces"

### Command not found

**Fix:**
```bash
# Verify langsmith-fetch is installed
pip list | grep langsmith-fetch

# Reinstall if needed
pip install --upgrade langsmith-fetch
```

---

## 🤝 Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Ideas for contributions:**
- Additional analysis workflows
- More debugging patterns
- Performance optimization tips
- Better error categorization
- Integration examples

---

## 📖 Resources

- **LangSmith Fetch CLI:** https://github.com/langchain-ai/langsmith-fetch
- **LangSmith Studio:** https://smith.langchain.com/
- **LangChain Docs:** https://docs.langchain.com/
- **Claude Code Skills:** https://code.claude.com/docs/en/skills
- **Awesome Claude Skills:** https://github.com/ComposioHQ/awesome-claude-skills

---

## 📝 License

MIT © [Ahmad Othman Ammar Adi](https://github.com/OthmanAdi)

---

## 👨‍💻 Author

**Ahmad Othman Ammar Adi**
- 🏢 AI Agents Orchestrator at migRaven
- 🌐 Website: [othmanadi.com](https://othmanadi.com)
- 💼 LinkedIn: [codingwithadi](https://linkedin.com/in/codingwithadi)
- 🐙 GitHub: [@OthmanAdi](https://github.com/OthmanAdi)

---

## 🌟 Show Your Support

If this skill helps you debug your agents, please:
- ⭐ Star this repository
- 🐛 Report issues you find
- 💡 Suggest improvements
- 🤝 Contribute enhancements
- 📢 Share with the community

---

## 🔗 Related Projects

- [PromptFusion](https://github.com/OthmanAdi/promptfusion) - Semantic weighted prompt composition for AI agents

---

## 📊 Stats

- **Version:** 0.1.0
- **Status:** Active Development
- **First Released:** December 2025
- **Category:** AI Observability & Debugging

---

## 🎄 Season's Greetings

Wishing you a Merry Christmas and a Happy New Year 2026! 🎉
May your agents run smoothly and your debugging be swift in the year ahead!

*(This message will be updated in future releases)*

---

**Built with ❤️ by [Ahmad Othman Ammar Adi](https://github.com/OthmanAdi) for the AI debugging community**

*This is the AI observability skill for Claude Code. Help us make it better!*
