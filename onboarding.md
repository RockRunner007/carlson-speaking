# Team Onboarding

How to get new contributors productive quickly.

## Pre-Arrival (1 week before)

### Prepare for New Person

- [ ] Create GitHub account & add to team
- [ ] Set up Slack account
- [ ] Add to calendar invites (standups, planning)
- [ ] Assign onboarding buddy
- [ ] Create welcome document

### Welcome Package

Email template:

```text
Subject: Welcome to the Team! 🎉

Hi [Name],

Welcome to our team! We're excited to have you here.

Here's what to expect during your first week:

DAY 1:
- Meet the team (10:00 AM call)
- Get familiar with the repository structure
- Tour of the guidance collection
- Q&A with your buddy

DAYS 2-5:
- Specification-driven content training
- Guidance review participation
- Small documentation improvement task
- Team meetings and rituals

RESOURCES:
- [Getting Started Guide](../docs/runbooks/first-time-setup.md)
- [Spec-Driven Development](../specs/readme.md)
- [Contributing Guidelines](../CONTRIBUTING.md)
- [Slack Channel](https://slack.com/...)

Your buddy: @bob - he'll be your go-to person for questions

Looking forward to working with you!
```

## First Day

### 9:00 AM - Welcome

- [ ] Welcome & brief company/team overview
- [ ] Tech setup (laptop, GitHub access, Slack)
- [ ] Show office/workspace
- [ ] Introduce team members

### 10:00 AM - Contributor Onboarding Starts

**Step 1: Clone repository**

```bash
git clone https://github.com/stevencarlson/carlson-speaking.git
cd carlson-speaking
```

**Step 2: Review Content Standards**
- Read `docs/governance/code-review-standards.md`
- Review the `specs/` directory and `docs/personas/`.

### 11:00 AM - Guidance Tour

Walk through:
- Project structure (`docs/`, `specs/`, `prompts/`)
- How to propose new speaking guidance topics.

### 12:00 PM - Lunch

Go to lunch with team, buddy, or solo depending on preference.

### 1:00 PM - Contribution Workflow

Teach:

- [ ] Git workflow (main → feature branch → PR)
- [ ] How to make a commit
- [ ] How to create and push a PR
- [ ] Guidance review process

**Hands-on:** First commit

- [ ] Create `docs/team/[name].md` file
- [ ] Write self-introduction (3 sentences)
- [ ] Create PR, get review, merge

### 2:00 PM - Specification-Driven Content

Intro to SDD methodology:

- [ ] How specs are structured
- [ ] How to read a spec
- [ ] Connection between a spec and the final guidance document

Example: Walk through `specs/001-example/`

### 3:00 PM - Team Processes

Explain:

- [ ] Daily standup (who, when, what)
- [ ] Content planning
- [ ] Guidance review culture
- [ ] Paired writing (optional)
- [ ] How to ask for help

### 4:00 PM - First Assignment

Pick one small task:

**Option 1: Improve Existing Guidance**

- [ ] Find a page with a typo or unclear sentence and fix it.
- [ ] Add an example to an existing piece of guidance.

**Option 2: Draft New Content**

- [ ] Read an existing spec in `specs/`.
- [ ] Draft a small section of the guidance based on the spec.
- [ ] Submit a PR for feedback.

### 5:00 PM - Wrap-Up

- [ ] What did they accomplish?
- [ ] What questions do they have?
- [ ] What's tomorrow's focus?
- [ ] Buddy available on Slack anytime

## Week 1 Goals

### Monday

- [ ] GitHub repository cloned and accessible
- [ ] First PR merged (any kind)
- [ ] Met entire team

### Tuesday-Wednesday

- [ ] Understanding the specification-driven content approach
- [ ] Made 2-3 small contributions (commits)
- [ ] Participated in a guidance review
- [ ] Attended team standup

### Thursday

- [ ] Started on a small guidance draft or improvement
- [ ] Asking questions (good sign!)
- [ ] Comfortable with git workflow

### Friday

- [ ] First content PR ready for review
- [ ] Attended content planning
- [ ] Paired with someone on writing/editing
- [ ] First week retrospective

## Week 1-2 Checklist

### Technical

- [ ] Comfortable with local markdown editor
- [ ] First PR merged
- [ ] Understanding repository structure
- [ ] Knows where to find documentation

### Process

- [ ] Understands git workflow
- [ ] Knows guidance review process
- [ ] Attended standup
- [ ] Knows who to ask for help
- [ ] Knows team meeting schedule

### Team

- [ ] Met all team members
- [ ] Has assigned buddy
- [ ] Knows Slack channels
- [ ] Knows email contacts
- [ ] Attended team social event

### Knowledge

- [ ] Read README and Contributing guide
- [ ] Understands specification-driven content approach
- [ ] Knows current project focus
- [ ] Familiar with the personas in `docs/personas/`
- [ ] Knows content governance standards

## Month 1 Goals

### Productivity

