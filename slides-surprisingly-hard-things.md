---
paging: Slide %d / %d
---

# Surprisingly Hard Things in Software Engineering

---

## Slide 1: The Infamous Quote

> "There are only two hard things in Computer Science: cache invalidation and naming things... and off-by-one errors"
>
> — Phil Karlton (Netscape, 1995-97)

### Why This Resonates

These aren't algorithm complexity problems or Big-O notation challenges. They're **deceptively simple** concepts that become **surprisingly complex** at scale.

**The Pattern:** Simple to understand, impossible to perfect.

---

## Slide 2: Four Hard Things Unpacked

### 1. **Time** ⏰
- Timezones, leap seconds, DST, monotonic vs wall-clock
- Distributed clocks: NTP drift, clock skew
- "What time is it?" has no universal answer

### 2. **Names** 📝
- Cache invalidation (stale data vs performance)
- Variable/function naming (clarity vs brevity)
- DNS, URLs, identifiers (uniqueness vs readability)

### 3. **Exactly Once** 🎯
- **Impossible** in distributed systems (FLP, Two Generals)
- At-most-once: fast but lossy
- At-least-once: reliable but duplicates
- "Exactly-once" = at-least-once + idempotency

### 4. **Auth** 🔐
- Eternal cat-and-mouse game
- Password → MFA → biometrics → AI detection
- Each defense spawns new attacks (phishing, social engineering)

---

## Slide 3: The Deeper Pattern

### Why These Stay Hard

**Fundamental impossibilities:**
- Distributed consensus (time, exactly-once)
- Human creativity vs machine logic (names)
- Adversarial dynamics (auth)

### The Engineering Response

1. **Accept imperfection** — Design for failure modes
2. **Trade-offs over solutions** — No silver bullets exist
3. **Boring tech understands this** — Proven failure modes beat unknown unknowns

**Takeaway:** These problems don't get solved. They get **managed**.
