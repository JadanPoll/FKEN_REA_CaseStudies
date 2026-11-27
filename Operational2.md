# An Open-Ended Investigative Problem Book

Think of each folder as the title of an open-ended investigative problem book on the subject of that case study. Asymptotically we want it to be the authoritative and seminal book on the subject, but the kind of book that I simply can't put down. That is, it maximally activates and fires my neurons.

Imagine opening a book on robotics and coming across these questions:

- How does a robot distinguish two identical-looking hallways?
- If I move a robot elsewhere, can it find itself again?
- Why does a robot arm suddenly need huge joint speeds?
- What demonstration would convince me that I can build a useful robot?

I don't need to know much about robotics to be curious about these questions, imagine situations in which they might matter, or begin asking follow-up questions. And yet each of them could lead me to some very rich technical material, experiments, and other interesting problems I didn't even think to ask about.

Unlike an ordinary problem book, we needn't already know the answers or even the trajectory to the answers. We might discover that we were asking the wrong question, or learn something that opens up an entirely new landscape of problems. The book itself should develop as we investigate.

## The two directions

**Forward criterion:** If I have a question about how to do or go about XYZ, did we:

a. Save enough information so the answer is trivially inferable, especially with an LLM looking at the repo?

b. Save enough directional and source information and certificate so the answer is trivially investigable by an LLM, even if it has to redo a particular flow?

c. Save enough information so a.) and b.) compose, that is, the extended answer, precise answer and deeper answer can be recovered without having to redo the entire investigation?

Suppose we investigated a cardboard wing a month ago and now want to build a much larger plane. "The wing worked!" is of very little use. But if we preserved the structural arrangement, relevant dimensions, loading conditions, observations, limitations and references to the actual experiment, we can build upon what we learned. We don't need to have investigated the larger plane yet to have made that investigation considerably easier.

**Inverse criterion:** Questions and enough content should be preserved that the book is itself generative of the landscape of possible questions, curiosity and wonder. Simply from looking through it, we should learn so much and get a rich sense of the interesting and generative questions to ask. It should actively expand our conception of what is interesting, possible and even worth investigating.

Consider the question of making a cardboard wing rigid. What if we discovered that under certain conditions some deformation of the wing might actually be useful? Suddenly we're curious about something we didn't even think to ask. Why do we want rigidity in the first place? Could we design the way the wing deforms?

We don't have to claim that this will work. The interesting thing is that we've exposed a new landscape of questions worth investigating.

## The landscape of questions

Questions partition intellectual territory. Think of the book as a tree data structure and the questions as its nodes. A question should make sense as a chapter, subchapter or subsection title in that particular investigative problem book.

Asymptotically the chapter titular set of questions should endeavor to form a convex set. By this I particularly mean that adding the n + 1 question to the n-present questions should add dimensions not already represented, rather than simply reword or investigate another instance of the same problem. Of course we can do this recursively within a chapter or subchapter.

For example, four questions about different ways of making cardboard wings rigid might make for a rich subchapter, but a rather poor table of contents for the entire RC plane book. Where are the questions about achieving flight, propulsion, stability, control, construction and testing? Conversely, a chapter on cardboard wing structures might be quite poor if it doesn't expose the interesting variance within that particular territory.

Careful though! We aren't trying to make each individual question as general as possible, nor are we trying to generate every conceivable question. We're trying to develop a rich landscape of problems that we would actually care to investigate. An independent reading of a question should make its intellectual territory and the kind of book it belongs to clear or recoverable.

## The kind of questions we actually care about

A hyper-specific question that doesn't expose a landscape of thinking or ideas is just technical slop at the wrong level of the tree. A vague, generic question that could easily appear in a different book is just question-generating slop. Neither should be confused with a concrete, curiosity-led problem.

Consider these three possible questions in our cardboard RC plane book:

