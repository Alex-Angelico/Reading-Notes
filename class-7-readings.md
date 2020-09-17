# Class 7: Programming with JavaScript

## Chapter 1a of JavaScript/jQuery

JavaScript allows developers to create series of programmatic instructions called scripts which can access and modify the content of HTML page, stipulate rules for a browser to follow while on that page, and react to events triggered by the browser or user. Examples of how these abilities can be applied are:

- Advanced presentation constructs (e.g. visual slideshows)
- Data input (e.g. a subscription form)
- Selective dynamic reloading of page elements (e.g. frames)
- Filtering data (e.g. through a user search)

The core feature of scripts is that they are programmatic. This means they are explicit, specific, thorough, and consistent in the nature of the instructions that they provide to a computer. Scripts must be written this way in order to be interpreted properly by a computer's operating system and CPU.

With that in mind, it is equally important for a software developer to have concrete goals for scripts they are writing before they start. This will help make their design clearer and less likely to cause errors due to ambiguity.

## Chapter 2 part 3 of JavaScript/jQuery

Expressions and operators are a basic mechanism of all programming languages, not just JS.

### Expressions

There are two types of expressions:

- Direct assignment of a value to a variable (e.g. `var a = 2;`)
- Computational assignment of two or more values to a variable (e.g. `var b = 3 * 2;`)

### Operators

There are several major classes of operators:

- Assignment (e.g. `=`)
- Arithmetic (e.g. `+`, `-`, `*`, `/`, `%`)
- String (e.g. `+`)
- Comparison (e.g. `==`, `>`)
- Logical (e.g. `&&`, `||`, `!`)

Arithmetic operators follow the standard mathematical order of operations.

There is only one string operator. `+` is used for concactenation.

## Chapter 3 part 1 of JavaScript/jQuery

Functions are one of the most important building blocks of effective scripts in JS. By combining a series of statements into a cohesive coding block, they allow a script file to perform useful dynamic actions on a web page such as requesting user input and manipulating data. The code block can then be called as many times as possible throughout the script just by invoking the function's name.

_Standard notation for declaring a function in JS:_
`function exampleFunction(){---code block for function goes here---}`

Note that the function must first be declared using the keyword `function` at the start of the line.

A function can be made capable of handling more complex tasks by incorporating parameters, which appear between the parentheses.

`exampleFunction(testNumber, nameString)`

These parameters are places where programmatic or user-defined inputs are provided in the form of arguments. Once passed into a funciton,these parameters can be processed in any number of ways.

A function can also return a processed value to a script for later use.

`return newValue`

This value can take the form of any kind of data.
