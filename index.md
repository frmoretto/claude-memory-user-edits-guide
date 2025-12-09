---
layout: default
title: Claude Memory User Edits Guide
description: The undocumented power tool for reliable AI memory. Learn how memory_user_edits achieves 62% fewer errors.
---

<style>
:root {
  --font-sans: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, "Fira Sans", "Droid Sans", "Helvetica Neue", Arial, sans-serif;
  --font-mono: "SF Mono", "Fira Code", Menlo, Monaco, Consolas, monospace;
  --color-primary: #2563eb;
  --color-text: #1f2937;
  --color-border: #e5e7eb;
}
body, p, li, td, th, blockquote, span, div { font-family: var(--font-sans) !important; }
body { font-size: 16px !important; line-height: 1.7 !important; color: var(--color-text) !important; }
h1, h2, h3, h4, h5, h6 { font-family: var(--font-sans) !important; font-weight: 700 !important; color: var(--color-text) !important; }
code, pre { font-family: var(--font-mono) !important; }
table { width: 100% !important; border-collapse: collapse !important; margin: 1.5rem 0 !important; }
th, td { padding: 0.75rem 1rem !important; text-align: left !important; border: 1px solid var(--color-border) !important; }
th { background-color: #f9fafb !important; font-weight: 600 !important; }
tr:nth-child(even) { background-color: #fafafa !important; }
blockquote { border-left: 4px solid var(--color-primary) !important; background-color: #eff6ff !important; font-style: normal !important; padding: 1rem !important; }
a { color: var(--color-primary) !important; }
.main-content h1 { font-size: 2rem !important; }
.main-content h2 { font-size: 1.5rem !important; }
</style>

# The Complete Guide to Claude's `memory_user_edits`

> **The undocumented power tool for reliable AI memory**
> 
> Systematic testing proves: 62% fewer errors • Up to 100% accuracy improvement

---

## 🎯 The Core Insight

**Memory edits work for FACTS, not BEHAVIORS.**

<table>
  <thead>
    <tr>
      <th>✅ Works</th>
      <th>❌ Doesn't Work</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>"Backend stores 7KB per user"</td>
      <td>"Always check docs first"</td>
    </tr>
    <tr>
      <td>"Architecture: two-layer model"</td>
      <td>"Prioritize architecture over details"</td>
    </tr>
  </tbody>
</table>

This one insight separates failed experiments from 62% error reduction.

---

## 📊 Proven Results

From controlled testing with 5Levels (48 documentation files, 35 database tables, 11 modules):

<table>
  <thead>
    <tr>
      <th>Metric</th>
      <th>Improvement</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Architectural errors</td>
      <td>↓ 62% reduction</td>
    </tr>
    <tr>
      <td>First-try accuracy</td>
      <td>↑ 60% → 100%</td>
    </tr>
    <tr>
      <td>Context rebuilding</td>
      <td>↓ Zero needed</td>
    </tr>
  </tbody>
</table>

---

## 🚀 Quick Start

**5-Minute Test:**

1. Open a Claude Project
2. Ask Claude: "Please add a memory edit: 'User works on [YourProject]'"
3. Start a new conversation
4. Ask: "What project am I working on?"

Claude will remember—even though you never mentioned it in this conversation.

---

## 📖 Read the Guide

<table>
  <thead>
    <tr>
      <th>Chapter</th>
      <th>Topic</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="./guide/01_The_Discovery.html">Chapter 1</a></td>
      <td>The Discovery</td>
    </tr>
    <tr>
      <td><a href="./guide/02_Facts_vs_Behaviors.html">Chapter 2</a></td>
      <td>Facts vs. Behaviors (The Key Insight)</td>
    </tr>
    <tr>
      <td><a href="./guide/03_The_Four_Commands.html">Chapter 3</a></td>
      <td>The Four Commands</td>
    </tr>
    <tr>
      <td><a href="./guide/04_What_Works.html">Chapter 4</a></td>
      <td>What Works (And What Doesn't)</td>
    </tr>
    <tr>
      <td><a href="./guide/05_Case_Study_5Levels.html">Chapter 5</a></td>
      <td>Real-World Case Study: 5Levels</td>
    </tr>
    <tr>
      <td><a href="./guide/06_Best_Practices.html">Chapter 6</a></td>
      <td>Best Practices</td>
    </tr>
    <tr>
      <td><a href="./guide/07_Managing_Limits.html">Chapter 7</a></td>
      <td>Managing Your 30-Edit Limit</td>
    </tr>
    <tr>
      <td><a href="./guide/08_Troubleshooting.html">Chapter 8</a></td>
      <td>Troubleshooting</td>
    </tr>
    <tr>
      <td><a href="./guide/09_Limitations.html">Chapter 9</a></td>
      <td>The Honest Limitations</td>
    </tr>
  </tbody>
</table>

---

## 📋 Templates

Starter memory edit sets by project type:

- [Web Development](./templates/WEB_DEVELOPMENT.html)
- [Data Science](./templates/DATA_SCIENCE.html)
- [Mobile App](./templates/MOBILE_APP.html)
- [E-Commerce](./templates/ECOMMERCE.html)
- [Content Writing](./templates/CONTENT_WRITING.html)

---

## 📄 Alternative Formats

- [TL;DR Version](./TLDR.html) — 2-minute summary
- [Complete Guide (Single File)](./The_Complete_Guide_to_Claude_memory_user_edits.html) — Full 2000+ lines
- [PDF Version](./The_Complete_Guide_to_Claude_memory_user_edits.pdf) — For offline reading
- [GitHub Repository](https://github.com/frmoretto/claude-memory-user-edits-guide) — Source & contributions

---

## 👤 About

Created by **[Francesco Marinoni Moretto](https://linkedin.com/in/francesco-moretto)** while building [5Levels](https://5levels.io), a LinkedIn relationship intelligence platform.

**Related:** [Stream Coding](https://github.com/frmoretto/stream-coding) — The 10-20x methodology for AI-accelerated development

---

<p align="center">
  <strong>Stop fighting Claude's memory. Start controlling it.</strong>
</p>
