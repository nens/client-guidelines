# client-guidelines
Guidelines for code, architecture, design in front-end apps.  
In table of content chapters with a "--> contains content" behind it yet contain content.  
Other chapters probably do not contain content yet.  

# Table of content
[Summary](#summary)   
[What to contribute](#what-to-contribute)   
[When to contribute](#when-to-contribute)    
[Contribute Format](#contribute-format)    
[Content](#content)  
[HTML](#html)  
[CSS](#css)  

- [Which entities / Units ?](#which-entities-/-units-?)
  * [Pixels / REM / EM / % / VH](#pixels-/-rem-/-em-/-%-/-vh)
  * [HSLA / RGB / Color-name](#hsla-/-rgb-/-color-name)
- [Positioning and layout](#positioning-and-layout)
  * [Auto Wrapping](#auto-wrapping)   --> contains content
  * [Auto Scaling](#auto-scaling)    --> contains content
  * [Battle of layout - table block flex grid absolute](#battle-of-layout---table-block-flex-grid-absolute)
  * [Old style positioning - float-left display-block](#old-style-positioning---float-left-display-block)
- [Hide items on page](#hide-item-on-page)  
- [Animation](#animation)  
- [Selectors](#selectors)    
- [Scoping](#scoping)  
- [Grouping attributes within selectors](#grouping-attributes-within-selectors)  
- [Code re-use](#code-re-use)
- [best practices responsive designs](#best-practices-responsive-designs)  

[JavaScript](#javascript) 
- [State management](#state-management)  
- [Component based architecture](#component-based-architecture)  
- [Mitigate side effects](#mitigate-side-effects)   
- [Object oriented and Functional programming](#object-oriented-and-functional-programming)
- [Bad practices](#bad-practices)

# Summary
Goal of this document is for front-end developers to look up what would be the preferred solution for a given problem.  
It is a collection of problems and potential solutions.  
This document should also serve as a good way to navigate trough these solutions.  

The information in this repo should allow developer to:

- Find within reasonable time if this repo contains solution to the problem
- Judge if the information is applicable for the encountered problem
- Understand if/why the solution is preferred over other solutions
- Implement the solution described in this repository
- Judge if the information is outdated
- See where the information is coming from

#  What to Contribute
Developers may contribute to this document via pull request.  
Always be critical when to add more content.
Searching in this document can also cost time.  
When the answer to your question was found by a 1 minute google search it may not be a good problem to add here.  
For problems and solutions to add to this repository at least one of the following is true:

- Took considerable amount of time to look up through other channels (google, stack-overflow, other repo's)
- Looking it up took more knowledge about the problem then would be considered normal for a junior developer.
- It is difficult to select the right answer from a pile of not so good answers that pop up through google or stack-overflow
- Our answer to the problem might be different from mainstream, because of our specific technology, domain, architecture, app, customer etcetera.

# When to contribute
Whenever you **implemented** OR **reviewed** a feature that:  
- Is not yet in this repo  
- Meets the requirements of [What to contribute](#what-to-contribute)


# Contribute Format

Please have a look at the first article is this repository:  
[scale + wrap label and input depending on width](./code/wrap_label_input/README.md)  
Also add the link under the relevant header below.  
In the [Table of content](#table-of-content) add a "--> contains content" behind the link to mark that it has at least one article.  
Please make sure all links are working so users can navigate fast.  
If you disagree with any format/structure of this repository please let me know (Tom).  

# Content
For now I (Tom) focus on CSS, because that is where most chaos is.  
I also find it hardest for CSS to find good answers online.  
Feel free to add good JavaScript or HTML answers (or mixes of those).  
# HTML
# CSS
## Which entities / Units ?
### Pixels / REM / EM / % / VH or VW / 
### HSLA / RGB(A) / RGB / Color-name
## Positioning and layout
### Auto Wrapping
Problem:  
If the space to show 2 elements next to each other becomes to small,  
then they can often be shown beneath each other.  
This is called wrapping and can happen automaticly with CSS based on the available space.  
Below is an example using flexbox to scale a input + label.  
[scale + wrap label and input depending on width](./code/wrap_label_input/README.md)  
### Auto Scaling
Problem:  
Some elements can both be small or big.  
They should simply take up the available space.  
Below this is done for a input element using flexbox.  
[scale + wrap label and input depending on width](./code/wrap_label_input/README.md)  
### Battle of layout - table block flex grid absolute
#### Tables:
When something is a table we should try using a table, but ...
Tables are missing a few vital features:

- Tables cannot have a scrollabel body ( this is a real problem)
- Tables cannot wrap columns ( able to workaround with media queries end conditional displaying columns, but still very cumbersome)
#### Flexbox
Flexbox is scrollable and can wrap, but..
"cells" on top of each other will not align, unless specified a min or max width.
This makes sense because flexbox is NOT a 2-dimensional layout system (grid is).
Therefore making tables in flexbox maybe a bad idea.

#### GRID
Grid may be the solution, but I lack the knowledge there (Tom).
Also grid is not supported on Internet Explorer 11 (probably never going to be supported).
We should investigate on this.


### Old style positioning - float-left display-block
## Hide items on page
## Animation
## Selectors
## Scoping
## Grouping attributes within selectors
## Grouping selectors over CSS files
## Naming conventions Classes / Id's
## Code re-use
## best practices responsive designs
# JavaScript
## State management
## Component based architecture
## Mitigate side effects
## Object oriented and Functional programming
## Bad practices


