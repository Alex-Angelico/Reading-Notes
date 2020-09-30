# Reading 3: HTML Lists, CSS Boxes, JS Control Flow

## Chapter 3 of HTML/CSS

Lists come in three varieties:

- Unordered (`<ul>`)
- Ordered (`<ol>`)
- Definition (`<dl>`)

  - Definition term (`<dt>`)
  - Definition (`<dd>`)

Further, one list can be nested within another simply by indenting a new list element under an existing `<li>` element.

## Chapter 13 of HTML/CSS

Boxes are the basic constructs which undergird all visual HTML elements. They can be modified in many ways using CSS.

- **(min-/max-) width/height** - Changes dimensions of a box in ways that allow it to fit better in many different kinds of page layouts.
- **overflow (hidden/scroll)** - Governs how a box managed content it contains that is too substantial for presentation within itse set dimensions.
- **border/padding/margin** - These can all be used to change how prominent a box's boundaries are, and what they look like. In cases where discrete attribute values for the different sides of a box's boundary need to be set, the first value corresponds to the top of the box, and it cycles clockwise from there. Two of the most sophisticated variants are:

  - _border-image_
  - _border-radius_

- **display (inline/block/inline-block/none)** - Each of these attributes modifies how a seclected HTML element behaves in terms of whether it is formatted for inline or block presentation - or no presentation at all, in the case of 'none'.
- **box-shadow** - This facilitates the application of shadow effects to the perimeter of a box.

## Selection from Chapter 2 of JavaScript/jQuery

### Arrays

Arrays are highly versatile objects that essentially function as lists of other objects. These subsidiary objects can be accessed and their values modified within the array structure by using an index value attached to the object's variable name (e.g. `paintColors[0] = teal;`).

## Chapter 4 Part 2 of JavaScript/jQuery

### The Malleability of Values in JS

#### Typing

JS has weak typing. What this means is that the data type of value as generated in JS code can be changed through a mechanism called type coercion. The advantage of this is that is makes JS relatively capable of handling unexpected data types being passed to a statement that would otherwise cause a program to crash.

_Example: The condition ('5' > 4) can be coerced such that the 5 is no longer a string (as indicated by the quote marks), but instead a number. This permits the whole condition to be evaluated in Boolean.

#### Truthy & Falsy

These two terms refer respectively to values which are treated as boolean true, and values which are treated as boolean false, despite not being so under conditions where strictly equal comparison operators would be used.

#### Checking Eqaulity & Existence

Truthyness and falsyness makes it easy to search for the existence of an element on a HTML page, for instance. But beware, truthy and falsy only work when using `==` comparison operators, rather than `===`.

### For Loops and While Loops

In general terms, loops are code constructs which reiterate themselves subject to a boolean evaluated condition or series of conditions (often based on a numerical counter). This allows for a subsidiary code block to be repeatedly executed.

#### Types of Loops

There are three common types of loops employed in JavaScript:

- **for:** runs a specific number of times based on a bounded counting condition
- **while:** runs an indefinite or definite number of times, depending on if a bounded counting condition is used, or some other kind of boolean evaluation
- **do while:** similar to the while loop, except that its subsidiary code block will run at least once, even if its condition evaluates to false.

_Note: Standard practice for variables used as counters in loop conditions is that they are named 'i' or 'j'. One or both may be used._
