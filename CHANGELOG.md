# Changelog

All notable changes to the LangSmith Fetch Skill will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [0.1.0] - 2025-12-24

### 🎉 Initial Release

**The first AI observability & debugging skill for Claude Code!**

### Added

#### Core Features
- ✅ **Automatic debugging** - Claude autonomously fetches and analyzes LangSmith traces
- ✅ **Four core workflows:**
  1. Quick Debug Recent Activity (5-minute traces)
  2. Deep Dive Specific Trace (by trace ID)
  3. Export Debug Session (save to organized folders)
  4. Error Detection (find and categorize failures)

#### Skill Capabilities
- ✅ Fetch recent traces with time-based filtering
- ✅ Analyze specific trace by ID
- ✅ Export sessions to files with metadata
- ✅ Detect and categorize errors
- ✅ Review tool calls and results
- ✅ Check memory operations (LTM)
- ✅ Track token usage and costs
- ✅ Compare agent performance
- ✅ Identify bottlenecks
- ✅ Suggest optimizations

#### Documentation
- ✅ Complete `SKILL.md` with YAML frontmatter and detailed workflows
- ✅ Professional `README.md` with installation and usage guides
- ✅ `CONTRIBUTING.md` with contribution guidelines and templates
- ✅ MIT `LICENSE`
- ✅ This `CHANGELOG.md`

#### Examples & Guides
- ✅ Response format examples for each workflow
- ✅ Common use cases (Agent Not Responding, Wrong Tool Called, Memory Not Working, Performance Issues)
- ✅ Troubleshooting guide
- ✅ Best practices for debugging
- ✅ Quick reference command guide

#### Integration
- ✅ Seamless Claude Code integration
- ✅ Model-invoked activation (Claude decides when to use)
- ✅ PowerShell and Bash command examples
- ✅ Environment variable setup guide

### Requirements
- `langsmith-fetch` CLI (>= 0.1.0)
- `LANGSMITH_API_KEY` environment variable
- `LANGSMITH_PROJECT` environment variable

### Activation Keywords
Claude automatically activates this skill when users mention:
- "Debug my agent"
- "What went wrong?"
- "Show me recent traces"
- "Check for errors"
- "Analyze memory operations"
- "Review agent performance"
- "What tools were called?"

### Authors
- **Ahmad Othman Ammar Adi** - *Initial work* - [@OthmanAdi](https://github.com/OthmanAdi)

### Acknowledgments
- LangChain team for the excellent `langsmith-fetch` CLI
- Anthropic for Claude Code and the Skills framework
- The AI observability community

---

## [Unreleased]

### Planned Features
- Enhanced multi-agent orchestration debugging
- Cost tracking and optimization suggestions
- Performance profiling workflows
- Custom export formats
- Team collaboration features

---

**Note:** This is the first AI observability skill for Claude Code. We're excited to see how the community uses and improves it!

For full details on each release, see the [Releases page](https://github.com/OthmanAdi/langsmith-fetch-skill/releases).
