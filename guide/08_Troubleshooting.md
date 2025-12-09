# Chapter 8: Troubleshooting

---

Common problems and their solutions.

---

## Problem: Claude Ignores My Memory Edits

### Diagnosis

**1. Check if you're in a Claude Project**

Memory edits only work in Claude Projects, not regular chats.

Look at the top of your screen — do you see a project name?

If not, create a project and try again.

**2. Verify edit is a FACT not a BEHAVIOR**

| Type | Example | Works? |
|------|---------|--------|
| Behavioral | "Always check docs before answering" | ✗ |
| Factual | "Backend uses PostgreSQL 15" | ✓ |

**3. Check if query is relevant to the stored fact**

| Memory Edit | Query | Result |
|-------------|-------|--------|
| "Uses PostgreSQL 15" | "How should we implement authentication?" | Edit won't be used (not relevant) |
| "Uses PostgreSQL 15" | "What database do we use?" | Edit will be used |

**4. Ensure documentation isn't contradicting**

If you have 48 docs saying "MongoDB" and 1 memory edit saying "PostgreSQL", the docs will win.

### Fix

- Rewrite edit as more specific, atomic fact
- Ensure documentation supports the memory edit
- Test with a directly relevant query

---

## Problem: Memory Edits Work Inconsistently

### Common Causes

**1. Edit is vague**

| Type | Example |
|------|---------|
| ✗ Vague | "Uses good architecture" |
| ✓ Specific | "Uses two-layer architecture: client-heavy processing" |

**2. Edit contains conditionals**

| Type | Example |
|------|---------|
| ✗ Conditional | "If mobile query, check mobile docs first" |
| ✓ Factual | "Mobile: dashboard-only, no extension support" |

**3. Documentation overwhelms the memory edit**

- Problem: 48 docs (2MB) vs. 5 memory edits (656 chars = 0.03%)
- Solution: Use memory edits for facts NOT in docs, or facts Claude misinterprets

**4. Edit is behavioral**

| Type | Example |
|------|---------|
| ✗ Behavioral | "Always think about Layer 1 vs Layer 2" |
| ✓ Factual | "Layer 1: Chrome extension. Layer 2: Hetzner API" |

---

## Problem: Hit 30-Edit Limit, Need to Add More

### Solution

See [Chapter 7: Managing Limits](./07_Managing_Limits.md)

### Quick Fix

1. Run `memory_user_edits view`
2. Identify 3 lowest-priority edits
3. Remove them
4. Add new high-priority edit

---

## Problem: Memory Edits Worked at First, Now They Don't

### Common Causes

**1. Project evolved, edits are outdated**

| Old Edit | Reality | Fix |
|----------|---------|-----|
| "Deadline: Q4 2025" | Now Q1 2026 | Update the edit |

**2. Added too many edits, buried the important ones**

- Problem: 30 edits, only 5 are critical
- Fix: Remove 10-15 nice-to-haves, keep P0 edits only

**3. Documentation was added that contradicts edits**

- Problem: New docs say "three-layer", memory edit says "two-layer"
- Fix: Update documentation OR update memory edit

---

## Problem: Can't Tell If Memory Edits Are Being Used

### Solution: Test With Specific Queries

After adding a memory edit, ask a question that should trigger it:

```
Added: "Mobile strategy: dashboard-only viewing, no extension support"

Test query: "Can users scan LinkedIn on mobile?"

Expected: Claude should mention "dashboard-only" or "no extension support"

If not mentioned: Edit isn't being triggered
```

### Debugging Steps

1. Make query more directly relevant to edit
2. Check if edit is factual enough
3. Verify edit is under 200 chars
4. Try removing other edits to reduce noise

---

## Problem: Memory Edits Conflict With Each Other

### Example

```
Edit 1: "Uses PostgreSQL for database"
Edit 3: "Uses MongoDB for caching layer"

Query: "What database do we use?"

Claude: [Confused, mentions both]
```

### Solution: Be More Specific

```
Edit 1: "Primary database: PostgreSQL 15"
Edit 3: "Caching layer: Redis (NOT MongoDB)"
```

---

## Problem: Memory Edits Not Persisting

### Check These

1. **Are you in a Project?** Memory edits don't work in regular chat
2. **Did Claude confirm the add?** Look for "Added memory #X" response
3. **Are you in the same Project?** Each Project has separate memory edits
4. **Did you accidentally remove it?** Run `view` to check

---

## Problem: Claude Doesn't Acknowledge Memory Edits

### This Is Normal

Claude doesn't always explicitly reference memory edits in its responses. The edits influence its behavior without being quoted.

### How to Verify

Ask: "What do you know about my project's architecture?"

Claude should mention facts from your memory edits without you prompting them.

---

## Quick Troubleshooting Checklist

| Check | Fix |
|-------|-----|
| In a Claude Project? | Create project if not |
| Edit is factual? | Rewrite as fact, not behavior |
| Under 200 chars? | Trim or split |
| Query is relevant? | Test with direct question |
| Docs contradicting? | Align docs and edits |
| Too many edits? | Remove P2, keep P0 |
| Edit confirmed? | Check for "Added memory #X" |

---

**End of Chapter 8**

---

← [Chapter 7: Managing Limits](./07_Managing_Limits.md) | [Chapter 9: Limitations →](./09_Limitations.md)
