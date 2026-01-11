# Contributing to Sunday R Learning Group

Welcome! This document provides guidelines for participating in our learning group and contributing to the shared repository.

## 🎯 Our Principles

1. **Learn Together**: We're all here to grow
2. **Help Each Other**: No question is too small
3. **Share Openly**: Code, struggles, victories
4. **Stay Consistent**: Show up, even when it's hard
5. **Be Kind**: We're all at different levels

---

## 📁 Repository Structure

```
sunday-r-learning/
├── README.md                   # Main project overview
├── CONTRIBUTING.md             # This file
├── Q1-Shiny-Dashboard/
│   ├── README.md              # Q1 details
│   ├── YourName-ProjectName/  # Your individual project
│   └── shared-resources/      # Shared code/tips
├── Q2-R-Package/
│   ├── README.md
│   └── packages/              # Links to package repos
├── Q3-Data-Story/
│   ├── README.md
│   └── analyses/              # Your analysis projects
├── Q4-Capstone/
│   ├── README.md
│   └── projects/
└── templates/
    └── weekly-update.md
```

---

## 🚀 Getting Started

### 1. Fork and Clone

```bash
# Fork the repository on GitHub (click Fork button)

# Clone your fork
git clone https://github.com/YOUR-USERNAME/sunday-r-learning.git
cd sunday-r-learning

# Add upstream remote
git remote add upstream https://github.com/SLALR/sunday-r-learning.git
```

### 2. Create Your Project Folder

```bash
# Navigate to current quarter
cd Q1-Shiny-Dashboard  # or Q2, Q3, Q4

# Create your project folder
mkdir YourName-ProjectName
cd YourName-ProjectName

# Initialize your project
# (R project, package, or Quarto as appropriate)
```

### 3. Naming Conventions

**Project Folders**:
- Format: `FirstName-ProjectName`
- Examples: 
  - `Sarah-PharmaMetrics`
  - `John-FantasyFootball`
  - `Maria-ClinicalDashboard`

**Branches** (if working in main repo):
- Format: `quarter/name/feature`
- Examples:
  - `q1/sarah/add-dashboard`
  - `q2/john/fix-tests`

**Commits**:
- Start with type: `feat:`, `fix:`, `docs:`, `refactor:`
- Examples:
  - `feat: add data filtering module`
  - `docs: update README with installation`
  - `fix: resolve reactivity bug in plot`

---

## 📝 Weekly Updates

Share your progress every week using this template:

```markdown
## Week [N] Update - [Your Name]

**What I accomplished:**
- Completed X
- Made progress on Y

**What I learned:**
- Learned about Z
- Discovered that...

**Blockers/Questions:**
- Having trouble with...
- Would appreciate help with...

**Next week goals:**
- Will work on...
- Plan to complete...

**Demo/Screenshot:**
[Optional: link or attach image]
```

**Where to post**:
1. In your project README
2. In GitHub Discussions
3. In group Slack/Discord

---

## 💬 Communication Channels

### GitHub Discussions
Use for:
- Technical questions
- Sharing resources
- Project ideas
- Feedback requests

**Categories**:
- 💡 Ideas
- 🙏 Help Wanted
- 📢 Show and Tell
- 💬 General

### Slack/Discord
Use for:
- Quick questions
- Scheduling pair programming
- Sharing interesting articles
- Casual chat

### Issues
Create issues for:
- Bugs in shared code
- Feature requests for group resources
- Suggestions for curriculum changes

**Label your issues**:
- `question` - Need help understanding something
- `bug` - Something isn't working
- `enhancement` - Idea for improvement
- `documentation` - Improvements to docs
- `good first issue` - Easy for newcomers

---

## 🤝 Collaboration Etiquette

### Code Reviews

When reviewing others' code:
- **Be kind**: Everyone is learning
- **Be specific**: "Consider adding error handling here" not "this is wrong"
- **Be constructive**: Suggest solutions, don't just point out problems
- **Celebrate wins**: Comment on things you like!

### Asking for Help

When asking questions:
1. **Show what you've tried**: Share your code and error messages
2. **Be specific**: "My plot won't render" → "My renderPlot gives error: ..."
3. **Provide context**: Share relevant code, not entire file
4. **Use reprex**: Create reproducible examples when possible

**Example good question**:
```markdown
## Problem: ggplot not showing in Shiny app

I'm trying to render a plot in my Shiny app but nothing appears.

**Code**:
```r
output$plot <- renderPlot({
  ggplot(data, aes(x, y)) + geom_point()
})
```

**Error**: No error, but plot doesn't appear

**What I've tried**:
- Checked that data loads (it does)
- Verified plot works in R console
- Tried different plot types

**Environment**: R 4.3, Shiny 1.8, ggplot2 3.4
```

### Giving Help

When helping others:
- **Ask questions**: Help them think through it
- **Don't just give answers**: Guide them to the solution
- **Share resources**: Link to documentation, tutorials
- **Celebrate their learning**: Acknowledge progress

---

## 📊 Sharing Your Work

### GitHub Repository

Your project should include:

```
YourName-ProjectName/
├── README.md              # What it is, how to use it
├── .gitignore            # Don't commit data/secrets
├── app.R or analysis.qmd # Main file
├── R/                    # Functions (if applicable)
├── data/                 # Small sample data only
├── tests/                # Tests (if applicable)
└── docs/                 # Documentation
```

### README Template

See `templates/README_TEMPLATE.md` for a comprehensive template.

