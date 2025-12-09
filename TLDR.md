# TL;DR: Memory User Edits in 2 Minutes

> **The one thing to remember:** Memory edits work for **FACTS**, not **BEHAVIORS**.

---

## What It Is

`memory_user_edits` = Sticky notes that persist across all conversations in a Claude Project.

---

## The Commands

| Command | What It Does | Example |
|---------|-------------|---------|
| `view` | See all edits | "Show my memory edits" |
| `add` | Create new edit | "Remember that I use PostgreSQL" |
| `remove` | Delete by number | "Remove memory edit #3" |
| `replace` | Update existing | "Update memory #5 to say January 2026" |

---

## What Works vs. What Doesn't

| ✅ FACTS (Work) | ❌ BEHAVIORS (Don't Work) |
|----------------|--------------------------|
| "Database: PostgreSQL 15" | "Always check docs first" |
| "User lives in Milan, Italy" | "Prioritize architecture" |
| "Deadline: January 2026" | "Remember to ask questions" |

---

## Constraints

- **30 edits** maximum
- **200 characters** per edit
- **Project-scoped** only (not regular chats)

---

## 5-Minute Test

1. Open a Claude Project
2. Say: "Add a memory edit: User is testing memory_user_edits"
3. Start a NEW conversation
4. Ask: "What am I testing?"
5. Claude should remember ✓

---

## Best Practice

**Write atomic facts:**
```
✅ "Backend: PostgreSQL 15 + Knex.js" (34 chars)
❌ "We use a really good database setup" (vague)
```

---

## The System

Memory edits work best with all four layers:

```
Project Instructions (HOW to work)
        +
Documentation (detailed knowledge)
        +
Memory Edits (critical facts) ← You are here
        +
Active Steering (real-time corrections)
```

---

## Results

From 5Levels case study:
- **62% fewer** architectural errors
- **100% first-try accuracy** (up from 60%)
- **Zero context rebuilding** needed

---

**→ [Read Full Guide](./guide/01_The_Discovery.md)**

---

*Guide by Francesco Marinoni Moretto — CC BY 4.0*
