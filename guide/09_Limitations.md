---
layout: default
title: "Chapter 9: Limitations"
---

# Chapter 9: The Honest Limitations

*What memory edits cannot do—and why that's okay.*

---

## What Memory Edits Cannot Do

Let's be brutally honest about limitations:

### 1. They Don't Scale With Complexity

**The Problem:**
- With 48 documentation files totaling 2MB, even perfect memory edits (6KB) represent **0.3%** of total context.

**What This Means:** 
Memory edits can get "drowned out" by massive documentation sets. They're not strong enough to override detailed technical specifications.

---

### 2. They Can't Enforce Workflows

**Doesn't Work:**
```
"Always search project knowledge before answering architectural questions"
```

**Why It Fails:** 
Claude's attention is distributed across multiple priorities. A memory edit can't force Claude to reorder this priority stack.

---

### 3. They Don't Prevent All Hallucinations

**Example:**
- Memory edit: "Uses PostgreSQL 15"
- Claude might still occasionally suggest: "Let's add a MongoDB collection for caching"

**Why:** 
In the moment, Claude might think MongoDB is a reasonable optimization without double-checking memory edits.

---

### 4. They Require Active Maintenance

**The Reality:**
- Projects evolve
- Facts change
- Terminology shifts
- Priorities reprioritize

If you don't maintain memory edits, they become stale and eventually misleading.

**Recommendation:** Review memory edits monthly.

---

### 5. They Can Create False Confidence

**The Danger:**
- User thinks: "I added memory edits, so Claude will always remember!"

**Reality:** 
Memory edits help significantly, but don't guarantee perfect recall.

**Solution:** 
Memory edits + active steering + good documentation.

---

## The Four-Layer System

Memory edits work best as part of a complete system:

| Layer | Contribution | Purpose |
|-------|-------------|---------|
| **Project Instructions** | 25% | Define working framework and behavioral patterns |
| **Documentation** | 35% | Provide comprehensive detailed information |
| **Memory Edits** | 30% | Keep critical facts in focus (punches above its weight!) |
| **Active Steering** | 10% | Real-time corrections when needed |

**The Insight:** 
Memory edits achieve 30% contribution from just 656 characters because they work synergistically with the other layers.

---

## When Memory Edits Work Best

✅ **Perfect for:**
- Core identity facts that never change
- Facts Claude gets wrong repeatedly
- Critical constraints (budget, deadline, compliance)
- Disambiguation of confusing terminology
- Small projects with simple facts

❌ **Not effective for:**
- Behavioral instructions ("always do X")
- Complex conditional logic
- Information that changes frequently
- Large, complex projects where they become a drop in the ocean

---

## The Bottom Line

Memory edits aren't magic. They won't fix:
- Bad documentation
- Unclear architecture
- Missing context

But they're more effective than the lack of mainstream success stories suggests. When used correctly—for the right problems, with realistic expectations—they provide measurable, significant improvements.

**They're a power-user tool that rewards understanding over casual use.**

---

← [Chapter 8: Troubleshooting](./08_Troubleshooting.html) | [Back to Guide Index →](../index.html)

---

*Guide by Francesco Marinoni Moretto — CC BY 4.0*
