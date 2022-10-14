# What is Computer Science?

Even though software engineering majors are available, why do developers get degrees in "computer science" instead of programming? Why do we continue to emphasize this topic even though most professional devs will agree that a CS degree teaches very little about the actual day-to-day job of a programmer? In some ways, it is similar to the relationship between music theory and music composition. You can write music without formally studying music theory, but you will still use it daily. The theory becomes a tool for musicians to improve the quality of their music. It doesn't create music by itself.

## What Books to Get for Self-Study CS?

If you ask a programmer which are the best books to buy for self-taught devs (or to create a foundation library), you will get very different answers. While it doesn't exactly match the list I ended up putting together, this list may be a reasonable starting point: [https://teachyourselfcs.com/](https://teachyourselfcs.com/). Keep in mind these are not inexpensive, and all the information is available freely online.

## Music Theory

For this example, we will focus on the European musical tradition (it's simply the one I am most familiar with). There are tons of other styles of music, each with its theory and practice.

When we break this type of music down, it comes down to seven notes, which we letter A through G (we repeat the first to make the eight notes of a scale). An additional five notes fall between some of those seven, and those twelve make up almost all of the music in the European tradition for the past 400 years. Some pieces are part of this tradition that don't use those twelve notes, but they are usually done to break those fundamentals intentionally and, in that way, are still based on them.

So if all this music is based on just 12 notes, why go to school for it? Why do we have advanced degrees with people spending their entire lives studying something so simple? We take those twelve notes and build scales, chords, phrases, rhythms, and structures. We play the notes on different instruments, sing lyrics, and listen in various performance venues. It's all about how we leverage those 12 notes, not so much the notes themselves. The study of music theory is about how to utilize all these tools.

If you want an example of how something so simple can be expanded into a massive variety of music, Axis of Awesome had a joke go viral about how many popular songs are based on 4 chords in the same progression. 

[![Axis of Awesome Video](https://img.youtube.com/vi/5pidokakU4I/0.jpg)](https://www.youtube.com/watch?v=5pidokakU4I)

When discussing computer science, we don't stop at bits, ones and zeros. Instead, we talk about how to use them in the context of programming to create all the technology we have today. This complexity is why "The Art of Computer Programming," one of the most famous works in programming, was first started in 1962 and is a little over half done and will probably never be finished.

## So What is Computer Science?

"The discipline of computer science includes the study of algorithms and data structures, computer and network design, modeling data and information processes, and artificial intelligence."
[Encyclopedia Britannica](https://www.britannica.com/science/computer-science)
(I'm personally skipping AI as it is a specific application of the other elements)

### Algorithms

When we talk about algorithms as programmers, we usually think of LeetCode or HackerRank. The dreaded whiteboard interview where we code from memory some algorithm we'll never write in our daily jobs. This is because we have moved past that point in programming- why implement a sorting algorithm when you can have the person or team who created the language already do it for you? In fact, it is usually bad practice to implement them yourself, as the language team will optimize the algorithm for their underlying systems.

So why do we care about learning these basic algorithms we won't ever write outside of an interview? Because they teach us how to approach writing algorithms that aren't built into a language. We might never discuss Big-O notation in real life. Still, I might be presented with a situation where I must choose between two options- running two operations in a single loop over a collection or splitting them and looping twice. The first (to me) feels like it should be more efficient- there is some overhead with building and executing the loop, but the second would be more readable.

Which one should I pick? While the first feels faster, they both have an O(n) runtime, so I would typically select the more readable, and probably more maintainable, second option.

O(n) just means that the increase in runtime is linear- if it takes 1 millisecond per item in my list, then 10 items would take 10 milliseconds, 100 would take 100 ms, etc.

![Johny Depp bad code](https://i.imgur.com/utHUSHq.jpeg)

### Data Structures

Data structures determine how we store and access data in memory or on disk. Here again, we see the dreaded "reverse a linked list" on sites like LeetCode, which we rarely use on the job.

This includes arrays, linked lists, stacks, queues, hash tables, trees, heaps, and graphs. While there are others, those are the ones that make the "every dev should know these" list. Some we use more than others and some may be built into the language but not really exposed to the developer. Whereas you can be a great dev without understanding big-O notation, you won't get very far if you don't know what an array is. The basics of this topic really are a requirement in coding.

![search trees](https://i.imgur.com/bN5992U.png)

### Computer Design

Unsurprisingly, computer design is about the hardware inside our computers actually works. In my experience, these courses often focus quite a bit on the architecture surrounding CPUs and memory since those systems have several layers designed to help with speed and processes like multithreading.

The closer to the metal you work, the more you will use this- If you are working on embedded systems or OS kernels, you need to understand this exceptionally well. However, most developers will run into challenges directly related to hardware limitations at some point.

A great example of this is floats. There are several ways to store numbers, but float is usually the default. The problem is that you might put the number eight into your variable and get out 7.99999999999999. Some languages handle this better than others, but they all have this feature. It's because of how floats are stored in binary- they can't be exact. So instead of sending the language devs a nasty email, we use rounding, types like decimals, or let the language fix it for us to ensure 1 == 1 doesn't randomly come out false.

![CPU is a rock](https://i.imgur.com/p0a81f8.jpg)

### Network Design

While computer design is more focused on hardware, I probably won't learn how to turn a raspberry pi into a router in a network design class. Instead, I'll learn how networks function and how to take a list of requirements and turn them into an implementation plan.

How useful is this one in the real world? We rarely build a system that doesn't have network connectivity. While you don't necessarily need to know every detail of how networking functions, a basic idea of protocols like TCP and UDP will go a long way towards understanding how different issues should be handled and which protocols to design your system around.

![TCO vs UDP joke](https://i.imgur.com/JpyKklY.jpeg)

### Data Modeling

Data structures explain how we store groups of data together. Data modeling is how we split data into different groups. Like networking, because most software connects to the internet, data modeling is essential because most programs work with persistent storage, with databases being the most common. Even if everything is in memory, object-oriented programing is the norm, which necessitates breaking our information into various classes to structure it in a meaningful way.

![Cloud security and bad data](https://cdn-cybersecurity.att.com/blog-content/cloud_joke_2.png)

### Information Processes

Unsurprisingly, information processing refers to how we process information in our systems. :) This is one of the main reasons code exists- a program that doesn't involve this concept isn't much of a program, and I'm not sure you could even write one. At a basic level, we start with CRUD (create, read, update, delete) as the basic operations we perform on data. Things like business or domain logic also fall into this category. Rules on what happens to the data between the user and the database.

![Clients vs AI](https://i.imgur.com/Gc6p9vu.jpeg)