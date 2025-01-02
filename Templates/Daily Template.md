---
tags:
  - daily-note
---
###### [[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>|↶ YESTERDAY]] ⁝ [[<% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>|TOMORROW ↷]]
 <% tp.date.now("dddd -  MMMM Do YYYY", 0, tp.file.title, "(📅) YYYY-MM-DD") %>

# ✔ Tasks
### Projects
This is where I put links to Projects inside and outside Obsidian.
[[ProjectA]]
[Big Project B Google Doc]()
[Big Project C Coda]()

### Jira

```jira-search
query: Project in (MYTEAM) AND (assignee in (currentUser()) OR issueFunction in subtasksOf("assignee in (currentUser())")) AND type not in (Epic, Incident) AND statusCategory != Done ORDER BY status, Priority DESC
columns: key, summary, STATUS, PRIORITY
```
Note: ^ won't work until you add a Jira token in the settings page and change the query to match the Jira Project you use
### 🟢 Completed Today
```tasks
done date is <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>
hide task count
```
### 🟡 Active Tasks
```tasks
due on or before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>
not done
hide task count
hide start date
hide scheduled date
sort by priority
sort by due
```
### 🟠 Scheduled Tasks
```tasks
due after <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>
starts on or before <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>
not done
hide task count
hide start date
hide scheduled date
sort by priority
sort by due
```
### 🔴 Backlog
```tasks
not done
no due date
```

# 📆 Day Planner

## Meetings
- [ ] 

## Tasks
- [ ] Catch up on messaging platforms
	- [ ] Slack
	- [ ] Email
	- [ ] Gerrit
- [ ] 
