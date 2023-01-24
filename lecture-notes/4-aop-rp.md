---
layout: page
title: Discussion - AOP and RP
permalink: /lecture-notes/4-aop-rp
parent: Calendar
nav_order: 3
---
# Discussion: AOP and RP Evaluation

These notes roughly capture the (mostly unedited) comments from the class:

## Aspect-Oriented Programming

### The hot takes
* Is it annoying to have to have an additional compilation/steps? And also, to have to learn new language(s)?
* Is this both easy to understand and efficient?
	* How do you actually evaluate the learnability of this, and the understandability of the resulting code?
* Is HTML/CSS a similar kind of “cross-cutting” concern
	* (In the context of setting styling for multiple objects)
* How does this actually work? Can you do it in interpreted language?
* This is a very different way to design programs, how to come up with new ways (like this and other?)
* Are these “just macros”?
* Are there some contexts where this works the best?
* How do you debug this!?
* Is it a good thing or a bad thing that the compiler is not “smart”?
	* Separating the compilation of the program from the aspects might help with reuse across different languages

### Aspects
* Why?
	* Coupling (Want low coupling) - Degree of interdependence between program units. Change in one unit requires change in many others (perhaps also hard to figure out which)
	* Cohesion (Want high cohesion) - Degree to which a program unit represents a single purpose
	* Defined in terms of “program unit”
		* Functional
		* Now: aspects, “cross-cutting concerns” to reduce “tangling” (when you try to do more than one thing at once)
		* What is tangling?
			* Subjective, but it can be more precise based on stated quality attribute goals
			* Perception of how complicated it is to determine “what is doing what”
* The example in section 3: Pixelwise
	* Loop fusion
	* Is this easier to understand?
		* Fewer lines of code != easier to understand
	* Is this easier to maintain?
		* Reducing copy/pasted code might help
		* This probably DOES make it much easier to maintain PROVIDED that the developers doing that maintenance fully understand it.
			* It can be hard to reason about what gets called when, if an aspect join point occurs - you won’t know upfront that it will be called/included. Hard to isolate things. Leaky abstraction
			* “<import performance>” sounds good
	* There are additional constraints to what kinds of things you can call “aspects” and how to program around
* Digital library example
	* Aspect: communication - avoid sending unnecessary information
	* Are there other alternatives?
		* Refactor Repository interface, method `unregister(book)` becomes `unregister(isbn)`
		* Make a subclass of book, called `RemoteBook` 
			* Challenge to both this and the aspect approach: what do you do when someone tries to access other properties?
		* Add the `transient` modifier to the other fields
	* Creating these aspects requires a strong understanding of the functionality that you are implementing and need to get to
	* Here is a next-level aspect: only copy what is needed, automatically
* How would/could you evaluate this?
	* User study - examine code, answer questions about it
	* Ask users to debug some code
		* How to design a controlled debugging experiment?
	* Another user-study idea: provide the participants with fragments of the solution ,and fragments that do not belong in the solution, and then asking users to arrange them (“parsons problem”)

## An empirical study on program comprehension with reactive programming
* Comparing the two examples in figure 1:
	* In the observer side, the dependencies are inverted: the “update c” logic has to be attached to a.
		* If there are a lot of dependencies inside of the variable, this problem cascades to become much worse
	* To find the dependencies, you need to find all of the add observer calls, in the RP version, it is in one spot (where the signal is)
* Does anyone have RP experiment, and if so, with what?
	* React
		* If you use only the RP parts, it’s good
		* React has asynchronous updates, which is a separate problem/mess
	* ShinyR
	* Hardware description languages
* Evaluation methodology:
	* Controlled experiment, measuring the time to complete tasks and and success rate, plus some qualitative feedback
	* What are the tasks?
		* “What do you expect this output to be?”
		* Some tasks were excluded based on being too straightforward in one case
		* Behavioral understanding, which require tracing the functional dependencies
		* What tasks might be harder in RP?
			* Tracing relationships between multiple parameters, this focuses mostly on dataflow
			* Know the order of _when_ things happen
	* What was the training?
		* 2 class sections on RP, 2 homework assignments on RP
		* Prior course experience on OOP, maybe from first year of studies (these are 4th year students). Observer pattern was learned in first year
	* They built a custom tool for running the user study
	* Findings:
		* RP is better
		* We liked the statistical tests
		* Liked the findings that were not statistically significant
	* Discussion/concerns
		* How do the goals of the tasks relate to the user interaction with the study and its training
		* Fairly impartial, not concerned about overlap of authors
		* The training quality is likely to be MUCH better than could be expected broadly. It would be very revealing to show the lectures and assignments, to see overlap
		* Having and reporting on a pre-test would be nice here, too (what was maximum level of exposure)
		* Showing the specific tasks in a table to line up with the results would help with further understanding/analysis
