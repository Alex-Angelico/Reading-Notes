# Reading 4: HTML Links, CSS Layout, JS Functions

## Chapter 4 of HTML/CSS

### Site Structure Organization

- Linking within a website using `<a>` elements in HTML can be achieved using relative URLs rather that absolute URLs.
- On large websites with many pages, practice good separation of concerns of HTML files for different pages by placing different related groups of page files in separate directories.

_Tip: Relative directory paths for linking to different pages on a large website, and the notation '..' refers to the directory above the active one (e.g. '../../index.html)._

### Other `<a>` Features

- `mailto:` can be used to prompt the creation of a new email to a specific address (e.g. `<a href="mailto:jon@example.org">Email Jon</a>`).
- `target="_blank"` can be used to open a link in a new window (e.g. `<a href="https://www.imdb.com" target="_blank">`).
- `<a href=id>` can be used to link to a specific part of the same page, or a different page, by pointing to a HTML element with an id attribute.

## Chapter 15 of HTML/CSS

### The Conceptual Basis of Positioning HTML Elements

The fundamental relationshp that connects positioning and other CSS styling to HTML elements is the box which contains all HTML elements. Depending on the element, its containing box will either be block-level, meaning it starts on a new line, and inline, meaning it follows immediately next to the previous element.

Additionally, the principle of containment, in how one element box may contain other element boxes is key to determining sight organizaiton and inherited styling via CSS.

### Controlling Elements with CSS Position Schemes

Using the position property available in CSS rules, one of four different kinds of effect can be achieved.

- **Normal:** Standard presentation, which does not actually require articulation in CSS. However, if it was necessary for some reason, (e.g. to override more general position rules, it would be expressed as `position: static;`.
- **Relative:** Moves elements from the position the would have occupied in normal flow, without affecting the position of other elements.
- **Absolute:** Repositions elements within their containing element without affecting the position of other elements, and allowing for overlap between these elements. Fixed elements follow a user's browser window as they scroll.
- **Fixed:** Similar to absolute positioning, except elements are placed in relation to the browser window, and do not follow user scrolling.

_Tip: Elements can also be moved around outside of normal positioning constraints (to the left or right) using `float`, which removes them from normal structural flow and turns them into block-level elements around which other elements flow._

## Chapter 3 Part 1 of JavaScript/jQuery

### The Basics of Functions

Functions are powerful constructs in programming that allow for superior organization and economy of code by grouping statements within a dynamic object that can receive data arguments to inform **parameters** that allow for complex processing, and output **return values** which can then be used in other parts of a program. Most importantly, they can be invoked at any position in a program after they are defined, without reproducing their entire subsidiary code block.

Moreover, functions also provide a **local variable scope**, meaning that variables which are declared and manipulated within them are isolated from the surrounding program. This enables developers to more safely make targeted changes to code within function, while better controlling the flow of data through a program. A less obvious advantage of the local scope of variables in functions is that they require less computer memory to retain--local variables are only held in memory while their parent function is active, whereas global variables in the main body of a program must be persistent.

### Anonymous Functions and IIFEs

Anonymous Functions and IIFEs (Immediately Invoked Function Expressions) are implementations of the function construct which are called as they are created, and have special non-recurrent use cases. These cases include:

- As an argument when another function is called, in order to calculate a value for said funtion
- To determine a value for an object property
- Within event handlers and listeners to perform a specific ask
- As a safeguard against variable name conflicts between connected scripts

IIFEs in particular are popular in jQuery.

## Summary of Pair Programming

### The Two Roles

- **Driver:** The programmer who undertakes all of the mechanical duties of coding: text editor management, file switching, version control--and most of all the writing of code.
- **Navigator:** This programmer provides no direct written input--they instead focus on how algorithm ideas can be translated into code, while researching solutions and documentation.

### The Advantages

#### Efficiency

Two sets of eyes and two sets of ears make much easier to catch one another's errors and jointly process ideas and problems, leading more quickly to a viable product.

#### Engagement

Two programmers working together are better able to maintain a higher degree of focus on a project due to mutual investment with another party.

#### Learning & Socialization

The simple reality of collaborating with another programmer is that it allows for further technical development based on exposure to complementary skillsets--and to improve interpersonal skills.

#### Professional Readiness

Many companies rely on pair programming paradigms both during their interview process, and in daily working situations. Thus, learning to pair program makes aspiring software developers more likely to find a job.
