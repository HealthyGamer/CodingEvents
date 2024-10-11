# Surviving Stack Overflow

Stack Overflow might be one of the world's most significant repositories of coding knowledge, but it doesn't have a particularly positive reputation.   A quick search of "Is Stack Overflow toxic?" will return threads like this one on Quora, with very few people disagreeing with the concept. [https://www.quora.com/Is-Stack-Overflow-toxic](https://www.quora.com/Is-Stack-Overflow-toxic)

Do I personally think Stack Overflow is a toxic pit of terrible people? Not really. The site and its community have a lot of issues. People are still asking and answering questions, which disproves the idea that it's "impossible" to interact on the site. It isn't possible to view deleted posts with < 10k reputation, so browsing through recent posts won't give you a complete picture, but it does show that only some questions or answers get immediately downvoted and closed. If it were impossible to interact on the site, we wouldn't be able to find good answers there- someone asked those questions and answered them.

What I think is common is that the site has an extremely high learning curve, so the first interaction is usually the worst. Add that to the site's reputation, and most will reasonably write off ever posting again.

I don't have answers to the Stack Overflow problem- the likely result is that it will eventually be replaced by something better. Still, I can explain what is happening and some of the beneficial lessons I've learned from answering questions on the site. The main benefit I see from this is not in helping people interact on Stack Overflow. That's just a bonus. The same principles that make an excellent Stack question will also improve the likelihood you will get help in any space, including the HG Discord pocket communities.

I want to acknowledge plenty of plain bad behavior exists on the site- and I've seen it personally. However, I doubt the site's reputation comes entirely from a couple of bad actors or that those people are the cause of the majority of negative experiences. This may vary significantly by technology and may be more prevalent in areas I don't work in.

If you are wondering, as of writing this, I have just under 200 answers on Stack, with only one with a negative score.

## WTF Happened?

So how did we get here? Once you start reading the site's documentation on asking and answering questions, a clearer picture appears. A bit of a hot take, but I break it down into two main categories, which can be summed up this way: Stack has some stringent guidelines on what can be posted there, and those guidelines are different from what we are used to in other online spaces.

### It's Hard For Newbies to Get Started

If you are new to Stack Overflow or new to coding (or worse, both), it won't be easy to interact with people on the site. If you are new to the site and haven't had to focus on writing well-thought-out questions, you'll likely be asked to read the rules on asking questions, downvoted, and the question will be closed.

If you are new to software development, you may still need to learn how to research the problem and explain what you need help with. In that case, your question gets marked as duplicates, or you get asked to read the rules for answering questions.

### Digital Communication is Hard

In real life, we use body language and vocal tone to express how we feel about things. Text communication lacks both, and it's easy to misinterpret what someone means by what they say. In forums we often use words specifically to indicate tone that we wouldn't generally while speaking, as well as emojis.

Something that I often see missing from the Stack Overflow toxicity discussion is that they do not allow that extra context required to communicate things like tone in a digital context.

From the [Stack Overflow help center](https://stackoverflow.com/help/behavior):

> Thanks and other statements of appreciation are unnecessary, and, like other chitchat, should not be included.
If you use signatures, taglines, greetings, thanks, or other chitchat, they will be removed to reduce noise in the questions and answers.

What impact does removing this look like?

When I join a regular forum, I might make my first post something like,

> Hi! I'm new and excited to be here! I have a question about the fizzbuzz library. When I use it to call the foobar API, I get a 418 response. Any idea what is going on here?

>> *Welcome! It's hard to know what's going on without being able to reproduce it. Could you share a minimal example of the code you think is causing the issue?*

> Thanks for answering! Here's the information you requested:
>
> ~code example~

>> *I see it- you have a mistake in your method call and the foobar API thinks you are a bot, so it's sending a meme response. Here's how to fix it.*

How does the first interaction look with the Stack recommended way of interacting with people? Let's assume that both people involved have the same positive view of the other person. The question isn't up to Stack Overflow guidelines, but a new user may not realize that.

> I'm using the fizzbuzz library. When I call the foobar API, I get a 418 response. How do I resolve this?

>> *Please include the relevant code and read the Stack Overflow guidelines on how to ask questions (downvote, vote to close).*

Now let's reframe that again. How might I understand that Stack conversation if I believe everyone on Stack Overflow is toxic?

> Hey. I'm too lazy to write a decent question, so I want you to read my mind about what my code looks like and fix my problem for me.

>> *Read the rules, idiot.*

The third option may be the intended tone, but it's impossible to know based on the content in the second. If you are nervous, frustrated, believe that the community is toxic, or tend to default to a negative reading of what people have to say, you are going to struggle. Being mindful that you cannot assume tone in Stack Overflow interactions may significantly affect how you view those interactions.

## Asking Good Questions

Regardless of your forum, asking good questions is the best way to get valuable answers. The downside is that asking good questions is difficult and often takes quite a bit of time. Only some questions will require every element I'm going to mention, but it will give you an outline to build on.

No one owes you an answer. Sometimes you won't get one even if you ask the best quality question possible. By crafting a good question, you gain two things. First, you ensure you understand what you are asking (which might be enough for you to answer your own question). Second, you are respecting the time of the people sharing their knowledge for free.

### Side Note - Does Anybody Know About ~X~?

If you are in a forum for asking questions, skip this and ask your question. Read through [Don't Ask to Ask](https://dontasktoask.com/) if you want a full explanation. In short, you are asking people to commit to helping you without knowing what you need. Whatever "X" is, no one person will be able to answer 100% of questions about it. Asking your actual question will allow people to determine whether or not they can help you better. You already know the question, and if someone says yes, you'll need to type it out anyway, so doing this takes more time and makes it unlikely you will get a response.

### Clearly Explain the Problem

No one can help until they know what's wrong. The goal is to provide all the info needed to answer the question in a single chunk. The more times you go back and forth, the more likely the person on the other side of the conversation will wander off. It doesn't have to be perfect. The person might have questions about things you didn't know you needed to include, but people can see when you are trying to be as clear as possible.

If you need help explaining your problem, that's a problem you can ask about! Maybe not on Stack, but in most forums, stating that you are having an issue but are having trouble explaining what is going on is fine. The person answering now knows that the solution's first part is to ask clarifying questions before moving on to the main problem.

### Include Relevant Code

This might not apply or look different if you are here from outside the tech community. When code breaks, one of the best tools for helping someone else fix their code is replicating the problem on your own machine. If I ask someone why my drawing of a cat looks more like a dog, I need to show them the picture to get help with that.

This does not require sharing private code, but it can take effort. Breaking the code down into the simplest example possible that causes the problem is a fantastic way to find the problem on your own. It removes all the proprietary stuff, but it also eliminates a lot of things that could be causing the issue.

### Share What You've Already Tried

This is a good defense against the dreaded Stack Overflow "duplicate question" closure. Your question is far less likely to get closed for that reason if you've explained why your question is different before people start marking it that way. In a practical sense, this allows people helping you to skip steps you've already taken.

### Explain What You Are Trying to Accomplish

Explaining why you are trying to do something often isn't relevant to the question. It allows people to look at the situation overall and suggest a different option entirely. Suppose there is a different approach that would better fit your scenario. In that case, there's little need to resolve the specific error you are stuck on.

## Giving Useful Answers

How "good" your answer needs to be in this context depends on the forum you are posting on. Somewhere like Discord, where your answer will be forgotten by tomorrow, it's fine to give the minimum info for solving that person's problem. Places like Stack Overflow, where the ideal life and answer is measured in years, there are some additional steps to take to ensure it will last.

### Ask Followup Questions When Needed

When asking a question, people may give only some of the info you need to provide an answer. Often this occurs with newer devs who don't realize that information is relevant. Making assumptions might work, but it might not. Asking clarifying questions helps everyone involved understand just what is going on.

### Restate the Problem

With a perfect question, this isn't necessary, but most questions aren't perfect. If there are areas where you need clarification on what they are asking, restating the problem gives the asker a chance to correct your understanding before trying out the rest of the solution. This is also handy if your answer is only for specific scenarios, which might or not apply to someone reading your response.

### Include Links and Other Info When Relevant

This doesn't necessarily mean you must hunt down links to back up everything you said. If you looked up some info you used in your answer, it's helpful to throw that link into the chat so the asker can read more if they want. If you are in a long-lived forum like Stack Overflow, it's also good to summarize the links' information in your post. Years later, the link might break, and your answer will be useless unless you've outlined that info in your post.

