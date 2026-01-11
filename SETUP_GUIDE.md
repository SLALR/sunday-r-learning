# Repository Setup Guide for Organizers

This guide walks you through setting up the Sunday R Learning Group repository from scratch.

## Prerequisites

- GitHub account with organization admin access
- Git installed locally
- Familiarity with basic Git/GitHub operations

---

## Step 1: Create the Repository

1. **Go to SLALR organization**: https://github.com/SLALR
2. **Click "New repository"**
3. **Configure:**
   - Name: `sunday-r-learning-2026`
   - Description: `Collaborative learning project for building R/Shiny portfolio pieces throughout 2026`
   - Visibility: Public (recommended) or Private
   - ✅ Initialize with README
   - ✅ Add .gitignore: R
   - ✅ Choose license: MIT

4. **Click "Create repository"**

---

## Step 2: Clone and Add Files

### Clone the repository

```bash
git clone https://github.com/SLALR/sunday-r-learning-2026.git
cd sunday-r-learning-2026
```

### Add all the files from this project

Copy all files from this structure into your cloned repository:

```
sunday-r-learning-2026/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── .gitignore
├── Q1-Shiny-Dashboard/
│   ├── README.md
│   └── .gitkeep
├── Q2-R-Package/
│   ├── README.md
│   └── .gitkeep
├── Q3-Data-Story/
│   ├── README.md
│   └── .gitkeep
├── Q4-Capstone/
│   ├── README.md
│   └── .gitkeep
├── templates/
│   ├── weekly-update.md
│   └── PROJECT_README_TEMPLATE.md
├── docs/
│   └── project-tracking-guide.md
└── .github/
    └── ISSUE_TEMPLATE/
        ├── bug_report.md
        ├── question.md
        └── idea.md
```

### Create .gitkeep files (to track empty directories)

```bash
touch Q1-Shiny-Dashboard/.gitkeep
touch Q2-R-Package/.gitkeep
touch Q3-Data-Story/.gitkeep
touch Q4-Capstone/.gitkeep
```

### Commit and push

```bash
git add .
git commit -m "Initial repository setup with all quarterly resources"
git push origin main
```

---

## Step 3: Configure Repository Settings

### Enable Discussions

1. Go to repo Settings → General
2. Scroll to "Features"
3. ✅ Check "Discussions"

### Configure Discussions Categories

Go to Discussions tab → Categories → Edit

**Recommended categories:**
- 💡 **Ideas** - Suggestions and proposals
- 🙏 **Help Wanted** - Questions and assistance
- 📢 **Show and Tell** - Share your progress
- 💬 **General** - Anything else
- 📚 **Resources** - Useful links and materials
- 🎉 **Celebrations** - Wins and milestones

### Enable Issues

Should be enabled by default. Verify:
1. Settings → General → Features
2. ✅ "Issues" should be checked

### Configure Issue Labels

Already created via templates, but add these additional labels:

```bash
# Using GitHub CLI (install from https://cli.github.com/)
gh label create "Q1-Dashboard" --color "0E8A16" --description "Q1 Shiny Dashboard projects"
gh label create "Q2-Package" --color "1D76DB" --description "Q2 R Package development"
gh label create "Q3-Analysis" --color "5319E7" --description "Q3 Data Story projects"
gh label create "Q4-Capstone" --color "D93F0B" --description "Q4 Capstone projects"

gh label create "priority:high" --color "D93F0B" --description "High priority"
gh label create "priority:medium" --color "FBCA04" --description "Medium priority"
gh label create "priority:low" --color "0E8A16" --description "Low priority"

gh label create "help-wanted" --color "008672" --description "Need assistance"
gh label create "good-first-issue" --color "7057ff" --description "Good for newcomers"
```

---

## Step 4: Set Up GitHub Projects

### Create Organization Project

1. Go to https://github.com/orgs/SLALR/projects
2. Click "New project"
3. Select "Board" template
4. Name: "2026 Sunday Learning Progress"
5. Click "Create"

### Configure Project Board

