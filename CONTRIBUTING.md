# Contributing to LangSmith Fetch Skill

Thank you for your interest in contributing! This is the first AI observability skill for Claude Code, and we welcome contributions from the community.

## 🎯 Ways to Contribute

- 🐛 Report bugs and issues
- 💡 Suggest new features or improvements
- 📝 Improve documentation
- 🔧 Submit bug fixes
- ✨ Add new debugging workflows
- 🎓 Share usage examples
- 📊 Add analysis patterns

---

## 🚀 Getting Started

### 1. Fork the Repository

Click the "Fork" button at the top of this repository.

### 2. Clone Your Fork

```bash
git clone https://github.com/YOUR_USERNAME/langsmith-fetch-skill.git
cd langsmith-fetch-skill
```

### 3. Create a Branch

```bash
git checkout -b feature/your-feature-name
# or
git checkout -b fix/your-bug-fix
```

---

## 📝 Making Changes

### For SKILL.md Updates

When modifying `SKILL.md`:

1. **Test thoroughly** - Ensure Claude correctly interprets your changes
2. **Keep it focused** - Don't try to do everything in one update
3. **Maintain structure** - Follow the existing format
4. **Add examples** - Show how new features work
5. **Update version** - Bump version number if significant changes

**Testing checklist:**
- [ ] YAML frontmatter is valid
- [ ] Description clearly states when to use the skill
- [ ] Instructions are clear and actionable
- [ ] Examples work as shown
- [ ] Commands run successfully
- [ ] Claude activates skill appropriately

### For Documentation Updates

When updating README or other docs:

1. **Be clear and concise**
2. **Include code examples**
3. **Keep formatting consistent**
4. **Check for typos**
5. **Verify all links work**

---

## 🧪 Testing Your Changes

### Local Testing

1. **Install the skill locally:**
   ```bash
   mkdir -p ~/.claude/skills/langsmith-fetch-test
   cp SKILL.md ~/.claude/skills/langsmith-fetch-test/
   ```

2. **Test with Claude Code:**
   - Ask debugging questions
   - Verify Claude uses the skill
   - Check command execution
   - Validate output format

3. **Test edge cases:**
   - No traces available
   - Invalid API keys
   - Network failures
   - Large datasets

### Test Scenarios

Try these scenarios:

```
✅ "Debug my agent"
✅ "Show me recent traces"
✅ "What went wrong with trace abc123?"
✅ "Export my debug session"
✅ "Find errors in the last hour"
✅ "Why is my agent slow?"
```

---

## 📋 Pull Request Process

### 1. Commit Your Changes

```bash
git add .
git commit -m "feat: Add performance analysis workflow"
```

**Commit message format:**
- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation update
- `refactor:` Code refactoring
- `test:` Testing updates
- `chore:` Maintenance tasks

### 2. Push to Your Fork

```bash
git push origin feature/your-feature-name
```

### 3. Create Pull Request

1. Go to the original repository
2. Click "New Pull Request"
3. Select your branch
4. Fill out the PR template:

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Breaking change

## Testing
- [ ] Tested locally
- [ ] Works with Claude Code
- [ ] Examples verified
- [ ] Documentation updated

## Screenshots (if applicable)
Add screenshots showing the feature in action
```

### 4. Wait for Review

- Maintainers will review your PR
- Address any requested changes
- Once approved, your PR will be merged!

---

## 🎨 Style Guidelines

### SKILL.md Style

- **Clear headings** - Use descriptive section titles
- **Code blocks** - Always use proper syntax highlighting
- **Concise** - Get to the point quickly
- **Examples** - Show, don't just tell
- **Formatting** - Use bullet points and tables

### Code Examples

```bash
# Good - Clear, commented, complete
langsmith-fetch traces --last-n-minutes 5 --limit 5 --format pretty

