---
layout: default
title: "Chapter 5: Case Study - 5Levels"
---

# Chapter 5: Real-World Case Study — 5Levels

---

Let me show you exactly how memory edits performed in production.

---

## The Setup

| Aspect | Details |
|--------|---------|
| **Project** | 5Levels — LinkedIn intelligence platform |
| **Complexity** | 48 documentation files, 35 database tables, 11 intelligence modules |
| **Timeline** | 1 month documented work |
| **Challenge** | Keep Claude aligned across dozens of conversations |

---

## The Memory Edits Added

```
1. "5Levels Layer 1: Chrome extension on user PC does feed scanning and 
    intelligence processing locally at zero server cost" (142 chars)

2. "5Levels Layer 2: Hetzner servers only handle AI features (GPT-4/Claude 
    checks) and store final suggestions (~7KB per user)" (132 chars)

3. "5Levels mobile strategy: Dashboard-only viewing. Desktop extension 
    collects and processes, mobile displays synced suggestions" (145 chars)

4. "Two-layer architecture provides strong anti-piracy: backend only has 
    final action cards, not algorithms, raw data, or processing logic" (140 chars)

5. "Browser extensions don't work on iOS/Android Chrome. Mobile users 
    access via web dashboard only" (97 chars)
```

**Total: 5 edits, 656 characters (average 131 chars per edit)**

---

## Test Methodology

### Sample Size
- 30 queries across 3 conversations
  - 10 architectural questions ("How does sync work?")
  - 10 terminology questions ("What is the stitching engine?")
  - 10 feature questions ("Does mobile support scanning?")

### Scoring

| Score | Definition |
|-------|------------|
| ✓ **Correct** | First response was accurate, no corrections needed |
| ~ **Partial** | Response had right direction but missed details |
| ✗ **Wrong** | Required correction or re-explanation |

### Time Period

| Period | Description |
|--------|-------------|
| **Before** | Weeks 1-4 of development (no memory edits) |
| **After 1 week** | Week 5 (with 5 memory edits) |
| **Fresh test** | November 2, 2025 (clean session, same 5 edits) |

### Environment

- Claude Sonnet 4.5
- Project with 48 documentation files (2MB total)
- 5 memory edits (656 chars total = 0.03% of documentation size)

---

## The Fresh Test (November 2, 2025)

### The Test Question

> "How do we sync desktop to mobile?"

This exact question had previously caused architectural confusion.

### Before Memory Edits

```
User: "How do we sync desktop to mobile?"

Claude: [Sees Hetzner deployment docs]
        [Assumes traditional SaaS architecture]
        [Suggests centralized backend processing]

User: "No, backend runs on user pc"

Claude: [Corrects understanding]
        [Finally gets two-layer architecture right]
```

### After Memory Edits (Fresh Test)

```
User: "How do we sync desktop to mobile?"

Claude: [Immediately runs 3 project_knowledge_search queries]
        [Correctly identifies two-layer architecture]
        [Accurately describes both layers]

Response: "Based on the project documentation, here's how desktop-to-mobile 
sync works in 5Levels:

Layer 1: Desktop Extension (Data Collection & Processing)
The Chrome extension on the user's desktop scans LinkedIn feed at tiered 
intervals, processes intelligence locally, stores in IndexedDB.

Layer 2: Backend Storage (Hetzner Servers)
When the extension generates actionable intelligence, it sends final action 
cards to the backend... stores these in the daily_actions table (~7KB per 
user total)...

Layer 3: Mobile Access (Dashboard Only)
Mobile users access via app.5levels.io web dashboard... browser extensions 
don't work on mobile... Processing happens desktop-side... Backend stores 
only final cards — not raw data or algorithms (anti-piracy protection)... 
Mobile is display-only..."
```

---

## Performance Comparison

| Aspect | Without Memory Edits | With Memory Edits |
|--------|----------------------|-------------------|
| Initial Behavior | Skipped to conclusions | 3 searches first |
| Architecture Understanding | Assumed traditional SaaS | Identified two-layer correctly |
| Layer 1 Description | Wrong/missing | 100% accurate |
| Layer 2 Description | "Centralized processing" | "Minimal storage (~7KB)" |
| Mobile Strategy | Confused/incomplete | Crystal clear (dashboard-only) |
| Anti-Piracy Mention | Missed entirely | Explicitly stated |
| Needed Corrections | Yes (multiple) | No (perfect first try) |
| Response Quality | 4/10 | 10/10 |

---

## Success Metrics Over Time

| Metric | Before | After 1 Week | Fresh Test (Nov 2) |
|--------|--------|--------------|-------------------|
| Architectural errors | ~40% | ~15% | 0% (perfect) |
| Terminology consistency | 60% | 90% | 100% |
| Mobile strategy errors | 30% confusion | 0% | 0% |
| Need for corrections | Every 2-3 messages | Every 6-8 messages | Zero needed |
| First-try accuracy | 60% | 85% | 100% |
| Search-first behavior | 40% | 75% | 100% |

---

## Key Findings

The memory edits worked perfectly for this specific scenario because:

1. **Directly relevant** — All 5 memory edits related to the question
2. **Well-written** — Clear, factual, specific
3. **Complementary** — They provided context for interpreting project docs
4. **Recent** — Claude accessed them before jumping to conclusions

### The November 2, 2025 test proved that memory edits can achieve **100% accuracy** when:

- Question directly aligns with stored facts
- Edits are recent and unambiguous
- Documentation supports the memories
- Query design triggers the right memories

This moves memory edits from "helpful but unpredictable" to **"highly reliable when used correctly."**

---

## The Math

| Component | Size |
|-----------|------|
| Documentation | 2MB (48 files) |
| Memory edits | 656 chars (5 edits) |
| Memory edits as % of docs | **0.03%** |
| Error reduction | **62%** |

Memory edits punch far above their weight.

---

**End of Chapter 5**

---

← [Chapter 4: What Works](./04_What_Works.html) | [Chapter 6: Best Practices →](./06_Best_Practices.html)
