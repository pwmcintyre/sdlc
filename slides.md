---
theme: "black"
transition: "slide"
highlightTheme: "monokai"
slideNumber: true
title: "Software Delivery in the Real World"
---

# Software Delivery in the Real World

What it actually means to ship software at scale

<br>

Principal Software Engineer | Melbourne
20 years building enterprise systems

---

## What We'll Cover Today

- The Software Development Lifecycle (SDLC) {.fragment}
- The technical stack & tools we use {.fragment}
- Agile & ways of working {.fragment}
- Real challenges you'll face {.fragment}
- What to expect in your career {.fragment}

Note: Set expectations: this is the real-world view, not the textbook version. I want you to walk away knowing what day-to-day software delivery actually looks like.

---

## The Software Development Lifecycle

Or: How software actually gets built

--

### The Textbook Version

<div style="display: flex; justify-content: center; align-items: center; gap: 1rem; font-size: 1.5em;">
<span class="fragment">Plan</span>
<span class="fragment">→</span>
<span class="fragment">Code</span>
<span class="fragment">→</span>
<span class="fragment">Build</span>
<span class="fragment">→</span>
<span class="fragment">Test</span>
<span class="fragment">→</span>
<span class="fragment">Deploy</span>
<span class="fragment">→</span>
<span class="fragment">Monitor</span>
</div>

Note: This is what you'll see in most introductory materials. It's not wrong, but it's overly simplified.

--

### The Reality

- It's a **continuous loop**, not linear {.fragment}
- Monitoring feeds back into planning {.fragment}
- You're often coding, testing, and fixing simultaneously {.fragment}
- Production issues interrupt everything {.fragment}
- Requirements change mid-sprint {.fragment}

Note: The SDLC is more like a circle with lots of smaller circles inside it. You'll rarely complete one phase before starting another.

--

### A Day in the Life

- **9:00am:** Daily standup - what did I do yesterday? what will I do today? {.fragment}
- **9:15am:** Start coding the new feature from sprint backlog {.fragment}
- **10:30am:** Production alert - investigate and hotfix {.fragment}
- **11:30am:** Code review for teammate's PR {.fragment}
- **1:00pm:** Back to feature work {.fragment}
- **2:00pm:** Sprint planning meeting {.fragment}
- **3:30pm:** Debug failing CI pipeline {.fragment}
- **4:30pm:** Finish feature, open PR, write tests {.fragment}

Note: This is why time management and context switching are critical skills. You're juggling multiple phases of SDLC throughout the day.

---

## The Technical Stack

Tools you'll use every single day

--

### Development Environment

- **IDE:** VS Code, IntelliJ, etc. {.fragment}
- **Version Control:** Git (GitHub, GitLab, Bitbucket) {.fragment}
- **Local Environment:** Docker, Docker Compose {.fragment}
- **Package Managers:** npm, pip, maven, gradle {.fragment}

Git is non-negotiable. Learn it well. {.fragment}

Note: You'll spend 80% of your time in your IDE and terminal. Docker lets you run complex systems locally without installing everything natively.

--

### The CI/CD Pipeline

Continuous Integration / Continuous Deployment

- **CI Tools:** Jenkins, GitHub Actions, GitLab CI, CircleCI {.fragment}
- **What happens:** {.fragment}
  1. You push code to a branch
  2. Pipeline runs: lint, unit tests, integration tests
  3. Build Docker image
  4. Push to container registry
  5. Deploy to dev/staging environment
  6. Automated tests run in staging
  7. Manual approval for production
  8. Deploy to production

Note: This automation is what allows us to deploy multiple times per day safely. Without it, every deployment would be manual and error-prone.

--

### Cloud Infrastructure (AWS)

<div style="display: flex; gap: 2rem;">
<div style="flex: 1;">

**Compute**
- EC2 (virtual servers)
- ECS (containers)
- Lambda (serverless)

**Storage**
- S3 (object storage)
- RDS (databases)
- DynamoDB (NoSQL)

</div>
<div style="flex: 1;">

**Networking**
- VPC (private networks)
- Load Balancers
- CloudFront (CDN)

**Infrastructure as Code**
- Terraform
- CloudFormation

</div>
</div>

Note: At enterprise scale, you're not managing servers manually. Everything is code, everything is automated.

--

### Monitoring & Observability

- **Application Monitoring:** DataDog, New Relic, Dynatrace {.fragment}
- **Error Tracking:** Sentry, Rollbar {.fragment}
- **Logs:** CloudWatch, Elasticsearch/Kibana, Splunk {.fragment}
- **Metrics:** Prometheus, Grafana {.fragment}
- **Alerting:** PagerDuty, OpsGenie {.fragment}

