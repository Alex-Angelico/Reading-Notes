# Reading 7: HTML Tables, JS Constructor Functions

## Domain Modeling

The process of creating a conceptual model in code for a specific problem. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model.

To model objects that will be instantiated many times in a program, developers build constructor functions, which are the template of an object's attributes and behaviors.

### Tips for Building Domain Models

1. When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.
2. Model its attributes with a constructor function that defines and initializes properties.
3. Model its behaviors with small methods that focus on doing one job well.
4. Create instances using the new keyword followed by a call to a constructor function.
5. Store the newly created object in a variable so you can access its properties and methods from outside.
6. Use the this variable within methods so you can access the object's properties and methods from inside.

### Prototypes

Prototypes are where methods are placed for a constructor funciton. Much as with a constructor function, prototpyes are referred to repeatedly by a program whenever it needs to call that particular method. Hence, while it takes somewhat longer to locate methods in a prototype, they save on memory during program execution. For this reason, use of prototypes is considered a best practice in JavaScript.

## Chapter 6 of HTML/CSS

In HTML, tables are built using a several different elements.

- `<table>` - Initiates the table, similar to `<ul>` or `<ol>`
- `<tr>` - 'table row', which encapsulates one or more `<td>`
- `<tr>` - 'table data', meaning they hold specific values
- `<th>` - 'table heading', used with the attribute `scope="col"/"row"` to create labels for columns and rows; first child element of a `tr`

Additionally, `<thead>`, `<tbody>`, and `<tfoot>` can be used for longer tables, to provide extra information to screen readers, and to stylize the major parts of a table in distinct ways.

## Chapter 3 Remainder of JavaScript/jQuery

Creating objects with constructor syntax allows developers to use the same template more many instantiations of the same object while only referring to a single block of code to create it. Aside from being much more economical and easier to write in code, constructor objects also demand less computer memory in execution.

### Example of an Object Written in Constructor Notation

function Hotel(name, rooms, booked) {
  this.name = name;
  this.rooms = rooms;
  this.booked = booked;
  this.checkAvailability = function() {
    return this.rooms - this.booked;
  };
}

The key to constructor notation is the use of `this`, a vital keyword. The meaning of `this` can change depending on where a function is declared, but it always refers to a single object - and usually the same instantiation in which its function is operating.

### Storing Data in JavaScript

There are four modes in which data is stored:

- Variables
- Arrays
- Individual objects
- Multiple objects

For the purposes of storing data, arrays are also a type of object. They are comprised of key/value pairs--the key for each value is simply its index number. Arrays can also store other objects within themselves, using the following scheme for example array "costs":

Index # | Value
------- | --------------
0       | {accomodaitons: 420, food: 40, phone: 10}
1       | {accomodaitons: 460, food: 20, phone: 20}
2       | {accomodaitons: 230, food: 0, phone: 0}
3       | {accomodaitons: 620, food: 150, phone: 60}

To access an individual value, the form `costs[2].phone` would be used.

### Strings as Objects With Methods

- `toUpperCase()` - converts to all upper case
- `toLowerCase()` - converts to all lower case
- `chartAt()` - accepts an index position argument and returns character value at index
- `indexOf()` - accepts character(s) as an argument and returns first index position where found
- `lastIndexOf()` - accepts character(s) as an argument and returns last index position where found
- `substring()` - accepts two index positon arguments separated by a comma, and returns characters found between (first position inclusive)
- `split()` - accepts a character argument and splits a string wherever that chracter is found
- `trim()` - removes whitespace from end of string
- `replace()` - accepts two character arguments, with the first one being replaced by the second in the first instance that the first argument is found