**Add columns:**
1. 📋 Backlog
2. 📝 To Do (This Quarter)
3. 🏃 In Progress
4. 👀 Review
5. ✅ Done

**Add custom fields:**
1. Click "⚙️" → "Settings"
2. Add fields:
   - **Quarter**: Single select (Q1, Q2, Q3, Q4)
   - **Owner**: Text
   - **Type**: Single select (Project, Learning, Documentation, Bug)
   - **Priority**: Single select (High, Medium, Low)
   - **Due Date**: Date

**Enable automation:**
1. Settings → Workflows
2. Enable:
   - ✅ Item added to project
   - ✅ Item closed
   - ✅ Pull request merged

### Create Initial Milestones

Go to Issues → Milestones → New milestone

Create these four milestones:

**Q1: Shiny Dashboard**
- Due: March 30, 2026
- Description: Deploy production-ready Shiny dashboard

**Q2: R Package Development**
- Due: June 29, 2026
- Description: Publish R package with documentation

**Q3: Data Story Project**
- Due: September 28, 2026
- Description: Complete data analysis with published website

**Q4: Capstone Integration**
- Due: December 31, 2026
- Description: Production-ready capstone project

---

## Step 5: Invite Team Members

### Add Collaborators

1. Settings → Collaborators and teams
2. Click "Add people"
3. Enter GitHub usernames
4. Set permission level:
   - **Write** - For all participants (can push to repo)
   - **Maintain** - For co-organizers (can manage issues, projects)
   - **Admin** - For primary organizers

### Send Invitation Email Template

```
Subject: Welcome to Sunday R Learning Group 2026!

Hi [Name],

You're invited to join the Sunday R Learning Group GitHub repository!

Repository: https://github.com/SLALR/sunday-r-learning-2026

Next steps:
1. Accept the GitHub invitation
2. Read the README: https://github.com/SLALR/sunday-r-learning-2026/blob/main/README.md
3. Review CONTRIBUTING.md for guidelines
4. Add your name to the participants table in README.md (via PR)
5. Join our [Discord/Slack] channel: [link]

Our first session is [Date] at [Time].

See you then!

[Your Name]
```

---

## Step 6: Create Starter Issues

Create some initial issues to get things going:

### Issue 1: Introduce Yourself

```markdown
Title: [Your Name] - Introduction

Hi everyone! 

**About me:**
- Name:
- Current role:
- R/Shiny experience level:
- What I hope to learn this year:

**Q1 Project Ideas:**
1. [Idea 1]
2. [Idea 2]

Looking forward to learning with you all!

Labels: Q1-Dashboard
Milestone: Q1: Shiny Dashboard
```

### Issue 2: Q1 Project Planning

```markdown
Title: Q1 Week 1: Project Selection

**Tasks for Week 1:**
- [ ] Review Q1 README
- [ ] Brainstorm 2-3 project ideas
- [ ] Choose primary dataset/domain
- [ ] Post introduction issue
- [ ] Set up project repository

**Due:** [Date of Week 1 session]

Labels: Q1-Dashboard
Milestone: Q1: Shiny Dashboard
```

---

## Step 7: Set Up Communication Channels

### Option A: Discord Server

1. Create Discord server
2. Create channels:
   - #announcements (read-only)
   - #general
   - #q1-dashboard
   - #q2-package
   - #q3-analysis
   - #q4-capstone
   - #code-help
   - #resources
   - #off-topic

### Option B: Slack Workspace

1. Create Slack workspace
2. Create channels (same as Discord)
3. Set up integrations:
   - GitHub notifications
   - Google Calendar

### Option C: GitHub Discussions Only

If no separate chat platform, rely on GitHub Discussions with regular check-ins.

---

## Step 8: Create Shared Resources

### Google Calendar

1. Create "Sunday R Learning" calendar
2. Add weekly events (every Sunday, 1 hour)
3. Share with all participants
4. Include:
   - Zoom/meet link
   - Week number and topic
   - Link to relevant README section

### Shared Drive/Folder (Optional)

Create a shared folder for:
- Meeting recordings
- Slide decks
- Large datasets (not in Git)
- Certificates

---