| Question | Why or why not? |
| --- | --- |
| How do we optimize structural performance? | Too generic. What am I even supposed to imagine or be curious about? |
| Why did the third rib deform by 2 mm during test 7? | Potentially interesting technical material under a question, but not a particularly generative chapter title. |
| How can I make a cardboard wing strong enough to fly without making it too heavy? | I can imagine the problem, why it matters and several directions to investigate, even if I don't know much about aircraft. |

### Negative case — generalizing away the curiosity

An LLM previously interpreted the original operational criteria and recommended replacing perfectly good questions with the following abstractions:

| Positive case — preserve | Negative case — replacement |
| --- | --- |
| How does a robot distinguish two identical-looking hallways? | How can robots resolve ambiguity in their observations? |
| If I move a robot elsewhere, can it find itself again? | How can robots recover from incorrect state estimates? |
| What demonstration would convince me that I can build a useful robot? | What capabilities and evidence establish robotic autonomy? |
| Why does a robot arm suddenly need huge joint speeds? | What determines the limits of a robot's achievable motion? |

The problem isn't simply that the questions on the right are dry or dull. They provide high friction for natural application or situation-based recognition of the problem and/or its solution, and are decidedly the opposite of curiosity-led or naturally generative follow-up questions.

Suppose I'm building a robot and it gets confused in two identical-looking hallways. Having encountered the question on the left, I might immediately recognize the problem and recall some things I learned about it. With the question on the right I might need to already understand observational ambiguity just to recognize that it's relevant.

What if the robot remembers how it got there? What if it deliberately moves somewhere from which it could distinguish the two hallways? These are natural questions one could ask before even knowing the words localization, perceptual aliasing or active perception.

**Generalize the territory, not away from the thing that made us curious.** Concrete doesn't mean hyperspecific. If the original question is already a good problem at its level of the tree, preserve it. Put the technical abstractions in the glossary and content, or introduce a genuinely interesting parent question when needed. Don't bury a perfectly good curiosity as a search alias just to make the tree look more general.

## The glossary

The questions partition the intellectual territory and the glossary terms populate it and fill in the nodes. The glossary should enable someone to rapidly estimate:

- **Breadth:** What kinds of ideas and problems might this book contain?
- **Depth:** How far into those ideas could I investigate?
- **Variance:** What different mechanisms, approaches or dimensions are represented?
- **Fill:** From the book level, do the terms adequately color in all chapter-level ideas; from a chapter, all subchapter-level ideas; from an idea, that particular idea?
- **Novelty:** Does giving the glossary a once-over expose me to things I didn't know existed?
- **Recoverability:** Can vague interests or curiosities, if followed through, lead to precise technical material, even if that material is directional?

Imagine trying to find a location simply by describing what you believe it and its surrounding environment should look like. You shouldn't need to happen to know the name of the location to eventually find it. Similarly, I might be curious about why a plane keeps moving its nose up and down even though I'm not moving the controls. I shouldn't have to know the words pitch oscillation, longitudinal stability or phugoid beforehand to recover the relevant landscape.

A glossary with hundreds of structural mechanics terms might have remarkable depth in one region of our book and very poor fill across the rest of it. Conversely, an interesting cluster of glossary terms might expose a whole region of the question landscape we haven't thought to investigate yet. Terms needn't wait for a corresponding answered question to be useful.

## How do we tell if we've done a good job?

Give someone the book, perhaps just its chapter and subchapter titles and glossary to begin with. Can they get a rich sense of the landscape of things they could investigate? Are they unable to put it down? Can they recognize something relevant to a situation they're actually in without already knowing the precise terminology? Can they follow a vague curiosity to interesting and precise material, and can another investigator recover the evidence or continue the investigation?

And after reading the book, when they encounter a different situation in the world, are they more likely to recognize an interesting problem, a possible solution or an opportunity to apply what they've learned?

This is what the forward and inverse criteria, variance, fill and the rest of our criteria are trying to accomplish. Merely classifying questions, making them more abstract, or increasing their number doesn't establish that we've accomplished any of these things.

For the more extensive exposition and calibration examples, see [OPERATIONAL.md](OPERATIONAL.md).
