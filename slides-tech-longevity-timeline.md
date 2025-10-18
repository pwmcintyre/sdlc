# Technology Longevity Timeline

---

## Slide 1: The Lindy Effect in Software

> "The longer a technology has survived, the longer it is likely to stay alive."
>
> — The Lindy Effect

### The Champions Still Standing (2025)

| Technology | Age | Status |
|------------|-----|--------|
| **C Language** | 52 years (1973) | Powers Linux, databases, embedded systems |
| **SQL** | 48 years (1977) | Every database speaks it |
| **Unix/Linux** | 54/34 years | Runs the internet |
| **Perl** | 38 years (1987) | Text processing immortal |
| **Python** | 34 years (1991) | AI/ML standard |
| **PostgreSQL** | 39 years (1986) | Better with age |
| **Git** | 20 years (2005) | Version control solved |

### The Pattern: Backend Lasts Decades

**Why these endure:**
- Solve fundamental problems (data, computation, storage)
- Problem space doesn't change
- Breaking changes are too expensive
- Community knowledge compounds over time

---

## Slide 2: The Frontend Graveyard

### The 3-7 Year Frontend Lifecycle

**Dead or Dying:**
```
Flash (1996-2020)     → 24 years, killed by iPhone
Backbone (2010-2015)  → 5 years, peak to obsolete
AngularJS (2010-2022) → 12 years, killed by own successor
Ember (2011-2018)     → 7 years, faded away
jQuery (2006-~2020)   → 14 years, browsers caught up
```

**Currently Dominant (but for how long?):**
```
React (2013)    → 12 years, current king
Vue (2014)      → 11 years, rising
Svelte (2016)   → 9 years, new challenger
```

### The Device Disruption Timeline

**Each new device = frontend revolution:**

- **2007:** iPhone → Killed Flash, changed everything
- **2010:** iPad → Responsive design era begins
- **2011-2014:** Bootstrap, mobile-first philosophy
- **2013+:** JavaScript framework wars
- **2015+:** PWAs, app-like web experiences
- **2020+:** Framework consolidation (React wins... for now)

**Key insight:** Frontends don't age out because of tech debt. They age out because **devices change how humans interact with computers**.

---

## Slide 3: The Layer-Dependent Strategy

### Backend: Choose the Oldest (Boring Always Wins)

**Typical lifespan: 20-40+ years**

**Why backend tech lasts:**
- Data structures don't change (trees are still trees)
- Business logic is device-agnostic
- Performance matters more than aesthetics
- Users don't see it, so it doesn't "look outdated"
- Breaking changes are catastrophically expensive

**Strategy:** Pick technology invented 20+ years ago.

**Examples:**
- Database? Postgres (39 years) or MySQL (30 years)
- Language? Python (34 years) or Java (30 years)
- Infrastructure? Linux (34 years), Docker (12 years)

### Frontend: Accept the Churn (Devices Win)

**Typical lifespan: 3-7 years before major rewrite**

**Why frontend tech churns:**
- New devices (phones → tablets → watches → AR/VR)
- Screen sizes (320px → 4K displays)
- Input methods (mouse → touch → voice → gestures)
- Network speeds (3G → 4G → 5G → changed what's possible)
- User expectations evolve ("modern" UI feels dated in 3 years)

**Strategy:** Choose momentum, not longevity.

**Current safe bets (with asterisks):**
- React (largest community, Meta-backed)
- Vue (second-place, gentler learning curve)
- Progressive enhancement (HTML/CSS outlive frameworks)

**Plan for:** Full frontend rewrite every 5-7 years as normal lifecycle.

### The Revised "Choose Boring" Wisdom

**Backend (infrastructure):**
```
Age = Robustness → Choose the oldest
Innovation tokens = 0
```

**Frontend (UI):**
```
Age = Outdated → Choose momentum
Accept churn = Device evolution
Innovation tokens = 1 (on framework choice)
```

**The separation is critical:**
- Boring backend enables **business longevity**
- Churn-accepting frontend enables **user experience evolution**
- Don't let frontend trends dictate backend choices
- Don't expect frontend to last as long as backend

**Ultimate wisdom:** Your **data model** will outlive your **UI framework** by 20+ years. Design accordingly.
