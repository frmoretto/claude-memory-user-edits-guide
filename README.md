# The Complete Guide to Claude's `memory_user_edits`

> **The undocumented power tool for reliable AI memory**
> 
> Systematic testing proves: 62% fewer errors • Up to 100% accuracy improvement

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by/4.0/)
[![Research](https://img.shields.io/badge/Research-Systematic%20Testing-blue)](https://github.com/frmoretto/claude-memory-user-edits-guide)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/frmoretto/claude-memory-user-edits-guide/pulls)

---

## 🌐 Read Online

**→ [frmoretto.github.io/claude-memory-user-edits-guide](https://frmoretto.github.io/claude-memory-user-edits-guide/)**

**→ [Complete Guide (Single File)](./The_Complete_Guide_to_Claude_memory_user_edits.md)** — Full 2000+ line guide in one document

---

## 🎯 The Core Insight

**Memory edits work for FACTS, not BEHAVIORS.**

| ✅ Works | ❌ Doesn't Work |
|----------|----------------|
| "Backend stores 7KB per user" | "Always check docs first" |
| "Architecture: two-layer model" | "Prioritize architecture over details" |

This one insight separates failed experiments from 62% error reduction.

---

## 📊 Proven Results

From controlled testing with [5Levels](https://github.com/frmoretto/5levels) (48 documentation files, 35 database tables, 11 modules):

| Metric | Improvement |
|--------|-------------|
| **Architectural errors** | ↓ 62% reduction |
| **First-try accuracy** | ↑ 60% → 100% |
| **Context rebuilding** | ↓ Zero needed |
| **Steering required** | ↓ 3x less |

---

## 🚀 Quick Start

**5-Minute Test:**

1. Open a Claude Project
2. Ask Claude: "Please add a memory edit: 'User works on [YourProject]'"
3. Start a new conversation
4. Ask: "What project am I working on?"

Claude will remember—even though you never mentioned it in this conversation.

**→ [TL;DR Version](./TLDR.md)** (2-minute read)

---

## 📖 The Guide

The [`/guide`](./guide) folder contains the complete methodology:

| Chapter | Topic |
|---------|-------|
| [Chapter 1](./guide/01_The_Discovery.md) | The Discovery |
| [Chapter 2](./guide/02_Facts_vs_Behaviors.md) | Facts vs. Behaviors (The Key Insight) |
| [Chapter 3](./guide/03_The_Four_Commands.md) | The Four Commands |
| [Chapter 4](./guide/04_What_Works.md) | What Works (And What Doesn't) |
| [Chapter 5](./guide/05_Case_Study_5Levels.md) | Real-World Case Study: 5Levels |
| [Chapter 6](./guide/06_Best_Practices.md) | Best Practices |
| [Chapter 7](./guide/07_Managing_Limits.md) | Managing Your 30-Edit Limit |
| [Chapter 8](./guide/08_Troubleshooting.md) | Troubleshooting |
| [Chapter 9](./guide/09_Limitations.md) | The Honest Limitations |

**Prefer a single file?** → [Complete Guide (all chapters)](./The_Complete_Guide_to_Claude_memory_user_edits.md)

---

## 📋 Templates

The [`/templates`](./templates) folder contains starter sets by project type:

| Template | Use Case |
|----------|----------|
| [Web Development](./templates/WEB_DEVELOPMENT.md) | Full-stack web projects |
| [Data Science](./templates/DATA_SCIENCE.md) | ML/AI projects |
| [Mobile App](./templates/MOBILE_APP.md) | iOS, Android, React Native, Flutter |
| [E-Commerce](./templates/ECOMMERCE.md) | Online stores, marketplaces |
| [Content Writing](./templates/CONTENT_WRITING.md) | Blogs, social media, documentation |

---

## 🔧 Claude Integration

The [`SKILL.md`](./SKILL.md) file is designed for Claude's Skills feature.

**How to use:**
- **Claude Web/Desktop:** Upload via Skills interface (Settings → Features → Skills)
- **Claude Projects:** Add to project knowledge

---

## 📄 Alternative Formats

| Format | Best For |
|--------|----------|
| **[Web Version](https://frmoretto.github.io/claude-memory-user-edits-guide/)** | Reading online with navigation |
| **[Complete Markdown](./The_Complete_Guide_to_Claude_memory_user_edits.md)** | Single-file, LLM-friendly |
| **[PDF Version](./The_Complete_Guide_to_Claude_memory_user_edits.pdf)** | Printing or tablet reading |
| **[Word Version](./The_Complete_Guide_to_Claude_memory_user_edits.docx)** | Editing or annotations |
| **[TL;DR](./TLDR.md)** | 2-minute summary |

---

## 🎓 Who This Is For

**Perfect for:**
- 🏢 Enterprise AI teams managing complex projects
- 👨‍💻 Developers building multi-agent systems
- 🔧 Solution architects designing AI workflows
- 📚 Technical leads coordinating AI development
- 🚀 Power users wanting expert-level Claude performance

**Not for:**
- ❌ Casual Claude users (regular memory works fine)
- ❌ Simple single-conversation tasks
- ❌ Projects without documentation

---

## 🤝 Contributing

Found something that works even better? Discovered a new pattern?

**Contributions welcome:**
- 📝 Additional examples
- 🧪 Testing results from other projects
- 🐛 Bug reports or clarifications
- 💡 Best practices from your experience

**→ [Contributing Guidelines](CONTRIBUTING.md)**

---

## 📜 License & Attribution

**License:** [Creative Commons Attribution 4.0 International (CC BY 4.0)](http://creativecommons.org/licenses/by/4.0/)

**You are free to:**
- ✅ Share and redistribute
- ✅ Adapt and build upon
- ✅ Use commercially

**Under these terms:**
- 📌 Give appropriate credit
- 📌 Link to license
- 📌 Indicate if changes were made

---

## 👤 About the Author

**Francesco Marinoni Moretto**  
Enterprise AI Leader | Constitutional AI Expert | N1AI Community

- 🔗 LinkedIn: [francesco-moretto](https://linkedin.com/in/francesco-moretto)
- 💼 N1AI: Community of 300+ AI professionals

**Related Work:**
- [Stream Coding](https://github.com/frmoretto/stream-coding) — The 10-20x methodology for AI-accelerated development
- [5Levels](https://5levels.io) — LinkedIn relationship intelligence platform

---

## 📚 Resources

**Official Documentation:**
- [Anthropic Memory Tool Docs](https://docs.claude.com/en/docs/agents-and-tools/tool-use/memory-tool)
- [Claude API Reference](https://anthropic.mintlify.app/en/release-notes/overview)

**Community:**
- [r/ClaudeAI](https://reddit.com/r/ClaudeAI)
- [r/ClaudeCode](https://reddit.com/r/ClaudeCode)
- [r/claudexplorers](https://reddit.com/r/claudexplorers)

---

## ⭐ Star This Repository

If this guide helped you achieve better Claude performance, **star this repository** to help others discover it.

**Questions? Issues? Ideas?**  
→ [Open an Issue](https://github.com/frmoretto/claude-memory-user-edits-guide/issues)

---

**Last Updated:** December 2025  
**Version:** 3.0  
**Status:** Actively Maintained

---

<p align="center">
  <strong>Stop fighting Claude's memory. Start controlling it.</strong><br>
  <a href="https://frmoretto.github.io/claude-memory-user-edits-guide/">Read Online</a> • <a href="./TLDR.md">TL;DR</a> • <a href="./The_Complete_Guide_to_Claude_memory_user_edits.md">Full Guide</a>
</p>