## Step 9: Prepare for Week 1

### Create Slide Deck

**Week 1 Agenda:**
1. Welcome and introductions (15 min)
2. Review year plan and quarterly structure (10 min)
3. GitHub repository tour (10 min)
4. Q1 project brainstorming (20 min)
5. Homework and next steps (5 min)

### Create Zoom/Meet Room

- Set up recurring meeting
- Enable recording (with permission)
- Add to calendar invite

### Send Pre-Session Email

```
Subject: Sunday R Learning - Week 1 Tomorrow!

Hi everyone,

Excited for our first session tomorrow!

**When:** [Date and Time]
**Where:** [Zoom/Meet link]

**Before the session:**
1. Accept GitHub invitation
2. Review the main README: [link]
3. Think about project ideas
4. Test your Zoom/Meet connection

**During the session:**
- Introductions
- Year plan overview
- Q1 project selection

**After the session:**
- Set up your project folder
- Post introduction issue

See you tomorrow!

[Your Name]
```

---

## Step 10: Week 1 Session

### Opening (5 min)
- Welcome everyone
- Overview of goals
- Icebreaker question

### Introductions (15 min)
- Each person: Name, experience, goals
- Note who's new to R/Shiny vs experienced

### Repository Tour (10 min)
- Show README structure
- Explain quarterly breakdown
- Demo GitHub Projects
- Show issue templates

### Q1 Planning (25 min)
- Review Q1 goals
- Brainstorm project ideas
- Form pairs for mutual support
- Choose your project

### Wrap-up (5 min)
- Homework: Create project folder, post intro
- Next week: Architecture and UI
- Answer questions

---

## Ongoing Maintenance

### Weekly Tasks (as organizer)

**Before session:**
- [ ] Update project board
- [ ] Review questions in Discussions
- [ ] Prepare content for week's topic
- [ ] Test demo code

**During session:**
- [ ] Record session (if permitted)
- [ ] Take notes on common questions
- [ ] Track attendance

**After session:**
- [ ] Post session notes
- [ ] Upload recording
- [ ] Create next week's tasks
- [ ] Follow up on blocked participants

### Monthly Tasks

- [ ] Review project progress
- [ ] Generate progress report
- [ ] Send newsletter/update
- [ ] Plan next month
- [ ] Retrospective with co-organizers

### Quarterly Tasks

- [ ] Showcase preparation
- [ ] Collect feedback
- [ ] Update hall of fame
- [ ] Plan next quarter
- [ ] Issue certificates (if applicable)

---

## Troubleshooting

### Common Issues

**Low attendance:**
- Survey for better times
- Make recordings available
- Allow asynchronous participation

**People falling behind:**
- Offer 1:1 help sessions
- Reduce scope if needed
- Pair struggling with advanced

**Conflicts/disagreements:**
- Refer to CODE_OF_CONDUCT
- Address promptly and kindly
- Involve co-organizer if needed

**Technical issues:**
- Maintain FAQ in Discussions
- Encourage peer helping
- Bring in external speakers for complex topics

---

## Success Metrics

Track these quarterly:

### Participation
- Attendance rate (target: 80%)
- Active contributors (GitHub activity)
- Completion rate of projects

### Engagement
- Number of discussions posts
- Code reviews given
- Help provided to others

### Outcomes
- Projects completed
- Skills gained (survey)
- Career benefits (jobs, promotions)
- External recognition (conference talks, blog posts)

---

## Resources for Organizers

### Community Management
- [Open Source Guides](https://opensource.guide/)
- [Mozilla Community Participation Guidelines](https://www.mozilla.org/en-US/about/governance/policies/participation/)

### Technical Resources
- [R for Data Science Online Learning Community](https://www.rfordatasci.com/)
- [Shiny User Showcase](https://shiny.rstudio.com/gallery/)

### Inspiration
- [TidyTuesday](https://github.com/rfordatascience/tidytuesday)
- [R4DS Learning Community](https://www.rfordatasci.com/)

---

## Contact

Questions about setup? Open an issue or discussion in the repository.

---

*Good luck with your learning group! 🚀*