- [ ] Published at least 1 new piece of guidance or made 5+ significant improvements
- [ ] Guidance review quality is high (providing actionable feedback)
- [ ] Can create a new guidance document from a spec
- [ ] Can identify and fix issues in existing content independently

### Knowledge

- [ ] Understands the full scope of the guidance collection
- [ ] Can explain the purpose and use of each persona
- [ ] Knows the process for proposing and publishing new content

### Integration

- [ ] Active in team meetings
- [ ] Asked thoughtful questions
- [ ] Participated in content strategy discussions
- [ ] Comfortable asking for help
- [ ] Paired with team members on writing/editing

## Month 3 Goals

### Independence

- [ ] Can estimate effort for new content accurately
- [ ] Writes clear commits and PRs for content changes
- [ ] Reviews guidance effectively and mentors others on reviews
- [ ] Mentors others
- [ ] Identifies improvements

### Expertise

- [ ] Deep knowledge of one area
- [ ] Can explain content and persona strategy decisions
- [ ] Suggests optimizations
- [ ] Leads review for new specs
- [ ] Owns a section of the guidance collection

## Onboarding Activities

### Paired Writing Sessions

**Week 1:** Observe and ask questions

```text
Pair with: @bob
Duration: 2 hours
Task: Draft a small piece of guidance together
Buddy writes, new person contributes ideas and edits
```

**Week 2:** Co-implement feature

```text
Pair with: @alice
Duration: 2 hours
Task: Work on medium feature
Take turns driving
```

**Month 1:** Mentor mode

```text
Pair with: New person from team
Duration: 2 hours
Task: Help them learn
New person drives, mentor helps
```

### Meetings to Attend

**Daily (optional):**

- [ ] Standup (15 min, 10 AM)

**Weekly:**

- [ ] Team sync (1 hour, Monday)
- [ ] Design review (1 hour, Wednesday)
- [ ] Release planning (1 hour, Friday)

**Monthly:**

- [ ] Retrospective (1 hour)
- [ ] Engineering all-hands (1 hour)
- [ ] 1-on-1 with manager

### Learning Resources

Provide links to:

- [ ] Company wiki/handbook
- [ ] Architecture documentation
- [ ] API documentation
- [ ] Infrastructure guides
- [ ] Security policies
- [ ] Helpful Slack channels

## Onboarding Buddy Role

### Buddy Responsibilities

**Before arrival:**

- [ ] Prepare welcome
- [ ] Send setup guide
- [ ] Make sure GitHub access ready

**First day:**

- [ ] Be available for questions
- [ ] Help with environment setup
- [ ] Introduce to team
- [ ] Explain workflows
- [ ] Eat lunch together

**First week:**

- [ ] Check in daily (quick chat)
- [ ] Validate they can run tests
- [ ] Review first PR
- [ ] Pair program if possible
- [ ] Connect to other team members

**Month 1:**

- [ ] Weekly check-in
- [ ] Provide feedback on progress
- [ ] Share tips and tricks
- [ ] Introduce to specialists

**Ongoing:**

- [ ] Answer questions
- [ ] Provide support
- [ ] Share knowledge
- [ ] Be the friendly face

### Buddy Training

Before becoming a buddy, train on:

- [ ] How to explain the codebase
- [ ] Teaching vs doing
- [ ] Patience and empathy
- [ ] How to answer questions
- [ ] When to escalate

## Measuring Success

### First Week

- New person can run app and tests ✅
- Completed first PR ✅
- Comfortable asking questions ✅
- Attended meetings ✅

### Month 1

- Shipped feature or multiple bugs ✅
- Understands codebase ✅
- Active participant ✅
- Knows who to ask ✅

### Month 3

- Productive on own ✅
- Quality contributions ✅
- Integrated with team ✅
- Considering improvements ✅

### Month 6

- Expert in one area ✅
- Can mentor others ✅
- Driving improvements ✅
- Leadership potential ✅

## Feedback Loop

### End of Week 1

- Informal feedback from buddy
- New person's impressions
- Any blocking issues?

### End of Month 1

- Formal 1-on-1 check-in
- How is ramp-up going?
- What helped? What didn't?
- Adjust as needed

### End of Month 3

- Review progress against goals
- Identify strengths
- Recommend next steps

## Template

Create file: `docs/team/[name].md`

```markdown
# [Full Name]

**Role:** [Job Title]  
**Started:** [Date]  
**Timezone:** [Timezone]  
**Buddy:** [Name]  

## Background

[2-3 sentences about background and experience]

## Interests

[2-3 areas of interest or expertise]

## Areas Learning

[What they're currently learning]

## Fun Fact

[Something fun/interesting about them]

## Contact

- Email: [email]
- Slack: @[username]
- GitHub: [github_username]
```

## References

- [First-Time Setup](first-time-setup.md)
- [Contributing Guidelines](../../CONTRIBUTING.md)
- [Spec-Driven Development](../../specs/readme.md)
- [Code Review Standards](code-review-standards.md)
