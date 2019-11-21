# Section One: Introduction to Algorithm Design
> An algorithm is a procedure to accomplish a specific task.
- We (as engineers) look for three things in a good algorithm. It should be *correct*, *efficient*, and *easy to implement.* Sometimes, all of these can't be achieved but we can find an algorithm that's "good enough."

- An *algorithm* always produces a correct result, whereas a *heuristic* typically provides a result that's good enough with no guarantee to always produce the correct result. There may be edge input cases that produce sub-optimal behavior. (Ex. Traveling Salesman Problem) 

- Algorithms that look "reasonable" can easily be incorrect. It's important to show that your algorithms are correct. 

---

- Algorithms can be expressed in *pseudocode*, *actual code*, or *English.* 
	- Each has its own trade-offs between "ease of expression" and precision
- Use whichever as long as you are **clearly** expressing the idea behind your
  algorithm.
- A well-defined algorithm requires a well-defined problem. Both the input and
  properties of the output should be clear. 
- A good technique is to restrict the set of valid inputs until a "correct and
  efficient" algorithm can be found.
	- Restrict graphs to trees.
	- Restrict a 3D problem to 2D.
- Two common traps to defining output requirements
	- Ill-defined questions (ex. Find *best* routes -- What does "best" mean in
	  this context?)
	- Compound goals: Trying to achieve multiple well-defined goals makes life
	  much more complicated.

## Is my Algorithm Correct?

- Before trying to prove correctness, can we first easily show that it's wrong?
- The best way to show that an algorithm is wrong is a *counter-example.*
- A good counter-example should be easily verifiable.
	- Know what answer your algorithm gave, and show that there is a better one.
- A good counter example should also be simple.
	- Try to strip away all unnecessary detail. Simplify. Simplify. Simplify. 
- Finding good counter-examples is a *very* useful skill. There are a few things
  to keep in mind while looking for them.
	- *Think small.* Smaller examples are easier to think about and easier to
	  test.
	- *Think exhaustively.* There all only a few possibilities for the smallest
	  non-trivial values of n. Think about all of the interesting cases and use
	  them to build your counter-example.
	- *Go for a Tie.* If you want to break a greedy heuristic, make everything
	  the same size. There's nothing to base decisions on anymore.
	- *Seek Extremes.* Many counter-examples hinge on extreme cases. Huge and
	  tiny. Far and near. Few and many. Left and right.

> ... when algorithms fail, there is usually a very simple example on which they
> fail.

### Induction and Recusion a.k.a Magic

- If you don't find a counter-example, you can't just *assume* an algorithm is
  correct. You need a proof.
- Induction is an **extremely** powerful tool to prove the correctness of an
  algorithm. In general, there are two "steps" to a proof by induction:
	- First, you have to prove that the algorithm works for certain base cases
	  (or boundary conditions)
	- Then, assuming that the algorithm is correct for the *n - 1* case, show
	  that the *n* case is also true.
	- That's it. Really.
- Induction is very similar to recursion in that regard. Both break problems
  down while looking for certain "base cases."
- Proofs by Induction are susceptible to subtle reasoning errors.

## Modeling

- The art of relating the problem to another well-defined problem.
- Modeling can eliminate the need to design an algorithm in the first place.
- Real-world problems involve real-world things.
  Algorithms, on the other hand, are designed to work with abstract structures like graphs, sets, and lists. 
- Modeling allows you to express a real-world problem in terms of more abstract
  structures.

---

- You're not special and neither are your problems. Chances are good that
  someone *somewhere* has dealt with your problem before in some context. But
you won't be able to leverage their solution without looking at your problem
through the lens of "computing properties of common structues."
- Let's look at some:
	- *Permutations:* Any problem that involves the arrangement or ordering of a
	  set of items. Keywords are *sequence*, *tour*, *arrangement*, and
*ordering* (obviously).
	- *Subsets:* Any problem that involves a selection of items from a set.
	  Keywords are *cluster*, *collection*, *committee*, *group*, *packaging*,
and *selection.*
	- *Trees:* Any problem that involves hierarchical relationships. Keywords
	  are *hierarchy*, *dominance relationship*, *ancestor/decendant*, and
*taxonomy.*
	- *Graphs:* Any problem that involves relationships between arbitrary pairs
	  of objects. Keywords are *network*, *circuit*, *web*, and *relationship.*
	- *Points:* Any problem that involves locations in some geometric space.
	  Keywords are *sites*, *positions*, *data records*, and *locations.*
	- *Polygons:* Any problem that involves regions in some geometric space.
	  Keywords are *shapes*, *regions*, *configurations*, and *boundaries.*
	- *Strings:* Any problem that involves a sequence of characters. Keywords
	  are *text*, *characters*, *patterns*, and *labels.*

---

All of the abstract structures defined above are also **recursive objects.**
Meaning that each is made from "smaller things that are exactly the same type as
the big thing." Removing a node from a tree results in smaller trees, removing
a character from a string results in a smaller string, etc...
