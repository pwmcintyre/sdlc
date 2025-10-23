---
author: Peter McIntyre
date: October 23, 2025
paging: Slide %d / %d
---

# Software Engineering

Peter McIntyre

Principal Software Engineer

---

## What We'll Cover

- My story
- What is software delivery
- Patterns that emerge
- Tools of the trade
- The impact of AI
- Questions

---

## My Story

- Started with excitement for cutting-edge tech
- Learned through complexity and 3am incidents
- Now find joy in simplicity and deletion
- Watched technology shift from impossible to trivial

---

## What is Software Delivery?

Plan → Build → Test → Release → Monitor

It's a continuous loop, not linear.

---

## SDLC, Agile, DevOps

- **SDLC:** The framework (the "what")
- **Agile:** Working iteratively (the "how")
- **DevOps:** Automation & continuous delivery (the "shipping")

---

## The Reality

- Monitoring feeds back into planning
- Production issues interrupt everything
- Requirements change mid-sprint
- You're coding, testing, and fixing simultaneously

---

## Patterns: Choose Boring Technology

> "Let's say every company gets about three innovation tokens."
> — Dan McKinley

Spend them on your competitive advantage, not databases.

---

## Known vs Unknown Unknowns

**Boring tech:**
- Known failure modes
- Documented workarounds
- Vast community knowledge

**Shiny tech:**
- Unknown unknowns emerge at 3am
- You are the community

---

## Surprisingly Hard Things

- Time (timezones, leap seconds, distributed clocks)
- Names (cache invalidation, naming variables)
- Exactly once (impossible in distributed systems)
- Auth (eternal cat-and-mouse game)

These don't get solved. They get managed.

---

## The Joy Evolution

**Early career:** "We're using Rust + GraphQL!"
- Joy from learning new tech
- Building résumé

**Later career:** "We shipped it in two days with Rails."
- Joy from shipping features
- Going home on time

---

## The Simplicity Paradox

> "I have made this letter longer than usual, only because I have not had the time to make it shorter."
> — Blaise Pascal

Adding complexity is easy.

Achieving simplicity is hard.

---

## Code is a Liability

**Traditional thinking (WRONG):**
- More code = More productivity

**Reality:**
- Code = Maintenance burden
- Best code = Code you didn't write

The most productive PRs delete 10x more than they add.

---

## Deletion as a Feature

> "Perfection is achieved, not when there is nothing more to add, but when there is nothing left to take away."
> — Antoine de Saint-Exupéry

Examples:
- Apple 1997: Deleted 70% of products, saved the company
- iPhone: Traditional phone minus physical keyboard
- Tesla: Traditional car minus hundreds of mechanical parts

---

## Desire Meets Possibility

**The Pattern:**
1. Desire exists (users want it)
2. Technology can't deliver (infeasible)
3. Workarounds accumulate (complexity builds)
4. Technology breakthrough (constraint removed)
5. **DELETE all the workarounds**

---

## Example: Natural Language Interfaces

**Desired since 1950s:** Talk to computers naturally

**Impossible until 2017:** Rule-based NLP was fragile

**Workarounds:** GUIs, menus, training manuals, syntax

**Breakthrough:** Transformers, GPT, ChatGPT (2022)

**Result:** Delete 90% of traditional UI complexity

---

## Tools of the Trade

**Essential:**
- Git (non-negotiable)
- Terminal/CLI
- IDE (VS Code, IntelliJ)
- Docker/containers

Everything else is convenience.

---

## The CI/CD Pipeline

Push code → Lint → Test → Build → Deploy

Continuous Integration / Continuous Deployment

Automate everything that can be automated.

---

## Cloud Infrastructure

**Compute:** EC2, containers, Lambda (serverless)

**Storage:** S3, databases (RDS, DynamoDB)

**Monitoring:** Logs, metrics, alerts

**Infrastructure as Code:** Terraform, CloudFormation

---

## Working in Teams

- Daily standups (what did you do? blockers?)
- Sprint planning (2-week cycles)
- Code reviews (catch bugs, share knowledge)
- Retrospectives (what can improve?)

Software engineering is a team sport.

---

## Real Challenges

**Production incidents:**
- Not "if", but "when"
- On-call rotation
- Blameless postmortems

**Legacy code:**
- You'll read more than you write
- Technical debt accumulates
- Balance features vs. paying down debt

---

## Making Tradeoffs

Perfect solution:
- 100% test coverage
- Takes 6 months

Good enough:
- 80% test coverage
- Ships in 6 weeks

Shipping imperfect software beats perfect software that never ships.

---

## Career Progression

- **Junior (0-2 years):** Learn basics, fix bugs
- **Mid (2-5 years):** Own features, mentor juniors
- **Senior (5-10 years):** Design systems, architectural decisions
- **Principal (10+ years):** Set technical direction, org-wide impact

Focus on impact, not titles.

---

## Your First Job

- You won't know everything (nobody does)
- Imposter syndrome is normal
- Ask questions - it's expected
- Find a mentor
- Own your mistakes and learn

---

## Continuous Learning

Technology changes constantly.

**Ways to keep learning:**
- Read other people's code
- Build side projects
- Contribute to open source
- Learn from production incidents
- Focus on fundamentals (algorithms, data structures, design patterns)

---

## Red Flags in Companies

- No code reviews or testing
- Constant firefighting
- Blame culture
- No documentation
- Unlimited overtime expectations

---

## Green Flags in Companies

- Strong engineering culture
- Automated CI/CD
- Blameless postmortems
- Time for tech debt and learning
- Good documentation
- Work-life balance

---

## Skills Beyond Code

- **Communication:** Explaining technical concepts clearly
- **Empathy:** Understanding users and team dynamics
- **Time management:** Balancing priorities
- **Problem-solving:** Breaking down complexity
- **Adaptability:** Technologies and priorities change

These become more important as you advance.

---

## The Impact of AI

**What's changing:**
- Natural language interfaces replacing complex UIs
- AI-assisted coding (GitHub Copilot, Claude Code)
- Less code = Less maintenance

**What's not changing:**
- Need to understand fundamentals
- System design and architecture
- Human judgment and tradeoffs

---

## AI: Deletion Opportunity

Before LLMs:
- Hierarchical menus
- Training manuals
- Complex wizards
- Keyboard shortcuts to memorize

After LLMs:
- Text box: "What do you want?"
- Natural conversation
- Zero training needed

---

## Key Takeaways

- Master the basics: Git, CLI, containers
- Choose boring technology, spend innovation tokens wisely
- Code is a liability - celebrate deletions
- Simplicity is hard work, complexity is easy
- Watch when technology shifts impossibility boundaries
- Communication > solo coding
- Keep learning, stay curious
- Find good engineering culture

---

## Questions?

Ask me anything about software delivery, career paths, or working in the industry.

