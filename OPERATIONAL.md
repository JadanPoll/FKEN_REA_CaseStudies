# Operational criteria for case-study books

Folder and question quality should be evaluated on this basis:
## Forward Criterion:

If I have a question about how to do or go about XYZ. Did we:

- **a.** save enough information to the answer is trivially inferable, especially with an LLM looking at the rep
- **b.** save enough directional and source information and certificate so the answer is trivially investigate by an LLM, even if it has to redo a particular flow.
- **c.** save enough directional information so a.) and b.) compose, that is the extended answer, precise answer and deeper answer can be trivially recovered by an LLM, even if it has to redo a particular flow such as a precise websearch(egg: cause we left a clear link there) or redebug something cause it might have contains sensitive stuff we couldn’t put in this repo.

## Question quality and intellectual territory

Asymptoticaly we should be able to answer and get the sense of the landscape of any general question we might ask on a particular folder, the repo should at the very least contain enough data for that. When it comes to the complexity of the questions, it should be the kind that you might see as a topic, subtopic or subsection header, Think of folders as books, in fact, the folder is the title of the case study book that could be written on the subject ‘FOlDER_NAME’ questions should be specific and rich enough to the book but worded readably enough that it’s conceivable it would be one of CRITERION A:

- **a.** Chapter title
- **b.** Subchapter title
- **c.** Subsection title

### Variance and recursive coverage

Asymptotically we aim to be the authoritative and seminal “Book” on this subject and hence questions should endeavor to form a convex set. By this we particularly mean the chapter titular set of questions. They should also have variance, when adding the n + 1 question to the convex set of n-present titular questions should “add dimensions” not already represented by the set of n questions. Of course this can be done recursively, for b. and c. take a titular question, and form its convex set of “subchapter titular” questions.

If it doesn’t fulfill either of these criterion it means the question is slop, or worded to complex or too hyperspecific. In other words, an LLM that doesn’t speak in human vernacular likely write it and couldn’t care about actual generative or readable quality. If you want hyper specificity it should be in the data under the question, not the question itself. 

### CRITERION B:

an independent reading of the question makes it clear or recoverable what kind of ‘book’ it belong to, if it doesn’t fulfill this particular criterion it means the question is too generic to the point it might be hopeless dull.

## Inverse Criterion:

Questions and enough content should be preserved that it is itself generative of the landscape of possible questions, curiosity and wonder. That is simply from looking through you learn so much and get a rich sense of the interesting and generative questions to ask

Exploring it should actively expand our conception of what is interesting, possible and even worth investigating. It should educate you or clue you in on things you didn’t even think to ask. To thst end, part of actually evaluating this is

- **a.** variance
- **b.** unique dimensions offered

## The glossary

glossary plays a critical role in fulfilling this but so do questions, especially when an LLM is figuring out what a good question would be. Glossaries should enable me to 

