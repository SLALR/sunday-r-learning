# Progress Tracking with GitHub Projects

This guide explains how to use GitHub Projects to track individual and group progress throughout the year.

## Overview

GitHub Projects provides a kanban-style board perfect for tracking:
- Individual project milestones
- Group quarterly goals
- Weekly tasks
- Learning objectives

---

## Setting Up Projects

### Organization-Level Project (Group Progress)

**Create the project:**
1. Go to https://github.com/orgs/SLALR/projects
2. Click "New project"
3. Choose "Board" template
4. Name: "2026 Learning Progress"

**Configure columns:**
- 📋 **Backlog** - Future tasks/ideas
- 📝 **To Do (This Quarter)** - Current quarter tasks
- 🏃 **In Progress** - Actively working
- 👀 **Review** - Ready for feedback
- ✅ **Done** - Completed

**Add custom fields:**
- **Quarter**: Q1, Q2, Q3, Q4
- **Owner**: Person responsible
- **Type**: Project, Learning, Documentation
- **Priority**: Low, Medium, High
- **Due Date**: Date field

---

### Individual Project Boards

Each person can create their own project for detailed tracking:

**Setup:**
1. In your fork: Settings → Projects → New project
2. Choose "Board" template
3. Name: "[Your Name] - 2026 Projects"

**Columns:**
- 📋 **Ideas** - Future project ideas
- 📅 **This Week** - Current week's tasks
- 🏃 **Working On** - Active tasks
- 🚧 **Blocked** - Waiting for help/resources
- ✅ **Done** - Completed

---

## Creating Tasks/Issues

### For Group Milestones

**Example quarterly milestone:**
```markdown
## Q1 Goal: Deploy Shiny Dashboard

**Owner:** Everyone

**Tasks:**
- [ ] Week 1: Project selection
- [ ] Week 6: Working prototype
- [ ] Week 12: Peer review
- [ ] Week 13: Deployment

**Success Criteria:**
- [ ] All participants have deployed dashboard
- [ ] All apps publicly accessible
- [ ] Documentation complete

**Timeline:** Jan 5 - March 30, 2026
```

### For Individual Tasks

**Example weekly task:**
```markdown
## Week 3: Build filter UI

**Project:** PharmaMetrics Dashboard

**Tasks:**
- [ ] Design filter layout
- [ ] Implement date range picker
- [ ] Add category selector
- [ ] Connect to reactive data
- [ ] Test all filters

**Blockers:** None

**Due:** January 21, 2026
```

---

## Automation

### Automated Workflows

GitHub Projects can automatically move cards:

**Auto-move to "In Progress":**
When you assign yourself to an issue → moves to "In Progress"

**Auto-move to "Done":**
When you close an issue → moves to "Done"

**Setup automation:**
1. Open project settings
2. Go to "Workflows"
3. Enable built-in workflows:
   - Item added to project
   - Item closed
   - Pull request merged

---

## Labels for Organization

### Recommended Labels

**By Quarter:**
- `Q1-Dashboard`
- `Q2-Package`
- `Q3-Analysis`
- `Q4-Capstone`

**By Type:**
- `bug` - Something isn't working
- `enhancement` - New feature or improvement
- `question` - Need help or clarification
- `documentation` - Docs improvements
- `good-first-issue` - Good for newcomers

**By Priority:**
- `priority:high` - Urgent
- `priority:medium` - Important
- `priority:low` - Nice to have

**By Status:**
- `blocked` - Can't proceed
- `help-wanted` - Need assistance
- `in-review` - Awaiting feedback

**Create labels:**
```bash
# Using GitHub CLI
gh label create "Q1-Dashboard" --color "0E8A16"
gh label create "Q2-Package" --color "1D76DB"
gh label create "Q3-Analysis" --color "5319E7"
gh label create "Q4-Capstone" --color "D93F0B"
```

---

## Milestones

Use milestones for major checkpoints:

### Quarterly Milestones

**Q1 Milestone:**
- Title: "Q1: Shiny Dashboard"
- Due date: March 30, 2026
- Description: Deploy production-ready dashboard

**Create milestone:**
1. Go to Issues → Milestones
2. Click "New milestone"
3. Set title, due date, description
4. Add issues to milestone

### Weekly Milestones

For detailed tracking within quarters:
- "Q1 Week 1: Kickoff"
- "Q1 Week 6: Prototype"
- "Q1 Week 13: Launch"

---

## Views

Create different views for different perspectives:

### Board View (Default)
Kanban-style for workflow tracking

### Table View
Spreadsheet-like for detailed info

**Useful columns:**
- Title
- Assignees
- Status
- Quarter
- Priority
- Due date
- Labels

### Timeline View
Gantt chart for schedule tracking

**Setup:**
1. Click "+ New view"
2. Select "Timeline"
3. Group by: Quarter
4. Sort by: Due date