If you can't measure it, you can't improve it. {.fragment}

Note: You'll spend a lot of time looking at dashboards and logs. When something breaks at 3am, these tools are how you figure out what went wrong.

--

### Example: Deploying a Feature

```bash
# 1. Create feature branch
git checkout -b feature/user-notifications

# 2. Write code, commit frequently
git add .
git commit -m "Add notification service"

# 3. Push and open Pull Request
git push origin feature/user-notifications

# 4. CI runs automatically:
#    - Linting (ESLint, Prettier)
#    - Unit tests (Jest, pytest)
#    - Security scans (Snyk)
#    - Build Docker image
#    - Deploy to dev environment

# 5. Code review from team
# 6. Merge to main
# 7. Auto-deploy to staging
# 8. QA testing
# 9. Deploy to production
```

Note: This whole process might take a few hours to a few days. The key is automation - most of this happens without manual intervention.

---

## Agile in Practice

How teams actually work together

--

### The Sprint Cycle (2 weeks)

- **Sprint Planning:** Team picks work from backlog for next 2 weeks {.fragment}
- **Daily Standup:** 15min sync - what did you do? what will you do? any blockers? {.fragment}
- **Sprint Work:** Code, review, deploy, repeat {.fragment}
- **Sprint Review:** Demo completed work to stakeholders {.fragment}
- **Retrospective:** What went well? What can improve? {.fragment}

Then repeat. Forever. {.fragment}

Note: Agile is about iteration and continuous improvement. It's not about being perfect, it's about getting better every sprint.

--

### Tickets & Story Points

- **Tools:** Jira, Linear, Azure DevOps {.fragment}
- **Story Points:** Relative effort (1, 2, 3, 5, 8, 13) {.fragment}
- **Ticket States:** Backlog → In Progress → Code Review → QA → Done {.fragment}
- Your velocity improves as you learn the system {.fragment}

Note: Story points are not hours. They're relative complexity. A 5-point story is roughly 5x more complex than a 1-point story.

--

### Code Reviews

One of the most important practices

- **Why:** Catch bugs, share knowledge, maintain quality {.fragment}
- **What reviewers look for:** {.fragment}
  - Does it solve the problem?
  - Are there bugs or edge cases?
  - Is it readable and maintainable?
  - Does it follow team conventions?
  - Are tests included?
- **Pro tip:** Small PRs get reviewed faster {.fragment}

Note: Code reviews are where you'll learn the most as a junior dev. Both from receiving feedback and from reviewing others' code. Don't take feedback personally - everyone's code gets reviewed.

--

### Collaboration is Key

- You'll spend more time communicating than coding {.fragment}
- Slack/Teams for async communication {.fragment}
- Video calls for complex discussions {.fragment}
- Documentation for knowledge sharing {.fragment}
- Pair programming for complex problems {.fragment}

Software engineering is a team sport. {.fragment}

Note: The lone genius programmer is a myth. Real work happens through collaboration and clear communication.

---

## Real Challenges

The stuff they don't tell you in tutorials

--

### Production Incidents

- **It's not "if", it's "when"** {.fragment}
- **On-call rotation:** You're responsible for production health {.fragment}
- **Incident response:** {.fragment}
  1. Alert fires (PagerDuty wakes you up)
  2. Assess impact and severity
  3. Mitigate/rollback if needed
  4. Investigate root cause
  5. Write postmortem
  6. Implement fixes to prevent recurrence
- **Blameless culture:** Focus on systems, not individuals {.fragment}

Note: Everyone breaks production eventually. It's how you respond that matters. Good companies have blameless postmortems to learn from incidents.

--

### Legacy Code & Technical Debt

- You'll spend more time reading code than writing it {.fragment}
- Most codebases are 5-10+ years old {.fragment}
- Technical debt accumulates from: {.fragment}
  - Rushed deadlines
  - Changing requirements
  - Technologies becoming outdated
  - People leaving and taking context with them
- Balance: new features vs. paying down debt {.fragment}

Note: The code you write today is tomorrow's legacy code. Write it with future-you in mind.

--

### Scaling Challenges

- **Performance:** What works for 100 users doesn't work for 1M {.fragment}
- **Database bottlenecks:** Query optimization, caching, sharding {.fragment}
- **Distributed systems:** Multiple services, eventual consistency {.fragment}
- **Load balancing:** Spreading traffic across servers {.fragment}
- **Cost optimization:** AWS bills can get expensive fast {.fragment}

Premature optimization is evil, but so is ignoring scale. {.fragment}

