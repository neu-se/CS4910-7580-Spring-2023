---
layout: page
title: Discussion - Design
permalink: /lecture-notes/3-design
parent: Calendar
nav_order: 2
---
# Discussion: The Quality Without a Name and Reuse/Compression

These notes roughly capture the (mostly unedited) comments from the class:

## The quality without a name, and software
* How does RPG/Christopher Alexander describe this?
	* "Alive" - something that is updated and grow/be updated. In OSS: something where contributors can come along, open a PR, and make a contribution. The artifact itself has needs and requires care and artfulness. Lifecycle. Unique
	*  It is only the "whole" when it is considered with the greater part of the system, which includes all of the future pieces, and all of the human pieces - the
* How would you?
	* Is it "Elegance" - integration, beauty with functionality?
		* Elegance is in the eye of the beholder, "maximize depth (selected quality attributes) while minimizing complexity"
	* Is it "usability" (in the sense of usable by the developers, not neceassarily by the users) - necessary, but not sufficient. Maybe this is too neutral of a word (need to also consider habitability and overall happiness)
	* Trustworthiness - how this operates and provides value to humans
* Have you worked with software in a way that resembles this?
	* We have worked with codebases where it DEFINITELY DOES NOT, and perhaps some where it is better...
* How do we make software in this manner?
* Is it possible to objectively define "good design" in software?
	* ...Or is it "unobtainium" (something to strive for, we can always get closer to)
	* These words are not meant to be definitions, they require contextual and cultural analysis
	* Lack of internal contradictions 
	* Maybe this is the wrong goal - or at least a very hard job

## Reuse and Compression

* In what ways /can/ we reuse code? Which ways does RPG miss?
	* One way: copy/paste. This does not "compress"
	* Use packages (e.g. system packages, libraries, components)
	* Use standard interfaces (e.g. POSIX) - Get the INTERFACE right (this is a very big risk, separate from getting the implementation right)
	* Algorithmic abstractions - generic algorithms that can be applied to many instances
	* Reuse requirements (including the lower-level specifications). Example: automotive/self-driving cars.
	* "We got it right once, reuse it" (for requirements, for code) - assuming that it has!
		* What is the incentive for the person that makes the library? It is hard to make the "perfect" code, and there are more risks to those bugs if others come in and depend on our code
* Why compare reuse and compression?
	* Code is more dense - could be good or bad, or both... Utilizes context, and there is some burden on the developer trying to understand it to understand that context
	* If you understand the library that you are reusing, then compression will help you understand more about the application
	* Law of leaky abstractions: all abstractions are leaky (not perfect - leaks the underlying complexity)
	* The more you write code, it can become denser, good for adding new things, but need to know the context... or hard, because it's complicated to read/understand when you come in to change things
	* RPG: locality is important, so that someone who comes along and needs to read/understand, can find that context
	* Compression is a way to describe reuse-like property of OOP