---
layout: default
title: "7. Managing Limits"
parent: Guide
nav_order: 7
---

# Chapter 7: Managing Your 30-Edit Limit

---

When you hit 30 edits, use this priority framework to decide what to remove.

---

## Priority Framework

### P0 — Keep Always

- Core architecture facts that Claude gets wrong repeatedly
- Critical constraints (legal, budget, timeline)
- Terms Claude consistently misinterprets

### P1 — Keep If Space

- Important preferences (language, framework choices)
- Key definitions and terminology
- Anti-patterns that Claude suggests occasionally

### P2 — Remove First

- Information already well-documented
- Outdated facts from earlier project phases
- Nice-to-haves that don't cause errors

---

## Migration Strategy

### Step 1: Audit Your Current Edits

Run: `memory_user_edits view`

Review each edit and mark it: P0 / P1 / P2

### Step 2: Remove Low-Priority Edits

- Delete all P2 edits first
- If still at limit, evaluate P1 edits

### Step 3: Consolidate Related Edits

Look for edits that can be combined (see examples below)

### Step 4: Add New High-Priority Edit

Only add P0 edits when at capacity

---

## Consolidation Examples

### Example 1: Three → One

**Before (3 edits, 120 total chars):**
```
1. "Layer 1: Chrome extension does scanning" (41 chars)
2. "Layer 1 does intelligence processing" (37 chars)
3. "Layer 1 stores data locally in IndexedDB" (42 chars)
```

**After (1 edit, 90 chars):**
```
1. "Layer 1 (Chrome extension): scanning, intelligence processing, local IndexedDB storage"
```

**Result:** Saved 2 edit slots, reduced chars from 120 → 90

### Example 2: Two → One

**Before (2 edits, 65 total chars):**
```
1. "Uses PostgreSQL 15" (18 chars)
2. "Uses Knex.js query builder for database access" (47 chars)
```

**After (1 edit, 54 chars):**
```
1. "Database: PostgreSQL 15 with Knex.js query builder"
```

**Result:** Saved 1 edit slot, reduced chars from 65 → 54

---

## Maintenance Checklist

### Monthly Review

- [ ] Run `memory_user_edits view`
- [ ] Check if any facts are outdated
- [ ] Remove obsolete edits (completed phases, changed decisions)
- [ ] Test 3-5 random queries to verify edits still trigger
- [ ] Consolidate related edits if approaching 30 limit
- [ ] Update version tags if architecture evolved

### After Major Project Changes

- [ ] Review architectural edits for accuracy
- [ ] Update deadlines, constraints, preferences
- [ ] Add new terminology from recent work
- [ ] Remove deprecated technology mentions

### Red Flags (Review Immediately)

- Claude starts getting facts wrong again
- New team member sees inconsistent responses
- Project pivot changes core assumptions
- You're explaining the same thing repeatedly again

---

## Decision Tree: Should You Use Memory Edits?

```
START: Have you set up Project Instructions for this project?
 │
 ├─ NO  →  Set up Project Instructions FIRST
 │        (Define HOW Claude should work)
 │        Then return here to add Memory Edits
 │
 └─ YES →  Do you use Claude for complex technical work?
    │
    ├─ NO  →  Memory edits probably not worth the effort
    │
    └─ YES →  Are you in a Claude Project?
       │
       ├─ NO  →  Memory edits won't work (create a project first)
       │
       └─ YES →  Do you have >20 documentation files OR >3 month timeline?
          │
          ├─ NO  →  Documentation + Instructions might be sufficient
          │        (But try 3-5 memory edits as insurance)
          │
          └─ YES →  Does Claude repeatedly get the same facts wrong?
             │
             ├─ NO  →  Monitor for a week, then reassess
             │
             └─ YES →  ✅ USE MEMORY EDITS
                      Start with 5-10 edits targeting your top errors
```

---

## Quick Self-Assessment

Check all that apply:

- [ ] I work on technical projects with Claude
- [ ] I'm in a Claude Project (not regular chat)
- [ ] Claude gets the same facts wrong repeatedly
- [ ] I have the patience to write clear, factual memory edits
- [ ] I'm willing to maintain them monthly

| Checked | Recommendation |
|---------|----------------|
| 3+ | Memory edits will help significantly |
| 1-2 | Might help, but low priority |
| 0 | Skip memory edits for now |