---

## Tracking Progress

### Individual Progress Dashboard

**Create a view showing:**
- Your assigned tasks
- Filtered by current quarter
- Sorted by priority

**Filter settings:**
```
Assignee: @yourusername
Quarter: Q1
Status: not Done
```

### Group Overview Dashboard

**Create a view showing:**
- All participants' progress
- Color-coded by owner
- Sorted by due date

**Filter settings:**
```
Quarter: Q1
Status: any
Group by: Owner
```

---

## Weekly Updates via Projects

### Update Project Board

Every Sunday, update your cards:

1. **Move cards** to appropriate columns
2. **Add comments** with progress notes
3. **Update status** fields
4. **Add new cards** for next week
5. **Close completed** cards

### Generate Progress Report

Projects can generate reports:

1. Go to Project → Insights
2. See charts for:
   - Burndown chart
   - Velocity
   - Cycle time
   - Items by status

---

## Integration with Code

### Link Issues to Commits

```bash
git commit -m "feat: add data filtering

Implements filters for Q1 dashboard
Closes #12"
```

This automatically closes issue #12 and moves it to Done!

### Link Issues to PRs

When creating a PR:
```markdown
## Changes
- Added data filtering module

## Related Issues
Closes #12
Addresses #13
```

---

## Examples of Good Task Cards

### Example 1: Feature Development

```markdown
Title: Add downloadable reports feature

**Description:**
Users should be able to download their filtered data as CSV or Excel

**Acceptance Criteria:**
- [ ] Add download buttons to UI
- [ ] Implement CSV export
- [ ] Implement Excel export
- [ ] Add data validation before export
- [ ] Write tests

**Technical Notes:**
- Use `downloadHandler` in Shiny
- Consider using `writexl` for Excel export

**Priority:** Medium
**Quarter:** Q1
**Estimate:** 4 hours
```

### Example 2: Learning Task

```markdown
Title: Learn shinytest2

**Goal:**
Understand automated testing for Shiny apps

**Tasks:**
- [ ] Read shinytest2 documentation
- [ ] Watch tutorial video
- [ ] Create simple test
- [ ] Test my dashboard

**Resources:**
- [shinytest2 docs](https://rstudio.github.io/shinytest2/)
- [Tutorial video](link)

**Outcome:**
Can write automated tests for Shiny apps

**Quarter:** Q1
**Type:** Learning
```

### Example 3: Bug Fix

```markdown
Title: Fix reactive plot not updating

**Bug:**
Plot doesn't update when filter changes

**Expected:**
Plot should re-render with new filter values

**Actual:**
Plot stays the same

**To Reproduce:**
1. Change date filter
2. Observe plot doesn't change

**Investigation:**
- Checked reactive dependencies
- Tried adding `observeEvent`
- Need help understanding reactive context

**Priority:** High
**Labels:** bug, help-wanted
```

---

## Monthly Reviews Using Projects

### End of Month Ritual

1. **Generate report:**
   - Open Project Insights
   - Take screenshot of progress
   - Note completion rate

2. **Review and adjust:**
   - What got done?
   - What's blocked?
   - Need to re-prioritize?

3. **Plan next month:**
   - Create new tasks
   - Update priorities
   - Set realistic goals

---

## Tips for Effective Project Management

### Do's
✅ **Keep tasks small** - Break large tasks into smaller ones  
✅ **Update regularly** - Every session, move cards  
✅ **Be specific** - "Add plotly chart" not "improve viz"  
✅ **Link everything** - Connect issues, PRs, commits  
✅ **Celebrate wins** - Close cards, mark done!  

### Don'ts
❌ **Don't ignore blocked tasks** - Ask for help  
❌ **Don't accumulate "In Progress"** - Finish before starting new  
❌ **Don't skip updates** - Outdated boards are useless  
❌ **Don't over-engineer** - Simple is better  
❌ **Don't work in isolation** - Use board to collaborate  

---

## Quarterly Review Template

At end of each quarter:

```markdown
# Q[N] Retrospective

## Statistics
- Total tasks created: [number]
- Tasks completed: [number]
- Completion rate: [percentage]
- Average time per task: [estimate]

## What Went Well
- [Success 1]
- [Success 2]

## What Could Improve
- [Challenge 1]
- [Challenge 2]

## Lessons Learned
- [Lesson 1]
- [Lesson 2]

## Adjustments for Next Quarter
- [Change 1]
- [Change 2]
```

---

## Resources

- [GitHub Projects Docs](https://docs.github.com/en/issues/planning-and-tracking-with-projects)
- [GitHub Projects Best Practices](https://github.blog/2022-02-02-feature-preview-projects-more-flexible/)
- [Project Automation](https://docs.github.com/en/issues/planning-and-tracking-with-projects/automating-your-project)

---

*Questions about project tracking? Open a [Discussion](../../discussions)!*