- **a.** quickly estimate how seminal or authoritatively comprehensive the ‘book’ is.
- **b.** excite me about twist info the book might contain if I was giving it a once over(gives me a landscape of all the dimensions, and spectral variance or set of terms within any particular dimension of the book.
- **c.** enable me, through pseudo-deterministic semantics, to locate any relevant content in the book even if I have a sort of vague idea bout what I want to look into, say ‘security’ or “payment” systems.

### Breadth, depth, variance, fill, novelty and recoverability

In other words the glossary should enable someone to rapidly estimate breadth, depth, variance and fill(from the book level, the terms adequately color in all chapter level ideas, from a chapter, the terms adequately color in all Subchapter level ideas, from an idea, the terms adequately color in that particular idea), novelty and recoverability(can vague interests or curiosities if followed through lead to precise technical material, even if the material is directional)

### Navigating intellectual territory

Think of it like this, question partition intellectual territory and books as if it were a tree data structure, and the questions were nodes, 
glossary terms populate it and fill in the nodes as well. Glossary terms are like finding a location simply by describing what you believe it should look like and what you believe the surrounding environment should look like. You shouldn’t need to happen to know the precise terms to be able to eventually navigate to what or what you want.

## The meta rule

Again, it should make sense if the folder was a title of the case study book. This prevents the accumulation on :slop that is simply asking questions just to ask. I do have a meta rule for this
**The ‘book’ should asymptotically be in such a way that I simply can’t out it down.** That is it maximally activates and fires my neurons. This can be done recursively of course, on a, b, and c in the earlier specified criterion A., am I unable to put the chapter titular questions down, within a chapter titular question, am I unable to put its Subchapter titular questions down etc.

### Two opposing forms of slop

**A hyper-specific question** that does not expose a landscape of thinking or ideas and is not generating and so is just technical slop. If you find it relevant identify the actual big picture question and persist the more technical important or nuanced stuff in the content under it

**A vague, generic question** that could easily appear in a ‘Book’ with a different title is just question-generating slop, in other words asking just to ask. Question like this offer no navigational usefulness or excitement

## A failure mode — generalizing away the curiosity

Suppose we're developing a book on robotics and have the question **"How does a robot distinguish two identical-looking hallways?"**

An LLM might recognize that this belongs to the larger landscape of problems concerning ambiguity in observations, and replace the question with "How can robots resolve ambiguity in their observations?"

But notice what we've just lost. The first question lets someone who knows almost nothing about robotics imagine a robot looking down two identical hallways and wonder how it could possibly know where it was. The second almost presupposes that the reader already understands why observational ambiguity is interesting.

We should distinguish **the generality of the territory a question opens up from the generality of the language we use to enter that territory**. The original question might very well be a subchapter title, and a particularly good one at that. We can expose the larger landscape by connecting it to other questions, rather than by replacing it with an abstract description of the landscape.

| A question worth preserving | An unnecessarily abstract replacement |
| --- | --- |
| How does a robot distinguish two identical-looking hallways? | How can robots resolve ambiguity in their observations? |
| If I move a robot elsewhere, can it find itself again? | How can robots recover from incorrect state estimates? |
| What demonstration would convince me that I can build a useful robot? | What capabilities and evidence establish robotic autonomy? |
| Why does a robot arm suddenly need huge joint speeds? | What determines the limits of a robot's achievable motion? |

The questions on the right can be useful descriptions of a technical territory, although some also change the spirit or scope of the question on the left. They aren't necessarily improvements to the questions a person actually reads. In fact, the glossary can help us make precisely these connections without requiring us to sacrifice the original questions.

Consider the RC plane example in RSM. If we replaced "Can I make an RC plane out of cardboard?" with "What are the feasibility constraints of unconventional aircraft materials?", we might have technically generalized the question while making someone considerably less interested in investigating it.

Careful though! A concrete question isn't necessarily a hyperspecific question. Two identical-looking hallways could be an instance of a much richer problem; the exact value of a parameter in one particular experiment might not be. We should distinguish between details that help us imagine the problem and details that arbitrarily restrict what we can learn from it.

**Generalize the underlying landscape, not away from the thing that made us curious in the first place.** If the original question is already readable, distinctive, and generative at its level of the tree, why change it? If we need a larger parent question, can we introduce one that is just as interesting, and preserve the original as a visible constituent question rather than bury it in a search alias?

A useful test is to imagine someone browsing the chapter and subsection titles without the glossary, answers, or technical explanations in front of them. Can they imagine what the questions are about? Do they see why a question might matter before knowing the relevant terminology? Would they want to investigate something they hadn't even thought to ask? Then check whether that curiosity can actually lead to the larger technical landscape and its evidence. Merely having an LLM recognize that two questions are semantically related is not sufficient.

## Examples — what would applying these criteria actually look like?

The following are calibration examples, in the spirit of the cardboard RC plane example in [RSM-02.08](https://github.com/JadanPoll/Learning_Visualizations_Taxonomy/blob/main/Navigationals/The_Richer_Scientific_Method.md). Suppose we're developing a book called **Building RC planes out of cardboard**. We can use the same prospective book to understand several of the criteria, rather than invent a completely different example for each one.

### 1. Forward criterion — what can another investigator do with what we've left behind?

Suppose a month ago we investigated whether a particular cardboard wing could withstand the loads we expected during flight. A month later we want to build a much larger plane and wonder whether we could use the same structural arrangement.

Consider a few possible things we could have left behind:

- **A.** "The wing worked!" We don't know the dimensions of the wing, what we meant by worked, what we did to establish that it worked, or even whether we flew the plane or merely loaded the wing on a bench.
- **B.** A video of the experiment and a folder containing a great many measurements, with no indication of which observations were relevant to which question or what we actually learned. We have evidence, but someone may have to do much of the investigation again to make use of it.
- **C.** An explanation of the structural arrangement, what loading conditions we investigated, what happened, what seemed to limit its performance, and references to the relevant measurements or experiment. If we want to know whether a plane of roughly the same size could use the arrangement, much of the answer may already be inferable (forward criterion a.).
- **D.** Alongside C, we preserved the relevant dimensions, material properties, way we applied the loads, what to measure and where the design might cease to work. Perhaps we didn't investigate larger wings at all. But another investigator can now reproduce the experiment under a different loading condition or use our previous results to develop a more useful model for the larger plane (b. and c.).

Notice that D doesn't require us to have answered the question about the larger plane a month ago. It requires that what we learned then and what we might investigate now are able to compose.

The same thing happens when investigating a software product. Saying "the app uses a clever recovery mechanism" is not particularly useful. Preserving what triggers recovery, what state it tries to recover, and which source and observations led us to that understanding may be enough to answer several future questions. If we can't preserve the original material, can we at least preserve the trajectory by which someone could recover the relevant evidence?

Careful though! An experiment that established that a wing could support a particular static load doesn't establish that the aircraft flies safely. Similarly, successfully reading a function in the source doesn't establish that the corresponding mechanism was exercised at runtime. We should preserve what the certificate actually certifies.

### 2. Criteria A and B — at what resolution should a question live?

Imagine opening our book and encountering the following titles:

| Possible title | What's wrong with it, or what makes it useful? |
| --- | --- |
| How do things work? | This could be in almost any book. It tells us virtually nothing about where we're going or why we should go there. |
| Why did the third cardboard rib deform by 2 mm during test 7? | This might be a perfectly good question during an experiment. But as a chapter title it assumes we already care about that particular design, test and observation. |
| How do cardboard wings withstand flight loads? | Now we know roughly what we're going to learn, why cardboard matters, and can imagine several interesting constituent questions without already knowing the answers. |

Under the third title we might have subchapters on bending and twisting, how folds and corrugations distribute loads, the construction of lightweight spars, or how humidity changes the useful properties of the material. The third rib and its 2 mm deformation might be extremely interesting evidence under one of these ideas. We haven't lost any of the technical specificity by refusing to make it the title.

Similarly, in a book on ChatGPT, "How do we deal with asynchronous operations?" isn't particularly exciting. "How does ChatGPT know whether a message I asked it to send a moment ago is still the message I want to send?" leads us to a much more particular landscape of questions about changes to the composer, attachments, navigation, and the distinction between readiness and intent.

We don't need to artificially put the word cardboard or ChatGPT into every title. We should be able to recover the kind of book we're reading from the actual ideas in the title, not merely from a name that has been appended to an otherwise generic question.

### 3. Variance — are we adding another dimension or exploring the same dimension at a higher resolution?

Suppose the first four chapters of our cardboard RC plane book are:

1. How do cardboard wings withstand bending?
2. How do cardboard wings withstand twisting?
3. How do folds make cardboard wings more rigid?
4. How do we make cardboard wings more rigid without adding much mass?

These might all be interesting questions, but imagine how little sense we'd have of building an RC plane from reading that table of contents. Compare it with:

1. How do we design an aircraft that can lift its own weight?
2. How do we make a cardboard airframe light and sufficiently strong?
3. How do we select a propulsion system and understand how long the plane can fly?
4. How do we make the aircraft stable and controllable?
5. How do we construct, test, and repair the plane cheaply?

Now each new chapter gives us a different way of thinking about what makes the plane possible. Under the second chapter the original four questions might be very useful (although we might still want to distinguish rigidity from strength).

Notice that we haven't simply reduced the number of questions. We've changed the set of questions at the chapter level so that they better span what we care about. We can do the same thing recursively within each chapter.

Careful though! We don't need to force these dimensions to be independent in a mathematical sense. A change in structural mass can have profound consequences for propulsion and control. Such connections may be some of the most interesting things in the book.

### 4. Inverse criterion — could the book make us curious about something we didn't know to ask?

Suppose we're primarily curious about making a cardboard plane rigid. We open the book expecting to learn about thicker materials, reinforcements, or perhaps how to reduce bending.

One version of the book simply lists material properties and answers the question we came with. Another version exposes us to the idea of aeroelasticity: could some deformation of a wing actually be useful? Could we design the way the wing twists under loading rather than simply try to prevent all twisting?

Suddenly we're asking different questions. Why do we want rigidity in the first place? What motions must we prevent and which might we deliberately allow? Are there other designs that achieve the desired flight behavior without maximizing stiffness?

We haven't established that a flexible cardboard wing is necessarily better. But we've discovered an entire territory worth investigating that we didn't even know existed when we first opened the book.

This is one way to understand the meta rule about being unable to put the book down. It's not an excuse to exaggerate how ingenious every mechanism is. The actual ideas and distinctions ought to be interesting enough that they make us want to follow the next branch.

### 5. The glossary — how well does it color in the intellectual territory?

Imagine two glossaries for the same book. One contains hundreds of terms concerning cardboard fibers, folds, joints, adhesives and different ways of measuring structural strength. The other contains far fewer terms but exposes us to wing loading, stall, center of gravity, static margin, thrust-to-weight ratio, servo torque, battery sag, sandwich structures and aeroelasticity.

The first glossary may have much greater depth in structural mechanics. The second may give us a much better sense of the breadth and variance of the entire book. Neither is necessarily sufficient.

Suppose we zoom in on the chapter about stability and control. Its vocabulary contains center of gravity, neutral point, static margin and trim. These are meaningful terms, but if we've also got subchapters on steering, disturbances and feedback control, where is the vocabulary about control surfaces, actuator saturation, damping or response to gusts? We might have colored in one region of the chapter rather well while leaving several other regions almost blank.

And if we zoom in further on the idea of static margin, does the vocabulary help us understand the relationship between center of gravity, neutral point and longitudinal stability? Or is static margin simply a technical word in a list?

This is what we mean by fill. **The number of terms in a glossary tells us very little about the amount of intellectual territory it actually colors in at any particular resolution.** A rich cluster of terms that doesn't seem to belong anywhere in our existing question tree might even expose a missing question or chapter. We shouldn't remove those terms simply because we haven't written that chapter yet.

### 6. Recoverability — finding the place without knowing its name

Imagine we're trying to find a town we once visited. We don't remember its name but recall that it was somewhere near a river, had a railway station and was surrounded by mountains. It would be quite useless to have a map that only allowed us to look up the exact name of the town.

We might first find the river, narrow the search to the towns near the railway, and eventually recognize the place from the surrounding terrain. Some of what we remembered might even have been wrong.

Consider the corresponding experience of learning about planes. We ask, "Why does my plane keep turning its nose upwards and then downwards again, even though I'm not moving the controls?" We may not know what pitch oscillations, longitudinal stability, damping or a phugoid are.

A poor glossary only returns something if we already know to search for those words. A useful one allows us to get from descriptions of the motion, the absence of control inputs and the behavior of the aircraft over time, to several possible ideas. We might then find ourselves investigating the difference between a short-period oscillation, a phugoid, a control-system oscillation or a stall-related motion.

The glossary shouldn't simply decide which of these we're experiencing. The description alone may not be sufficient. But can it get us to the relevant technical territory and expose the distinctions or observations that would help us figure it out?

In much the same way we might ask about a software application, "What happens if the text changes while the app is waiting to upload a file?" We needn't already know the words currentness predicate or post-await validation to find a useful direction.

This gives us a rather simple test of a question landscape and its glossary: give them to someone who is curious about the book but doesn't yet know its terminology. Can they find things they were looking for, and discover things they weren't looking for but now want to understand? Can another investigator then follow their questions all the way to the relevant evidence or a precise direction for obtaining it?

We should evaluate both directions. A book that is very easy to retrieve exact answers from but doesn't make us curious may satisfy much of the forward criterion and little of the inverse criterion. A book full of fascinating but unsupported ideas may do the opposite. What we're trying to develop is a book in which these two properties reinforce one another.
