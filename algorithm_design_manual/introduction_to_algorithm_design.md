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

---

- The best way to show that an algorithm is wrong is a *counter-example.*
- A good counter-example should be easily verifiable.
	- Know what answer your algorithm gave, and show that there is a better one.
- A good counter example should also be simple.
	- Try to strip away all unnecessary detail. Simplify. Simplify. Simplify. 
- Finding good counter-examples is a *very* useful skill. There are a few things
  to keep in mind while looking for them.
	- *Think small.* Smaller examples are easier to think about and easier to
	  test.
> ... when algorithms fail, there is usually a very simple example on which they
> fail.
	- *Think exhaustively.* There all only a few possibilities for the smallest
	  non-trivial values of n. Think about all of the interesting cases and use
	  them to build your counter-example.
