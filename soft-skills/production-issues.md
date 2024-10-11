# Dealing With Production Issues

No system will work perfectly 100% of the time. Some part of the system will inevitably break, and part of most tech workers' jobs is to deal with that scenario in some capacity. How well this goes depends significantly on what we do before, during, and after the event.

## A Note About the "Human Part" of the Issue

Something that I think isn't discussed much in the industry is just how much responsibility many tech workers have, and because of this, we aren't always prepared to deal with it. In my first four years as a developer, I've had access to millions of people's personal data, been in situations where a mistake on my part could affect whether or not thousands of people could afford food and shelter, and worked on systems where my recommendations could affect how easily people could access healthcare.

A part of being in tech should be, in my opinion, acknowledging that this can be draining at times and that it can significantly increase the stress involved in dealing with production issues. Take care of yourself and your teammates.

## Take Responsibility

A common theme in many of these sessions will be responsibility. A team that takes responsibility for the situation is a team that can build the trust needed to work together effectively. A team that dumps everything on scapegoats or tries to hide the problems will devolve into a toxic pit, and work quality will suffer.

Often we use on-call rotations to determine who will take primary responsibility for an issue when it occurs, who then coordinates with other team members as needed and communicates with the affected people. In larger companies, entire teams may exist that specialize in handling these scenarios.

### Solutions Not Excuses

Taking responsibility for the situation is not the same as taking responsibility for the cause. We are talking about the first- in an outage. People need to step up and deal with the issue. Blame isn't going to fix anything. It just causes distractions.

Instead, whoever is working on the resolution should be focused purely on resolving it. An arson investigation doesn't happen until the fire is out. While understanding why something broke can be crucial in fixing it, the why should be left till later.

## Plan For Things to Break

The first step in outage management comes long before an outage even occurs. When we have the tools to deal with issues, dealing with them causes a minimal interruption in the business.

There isn't much code written in complete isolation. We rely on everything from libraries and frameworks to compilers, operating systems, and firmware to make us more productive and push the boundaries on what tech can accomplish. Even if everything you do is perfect, other people in this ecosystem will mess things up, and when that breaks, the responsibility is still on you to deal with it.

### Bug Management

There are two aspects to bugs that are important to consider: Severity and priority. Severity is how much the system is affected. Priority is how much your users are impacted. The first step is to get an idea of the severity and priority involved whenever an issue is discovered. From there, you can determine how to proceed.

Generally speaking, high impact, high severity bugs are the ones where current development work stops until it is resolved- entire features used by many people are completely broken. Low impact, low severity bugs can go in the normal process. Sometimes, the impact and severity are so small that teams never get around to fixing it.

When you are in the middle, it often takes a judgment call to decide when something gets done. A minor issue that really annoys the CEO might get done before a more serious one affecting many end users. Whether or not there is a way to work around the issue is also important. A feature might be completely broken, but if it can easily be solved by a user taking a slightly different action, you would probably lower the priority.

However, allowing bugs to stack up can also cause issues as a low severity bug can easily cause a high severity one. When planning out your work, one common way to address this is to work on any bugs first before implementing any new features.

### Logging

There are two main reasons logging is essential. The first is for things like reporting and marketing. That's not what we are talking about now. We are looking at logging that tells us what happened and when so we can diagnose issues. Good logging can differentiate diagnosing an issue in minutes instead of hours or even days. However, it also increases system load and storage costs, so there's always a balancing act.

When determining what to log, you can think of it this way- what is the minimum amount of information needed to determine what happened? Often this is a lot more than you initially think. Fortunately, our tools usually help us balance the amount of data needed with the resources required. We use log levels (often labeled error, warn, debug, and info) to determine how much a given system will log. Production systems will often turn off the lowest level or two to reduce the amount of data produced. On the other end, development environments will let you inspect every detail of the system as it runs, whether it is logged or not.

### Disaster Recovery Plans

Disaster recovery plans are something a business creates so they know what to do when sh*t seriously gets ugly. For IT, "what do we do if a meteor hits the data center?" is not an unreasonable way to ensure that you are scoping your plan correctly.

#### Backup

The foundation of any tech DR plan will be backups. The key elements of a backup plan are where they are, how often they are updated, and how they are tested to ensure they are good. A single copy of your data isn't much better than no copies in this regard- anything that physically destroys or corrupts the data can quickly make it unrecoverable (take it from an ex-data recovery tech). Data should always be stored in two or more devices and preferably in two or more physical locations. This is one of the fundamental benefits of the cloud- they should handle this for you or at least provide solutions for making this happen.

#### Uptime/SLA and data loss

Another thing we want to define is the business's tolerance for downtime and data loss. This requires a lot of communication and boundary setting. Unless you have a CEO that is tech-savvy, if you ask what their % uptime requirements are, they will usually say 100%, which is impossible to achieve. It can only be 100% so far. Similarly, we measure data loss in time- if the business loses 5 seconds of data changes, is that acceptable? What about an hour or a day? The CEO will again say zero, which is impossible with current technology. Instead, discuss the cost of maintaining a system that is reliable enough to meet their standards with the cost of that loss. There will be a break-even point somewhere- once the numbers are laid out, it is much easier for managers to agree to the plan.

## Minimize the Issues

The best way to deal with issues is to prevent them from happening in the first place. When we talk about "best practices," preventing future problems is a huge piece of why we create and use them.

### Stay Vigilent

Code quality will always decrease unless the team stays on top of things. This is because software rarely gets simpler; instead, we constantly make changes and add new features. The more complex the code, the harder it is to keep it clean and organized. To a certain extent, we mitigate this by building for changes at the beginning, but this can also cause unneeded complexity and optimization. Instead, we focus on the sections that we know will grow and change. Parts that we think will stay the same can be left in a simpler design. If that changes, we update the design to accommodate.

An ideal situation is to build maintenance into your timelines. Managers don't always understand the value in maintaining code, so it is often required for devs to hide this work inside new features. Padding time estimates can go a long way towards keeping a clean code base.

### Allow Things to Crash

There's a principle that developers sometimes push for that we should handle every error and exception. This can be a nightmare to code for. What is often more effective is just to let the error happen and instead create a system that is resilient to having things fail. We see this in the form of software systems capable of restarting themselves when they crash or giving the user an error message they can use to either adjust their input or tell support what happened.

We still might want to handle some errors ourselves. Still, by designing systems that can recover from any error, we don't end up in a scenario where the system went down entirely because of an exception no one realized was possible.

### Trust Your Instincts, Not Your Code

One of the advantages that can come with having experienced devs on the team is that they've experienced a lot of different types of failures personally. This makes it easier to come up with solutions when similar events occur, but it is also a repository of information for spotting similar circumstances where a problem could occur. If something seems off, take a few minutes to check it. If your team does testing, write a test for that scenario and see if it passes. Worst case, you've verified that the thing is working as intended.

On the flip side, we have what is known as "code blindness." Working on something for a long time often makes it difficult to see problems with the system. Simple bugs can slip in because we don't notice them. Testing and code review are the main tools we have for combating this. Testing allows us to define and verify that the code does what we want it to do, not just what we think it does. Code review provides an outside perspective to spot things you forgot to test for or a way to improve your solution.