Minimum sections:
1. **Title and description**
2. **Installation/Setup**
3. **Usage** (with examples)
4. **Screenshots/Demo**
5. **Technologies used**
6. **License**

### During Showcase

Prepare for your 5-minute presentation:
- [ ] Test demo ahead of time
- [ ] Have backup screenshots
- [ ] Keep to time limit
- [ ] Focus on interesting parts
- [ ] Mention challenges overcome

---

## 🎨 Code Style

### R Code

Follow the [Tidyverse Style Guide](https://style.tidyverse.org/):

**Good**:
```r
# Use snake_case for functions and variables
calculate_mean_age <- function(birth_dates) {
  current_year <- year(Sys.Date())
  ages <- current_year - year(birth_dates)
  mean(ages, na.rm = TRUE)
}

# Use spaces around operators
x <- 1 + 2

# Use meaningful names
patient_ages <- calculate_mean_age(patient_birth_dates)
```

**Avoid**:
```r
# camelCase (use snake_case instead)
calculateMeanAge <- function(birthDates) { }

# No spaces
x<-1+2

# Cryptic names
pa <- cma(pbd)
```

### Use styler

```r
# Install
install.packages("styler")

# Style a file
styler::style_file("app.R")

# Style entire project
styler::style_dir()
```

---

## 🔍 Code Review Checklist

When reviewing code (yours or others'):

### Functionality
- [ ] Code runs without errors
- [ ] Handles edge cases
- [ ] Produces expected output

### Readability
- [ ] Functions have clear names
- [ ] Complex logic has comments
- [ ] Code follows style guide
- [ ] No repeated code (DRY principle)

### Documentation
- [ ] README explains purpose
- [ ] Functions have roxygen comments
- [ ] Examples are provided
- [ ] Dependencies are listed

### Best Practices
- [ ] No hard-coded paths
- [ ] Secrets not in code
- [ ] Error handling present
- [ ] Tests cover key functionality

---

## 🐛 Reporting Issues

### In Your Own Project
Create issues in your repo to track:
- Bugs to fix
- Features to add
- Ideas to explore

### In Shared Resources
If you find issues in shared materials:

1. **Check if it's already reported**
2. **Create a clear issue**:
```markdown
## Bug Report: [Brief description]

**What I expected:**
Description

**What actually happened:**
Description

**Steps to reproduce:**
1. Step one
2. Step two
3. ...

**Environment:**
- R version:
- Package versions:
- OS:

**Additional context:**
Screenshots, error messages, etc.
```

---

## 🎓 Learning Resources

### Adding Resources

Found a great tutorial? Share it!

1. Add to `resources/` folder or README
2. Include:
   - Title and author
   - Link
   - Brief description
   - Why it's useful
   - Difficulty level

### Requesting Resources

Need help with a topic?
- Open a Discussion
- Label it `help-wanted`
- Be specific about what you're trying to learn

---

## 🏆 Recognition

We celebrate:
- **Consistent Attendance**: Show up weekly
- **Helping Others**: Answer questions, review code
- **Sharing Knowledge**: Blog posts, tutorials, tips
- **Completion**: Finish quarterly projects
- **Excellence**: Outstanding projects

### Hall of Fame

Completed projects are added to the quarterly Hall of Fame in respective READMEs.

### Certificates

Participants who complete 3+ quarterly projects receive a certificate of completion.

---

## 📅 Attendance and Commitment

### Expected Participation
- **Attend**: 80% of sessions (aim for 10+ out of 13 weeks per quarter)
- **Contribute**: Weekly progress updates
- **Engage**: Help others when you can
- **Complete**: At least 2 major projects per year

### If You Need to Miss Sessions
- Post update in Discord/Slack
- Review recordings if available
- Catch up on your own time
- Ask for help if you fall behind

### If You Need a Break
Life happens! If you need to step away:
- Let the group know
- You can always rejoin
- Your projects stay in the repo
- No judgment!

---

## 🔐 Data and Privacy

### What to Share
- ✅ Code and algorithms
- ✅ Public datasets
- ✅ Aggregated/anonymized results
- ✅ Synthetic sample data

### What NOT to Share
- ❌ Proprietary company data
- ❌ Personal information
- ❌ Passwords or API keys
- ❌ Confidential information

### Using .gitignore

Always include:
```
# R
.Rproj.user
.Rhistory
.RData
.Ruserdata

# Data
*.csv
*.xlsx
data/
!data/sample.csv  # except explicitly included samples

# Secrets
.env
.Renviron
config.yml

# Large files
*.zip
*.tar.gz
```

---

## 🎉 Having Fun

Remember:
- **Celebrate small wins**: Fixed a bug? That's awesome!
- **Share failures**: We learn from mistakes
- **Be creative**: Try wild ideas
- **Help each other**: We're a team
- **Take breaks**: Avoid burnout

### Social Activities
- Monthly coffee chats
- Show-and-tell sessions
- Code debugging parties
- End-of-quarter celebrations
- Conference watch parties

---

## ❓ Questions?

- **Technical**: Post in GitHub Discussions or Discord
- **Organizational**: Contact group organizer
- **Private**: Direct message in Discord

---

## 📜 License

All code shared in this repository is licensed under MIT License unless otherwise specified.

By contributing, you agree to license your contributions under the same terms.

---

## 🙏 Acknowledgments

Thank you for being part of this learning community!

Every contribution, question, and project makes our group better.

---

*Last updated: January 2025*
