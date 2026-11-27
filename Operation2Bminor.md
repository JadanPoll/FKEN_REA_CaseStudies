# Working with the ideas — tacit capability

This is a smaller companion to [Operational2B.md](Operational2B.md).

Suppose I've read a chapter of our investigative problem book and can now recognize a number of interesting ideas, how they come up and why they're relevant. But could I actually work with them? Given a situation, could I figure out how these ideas compose, what equations I'd use, what I'd calculate, what code I'd write, or how I'd go about making something work?

This is what I mean by tacit here. Think of it as a more technical aspect of the problem book, where the hypothetical situation basically becomes the question. We can assume I can at the very least recognize the key terms or ideas already. What I want to develop is the ability to work with them in actuality.

## The landscape of applied challenges

Think of the tacits as a set of **big picture applied problem book challenges whose solutions compose the underlying topical, subtopical and subsectional machinery**. Their key purpose is to holistically expose how that machinery is relevant and how we actually work with it given the kinds of situations or challenges we might be shown or given in the real world.

Much like the questions in [Operational2.md](Operational2.md), the tacits should asymptotically endeavor to form a convex dimensional set. But rather than trying to color in every chapter and subchapter with a corresponding exercise, we're interested in the landscape of things we could actually do with the knowledge. When we add the n + 1 challenge to the n-present challenges, what interesting new dimension of applied capability or composition does it expose?

Imagine the tacit problems in a book on RC planes:

- Given a box of cardboard, a motor, a battery and a target flight time, can I work out whether I could make a plane that flies? How would I decide on its mass budget, wing area and propulsion system, and what would I actually measure to find out if my design is viable?
- My plane flies but keeps pitching up and down. How would I figure out whether the problem is its balance, its aerodynamic behavior or something the controller is doing, and what would I try changing?
- Could I make a plane that returns to where I launched it even when the wind changes and my GPS measurements are imperfect? How would I get the sensing, estimation, navigation and control to work together?

Notice the variance. The first challenge concerns designing something under competing constraints, the second concerns figuring out why something isn't behaving the way we want it to, and the third concerns composing mechanisms to achieve a richer capability. They may draw upon some of the very same constituent ideas, but they give us quite different experiences working with those ideas.

The appeal of these tacits is that I can already imagine what I'd be trying to do, and I'm curious about how I'd actually go about it. The problem gives me a natural reason to work with the equations, technical details, code, experiments and relationships in its solution.

### Negative case — an exercise for every subsection

Suppose an LLM sees that our book contains sections on lift, drag, battery capacity, motor efficiency and wing loading, and proceeds to create five unrelated plug-and-chug exercises, one for each section. It might have technically covered the topics, but has it exposed how any of these things compose when I actually want to build a plane?

Rather than adding another such exercise, could we go up the tree and find a bigger picture applied challenge in which several of them naturally compose? We might still need to work out the very same calculations, but now they are constituent problems of something I actually care about. We can preserve smaller challenges when they develop a useful constituent capability; they don't all need to be independent entries in the big picture set.

Careful though! Making a problem larger, more technically elaborate or dependent on more topics doesn't necessarily make it better. An artificially constructed challenge that requires me to use ten prescribed equations may be considerably less interesting than a small but natural problem in which I have to figure out which two equations are relevant. The composition should emerge from the actual needs of the challenge, not from an obligation to include particular machinery.

We don't need the same topical breakdown or fill criterion as the glossary. A challenge can draw on several chapters, and several challenges can draw on the same chapter. The important thing is whether the set exposes a rich variance of natural applications, whether each challenge is itself curiosity-led and generative, and whether we can actually work through or recover how its solution comes together. A large open challenge can also be decomposed into tractable constituent problems without losing sight of what we're trying to accomplish.

## 1. What does it look like to actually use an idea?

Suppose I know what a low-pass filter is, why a capacitor might be useful in a circuit and what a time constant is. Imagine the following problem:

**I'm reading a slowly changing sensor with a microcontroller. There's an unwanted 1 kHz signal superimposed on the sensor voltage. Can I reduce that signal to a tenth of its amplitude without taking more than 20 ms to settle within 1% of a change in the actual sensor voltage?**

### Negative cases

- "Use an RC low-pass filter. Relevant concepts include cutoff frequency, attenuation, time constant and settling time." I already recognize much of this terminology. What I want to see is how it composes to address the problem.
- "The cutoff frequency is 1/(2πRC). Calculate the cutoff frequency for R = 1 kΩ and C = 1 µF." This may be a perfectly useful constituent exercise, but by itself it gives me very little practice figuring out how to use a filter to accomplish what I actually care about.
- "Use a 3.3 kΩ resistor and a 1 µF capacitor." Perhaps this works, but how would I have arrived at those values myself? What happens if I change the requirements?

### Positive case — work it out

Let's try a simple first-order RC filter, with the output taken across the capacitor. For now assume an ideal voltage source and a sufficiently high-impedance load.

