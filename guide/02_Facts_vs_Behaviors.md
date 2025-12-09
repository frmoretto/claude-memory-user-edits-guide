---
layout: default
title: "Chapter 2: Facts vs. Behaviors"
---

# Chapter 2: The Philosophy — Facts vs. Behaviors

---

> **This is the most important chapter in the entire guide.**

Through extensive testing with 5Levels development, I discovered a critical distinction that explains why memory edits work for some people and fail for others.

---

## Memory Edits Excel At: FACTS

### What Works

- ✓ "User's name is Francesco"
- ✓ "Lives in Milan, Italy"
- ✓ "5Levels uses two-layer architecture"
- ✓ "Backend runs on Hetzner bare metal servers"
- ✓ "Project deadline: December 2025"
- ✓ "Prefers TypeScript for production code"

### Why It Works

Facts are discrete, verifiable, and don't require interpretation. Claude reads them and applies them directly.

---

## Memory Edits Struggle With: BEHAVIORS

### What Doesn't Work Reliably

- ✗ "Always check architecture docs before answering"
- ✗ "Prioritize philosophical principles over technical details"
- ✗ "Never assume traditional SaaS architecture"
- ✗ "Ask clarifying questions before making suggestions"

### Why It Struggles

Behavioral instructions require Claude to change its thinking process, not just recall information. Even with the instruction present, Claude still needs to:

1. Read it
2. Understand its relevance
3. Prioritize it over other context
4. Apply it correctly

---

## The Real-World Test

I added this memory edit:

> "CRITICAL: 5Levels uses two-layer architecture — 95% client-side processing"

Then asked: "How do we sync desktop to mobile?"

**Result:** Claude still initially assumed a traditional centralized backend approach, despite having the memory edit. Why? Because it saw "Hetzner deployment" in technical docs and jumped to conclusions.

### The Lesson

Memory edits provide context, but they don't override Claude's inference patterns. Behavioral change requires more than just instructions — it requires architectural understanding.

---

## The Golden Rule

| ✓ Store FACTS (what is true) | ✗ Don't store BEHAVIORS (what to do) |
|------------------------------|--------------------------------------|
| "Backend stores 7KB per user" | "Always remember the backend is minimal" |
| "Prefers Python over Ruby" | "Never suggest Ruby" |
| "Layer 1 = Chrome extension, Layer 2 = Hetzner API" | "Always distinguish between Layer 1 and Layer 2" |

---

## Cross-Domain Examples

### E-Commerce Project

**Before:** "What payment system should we use?"

Claude: *[Suggests Stripe, PayPal, Square without context]*

**After** (Memory Edit: "Payment: Stripe only, no PayPal due to dispute rates"):

Claude: "Based on your decision to use Stripe (avoiding PayPal due to dispute rates)..."

### Mobile App Project

**Before:** "Should we support Android?"

Claude: *[Discusses pros/cons of cross-platform]*

**After** (Memory Edit: "iOS-first strategy, Android postponed to v2.0"):

Claude: "Since you're focusing on iOS-first with Android planned for v2.0..."

### Data Pipeline Project

**Before:** "How should we handle ETL?"

Claude: *[Suggests various ETL tools]*

**After** (Memory Edit: "ETL: Apache Airflow on AWS, no cloud-vendor lock-in"):

Claude: "For your Airflow-based ETL on AWS…"

---

## The Reliability Spectrum

| Use Case | Reliability |
|----------|-------------|
| Pure facts (names, dates, tech choices) | ~90% |
| Anti-patterns with negatives | ~70% |
| Documentation pointers | ~60% |
| Behavioral instructions | ~30% |

---

**End of Chapter 2**

---

← [Chapter 1: The Discovery](./01_The_Discovery.html) | [Chapter 3: The Four Commands →](./03_The_Four_Commands.html)