Note: At enterprise scale, you can't just throw more servers at the problem. You need to think about architecture, data patterns, caching strategies.

--

### Making Tradeoffs

<div style="display: flex; gap: 2rem;">
<div style="flex: 1;">

**Perfect Solution**
- 100% test coverage
- Fully documented
- Zero technical debt
- Handles all edge cases
- Takes 6 months

</div>
<div style="flex: 1;">

**Good Enough**
- 80% test coverage
- Key parts documented
- Some technical debt
- Handles common cases
- Ships in 6 weeks

</div>
</div>

Shipping imperfect software beats perfect software that never ships. {.fragment}

Note: You'll constantly balance quality vs. speed. The key is knowing which tradeoffs are acceptable and which aren't. Security? Non-negotiable. Refactoring that function? Can wait.

--

### Working with Ambiguity

- Requirements are rarely crystal clear {.fragment}
- Ask questions early and often {.fragment}
- Build MVPs to validate assumptions {.fragment}
- User feedback will change everything anyway {.fragment}

Note: Get comfortable with uncertainty. Your job is to clarify requirements, not just implement them blindly.

---

## What to Expect in Your Career

The journey from junior to principal

--

### Junior → Mid → Senior → Principal

- **Junior (0-2 years):** Learn the basics, fix bugs, build features with guidance {.fragment}
- **Mid (2-5 years):** Own features end-to-end, mentor juniors, less supervision {.fragment}
- **Senior (5-10 years):** Design systems, lead projects, make architectural decisions {.fragment}
- **Principal (10+ years):** Set technical direction, solve org-wide problems, influence strategy {.fragment}

These are rough guidelines. Focus on impact, not titles. {.fragment}

Note: Progression isn't automatic. You grow by taking on more responsibility. Each level requires different skills - coding skills plateau, but leadership skills grow.

--

### Your First Job

- You won't know everything (nobody does) {.fragment}
- Imposter syndrome is normal {.fragment}
- Ask questions - it's expected {.fragment}
- Focus on learning, not looking smart {.fragment}
- Find a mentor or senior to learn from {.fragment}
- You'll make mistakes - own them and learn {.fragment}

Note: The difference between junior and senior isn't knowledge. It's knowing what you don't know and how to find answers.

--

### Continuous Learning

- Technology changes constantly {.fragment}
- What you learn in university is just the foundation {.fragment}
- Ways to keep learning: {.fragment}
  - Read other people's code
  - Contribute to open source
  - Build side projects
  - Read documentation (seriously)
  - Follow industry blogs and conferences
  - Learn from production incidents
- Focus on fundamentals that don't change: algorithms, data structures, design patterns {.fragment}

Note: The specific tools will change, but the underlying principles stay the same. Learn how to learn, not just what to learn.

--

### Red Flags in Companies

- No code reviews or testing {.fragment}
- Constant firefighting, no time for improvement {.fragment}
- Blame culture around mistakes {.fragment}
- No documentation or knowledge sharing {.fragment}
- Unlimited overtime expectations {.fragment}
- No investment in developer tools or training {.fragment}

Note: You'll learn bad habits at bad companies. Look for places that invest in quality and their people.

--

### Green Flags in Companies

- Strong engineering culture {.fragment}
- Automated CI/CD and testing {.fragment}
- Blameless postmortems {.fragment}
- Time allocated for tech debt and learning {.fragment}
- Good documentation and onboarding {.fragment}
- Healthy work-life balance {.fragment}
- Clear career progression paths {.fragment}

Note: Ask about these things in interviews. The company is interviewing you, but you're also interviewing them.

--

### Skills Beyond Code

- **Communication:** Explaining technical concepts clearly {.fragment}
- **Empathy:** Understanding user needs and team dynamics {.fragment}
- **Time management:** Balancing multiple priorities {.fragment}
- **Problem-solving:** Breaking down complex problems {.fragment}
- **Adaptability:** Technologies and priorities change {.fragment}

These "soft skills" become more important as you advance. {.fragment}

Note: At senior+ levels, your technical skills are assumed. What differentiates you is how you work with others and drive impact.

---

## Key Takeaways

- Software delivery is a cycle, not a waterfall {.fragment}
- Master the tools: Git, CI/CD, cloud platforms {.fragment}
- Agile is about people and iteration, not just process {.fragment}
- You'll spend more time on maintenance than greenfield {.fragment}
- Communication and collaboration > solo coding {.fragment}
- Keep learning, stay curious, ask questions {.fragment}
- Find a company with good engineering culture {.fragment}

---

# Questions?

Ask me anything about software delivery, career paths, or working in the industry