We have two requirements and both concern the same parameter, τ = RC.

The magnitude response at frequency f is

$$
|H(f)|=\frac{1}{\sqrt{1+(2\pi f\tau)^2}}.
$$

To reduce the unwanted 1 kHz signal to at most a tenth of its amplitude, we need

$$
\tau \geq \frac{\sqrt{99}}{2\pi(1000)} \approx 1.58\ \text{ms}.
$$

But if the actual sensor voltage changes suddenly, the fraction of the original error remaining after time t is

$$
\frac{|e(t)|}{|e(0)|}=e^{-t/\tau}.
$$

To have no more than 1% of the error remaining after 20 ms, we need

$$
\tau \leq \frac{20\ \text{ms}}{\ln(100)} \approx 4.34\ \text{ms}.
$$

Notice that we didn't start by arbitrarily selecting a cutoff frequency. We've reasoned backward from two things we actually want the circuit to do, and discovered a range of possible designs.

Choose R = 3.3 kΩ and C = 1 µF, giving τ = 3.3 ms. Our ideal filter leaves about 4.8% of the unwanted signal amplitude and about 0.23% of a step's original error after 20 ms. Both requirements are satisfied in the model.

Now what if I want the sensor to settle within 5 ms instead? The upper bound becomes about 1.09 ms, which is below our lower bound of 1.58 ms. No choice of R and C in this particular first-order model can satisfy both requirements. Perhaps a higher-order filter, a notch filter or a different way of acquiring the signal is worth investigating.

Careful though! Before treating this as a working circuit, we should also consider the actual sensor's output impedance, the ADC's input and sampling behavior, component tolerances and the nature of the interference. We've worked out a design under a particular model, not certified the physical circuit.

**What did we actually learn to do?** We worked backward from functional requirements, expressed two different behaviors in terms of a shared design parameter, intersected the resulting constraints, selected a design and recognized an obstruction when the requirements changed. This is a useful way of thinking about many engineering problems, not just RC filters.

## 2. Code can serve the same purpose

Suppose I'm making a search interface. The user types "robot", then quickly types "robotics". The second search finishes first. A moment later the first search finishes and overwrites the newer results.

**How do I make sure an old request can't overwrite the results of a newer search?**

A negative answer would be to tell me to use asynchronous programming, debouncing, cancellation and generation guards. Or give me a hundred lines of framework-specific code without exposing which part actually addresses the problem.

A much more useful starting point might be:

```js
let generation = 0;

async function search(query) {
  const mine = ++generation;
  const results = await lookup(query);

  if (mine !== generation) return;
  render(results);
}

function clearSearch() {
  ++generation;
  render([]);
}
```

Here lookup(query) is an asynchronous function returning search results, and render(results) displays them. Imagine the following order of events:

| Event | Current generation | What happens? |
| --- | ---: | --- |
| Search for robot | 1 | Request 1 starts |
| Search for robotics | 2 | Request 2 starts |
| Request 2 completes | 2 | Its results are displayed |
| Request 1 completes | 2 | Its results are discarded |

What if I clear the search field while both requests are still in progress? Clearing the search also invalidates their generations. Notice that the invariant we actually care about isn't that requests complete in order, or even that we cancel old requests. It's that only the current intent is allowed to update the interface.

The snippet deliberately isolates that mechanism. It assumes one search interface and successful lookup calls. In a fuller implementation, errors and loading indicators also need to respect the generation, and cancellation might save unnecessary work. The same idea could be explored in other situations involving delayed actions, e.g. submitting a message after preparing its attachments.

Now I have a small piece of code whose behavior I can reason about, reproduce with two deliberately reordered responses, and adapt to another situation. That's quite different from merely knowing the words generation guard.

## 3. A few things to be careful about

The point isn't to create a bank of trivial textbook exercises or to mechanically add a calculation or code snippet to every question. Nor is it to turn every curiosity into an engineering project.

We want the hypothetical situations to give us useful practice going from a problem to the technical machinery that actually addresses it. Sometimes what's interesting is figuring out which equations apply in the first place. Sometimes it's how several individually familiar ideas compose. Sometimes it's how we discover that the approach can't work under the given constraints, or how we'd diagnose a failure in a real implementation.

A good worked example might be very small. It should make it clear what we're trying to do, how we went about it, what the relevant assumptions are and why the result actually contributes to the problem. If we can vary a consequential condition and understand what changes, that is often much more valuable than ten nearly identical exercises where the numbers happen to be different.

We can also preserve an unworked variation so I can try it myself, or give me a situation in which I have to decide which of the things I've learned are relevant. But don't mistake reading a worked example for having developed the tacit capability. We'd have to actually work with some of the ideas to find out.

The test is whether, given a somewhat different situation in the world, I could recognize and work with the relevant knowledge without having to be led through every step. If I need to retrieve a particular equation, library or implementation along the way, that's fine. What matters is whether I know why I'd want it, how I'd use it and how I'd tell whether it did what I wanted.
