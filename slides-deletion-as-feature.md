---
paging: Slide %d / %d
---

# Deletion as a Feature: The Art of Subtraction

---

## Slide 1: Code is a Liability, Not an Asset

### The Fundamental Misunderstanding

**Traditional thinking (WRONG):**
```
More code = More productivity
Lines written = Value created
10,000 LOC project > 1,000 LOC project
```

**Reality:**
```
Code = Liability to maintain
Value = Functionality delivered
Best code = Code you didn't have to write
```

### Dijkstra's Wisdom (1972)

> "Lines of code should be regarded as 'lines spent' rather than 'lines produced'."
>
> — Edsger Dijkstra, Turing Award Lecture

**The accounting error:** Conventional wisdom foolishly books code on the wrong side of the ledger.

### Why Code is a Liability

**Every line of code incurs:**
- Maintenance cost (forever)
- Cognitive load (for every reader)
- Bug surface area (more places to fail)
- Dependency risk (libraries, APIs, platforms)
- Technical debt (as technology evolves)

**The actual asset:** Functionality that solves user problems
**The liability:** Code required to deliver that functionality

### The Most Productive Pull Request

**The best PRs have:**
```
+50 lines added
-500 lines deleted
```

**Why developers applaud deletions:**
- Preserved functionality with less code
- Reduced maintenance burden
- Lowered cognitive complexity
- Decreased bug surface area
- **Negative code is worth 10x positive code**

---

## Slide 2: The Psychology of Subtraction

### The Human Bias Toward Addition

**Research finding:** Humans are neurologically wired to solve problems by **adding**, not **subtracting**.

**Common pattern:**
- Problem arises → Add a feature
- Bug appears → Add validation logic
- Performance slow → Add caching layer
- Users confused → Add documentation

**Rarely considered:**
- Problem arises → Remove complexity causing it
- Bug appears → Delete fragile code path
- Performance slow → Remove unnecessary work
- Users confused → Delete confusing features

### Subtraction as Innovation

**Famous examples of winning by removing:**

**Apple (1997):** Steve Jobs returned and **deleted 70% of products**
- Before: Dozens of confusing SKUs
- After: 4 products (laptop/desktop × consumer/pro)
- Result: Saved the company

**iPod Touch:** iPhone **minus** cellular = New market segment

**Southwest Airlines:** Full-service airline **minus** meals, assigned seating, hub-and-spoke
- Result: Cheapest, most profitable airline

**Tesla:** Traditional car **minus** hundreds of mechanical parts
- Simplified, software-driven, fewer failure points

### Why Subtraction is Hard

**The paradox:** Removing features feels like **negative** progress.

**What prevents deletion:**
- "Someone might be using this"
- "We spent time building it"
- Sunk cost fallacy
- Fear of being wrong
- Addition feels productive, subtraction feels destructive

**The courage required:** Saying "no" is harder than saying "yes."

---

## Slide 3: Practical Deletion Strategies

### 1. Delete Ruthlessly (Use Version Control)

**The rule:** If you don't expect to reuse code in the near future, **delete it**.

**Why it's safe:**
- Git preserves history (you can always recover)
- Commented-out code rots and misleads
- "Just in case" code never gets used

**The practice:**
```bash
# Don't do this:
// function oldWay() {
//   ... 50 lines of commented code ...
// }

# Do this:
git rm old_way.js
# It's in history if you need it
```

### 2. Verify Before Deleting

**The strategy:** Log first, delete second.

```javascript
function suspiciousLegacyCode() {
  logger.warn("DEPRECATION: suspiciousLegacyCode called");
  // ... old logic
}
```

**After 1 month of zero logs:**
→ Safe to delete

### 3. Progressive Feature Removal

**The gentle approach:**

```
Step 1: Mark deprecated (warnings in logs)
Step 2: Make it do nothing (no-op)
Step 3: Remove from UI (code still exists)
Step 4: Delete the code (after grace period)
```

**Real-world result:** One team reduced codebase by **67%** using this method.

### 4. The Red Flag Test

**Code that should be deleted:**

| Red Flag | Why It's a Liability |
|----------|---------------------|
| **"No one knows what this does"** | Cognitive load, fear of change |
| **Commented-out code** | Rots, misleads new developers |
| **Unused imports/dependencies** | Security risk, bloat |
| **"Feature used by 0.1% of users"** | Maintenance cost > value |
| **Duplicated logic** | Multiple places to fix bugs |
| **"We'll need this someday"** | YAGNI violation |

### 5. Celebrate Deletions

**Cultural shift needed:**

**Bad culture:**
- "I wrote 5,000 lines this week!" (applause)
- "I deleted 500 lines" (silence)

**Good culture:**
- "I wrote 5,000 lines" (neutral)
- "I deleted 500 lines while preserving functionality" (🎉 celebration)

**Measure different:**
- Not: Lines of code written
- Instead: Value delivered per line of code

### The Ultimate Deletion Wisdom

> "Perfection is achieved, not when there is nothing more to add, but when there is nothing left to take away."
>
> — Antoine de Saint-Exupéry

**Applied to engineering:**

**Addition mindset:**
- What feature can we build?
- What code can we write?
- What complexity can we add?

**Subtraction mindset:**
- What feature can we remove?
- What code can we delete?
- What complexity can we eliminate?

### The ROI of Deletion

**Benefits of aggressive code removal:**

1. **Faster builds** (less to compile)
2. **Faster tests** (less to test)
3. **Faster onboarding** (less to learn)
4. **Fewer bugs** (less surface area)
5. **Easier refactoring** (less to change)
6. **Lower hosting costs** (smaller bundles)
7. **Happier developers** (less cognitive load)

**The compound effect:** Every deleted line pays dividends forever.

### Final Principle

**Any fool can add complexity. It takes genius to subtract it.**

The best developers are **master deleters**.
