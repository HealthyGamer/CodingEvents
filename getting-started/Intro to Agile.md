# Agile Project Management Basics

- What is Agile?
- What Agile Isn't
- Creating Tasks
- Scrum
- Kanban

## Resources

<https://www.atlassian.com/agile>

<https://agilemanifesto.org/>

## What is Agile?

- Individuals and interactions over processes and tools
- Working software over comprehensive documentation
- Customer collaboration over contract negotiation
- Responding to change over following a plan

The Agile Manifesto was created in 2001 to attempt to rethink how the software development process works. There are very few processes in Agile itself, but techniques like Scrum and Kanban came along and gave us that.

## What Agile Isn't

- Agile is not a replacement for long-term planning. There is no way to end up with a functional product without a goal. Instead, the idea is to change that goal more easily to reflect what you learn as you go along.
- It is not an excuse for poor-quality work. The short time frames aren't there to force more work in a shorter amount of time. You still need to give enough time to complete tasks with reasonable quality, even if that means the task takes multiple sprints.
- It is not an excuse for micromanagement. Many devs have experienced daily standups (more on that later) that take an hour or more as managers dig into every detail of what is happening. Agile values trust and autonomy.
- It is not a specific way of doing things. When people learn a technique like Scrum they often apply all the principles exactly as specified without considering whether or not they will work in their situation. Agile is a tool that should be modified to your situation.

## Creating Tasks

One thing that most Agile techniques use is that they create a hierarchy of tasks, from overall goals down to something that people can finish within a couple of days. The names of these tiers vary, but the concepts are similar. How many layers you use will depend on the complexity of your project.

- Initiatives - These are your big-picture end goals. They might take months to complete and usually don't have details on how you plan to get there. (ex. Build a website or clean my house)
  - Epics - This is a breakdown of the main items you will do to complete the initiative. (ex. Create a user interface or clean the kitchen)
    - Features - Individual elements that make up the epic that can be created independently of each other. (ex. User login or organize the pantry)
      - User Stories - A specific process that is part of the feature. It is usually focused on results rather than how to achieve them. (ex. Users can enter their email and password or clean the pantry shelves)
        - Tasks - How to implement the user story. Usually, these should take a maximum of a couple of days, but that time frame will vary based on the team. (ex. Send username and password to the server for verification or remove all items from the pantry shelves)

## Scrum

Scrum is one way that we layer processes on top of agile principles. The full process could be its own topic, but we'll review some main points.

### Sprints

Sprints are short periods (traditionally two weeks) where a team plans to do a set amount of work. At the beginning of each sprint, the team gets together to determine their work for the rest of the sprint. At the end of each sprint, anything that wasn't completed gets moved to the next sprint.

### Backlogs

Scrum uses two backlogs, the project backlog, and the sprint backlog. The project backlog is all the "stuff" the team is planning on doing, and in each sprint, the team pulls tasks from the project backlog into the sprint backlog. They will usually also have a way to track the status of the task within the sprint as well.

### Meetings

The team does three central meetings throughout the sprint to ensure that things continue progressing smoothly.

- Sprint Planning - At the beginning of the sprint, the team gets together to figure out what they will do for the rest of the sprint. This can include discussing how to complete specific tasks, what order they need to be done in, and how team members need to collaborate to finish things.
- Daily Standup - Every day the team gets together to answer three things:
  - What they did yesterday.
  - What they will do today.
  - If there is anything they need from others to accomplish their tasks.
It's called standup because team members are encouraged to stand during the meeting to encourage them to be as short as possible with their updates.
- Retrospective - At the end of the sprint, the team gets together to answer three different things:
  - What went well
  - Where can they improve
  - Action items for the next sprint based on the first two items (this is about process, not tasks)

## Kanban

Kanban has an interesting history in relation to software project management and agile. The tech industry didn't make it. Toyota created it in the 1940s to help them build cars.

Instead of set sprints, kanban uses a single board with different status columns for each task. Team members can pick up a task from the backlog and move it into the various columns (these may be things like to-do, in progress, and done) so everyone can easily see the status of these tasks at any time.

Unlike Scrum, there are no set periods for when tasks will be completed. Instead, each team member picks up a new task when they complete the last one ensuring continuous delivery of results.
