# My Obsidian Work Vault

This is a template of the Obsidian Vault that I use to organize my work. My primary interface and usage of it is via the Daily Notes ([example](2024-12-21)). It roughly follows the [PARA method](https://fortelabs.com/blog/para/) for organizing the files in a folder structure. The point of sharing this vault is to provide a starting point for your own vault rather than a full formed framework that you must strictly adhere to.  I view Obsidian a lot like Emacs, Vim, or oh-my-zsh: it is nice to pickup someone else's configuration and then modify it to fit your own workflow.

🗒 If you are reading this on GitHub, I highly recommend cloning the repo and opening this Vault in Obsidian.

The view from Obsidian:
![[Screenshot 2025-01-02 at 11.15.26 AM.png]]

# Quick Start

If you don't care about the details and just want to see the meat of my process, check out [this filled out daily note](2024-12-21) (in Obsidian, not GitHub).  If anything in there confuses you, check out the [[#Daily Note]] section below for more details.
# Why Obsidian?

Pros of Obsidian:
- Markdown based
	- The focus is ["file over app"](https://stephango.com/file-over-app)
	- Essentially, you own your data, and even if Obsidian bit-rots, your files are all still readable and useful
- Has a fully functional mobile app, including plugins
- Can use the same app (but separate vault) for Work and Personal
- Lots of [plugins](https://obsidian.md/plugins)
- Totally flexible and completely unopinionated
	- This can be a curse if you start to start from zero, but bootstrapping yourself with someone else's templates and customizing from there solves this.

Cons of Obsidian:

- You can spend too much time optimizing your Obsidian workflow and lie to yourself that you are being productive. Ask me how I know 😆
- Isn't as powerful as Notion when it comes to tables and acting as a lightweight database

# Daily Note

The [Daily Note](https://help.obsidian.md/Plugins/Daily+notes) is the primary touch point of this Vault.  Every day that I start work, I click the daily note button (![lucide-calendar.svg > icon](https://publish-01.obsidian.md/access/f786db9fac45774fa4f0d8112e232d67/Attachments/icons/lucide-calendar.svg) ) in the [ribbon](https://help.obsidian.md/User+interface/Ribbon)  From there I can see at a glance all of the tasks I should be working on and then plan my day.   You can see an example of a filled out daily note [here](2024-12-21). You can also press the daily note button to see what a blank one looks like.

## How I use it

This [filled out daily note](2024-12-21) is representative of how I use the daily note feature.

I use the top Projects, Jira, and Tasks sections to determine what tasks I should be working on today.  The tasks in the "Active Tasks" section should be limited to just the tasks that I think I can complete today.  Any tasks that I won't be able to complete today get bumped to later in the week.

I move to the Day Planner section and open the *Timeline in the right pane. I manually add in the meetings that I have for the day and then block off times for deep work on today's tasks.

I leave the daily note open on my second monitor so that as I knock off tasks, I can check them off and know exactly which task to pick up next.

If I pickup a new task over the course of the day, I can either add it to the bottom of the daily note or to the appropriate Project note. Either way, it will show up automatically in the appropriate daily note based on the due date.
## How it works

The [Jira Issue](https://obsidian.md/plugins?id=obsidian-jira-issue) plugin pulls down all of the open tasks I'm assigned in Jira and displays them sorted by priority. 

There are then 4 task sections:
- Completed tasks 🎉
	- Tasks with a completed date == today
- Active Tasks
	- Tasks with a due date <= today
- Scheduled Tasks 📆
	- Tasks with due date > today
- Backlog
	- Tasks with no due date set
	- I periodically scan this list and prune no longer important tasks or assign due dates to important tasks

 I use the [Dataview](https://obsidian.md/plugins?id=dataview) plugin to query tasks across all notes in the Vault. Meaning that you can enter tasks in your daily notes or in any of your PARA notes and they will show up in this section.
 
 The tasks function is handled by the [Tasks](https://obsidian.md/plugins?id=obsidian-tasks-plugin) plugin.  I have mine configured to only consider tasks with the #task tag to avoid vanilla checklist from being considered as tasks.

The [templater](https://obsidian.md/plugins?id=templater-obsidian) plugin is used to populate the daily note template.  The dataview/task queries are templated to use the daily note's date, as are the yesterday & tomorrow links.

The [Day Planner](https://github.com/ivan-lednev/obsidian-day-planner) is used to generate the time blocking timeline in the right pane.

# PARA

I used to just create all of my notes in the top-level of my Vault, but the lack of structure and order always bothered me.  The [PARA Method](https://fortelabs.com/blog/para/) is a relatively lightweight method for organizing the various notes I make throughout the day.

PARA stands for Project, Area, Resource, and Archive.  These are the 4 directories you see in this vault.  Quoting the [Forte Labs blog post on PARA](https://fortelabs.com/blog/para/)

> - Project: Short-term efforts in your work that you're working on now
> - Area: Long-term responsibilities you want to manage over time
> - Resource: Topics or interests that may be useful in the future
> - Archive: Inactive items from the other three categories

Whenever I create a new file, I consider which of these 4 folders I should put it in, and periodically I archive files by moving them to the Archive directory.

# Miscellaneous

💰Obsidian is free for personal usage. If you use it for work, make sure to [buy a commercial license](https://help.obsidian.md/teams/license), it is only $50 a year (and your employer may reimburse the cost).

# Alternatives Considered

## Sunsama

For almost two years, I used [Sunsama](https://www.sunsama.com/) to manage my days/tasks at work.  It is actually a really great app for time blocking and managing tasks.  My main reason for switching to Obsidian was to unify the system I use for personal and work.  I was also somewhat concerned about giving an app like that access to my work calendar, which is required to take full advantage of the time blocking features.  It also doesn't support note taking like Obsidian does, which may or may not be an issue for you.

## Org-mode

Since I'm an Emacs user, [org-mode](https://orgmode.org/) made a lot of sense.  At several points in graduate school, I would take all my notes and even write research papers in Org-mode (via latex exporting). I ended up not sticking with it due to the lack of a mobile app with convenient sync across all of my devices.  It seems like the landscape has changed a bit since I last looked, but I think Obsidian still has the edge due to the plugins and first-class syncing.

## Taskwarrior

When I worked for a National Laboratory that was fairly stringent about putting data in the cloud, I used [taskwarrior](https://taskwarrior.org/).  It is a neat CLI tool for managing a task list.  It was crazy easy and fast to add tasks, especially combined with [iTerm's hotkeys for a popup terminal](https://apple.stackexchange.com/questions/48796/iterm-as-a-slide-out-terminal-from-the-top-of-the-screen).  Similar to org-mode, my main pain point was the lack of a mobile app.  I had to email myself the task from my work phone and then manually enter the task when I got back to my laptop 🤮

## Notion

I tried out Notion for a couple of months.  It is a brilliantly built tool that is an absolutely joy to use.  The showstopper for me is that my data is not end-to-end encrypted.  To me, the risk of my personal notes and information leaking (due to a bug, hacking, etc) was too high. I also doubt that any corporate IT would give the go ahead to use Notion for work unless the company as a whole was using it.