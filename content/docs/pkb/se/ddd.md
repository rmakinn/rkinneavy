---
title: "DDD"
draft: true
bookCollapseSection: true
---

# Data-Oriented Design

In essence, data-oriented design is the practice of designing software by developing transformations for well-formed data where the criteria for well-formed is guided by the target hardware and the patterns and types of transforms that need to operate on it. Sometimes the data isn't well defined, and sometimes the hardware is equally evasive, but in most cases a good background of hardware appreciation can help out almost every software project.

---

Questions:

Consider how your data is being influenced by what it's called. Consider the possibility that the proximity of other data can influence the meaning of your data, and in doing so, trap it in a model that inhibits flexibility. For the consideration of the first principle, data is not the problem domain, it's worth thinking about the following items.

What is tying your data together, is it a concept or implied meaning?
Is your data layout defined by a single interpretation from a single point of view?
Think about how the data could be reinterpreted and cut along those lines.
What is it about the data that makes it uniquely important?
You are not targeting an unknown device with unknowable characteristics. Know your data, and know your target hardware. To some extent, understand how much each stream of data matters, and who is consuming it. Understand the cost and potential value of improvements. Access patterns matter, as you cannot hit the cache if you're accessing things in a burst, then not touching them again for a whole cycle of the application. For the consideration of the second principle, data is the type, frequency, quantity, shape, and probability, it's worth thinking about the following items.

What is the smallest unit of memory on your target platform?1.6
When you read data, how much of it are you using?
How often do you need the data? Is it once, or a thousand times a frame?
How do you access the data? At random, or in a burst?
Are you always modifying the data, or just reading it? Are you modifying all of it?
Who does the data matter to, and what about it matters?
Find out the quality constraints of your solutions, in terms of bandwidth and latency.
What information do you have that isn't in the data per-se? What is implicit?
---

Principle: Data is not the problem domain. Consider how many games are objects in worldspace at grid coordinates, rather than actually being driven by a grid. One ends up duplicating the data as far as necessary to navigate concepts with data attached, with all the myriad overlaid abstractions required by objects. 

The data-oriented approach gives up some of the human readability by leaving the problem domain in the design document, bringing elements of constraints and expectations into the transforms, but stops the machine from having to handle human concepts at any data level by just that same action.

...

When a class owns some data, it gives that data a context which can sometimes limit the ability to reuse the data or understand the impact of operations upon it. Adding functions to a context can bring in further data, which quickly leads to classes containing many different pieces of data that are unrelated in themselves, but need to be in the same class because an operation required a context and the context required more data for other reasons such as for other related operations [...]

We see this kind of contextual linkage all the time in the real world, and we manage the complexity very well in conversation, but as soon as we start putting these contexts down in hard terms we connect them together and make them brittle

...

When we consider the data from the data-oriented design point of view, data is mere facts that can be interpreted in whatever way necessary to get the output data in the format it needs to be. We only care about what transforms we do, and where the data ends up. In practice, when you discard meanings from data, you also reduce the chance of tangling the facts with their contexts, and thus you also reduce the likelihood of mixing unrelated data just for the sake of an operation or two.

Second principle: Data is the type, frequency, quantity, shape and probability

A data-oriented approach to code design considers the change in design through the lens of understanding the change in the meaning of the data. The data-oriented approach to design also allows for change to the code when the source of data changes, unlike the encapsulated internal state manipulations of the object-oriented approach. In general, data-oriented design handles change better as pieces of data and transforms can be more simply coupled and decoupled than objects can be mutated and reused.