# Bad - No context, unclear purpose
langsmith-fetch traces -l 5
```

### Documentation Style

- Use **active voice** ("Run this command" not "This command should be run")
- Be **specific** ("Set LANGSMITH_API_KEY" not "Configure environment")
- Include **why** not just **how**
- Add **examples** for complex concepts

---

## 💡 Feature Suggestions

### What We're Looking For

**High Priority:**
- Additional debugging patterns
- Error categorization improvements
- Performance analysis enhancements
- Multi-agent orchestration insights

**Medium Priority:**
- Cost tracking features
- Integration examples
- Visualization suggestions
- Automation workflows

**Nice to Have:**
- Advanced filtering
- Custom export formats
- Team collaboration features
- Analytics dashboards

### Suggesting Features

Create an issue with:

```markdown
## Feature Request: [Feature Name]

**Problem:**
What problem does this solve?

**Proposed Solution:**
How should it work?

**Alternatives Considered:**
What other approaches did you consider?

**Use Cases:**
When would users use this?

**Example:**
Show what it would look like
```

---

## 🐛 Reporting Bugs

### Before Reporting

1. **Search existing issues** - Maybe it's already reported
2. **Test with latest version** - Update and try again
3. **Check configuration** - Verify environment variables
4. **Try minimal example** - Isolate the problem

### Bug Report Template

```markdown
## Bug Report: [Bug Title]

**Description:**
Clear description of the bug

**To Reproduce:**
1. Step 1
2. Step 2
3. See error

**Expected Behavior:**
What should happen?

**Actual Behavior:**
What actually happens?

**Environment:**
- OS: [e.g., macOS 14.1]
- Claude Code Version: [e.g., 1.2.3]
- langsmith-fetch Version: [e.g., 0.3.1]
- Python Version: [e.g., 3.11]

**Additional Context:**
Screenshots, logs, traces, etc.
```

---

## 📚 Resources for Contributors

### Learning Materials

- [Claude Code Skills Docs](https://code.claude.com/docs/en/skills)
- [LangSmith Fetch CLI](https://github.com/langchain-ai/langsmith-fetch)
- [LangSmith Studio](https://smith.langchain.com/)
- [Claude Skills Best Practices](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills)

### Community

- **GitHub Issues:** For bugs and feature requests
- **GitHub Discussions:** For questions and ideas
- **Twitter:** [@othmanadi](https://twitter.com/othmanadi) (coming soon)

---

## ✅ Contribution Checklist

Before submitting:

- [ ] Code follows style guidelines
- [ ] Tested locally with Claude Code
- [ ] Documentation updated
- [ ] Examples work as shown
- [ ] Commit messages are clear
- [ ] PR description is complete
- [ ] No breaking changes (or clearly documented)

---

## 🎓 First-Time Contributors

New to open source? Welcome! Here's how to start:

1. **Start small** - Fix typos, improve docs
2. **Ask questions** - No question is too basic
3. **Learn by doing** - Pick a "good first issue"
4. **Be patient** - Reviews take time
5. **Have fun!** - This is a learning experience

**Good first issues:**
- Documentation improvements
- Adding usage examples
- Fixing typos
- Improving error messages

---

## 🏆 Recognition

Contributors will be:
- Listed in CONTRIBUTORS.md (coming soon)
- Thanked in release notes
- Recognized in README
- Part of building the first AI observability skill!

---

## 📞 Questions?

- **Technical:** Open an issue
- **General:** Start a discussion
- **Private:** Email (coming soon)

---

## 📜 Code of Conduct

### Our Pledge

We are committed to providing a friendly, safe, and welcoming environment for all contributors.

### Our Standards

**Positive behaviors:**
- Being respectful and inclusive
- Welcoming newcomers
- Giving and receiving constructive feedback
- Focusing on what's best for the community

**Unacceptable behaviors:**
- Harassment or discrimination
- Trolling or insulting comments
- Publishing others' private information
- Any unprofessional conduct

### Enforcement

Report issues to maintainers. We will review and take appropriate action.

---

Thank you for contributing to the first AI observability skill for Claude Code! 🎉

**Together, we're making agent debugging easier for everyone!**
