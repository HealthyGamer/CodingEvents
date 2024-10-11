# Requirements Gathering: What Do They Actually Want?

Code quality is useless if you aren't building the features your users need. The problem is that users rarely come to you with fully documented requirements ready for you to sit down and start coding. Instead, requirements gathering is more like a conversation, with the dev team guiding their users towards understanding what they want to be done.

For more minor software elements, you may not need every step, but for the sake of covering everything, I'll be using the concept of a large enterprise project as a foundation.

- Why Do We Go Through This Process?
- The Importance of Active Listening
  - Active Listening Components
- Understand the Problem
  - Problems Not Solutions (Yet)
  - Eliminate Ambiguity
    - Identify Edge Cases
  - Business/Functional Requirements vs. Technical Requirements
- Define "Done"
- Organize the Results (Write It Down)

## Why Do We Go Through This Process?

When given a task, the initial urge is often to devise a solution and immediately start hacking away at it. It might work out, but it might not. Instead, utilizing the requirements gathering process leads to more consistent outcomes.

It prevents wasting time building the wrong thing. Your brilliant solution doesn't do much if it solves the wrong problem.
Helps control scope creep. A certain amount of scope creep is inevitable since things will come up during implementation that no one expected, or business needs change requiring a different solution.
It's hard to set useful goals without a defined problem. This often leads to miscommunication and frustration between everyone involved.

## The Importance of Active Listening

As much as users might believe otherwise, devs are not mind-readers. We need them to tell us what they actually want to deliver a valuable product, and they may not even fully understand what that is. This can be particularly difficult for those of us who are neurodivergent or socially awkward. On the flip side, areas like project management and consulting rely even more heavily on these skills. It's a common scenario that PMs spend part of their time going between customers and engineers to translate user requests into something the engineers can implement (Office Space, anyone?). That doesn't absolve devs from learning to listen to users- it's a skill that creates better code just as much as things like learning algorithm design can.

### Active Listening Components

While I can't cover active listening here, there are a few concepts to highlight. There are a couple of links at the end to start learning more.

- Pay attention. When trying to understand your user's needs, you need to be focused on them, not the eventual solution. Later, we'll talk about the need to write everything down. This is an excellent time to start.
- Withhold Judgement. This can be easy to break if the user does something they "shouldn't." You probably have a plan for how everything is supposed to work, but your users can't read your mind any better than you can read theirs. The solution may be simply educating them, but be cautious about blaming them for not using something as intended.
- Reflect, Clarify, and Summarize. These are often listed separately but follow a similar theme. One of the best ways to be sure you understood someone correctly is to tell them what you thought they said. They'll usually tell you if you are wrong. As a bonus, this can lead to further information about the problem.

## Understand the Problem

### Problems Not Solutions (Yet)

One of the critical traps we can fall into is that when someone brings us a solution, we just go ahead and implement it. I run into this all the time when helping other devs. They have a solution for their problem, but this one bit doesn't work, and if they just fixed that error, everything would be fine. Sometimes, a completely different approach would work better, but there's no way to know without understanding the actual problem. The error message is only one small part of the story. 

The first question I'll often ask when someone wants to implement a solution or the problem doesn't seem like the right problem is, "What is your goal here?" Usually, something like that is enough to get the necessary info to find the starting point of the discussion, but sometimes it takes a couple of clarifying questions.

### Eliminate Ambiguity

Even if we've identified the root issue, we may not fully understand it. When digging in, it's important to define things as clearly as possible. This may involve multiple people, which is why this process can take some time. 

If marketing comes to me and says, "I need a button added to the website for a promotion we are running." I've got a reasonably good idea of what the problem is. They are running a promotion, and an element of that requires adding a button to the website. That's not nearly enough to actually start implementation, though.

Marketing might supply the general location, text, and what the button does, the designer provides information on what it needs to look like, and sales also need to approve the results before release. Part of my job is ensuring I have all that information before starting any code.

#### Identify Edge Cases

It's nearly impossible to identify every edge case, but we want to think about as many as we can. In the promotion button example, this may be things like which users can see the new button and do we want to do any A/B testing with the text now or in the future,

### Business/Functional Requirements vs. Technical Requirements

There are two main sets of requirements we need to gather. Functional requirements and technical requirements. Functional or business requirements are basically user-side. What does their experience need to be like? The user doesn't care whether the website backend is in python or ruby, just whether it works well and does what they need. This can also include things like budget and time constraints, though those may also fall under technical requirements.

When adding to an established project, you may not need to do much technical requirements gathering- it just gets implemented within the current project structure, which sets the requirements. For newer projects or ones that have a more significant impact on existing projects, you will also want to know the technical constraints of your design. Is there a particular technology you need to use? Does it have a maximum response or uptime? What technical resources do I have to work with?

## Define "Done"

One of the most important aspects of defining requirements is understanding what "done" is. If you've fully scoped out the requirements, this may be a bit of a copy/paste situation, but it isn't the end. Particularly, it is helpful to agree on what is out of scope, aka what work you won't do.

The primary reason to do this is scope creep. Every project has it- things that must be added to the requirements after the fact. However, suppose you specify out-of-scope items upfront. In that case, you can either turn down the extra work or request further modifications to the schedule or priorities. "You can either have feature A or feature B, but not both without extending the timeline. We discussed this in the beginning, and you agreed to it."

## Organize the Results (Write It Down)

Often there is a bit of an "if it isn't written down, it doesn't exist" aspect to gathering requirements. Memories fade, priorities change, and miscommunications happen. Writing things down and, when possible, sharing the relevant parts with your users goes a long way towards avoiding those issues.

This might be just an email or Slack message. Often it needs to be logged in a ticketing or project management system. It might be formatted as a statement of work if someone is paying the bill for it externally. On larger internal projects, you may even write out a large business requirements document (and that's just as much fun as it sounds). Follow the freelancer's first rule- don't work without a contract.

More reading:

- [https://www.youtube.com/watch?v=tIATzLf-y04](https://www.youtube.com/watch?v=tIATzLf-y04)
- [https://www.verywellmind.com/what-is-active-listening-3024343](https://www.verywellmind.com/what-is-active-listening-3024343)
- [https://www.mindtools.com/CommSkll/ActiveListening.htm](https://www.mindtools.com/CommSkll/ActiveListening.htm)
- [https://praxent.com/blog/software-requirements-gathering-formula-success](https://praxent.com/blog/software-requirements-gathering-formula-success)
- [https://nmgtechnologies.com/blog/requirement-gathering-solve-biggest-problems-consulting.](https://nmgtechnologies.com/blog/requirement-gathering-solve-biggest-problems-consulting.)
