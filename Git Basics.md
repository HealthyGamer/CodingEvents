# Git Basics

- Source Control History
- What Does Git Do For Us
- Git Clients
- Getting Code - init, clone, pull, remote
- Basic Commands - commit, push, pull
- Branching Strategies - branch, checkout, merge
- Advanced commands - stash, rebase

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

## Getting Code - init, clone, pull, remote
