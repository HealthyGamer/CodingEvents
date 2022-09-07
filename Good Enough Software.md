# Creating "Good Enough" Software

- Why do we care?
- Working With Users
  - Quality is a Requirements Issue
  - Early Feedback Results In Better Products
- Working On Yourself
  - Optimization Is a Trap
  - "Practice Makes Perfect"
  - Trust Yourself
- Steps For Good Enough Software

## Why?

- Even if we did manage to create "perfect" software, we are still relying on underlying systems that can and will fail. A pacemaker needs the best software we can write, but it's still dependent on a battery that will last 5-15 years.
- We can't anticipate every issue, even when, in hindsight, it seems obvious. In 1999 NASA lost a $125 million Mars orbiter because engineers forgot to convert some measurements from imperial to metric.
- Big companies mess up all the time- we've all dealt with issues from Facebook, Google, Amazon, or Microsoft. Are you setting a higher standard for yourself than companies with nearly unlimited resources?

## Working With Users

### Quality is a Requirements Issue

- Higher quality requires more time and money to produce. Time spent on a feature should balance the cost to build it versus the value it delivers.
- People understand this concept- we do these calculations every time we buy something. While non-technical stakeholders may not understand the technical requirements to produce better software, they know this is necessary. Take a lesson from Star Trek engineers- under-promise and over-deliver if needed.

### Early Feedback Creates Better Results

- People often struggle to explain what they need. However, once they have the result, they are pretty good at explaining what's wrong with it. Getting something to them quickly makes requirements gathering much easier.
- Often waiting until something is done results in a lot of effort put in the wrong direction. When we design software, we try to think about the user's experience, but we can't always do this properly for every type of user that might need to use our software. Let them tell you what they need.

## Work On Yourself

### Understand Optimization is a Trap

- CPU time is less valuable than developer time. If I spend a few hours on reducing the company's server costs by $10/month, it will take around a year (if not more) to recoup the cost of my time.
- It can be challenging to predict where bottlenecks will be. A database query that consumes a lot of resources may not use the most overall. A query that consumes quite a bit less can cause issues if it runs often enough.
- Learn the conventions for the language you are working in. Many of these exist to help you balance your time against the weaknesses of that language's interpreter.

### "Practice Makes Perfect" Is Kinda True

- Small, throwaway projects and prototypes help us explore new ideas.
- An excellent skill to learn is how to throw away code completely. "Good enough" can mean that the code isn't perfectly written or has a bug or two, or it can mean that it's done its job and it's time to walk away. Project graveyards aren't always a bad thing.
- These investments pay off when we write software that we do need to keep long-term. We can spend the same time and money while producing better software if we've worked on these projects.

### Trust Yourself to be Able to Handle Issues

- Devs make mistakes all the time. While coding, little mistakes happen constantly. It's a normal part of dev that we learn to deal with.
- Once you learn to debug software, the process is almost the same regardless of whether the code has been released or not.
- I don't know a single dev that has been entirely unable to deal with a production issue- you are capable of more than you think.

## Steps For "Good Enough" Software

1. Get the code working. You can consider things like existing architecture, but don't worry too much about quality. Basically a small-scale prototype.
2. (Part 1) Think about edge cases, try to spot bugs, and tightly-coupled code.
3. (Part 2) Get feedback from users.
4. Prioritize your to do list.
5. Work on the items in order of priority. You may even leave some low priority items out completely.
6. Go back to step 2.
