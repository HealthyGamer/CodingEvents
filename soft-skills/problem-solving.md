# Problem-Solving as Software Devs

- Attitude
  - Responsibility
  - Accepting that Problems Are Normal
  - Most (Coding) Problems Have a Solution
  - Old Solutions Don't Always Work for New Problems
- Getting to a Solution
  - Understand the Problem
    - Talk to Your Users
    - Read the &!*#ing Error Message
    - Rubber Duck Debugging
  - Find and Evaluate Solutions
    - Leverage Other People
    - Your Problem Probably Isn't as Unique as You Think
    - Break Bigger Problems Down Into Smaller Chunks
      - Combining Solutions Together
    - Evaluate Possible Solutions
    - Reflect on the Results
- Problem Solving Takes Practice, and It Can Be Learned

Every article on problem-solving is apparently required to start with the quote "All life is problem-solving" from Karl Popper, so let's get that out of the way. While that may be true, I'm narrowing this down to how we handle problems within tech- how to approach them internally and some high-level ways to actually solve them.

## Attitude

What can get in the way of approaching a given problem comes from what we discussed [last time](https://github.com/HealthyGamer/CodingEvents/blob/main/Debugging/Leveraging%20EQ%20in%20Programming.md)- the emotions that can come from confronting an issue. However, we don't have to stick with whatever our initial reaction to the situation is. A big part of why having EQ (emotional intelligence) is valuable within the context of problem-solving is that it allows us to move through our initial reaction and into a better space for addressing the problem. We want to look at problems as a challenge that will enable us to grow and improve- what is often referred to as a growth mindset.

### Responsibility

Responsibility in this context isn't about admitting fault. Blame isn't generally applicable when facing a problem. If it happens at all, it should be considered after the current issue is resolved. Responsibility in this context is about committing yourself to work towards a solution. It's tough to stay on task when trying to solve something that is someone else's responsibility.

### Accepting that Problems Are Normal

An ideal work day or coding session is not one where you don't face any problems. It's one where the issues are ones you can tackle on your own or with help. Many of us have worked in spaces where an impossible amount of work was expected. It's an overwhelming situation that is difficult, if not impossible, to thrive in. Understanding that problems are going to be part of your day

### Most (Coding) Problems Have a Solution

We can do a lot with the tech available to us. In most cases, the limit on what we can do is on the human side, not the technology side. The reason a solution doesn't exist is rarely that what we want is impossible, but because it would take too much time or money to implement.

### Old Solutions Don't Always Work for New Problems

We tend to go for the most comfortable solution, not the most effective one. Often that comfort comes from the solution being something we have done before or is something like an industry standard. We see this in software development when devs treat things like design patterns as rules instead of a path that leads to an effective solution. We want to build on what knowledge is already available, not mindlessly replicate it.

## Getting to a Solution

We can often skip a lot of this for something like a typo. The bigger the scale or impact of the problem, the more we need a good process. This is why junior devs are rarely assigned things like system architecture projects. They are still learning the process of tackling technical problems, so the solutions they create are seldom the best available.

### Understand the Problem

If we don't actually understand what has gone wrong, it's hard to solve the problem. With production bugs or feature design, this often happens by talking to users to get details around what they want. Since this is part of a series about debugging, we are going to skip that and cover it at a later date.

#### Read the &!*#ing Error Message

In modern software dev, the systems we work on tell us a lot about what went wrong. Many languages have some common useless messages ("Object reference not set to an instance of an object" is common in C#), but even those can hint at what is going on. That plus the stack trace (more about that next time) is a bit like the context we can get from talking to a user. The system is doing its best to explain the problem.

#### Rubber Duck Debugging

As soon as I mentioned we would talk about debugging chat started to fill with talk about rubber ducks. There is a good reason for this- it's a bit of software development tradition, and for a good reason.

A bit of a history lesson on why, specifically a rubber duck. The concept originated in one of the most famous books in software dev, The Pragmatic Programmer by David Thomas and Andrew Hunt, written back in 2000, which is also the book that is "inspiring" a lot of the topics we've been covering lately. According to the footnotes, Andrew Hunt was first introduced to this concept by a coworker, Greg Pugh, who often carried around a duck while working.

Basically, the idea is that we can often learn more about a problem simply by explaining it to someone else.

>A very simple but particularly useful technique for finding the cause of a problem is simply to explain it to someone else. The other person should look over your shoulder at the screen, and nod their head constantly (like a rubber duck bobbing up and down in a bathtub). They do not need to say a word; the simple act of explaining, step by step, what the code is supposed to do often causes the problem to leap off the screen and announce itself.

The argument is that because the key is the act of explaining, not anything the other person does, the "other person" doesn't have to be a person. It can be anything- a plant, your pet, or you can follow tradition and invest in a rubber duck.

### Find and Evaluate Solutions

#### Leverage Other People

In a healthy team, it's normal to ask for help. We also have huge communities within the tech industry dedicated to sharing knowledge and helping to find solutions. How to do that is out of scope for this topic, but learning how and when to ask for help makes you a significantly more effective dev. Some use the term "code blindness" for times when you've stared at something so long you simply can't see the flaws anymore. This is also why pair and mob programming are so valuable.

#### Your Problem Probably Isn't as Unique as You Think

There's a reason why Stack Overflow is one of the most popular sites on the web and definitely within the tech industry. It's because the problems we face daily are ones that many other people have faced as well. We joke in the industry that software dev has gotten to a point where we are just copying/pasting code from Stack and similar sites instead of writing stuff for ourselves.

![meme book "Copying and Pasting from Stack Overflow"](https://i.imgur.com/SZPjHwz.jpeg)

The key here is to evaluate the proposed solution and work through whether or not it actually fits your situation. Usually, it will take at least a little bit of customization to get it to fit your code. In some cases, all it will do is help lead you to a solution or rule out a possibility.

#### Break Bigger Problems Down Into Smaller Chunks

Most debugging issues won't be big enough to use this particular technique, but it is a good one to have on hand. As problems get more significant, it becomes likely that a single, overall solution will work. Instead, we must break the problem into individual components and tackle each separately. Two great examples of this are in estimation and in architecture design.

##### Combining Solutions Together

Of course, once we've solved each piece, we need to get them all to work together. This is another set of problems all on its own and where the creative part of software dev can really come into play.

If you want a low-pressure way to practice pulling together things that don't have anything to do with each other on the surface. This is actually where PerfectlyPanda comes from. Go find a [random word generator](https://randomwordgenerator.com/). Have it create nouns and adjectives and pick two that wouldn't usually go together. Try to get them to fit. It might be that they sound good together, that they are opposites, or that it creates a fun mental picture. Sometimes they just don't fit, which is a viable conclusion. For an extra stretch, that combo is now your new startup or website. What does it do?

#### Evaluate Possible Solutions

Sometimes the correct solution is obvious, but it's also common to be in a situation where multiple options are viable on the surface. In that case, we need to dig deeper.

- What is the cost of each option?
- How will it perform in the future as the project grows?
- What are the potential risks with it?

This exercise will usually let you narrow things down to two or three options if it doesn't highlight a specific one. Depending on the situation, this might be where you bring the options to someone above you in management and let them choose, or it might be close enough that you just pick the one you like the best.

### Implement the Solution

Here's a Panda original meme for you:

![Coding is like skydiving: Lots of careful prep, but eventually you have to say, "What's the worst that could happen?" and jump.](../images/codingskydiving.png)

There's [a video](https://www.youtube.com/watch?v=-YEoDAu1ET0&t=2706s) where Dr. K talks about the programmer mindset and how we tend to have this weird YOLO approach to things. That things are going to be messed up, but let's jump in and go for it anyway. It makes me laugh so hard because of just how true it is. I've been trying to figure out how to explain it for a long time, and this is the best I've come up with.

The thing is, YOLO implies recklessness, so I don't think it's a good metaphor on its own. This is why I believe skydiving might be a better choice- many things could go wrong, so we work to understand and minimize those risks. This whole process we've been talking about is that preparation.

The thing is, at a certain point, you just have to jump. Your solution probably isn't perfect, and things could happen outside your control. You could swallow a bug, drop your phone, or get caught in a tree. Sometimes it's even possible that the main parachute won't open, and you need to use the backup. And, yes, sometimes the software we write can cause serious harm to people if we mess it up.

It's also important to remember that sometimes the worst thing we can do is not act. Sometimes the engine is on fire, and we can jump or go down with the plane. It doesn't make jumping any easier. It just makes it more necessary. Creating a new startup and dealing with a production outage both have risks, but they also have very different consequences.

### Reflect on the Results

While old problems don't always fix today's problems, they can help. 

- What worked in your solution?
- What didn't work?
- What would you change next time?

These questions are essential in improving your ability to solve similar problems in the future.

## Problem Solving Takes Practice, and It Can Be Learned

People don't know how to debug code when they first start. They don't know how to design a program so that it is easy to maintain. These are skills we learn as developers over time. Unfortunately, this can be an extremely frustrating process. It's essential to be patient with yourself and ask for help when you need it.
