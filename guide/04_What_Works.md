# Chapter 4: What Works (And What Doesn't)

---

Based on real testing with complex projects, here are the patterns that succeed and fail.

---

## ✓ Highly Effective Uses (~90% reliability)

### 1. Core Identity Facts

| Chars | Example |
|-------|---------|
| 22 | "User name: Francesco" |
| 31 | "Company: 5Levels Intelligence" |
| 45 | "Location: Milan, Italy (CET timezone UTC+1)" |

### 2. Technical Architecture Facts

| Chars | Example |
|-------|---------|
| 57 | "Architecture: Two-layer client-heavy processing model" |
| 48 | "Backend stores only results, not raw data" |
| 35 | "Database: PostgreSQL 15, not MongoDB" |

### 3. Critical Constraints

| Chars | Example |
|-------|---------|
| 52 | "Must comply with LinkedIn Terms of Service (ToS)" |
| 64 | "Budget: €500K max (€300K development + €200K first-year ops)" |
| 41 | "Launch deadline: December 15, 2025 hard" |

### 4. Preferences & Technology Choices

| Chars | Example |
|-------|---------|
| 36 | "Prefers TypeScript over JavaScript" |
| 42 | "Hosting: Hetzner bare metal, not AWS" |
| 47 | "Query builder: Knex.js, never TypeORM" |

### 5. Project-Specific Terminology

| Chars | Example |
|-------|---------|
| 147 | "Stitching engine = cross-referencing data sources. NOT web scraping. NOT API calls. NOT automation." |
| 86 | "Temporal Intelligence: Module detecting birthdays, job changes, work anniversaries" |

---

## Moderately Effective Uses (~60-70% reliability)

### 1. Documentation Pointers

```
"Mobile strategy docs in 'Mobile and tablet extension strategy' chat from Nov 2"
```

*Note: Less reliable than pure facts; use as supplement, not primary information*

### 2. Workflow Preferences

```
"Prefers incremental development with frequent commits"
```

*Note: Works sometimes, but Claude may still suggest big-bang approaches*

### 3. Anti-Patterns

```
"NEVER suggest TypeORM. Always use Knex.js"
```

*Note: Helps, but doesn't prevent TypeORM mentions entirely*

---

## ✗ Ineffective Uses (~30% reliability)

### 1. Behavioral Instructions

```
"Always check project documentation before answering"
```

*Why: Claude has this in system prompt already; redundant*

### 2. Complex Reasoning Patterns

```
"When discussing architecture, prioritize philosophy over implementation"
```

*Why: Too abstract; Claude can't reliably apply this*

### 3. Conditional Logic

```
"If query is about mobile, search for mobile strategy chat first"
```

*Why: Memory edits don't support conditional logic*

---

## The Complete Reliability Matrix

| Use Case | Reliability | Recommendation |
|----------|-------------|----------------|
| Names, dates, locations | ~95% | ✓ Always use |
| Tech stack choices | ~90% | ✓ Always use |
| Architecture facts | ~90% | ✓ Always use |
| Constraints (budget, deadline) | ~85% | ✓ Always use |
| Terminology definitions | ~85% | ✓ Always use |
| Anti-patterns with "NEVER" | ~70% | ⚠️ Use with backup |
| Documentation pointers | ~60% | ⚠️ Extract facts instead |
| Workflow preferences | ~50% | ⚠️ Low priority |
| Behavioral instructions | ~30% | ✗ Use Project Instructions |
| Conditional logic | ~10% | ✗ Don't use |

---

## Memory Edits vs. Project Instructions

**Critical Understanding:** Memory edits work *together* with Project Instructions — they're not alternatives.

### Project Instructions: The Essential Framework

Project Instructions define:

- **HOW** Claude should work (process, methodology, workflow)
- What **role** Claude plays (specialized professional, domain expert)
- **Response structure** and format requirements
- **Writing style** rules and preferences
- **Decision-making frameworks** to follow

### Memory Edits: The Amplifier

Memory edits don't replace Project Instructions — they **AMPLIFY** them.

While Project Instructions define the working framework, memory edits ensure Claude never loses sight of critical facts — even with 48 documentation files and complex conversations.

### The Complete System

```
PROJECT INSTRUCTIONS (Essential Framework)
"HOW to work, what process to follow"
Role, methodology, structure, style
```

**+**

```
MEMORY EDITS (Critical Facts Focus)
"THESE specific facts, always visible"
Names, constraints, key architectural facts
```

**+**

```
DOCUMENTATION (Comprehensive Detail)
"All the detailed information"
Implementation guides, API docs, specs
```

**+**

```
ACTIVE STEERING (Real-time Guidance)
"Today's specific corrections"
In-conversation clarifications
```

**Together:** Claude works like an expert professional on your team.

---

**End of Chapter 4**

---

← [Chapter 3: The Four Commands](./03_The_Four_Commands.md) | [Chapter 5: Case Study →](./05_Case_Study_5Levels.md)
