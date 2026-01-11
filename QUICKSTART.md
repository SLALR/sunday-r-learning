# Quick Start Guide for Participants

Welcome to the Sunday R Learning Group! This guide will get you set up and ready for your first session.

## ⏱️ 10-Minute Setup

### 1. Accept GitHub Invitation (2 min)

Check your email for a GitHub invitation from SLALR organization. Click the link and accept.

### 2. Explore the Repository (3 min)

Visit: https://github.com/SLALR/sunday-r-learning-2025

**Read:**
- [ ] Main README (overview of year plan)
- [ ] CONTRIBUTING.md (participation guidelines)
- [ ] Q1 README (current quarter details)

### 3. Introduce Yourself (5 min)

Create your introduction issue:

1. Go to Issues → New issue
2. Use "Introduce Yourself" template
3. Share:
   - Your name and background
   - R/Shiny experience level
   - What you hope to learn
   - Initial project ideas

---

## 📚 What You'll Need

### Software

**Required:**
- R (≥4.0): [Download](https://cran.r-project.org/)
- RStudio (recommended): [Download](https://posit.co/download/rstudio-desktop/)
- Git: [Download](https://git-scm.com/)

**Optional:**
- GitHub Desktop: [Download](https://desktop.github.com/)
- Visual Studio Code (alternative to RStudio)

### Accounts

**Required:**
- GitHub account (free): [Sign up](https://github.com/join)

**Recommended:**
- shinyapps.io (free tier): [Sign up](https://www.shinyapps.io/)
- Netlify (for Q3): [Sign up](https://www.netlify.com/)

---

## 🚀 Getting Started with Git/GitHub

### Option A: GitHub Desktop (Easiest)

1. **Install GitHub Desktop**
2. **Clone repository:**
   - File → Clone repository
   - Search "sunday-r-learning-2025"
   - Choose location on your computer
   - Click "Clone"

3. **Create your project folder:**
   - Open cloned folder in Finder/Explorer
   - Navigate to Q1-Shiny-Dashboard/
   - Create folder: YourName-ProjectName/
   - Add a README.md file

4. **Commit and push:**
   - GitHub Desktop shows your changes
   - Write commit message: "Add my project folder"
   - Click "Commit to main"
   - Click "Push origin"

### Option B: Command Line

```bash
# Clone the repository
git clone https://github.com/SLALR/sunday-r-learning-2025.git
cd sunday-r-learning-2025

# Create your project folder
cd Q1-Shiny-Dashboard
mkdir YourName-ProjectName
cd YourName-ProjectName

# Create README
echo "# My Q1 Project" > README.md

# Commit and push
git add .
git commit -m "Add my project folder"
git push origin main
```

---

## 📁 Your First Project Setup

### 1. Create Project Folder

```
Q1-Shiny-Dashboard/
└── YourName-ProjectName/
    ├── README.md          # Project description
    ├── app.R             # Your Shiny app
    ├── .gitignore        # Files to ignore
    └── data/
        └── sample.csv    # Sample data only
```

### 2. Initialize R Project

In RStudio:
1. File → New Project → Existing Directory
2. Navigate to your project folder
3. Click "Create Project"

This creates a `.Rproj` file.

### 3. Write Your README

Use the template: `templates/PROJECT_README_TEMPLATE.md`

Minimum contents:
```markdown
# [Your Project Name]

## Overview
Brief description of what it does

## Installation
How to run it locally

## Status
- [x] Project setup
- [ ] UI design
- [ ] Core functionality
- [ ] Deployment
```

---

## 🗓️ Weekly Routine

### Before Sunday Session (30 min)

1. **Review this week's topic**
   - Read relevant section in quarterly README
   - Watch any prep videos
   - Note questions

2. **Work on your project**
   - Complete last week's homework
   - Push code to GitHub
   - Update your README

3. **Post weekly update** (use template)
   - What you accomplished
   - Where you're stuck
   - What you'll work on

### During Sunday Session (60 min)

1. **Learn segment** (20 min)
   - New concept/technique
   - Live coding demo
   - Q&A

2. **Work time** (35 min)
   - Code on your project
   - Pair program
   - Get help from others

3. **Share** (5 min)
   - Quick progress updates
   - Plan for next week

### After Sunday Session

1. **Push your work**
   ```bash
   git add .
   git commit -m "Week N progress: [brief description]"
   git push
   ```

2. **Help others**
   - Check Discussions for questions
   - Review someone's code
   - Share useful resources

---

## 💬 Communication

### GitHub Discussions
**Use for:**
- Technical questions
- Sharing resources
- Project feedback
- Longer discussions

**How to post:**
1. Go to Discussions tab
2. Choose category
3. Write clear title
4. Provide context
5. Add relevant labels

### Discord/Slack (if available)
**Use for:**
- Quick questions
- Scheduling pair programming
- Casual chat
- Urgent help

### Issues
**Use for:**
- Tracking your TODOs
- Reporting bugs
- Requesting features
- Specific problems

---

## 🆘 Getting Help

### When You're Stuck

**1. Try these first:**
- [ ] Google the error message
- [ ] Check package documentation
- [ ] Review similar examples
- [ ] Take a break and come back

**2. Ask for help:**

**Good question format:**
```markdown
## Problem: [Brief description]

What I'm trying to do: [Goal]

What's happening: [Current behavior]

What I expected: [Expected behavior]

What I've tried:
- Approach 1
- Approach 2

Code:
# Paste relevant code here

Error:
# Paste error message
```

**Post in:**
- Discord/Slack for quick questions
- GitHub Discussions for detailed questions
- Sunday session for live help

### Finding Answers

**Resources in order:**
1. Quarterly README (has links to docs)
2. GitHub Discussions (search first!)
3. RStudio Community forum
4. Stack Overflow
5. Package documentation
6. Ask the group

---

## 📊 Tracking Your Progress

### Use GitHub Project Board

**View your tasks:**
1. Go to Projects tab
2. Filter by your name
3. See: To Do, In Progress, Done

**Update weekly:**
- Move cards as you progress
- Add new tasks
- Close completed items

### Personal Checklist

**Quarter 1 (example):**
- [x] Week 1: Project selected
- [ ] Week 6: Working prototype
- [ ] Week 12: Peer review complete
- [ ] Week 13: Deployed and showcased

---

## 🎯 Success Tips

### Do's ✅

**Consistency:**
- Show up each week (even if behind)
- Push small commits frequently
- Update your README regularly

**Collaboration:**
- Ask questions early
- Help others when you can
- Give constructive feedback
- Celebrate others' wins

**Learning:**
- Start simple, add complexity
- Make it work, then make it pretty
- Document as you go
- Learn from mistakes

### Don'ts ❌

**Avoid:**
- Scope creep (keep projects focused)
- Perfectionism (done > perfect)
- Working in isolation (use the group!)
- Skipping documentation
- Committing secrets/passwords

---

## 📋 Checklists

### Week 1 Checklist

- [ ] Accept GitHub invitation
- [ ] Set up Git/GitHub
- [ ] Clone repository
- [ ] Create project folder
- [ ] Post introduction issue
- [ ] Choose project idea
- [ ] Attend Sunday session
- [ ] Join Discord/Slack (if applicable)

### Project Setup Checklist

- [ ] Project folder created
- [ ] README.md written
- [ ] .gitignore configured
- [ ] .Rproj file created
- [ ] Initial commit pushed
- [ ] Shared in Discussions

### Before Showcase Checklist

- [ ] Code clean and commented
- [ ] README comprehensive
- [ ] Project deployed
- [ ] Demo prepared (2-5 min)
- [ ] Screenshots added
- [ ] Tests passing (if applicable)

---

## 🎉 What Success Looks Like

### By End of Quarter 1
- ✅ Working Shiny dashboard
- ✅ Deployed publicly
- ✅ Clean GitHub repo
- ✅ Documentation complete
- ✅ Comfortable with Shiny basics

### By End of Year
- ✅ 3-4 portfolio projects
- ✅ Active GitHub profile
- ✅ Professional portfolio site
- ✅ Interview-ready projects
- ✅ Expanded R/Shiny skills
- ✅ Connections with peer learners

---

## 📞 Need Help?

### Technical Issues
- Post in GitHub Discussions
- Ask in Discord/Slack
- Bring to Sunday session

### GitHub/Git Issues
- Check [GitHub Docs](https://docs.github.com)
- Ask in #github-help channel
- Pair with experienced member

### Project Guidance
- Review quarterly README
- Ask for peer feedback
- Schedule 1:1 with organizer

### Taking a Break
- Let organizers know
- No judgment!
- Can catch up anytime
- Projects stay in repo

---

## 📚 Essential Resources

### Documentation
- [R for Data Science](https://r4ds.hadley.nz/)
- [Mastering Shiny](https://mastering-shiny.org/)
- [R Packages](https://r-pkgs.org/)

### Getting Help
- [RStudio Community](https://community.rstudio.com/)
- [Stack Overflow [r]](https://stackoverflow.com/questions/tagged/r)
- [R4DS Learning Community](https://www.rfordatasci.com/)

### Inspiration
- [Shiny Gallery](https://shiny.rstudio.com/gallery/)
- [R Graph Gallery](https://r-graph-gallery.com/)
- [TidyTuesday](https://github.com/rfordatascience/tidytuesday)

---

## 🚀 Ready to Start?

**Week 1 Prep:**
1. ✅ Complete 10-minute setup
2. ✅ Review Q1 README
3. ✅ Think about project ideas
4. ✅ Join communication channels
5. ✅ See you Sunday!

---

**Questions?** Post in GitHub Discussions or reach out to organizers.

**Welcome aboard! Looking forward to learning with you! 🎉**
