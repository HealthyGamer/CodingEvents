# Git Basics

- Source Control History
- What Does Git Do For Us
- Git Clients
- Getting Code - init, clone, pull, remote
- Basic Commands - add, commit, push
- Branching Strategies - branch, checkout, merge
- Advanced commands - stash, rebase, pull requests

Full list of commands: <http://git-scm.com/docs>

## A Short History of Version/Source Control

Definition: Source or Version control is a strategy for tracking different versions of files as they change.

Technically the first version control system was built in the 1960's but for normal use, we tend to go through a few phases.

Simplest Version: Once upon a time (and unfortunately this still happens). Changes were tracked manually, if at all. Devs would have to keep multiple copies of the software on their machine and any changes the made as a team would have to be manually integrated.

File Share: An upgrade to this system involves keeping the main versions of the software in a central location, but still tracking changes manually or not at all. This allows devs to have access to the same version of the work, and may have some tracking capabilities, but still makes it hard to integrate changes.

Modern Source Control: Modern systems have centralized storage, and also fully track every change that is made to the code. In addition, they allow things like blocking other devs from making changes to a specific file, merging different changes together, and easily moving back and forth between code versions. Git is probably the most popular, but others like mercurial and SVN still see a lot of use.

## Why Use Source Control?

There are two main reasons for using source control:

1. It creates a full history of all code changes and acts as a built-in backup system for code. If your computer fails, you can get another copy from source control instead of losing the data. You can also look at history, see what has changed, and revert to an earlier version if you want to undo something.
2. It smooths out the process of having multiple devs working on the same code. Even if you spread out the tasks to different developers, they occassionally will fall into scenarios where they need to make changes to the same files. Source control systems create strategies for handling those scenarios with a minimum of disruption to dev's work time.

## Git Clients

There are three ways to work with git on your machine. Each has it's advantages, and devs usually develop a preference for one of them.

1. Command line. This is the simplest way to interact with git, since it is what the base install comes with. It does take some time to memorize commands, but once you do it allows for the maximum amount of control as UI option often bundle multiple commands into a single step.
2. IDE integration. Visual Studio/VSC, Ecplipse, Jetbrains, etc. almost allways have integrations with source control built in. This is often the most convenient option since you can stay within the same software you are using to write the code.
3. Seperate GUI's. SourceTree, Git, and Github are probably the most common, but there are plenty out there. They tend to have more features than integrated UIs, so can be useful for difficult scenarios if you want to avoid command line.

I'll mostly be using command line to demo these things, as it's the simplest and most universal way to interact with git- no matter what client you are using, these are the commands being run.

### Git servers

Technically anyone can run a git server themselves, but most of us don't bother. As with many things, this is often outsourced to an external service. The most common choices are GitHub, GitLab, Bitbucket, and Azure Devops.

## Getting Code - init, clone, remote, fetch (pull)

### init

`git init` initializes a git repository and is almost always your first step when creating a new project. It creates a folder names '.git' that includes a whole bunch of files in it. For the most part we won't interact with these files directly, but basically this holds all the information about the repository and tracks every change made to the code over time. Basically this folder is where all the "magic" is.

### clone

`git clone <location>` copies all the code from a remote location. It's essentially a copy/paste command.

### remote

`git remote add <name> <location>` allows you to setup a place where you interact with your code remotely. Cloning gets the code but doesn't create a relationship between your code and that remote location. `remote` is something we can leverage multiple times to add our changes to the main repository and get changes from others.

### fetch

`git fetch` gets the latest changes from our remote. We often use a variant of this, `get pull` instead since that gets the changes and then automatically applies them to our copy.

## Basic Commands - add, commit, push

### add

`git add <file>` tells git you want to add the changes you've made to tracking, or "stage" them. `--all` or `.` adds all the changes you've made- just be sure you are setup to not include anything you didn't want like passwords!

### commit

`git commit -m "<commit message>"` tells git to take a snapshot of the current version of the code. Once we've created a commit we can return to that state at any point. You always include a message along with that to indicate what/why you've made those changes so other people know what is happenning.

### push

`git push` is the final step in making changes. It takes all the commits you've made on your machine and sends them back to your remote source. This allows other people to access those changes and update their own copies.

## Branching Strategies - branch, checkout, merge

We could probably spend an hour on branching strategies, and this is where most git newbies get lost, but here's how it works.

## Advanced commands - stash, rebase, pull requests

### stash

### rebase

### pull requests (merge requests)
