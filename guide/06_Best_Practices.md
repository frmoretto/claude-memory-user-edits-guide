# Chapter 6: Best Practices From Power Users

---

After analyzing Reddit discussions and extensive testing, here are the patterns that work.

---

## 1. Keep Edits Atomic and Factual

**Good (54 chars):**
```
Backend uses PostgreSQL 15 with Knex.js query builder
```

**Bad (98 chars):**
```
Backend database architecture follows modern best practices with proper 
indexing and query optimization using PostgreSQL
```

*Why: The first is a verifiable fact. The second is vague and requires interpretation.*

---

## 2. Use Present Tense, Not Imperatives

**Good (36 chars):**
```
User prefers TypeScript over JavaScript
```

**Bad (40 chars):**
```
Always use TypeScript, never JavaScript
```

*Why: Memory edits describe reality, they don't command behavior.*

---

## 3. Avoid Redundancy With System Prompts

**Don't Add:**
```
Check project knowledge before answering questions
```

*Why: Claude's system prompt already tells it to prioritize project_knowledge_search. Redundant memory edits just waste space.*

---

## 4. Prioritize Ruthlessly

You only get 30 edits of 200 characters each. That's 6,000 characters total (about 2 pages of text).

### Priority Framework

| Priority | Description | Action |
|----------|-------------|--------|
| **P0** | Facts Claude gets wrong repeatedly | Keep Always |
| **P1** | Important preferences, key definitions | Keep If Space |
| **P2** | Nice-to-haves, well-documented info | Remove First |

---

## 5. Version Your Memory Edits

When working on multi-month projects:

**Before (51 chars):**
```
Project deadline: Q4 2025
```

**After (77 chars):**
```
Project deadline: January 15, 2026 (extended from Q4 2025)
```

*Why: Including the "why" helps Claude understand context.*

---

## 6. Use Negative Definitions

When terminology could be confusing:

**Good (147 chars):**
```
Stitching engine = cross-referencing Sales Navigator data with LinkedIn 
feed patterns. NOT web scraping. NOT API calls. NOT automation.
```

*The negative examples help prevent misinterpretation.*

---

## 7. Avoid Over-Nesting

**Bad (198 chars at limit):**
```
Architecture: Layer 1 (extension with scanner, processor, storage) connects 
to Layer 2 (API with auth, intelligence, sync) which connects to database 
(PostgreSQL with 35 tables)
```

**Good:** Use 3 separate edits:

```
1. "Layer 1: Chrome extension does scanning, processing, local storage" (72 chars)
2. "Layer 2: Hetzner API handles auth, intelligence aggregation, sync" (76 chars)
3. "Database: PostgreSQL 15 with 35 tables, hosted on Hetzner" (58 chars)
```

*Why: Multiple simple edits > one complex edit.*

---

## 8. Test Your Edits

After adding memory edits, ask Claude questions that should trigger them:

| Memory Edit Topic | Test Query | Expected Mention |
|-------------------|------------|------------------|
| Mobile strategy | "What's our mobile strategy?" | "dashboard-only viewing" |
| Data storage | "Where do we store data?" | "two-layer architecture" |
| Database | "What database do we use?" | "PostgreSQL 15" |

If Claude doesn't use the memory edit in its answer, the edit is either:
- Too vague
- Not relevant to the query
- Buried under other context

---

## 9. Add Character Counts to Your Drafts

Before adding a memory edit, check the character count:

| Status | Chars | Example |
|--------|-------|---------|
| ✓ Good | 34 | "Backend: PostgreSQL 15 + Knex.js" |
| ~ Verbose | 89 | "Backend database uses PostgreSQL version 15 with Knex.js query builder for type safety" |
| ✗ Too long | 174 | "Our backend database architecture utilizes PostgreSQL version 15 along with the Knex.js query builder which provides excellent type safety and prevents SQL injection attacks" |

---

## 10. Strategic Redundancy for Critical Facts

For absolutely critical facts that are frequently misunderstood, state them multiple ways:

```
Edit 1 (60 chars): "Backend stores 7KB per user (final suggestions only)"
Edit 2 (66 chars): "Raw data and algorithms stay in Chrome extension (Layer 1)"
Edit 3 (86 chars): "Two-layer architecture provides anti-piracy (backend has no algorithms)"
```

### Why It Works
Increases probability Claude will catch at least one reference.

### Trade-off
Uses 3 edit slots instead of 1. Only do this for facts that are absolutely critical.

---

## Quick Reference: The 10 Best Practices

| # | Practice | Key Point |
|---|----------|-----------|
| 1 | Atomic and Factual | Verifiable facts, not opinions |
| 2 | Present Tense | Describe reality, don't command |
| 3 | No Redundancy | Don't duplicate system prompt |
| 4 | Prioritize | P0 > P1 > P2 |
| 5 | Version | Include "why" for changes |
| 6 | Negative Definitions | Say what it's NOT |
| 7 | No Over-Nesting | Simple edits > complex edits |
| 8 | Test Edits | Verify they trigger |
| 9 | Count Characters | Stay under 200 |
| 10 | Strategic Redundancy | Only for critical facts |

---

**End of Chapter 6**

---

← [Chapter 5: Case Study](./05_Case_Study_5Levels.md) | [Chapter 7: Managing Limits →](./07_Managing_Limits.md)
