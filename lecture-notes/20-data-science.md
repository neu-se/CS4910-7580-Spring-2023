---
layout: page
title: Discussion - Data Science
permalink: /lecture-notes/20-data-science
parent: Calendar
nav_order: 13
---

# Discussion: Notebooks and literate programming

## What's Wrong with Computational Notebooks? Pain Points, Needs, and Design Opportunities
* Methodology: Field observations and exploratory interviews. Follow-up with survey
	* What is the strength of the field observations?
		* Do not rely on people to remember what they did, or to be able to describe it
	* Sampling strategy
	* What is the role of the field study in the "mixed methods" methodology?
		* Exploratory - learn how people interact with notebooks in order to determine what questions to ask in the survey
		* "Limitations" paragraph sounds like a paragraph added in response to reviewer complaints 
	* Any concerns with this methodology?
		* Potential for bias from Hawthorne effect-  people behave differently when studied
* Pain points
	* What makes these pain points specific to data science, and not just pain points for programming? Or: What about data science makes these pain points even more painful?
		* Dependencies are painful in notebooks
		* Working with data: how to share the data and get access to it, share etc
		* Long-running computations - especially in the context of interactive programming, where you want to get the result quickly and then do something else based on that
			* Also limited in how many tasks a developer can do concurrently with one kernel (one)
		* Reliability of the kernel - when it crashes it is bad. Especially bad when tied to something that's long running
		* Tough to be both a documentation tool and a programming tool - it doesn't do either as well as we wished. Misaligned between the tool and the use-cases
			* What are those use-cases?
				* Debugging: When going through a notebook, there are data-centric debugging challenges. Might be many intermediate transformations, hard to see into them to understand what is changing
				* Creating visualizations: How to specify what kind of figures are wanted
				* Specific challenges around math/statistics
				* Building and evaluating models: There is a lot of data that needs to be consumed to e.g. build the model, then a lot of time to compute it, then you end up with more stuff that needs to be stored (model and parameters)
				* 
		* This is a means to an end for data scientists, and it's not really a good one - jupyter notebooks is lacking what we would consider to be "good development tools"
			* Lacks flexibility for tools that "traditional software engineers" need/use in iDEs?
	* What about pain points that are specific TO CELLS and not just to data science?
		* Interactions with cells are clunky (key strokes, undo/redo)
		* Lack of visibility between the different cells. Copying/pasting a cell to somewhere else might have unexpected results
		* What the heck is the semantic definition for a cell? Is it a function? What is the functional unit?
			* How long is a "readable" cell?
			* Comments within cells vs markdown around cells - tensions..
		* Line numbers usually disabled by default. This works great until you get an error. But, then when you get an error, it sure would help to know the line number. Line numbers start over in each cell
		* Is it a problem that cells can be run in different orders?
			* Some researchers feel it is a problem. Hard for reproducibility, good for exploration
				* Solution: "Restart kernel, run all cells"
				* Just because you CAN run cells out of order doesn't mean that you should in all cases (or maybe there is some anti-pattern, or maybe there should be some guard rails)
					* When you are programming overall, there are certainly many things that you need to maintain in mental model in head, some things can get lost...
				* Another problem for reproducibility:
					* We have some data files that are stored on our computer, paths might be hard-coded
			* How do data scientists communicate their mental model of data flow in a notebook to each other?
				* Intended to be top-to-bottom as a "narrative". Maybe not supposed to be run out-of-order?
				* Notebooks never intended to be reused in this kind of workflow - share and have someone else run it, then run automatically
				* This is a constraining requirement 
				* Embedded execution order shows the last set of runs, but nothing about what happened before that
				* Shows a slice of the workflow that generated the output in the notebook (which cells in which order, but not the history of those cells or their prior execution orders)
		* Is there an alternative to cells?
			* Immutable cells - once you run it, it becomes read only, can't add new cells above previously executed cells
			* Integration with assistive technologies like 3D, virtual reality
				* Organize cells in multiple dimensions
			* See recent CHI paper "sticky land" or something like this - separate the output from the code
			* What about constraints that limit global mutability?
				* At some point it just becomes a script with extra steps - and not a notebook anymore
		* Pain points around versioning and sharing:
			* There is a lot of metadata in the file, and that metadata is being versioned, and will cause conflicts
			* The output in the notebooks also goes into version control, diff'ing the output is NOT FUN.
			* The output might be large (especially images)
			* Resolving merge conflicts in notebooks?
				* NBDime 
			* What are the needs for versioning and sharing?
				* "I am going to put this in git and version it there so that I can work on one of two machines at once"
				* Useful to share so that someone can digest the output of a notebook
				* Extract key pieces to be reused elsewhere (demo that functionality)
				* Also might want to share all of the extra stuff (environment settings, the data, what versions of what libraries need to be installed)
		* Refactoring:
			* "For researchers, it's important that we support the languages data scientists actually use, not the languages we /wish/they would use. " - do we need languages without dynamic typing and reflection?
				* Languages that run faster
				* Less bug-prone/provide more of a safety net (especially in terms of type systems)

### Managing Messes
* What do we think of the characterization of "messes"? What precisely is a mess? Is this a common problem?
	* A "mess" is highly subjective
		* Is it a mess, or exploratory programming at its finest?
	* 3 types of messes:
		* "Disorder" (cells are run in a different order)
			* Is it really a problem to run in different orders? Does it impact output?
		* "Deletion" (cell deleted but the content still there)
			* Possibly an issue for reproducibility
		* "Dispersal" (code generating some results is spread across entire notebook, not in same area)
			* This is what they address in this work
	* Presentation of the tool: the use case and discussion
		* Program slicing
			* Static
			* Dynamic
			* It is not very simple to determine a valid slice:
```
int a = 1;
int b = 2;
if(a == 1){
	b = 3;
}
print(b); //slice on this
```

```
int b = 2;
int a = 1;
Object foo = null;
if(a == 1){
	foo.bar();
	b = 3;
}
print(b); //slice on this
```
*  What would convince you to adopt this code gathering tool?
	* Is this a problem that you've had with notebooks before?
	* Does it solve that problem?
		* Maybe, but it also creates another mess: "clutter across notebooks" - code clones
		* What evaluation would or does demonstrate that this tool reduces code dispersal?
			* Is this tool intended to prevent messes from being created in the first place, or to manage the messes? - evaluation just shows managing
			* How to evaluate directly: "Are the resulting notebooks less messy?"
			* Qualitative analysis demonstrates feasibility on a system-focused paper
* What are interesting future directions in "literate programming"? Considering notebooks, proof assistants, whatever...
	* Staging based on level of competency - provide easier paths to common solutions?
	* Develop more tools that are customized to the problems of notebooks. Code clones?
	* Do more user studies and collect more feedback to understand how these tools are used and what the challenges are
		* Use this as feedback to integrate better documentation and training
	* How to link and cross-reference in notebooks?

Some cool seminar on live and literate programming by Andrew Head - [Syllabus: Live and Literate Programming - Google Docs](https://docs.google.com/document/d/19icrT54F4fFdTCL7GFnjp6B3uQiIbcZwCH26IRnZWkc/edit#), [Course Schedule](https://docs.google.com/spreadsheets/d/1_k1B2wiKh8c6lT8oUg6EyOQRVZ4DULHgRIytCjYGCzc/edit#gid=1150769424), [Readings](https://docs.google.com/document/d/1v9EfBihAbIIW4-eGSLDBF4Xvc_RG6dtTs6Yz39B53jU/edit#heading=h.rc5arqe791m6)
