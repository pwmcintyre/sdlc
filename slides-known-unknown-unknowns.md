---
paging: Slide %d / %d
---

# Known Unknowns vs Unknown Unknowns

---

## Slide 1: The Rumsfeld Matrix for Software

> "There are known knowns... there are known unknowns... But there are also unknown unknowns—the ones we don't know we don't know."
>
> — Donald Rumsfeld, 2002

### The Four Quadrants

| | **Know We Don't Know** | **Don't Know We Don't Know** |
|----------------|------------------------|------------------------------|
| **Know It** | **Known Knowns** <br/>Postgres, HTTP, SQL | **Unknown Knowns** <br/>Tribal knowledge, tacit expertise |
| **Don't Know It** | **Known Unknowns** <br/>New feature, unclear requirements | **Unknown Unknowns** <br/>Black swans, production surprises |

### Why This Matters in Software

**Known unknowns** can be planned for: buffer time, research spikes, prototypes.

**Unknown unknowns** surface at 3am: database connection pool exhaustion, unicode edge cases, timezone bugs in production.

**The goal:** Convert unknown unknowns → known unknowns → known knowns.

---

## Slide 2: Boring Tech = Known Failure Modes

### The Critical Difference

**Boring Technology:**
```
Postgres at 100% CPU → Known problem
   ↓
Stack Overflow has 1,000+ answers
   ↓
Your team has seen it before
   ↓
Fix is well-documented
```

**Shiny Technology:**
```
New NoSQL DB acting weird → Unknown problem
   ↓
GitHub issues with "investigating..."
   ↓
No one on team has expertise
   ↓
Unknown unknowns compound
```

### The Unknowns Budget

**Boring tech:** Small magnitude of unknown unknowns
- Capabilities are well understood
- **Failure modes are well understood** ← This is the key
- Community knowledge is vast

**Shiny tech:** Large magnitude of unknown unknowns
- Capabilities still being discovered
- Failure modes emerge in production
- You're the community knowledge

### Risk Compounding

**1 unknown technology:** Manageable unknown unknowns
**2 unknown technologies:** Unknowns multiply
**3 unknown technologies:** Unknowns compound exponentially

**Example:**
- New language + new database + new deployment = Unknown³
- Each unknown masks problems in the others

---

## Slide 3: Converting Unknowns to Knowns

### Strategies for Software Projects

**1. Research Spikes & Tracer Bullets**
```
Unknown unknown: "Will this architecture scale?"
   ↓ [Build minimal prototype]
Known unknown: "Redis connection pooling needs work"
   ↓ [Research + implement]
Known known: "Connection pool sized to 50"
```

**2. Look in the Right Places**

Most "unknown unknowns" are actually **knowable unknowns** if you:
- Read post-mortems from similar systems
- Talk to teams who tried the tech
- Check the GitHub issues labeled "bug"
- Search for "[technology] in production"

**3. The Boring Technology Advantage**

Boring tech has already surfaced its unknown unknowns:
- Decades of production use
- Battle scars documented
- Known workarounds
- Predictable scaling behavior

**You inherit knowledge, not just software.**

### Project Planning Reality

**Traditional estimation:** Known work only
**Reality:** Unknown unknowns dominate timeline

**The boring tech shortcut:**
- Fewer unknown unknowns to discover
- Faster path to known knowns
- More accurate estimates

### The Meta-Lesson

**You can't eliminate unknown unknowns.**

**But you can choose technology where others have already found them for you.**

**That's the real value of boring technology.**
