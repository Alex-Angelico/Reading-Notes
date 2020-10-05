# Reading 6: JS Object Literals, The DOM

## Understanding the Problem Domain

The field of knowledge associated with understanding the languages of programming and their implementation is vast and ever-changing; however, the problem domain to which this knowledge is applied in various circumstances is underestimated in how difficult it can be to grasp.

In the context of software development, learning the scope of a new problem domain can be like trying to figure out how to put together a jigsaw puzzle without the picture. There are many undefined values that the developer has to specify on their own. The more complex the development requirements, the more confusing it gets. And in the absences of information, the same undefined problem gomdain can appear differently to different programmers on the same team. Yet the reality is that such teams are often not given complete or even sufficient information to understand what they have to do right away. _In fact, this modern software development cycles favor this kind of ambiguity by way of agile development prinicples._

Therefore, it is essential to understand the problem (domain) before one begins programming. Two obvious techniques are available for making this process easier:

1. **Scale down the problem domain.** Reduce it to a functional subset of the overall design requirement, and/or to certain use cases. This reduces complexity and makes it possible to address the bigger picture in smaller steps.
2. **Invest more time in specifying the problem domain.** Communicate as much as possible with stakeholders outside the development team who have issued the requirement. Use their expecations of end results to inform design specifications.

_Of course, real-world circumstances render these two techniques imperfect. External pressures such as production deadlines may restrict a team's ability to divide a problem domain into smaller pieces to be addressed in sequence. And external stakeholders may not actually have a good idea of what they want a development solution to accomplish for them.

## Chapter 3 Selection of JavaScript/jQuery

### What Are Objects

In JavaScript and other programming languages, "objects" consist of a set of variables and functions which model something recognizable from the real world. Within objects, functions and variables take on different names.

- Variables become **properties** - things which describe some characteristic of an object, using all the normal JS data types (even another object)
- Functions become **methods** - activities which an object can be subjected to, based on its variables

_Note: The name associated with individual properties and methods is called a key. It can be a string, number, or boolean._

In the context of web design, the concept of key:value pairs used in objects is not unique to JS; HTML uses attribute names and values, and CSS uses property names and values.

### Creating Objects in JS

There are several ways to create objects in JS. The most popular is literal notation. An example follows:

var = musicLibrary = {
    albumNumber: 999,
    artists: 357,
    genres: ['pop', 'punk', 'rock', 'classic', 'r&b', 'soundtrack', 'rap', 'techno', 'indie', 'funk', 'disco', 'metal'],

    checkLibrarySize: function() {
        return this.albumNumber - this.artists;
    }
}

_Note: In the above example, the keyword `this` is used to denote that the method is checking the `albumNumber` and `artists` properties for this specific obkect.

### Performing Operations With An Object

An object's properties and  methods are most commonly accessed and executed using dot notation, e.g. `musicLibrary.checkLibrarySize;`. The dot between the object and its method is called a member operator, referring to the fact that properties and methods are members of objects.

Alternatively, property and method access can be performed by using square brackets, e.g. `musicLibrary['checkLibrarySize']();`. This notation is best used in special circumstances listed below:

- The name of the property or method being accessed contains special characters, such as a dash
- The name of the property is a number (allowed by dot notation, but best avoided)
- A variable is being used instead of a property name

## Chapter 5 of JavaScript/jQuery

### The Document Object Model (DOM)

DOM is a concept which is implemented by all modern web browsers. It allows for the creation of a model of a HTML page, and specifies the way in which the model should be structured using a DOM tree, which is a type of object model (meaning simply that it is made of objects). Each object represents a different part of a page once it has been loaded by a browser, and each of these objects have defined properties and methods which can be used to update what the user sees in their browser. Because the DOM is a disposable, dynamic model of a page rather than being the page's source code itself, the changes that a web browser makes through interaction with the DOM are visibile only to the specific end user, and generally persist only for the duration of their session. In no way is the underlying HTML affected.

A DOM is in fact an application programming interface (API), meaning that it facilitates communication between programs and programs/scripts (for example, between a web browser and HTML+JavaScript).

#### The Four Nodes

DOM trees use four types of nodes to represent the different objects that make up a HTML web page.

1. **The Document Node:** The root of a DOM tree, it points to and provides access to all nodes on a page.
2. **Element Nodes:**  HTML elements on a page which provide access to attribute and text nodes, as well as child/sibling element nodes.
3. **Attribute Nodes:** Co-equal parts of element nodes which are changed by JavaScript during a user session (e.g. CSS rules for ID attributes).
4. **Text Nodes:** Containers for display text which cannot contain other child elements.

### Methods and Properties for Accessing DOM Element Nodes

Method/Property           | Description           | Page #
------------------------- | --------------------- | ------
getElementById() | selectes individual element by id attribute | 195
querySelector() | returns first element matching a CSS selector | 202
getElementsByClassName() | selects multiple elements by class attribute | p200
getElementsByTagName() | selects all elements with a given tag name | 201
querySelectorAll() | returns all elements matching a CSS selector | p202
parentNode | returns parent of current element node | 208
(previous/next)Sibling() | returns previous or next sibling in DOM tree | 210
(first/last)Child | returns first or last child in current element | 211

### Methods and Properties for Working With DOM Element Nodes

Method/Property           | Description           | Page #
------------------------- | --------------------- | ------------
nodeValue | accesses and updates text node contents | 214
innerHTML | allows access to text content inside current element's child elements | 218,220,227
textContent | allows access to only text | 216
createElement() | creates a new element node on a DOM | 219,222,227
createTextNode() | creates anew text node on a DOM | 219,222,227
(append/remove)Child() | adds/removes a child element on a DOM | 219,222,224,227
id | updates an individual element selected by id attribute | 232
className | updates multiple elements by class attribute | 232
(has/get)Attribute() | checks if attribute exists/retrieves attribute value | 232
(set/remove)Attribute() | updates attribute value/removes attribute | 232
