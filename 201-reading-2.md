# Reading 2: HTML Text, CSS Introduction, Basic JS Instructions

## Chapter 2 of HTML/CSS

Structural markup elements are used to modify the appearance of content on a webpage.

Semantic markup elements are used to provide additional information about content on a webpage that web browsers can detect. _These often have the side-effect of changing content appearance, but they are not meant for this purpose._

## Chapter 10 of HTML/CSS

CSS is the language of visual presentaion on the web in any capacity beyond the very basics offered by HTML itself. It offers and easy framework for applying different stylistic rules to different elements of HTML.

A CSS rule consists of two components:

- **Selector:** Used for selecting what element of HTML a CSS rule applies to. Multiple HTML elements can be selected by a single rule by separating them by a comma.
- **Declaration:** Provides the instructions for how the selected elements should be styled, as indicated by curly brackets. A declaration is itself made up of two components:

  - _Property:_ Denotes the part of the element to be changed by a rule. Multiple properties can be targeted in a single declaration.
  - _Value:_ Imparts the specific settings desired for a property, which either follow a set pattern, or are preset.

Examples of CSS rules:

- `header, p {font-family: Arial;  }`
- `article {background color: green; border: solid, white, 3px;}`
- `body {color: white;}`

Although CSS rules can be internal to a HTML file using the `<style>` HTML element within the `<head>` element on a page, it is considered best practice to create external CSS files to ensure appropriate scope of responsibility and separation of concerns. An external CSS file is connected to its corresponding HTML file using the element `<link>` with the attributes `href`, `type`, and `rel`.

_Standard composition of HTML `<link>` element for CSS file reference:_
`<link href="css/styles.css" type="text/css" rel="stylesheet" />`

There are three reasons using an external CSS file is considered best practice:

- Clearer organization for developers when shifting between editing HTML and CSS.
- Faster page loading for users due to the fact that all relevant CSS can be loaded from a single file rather than repeatedly on every web page that uses it.
- Ease of implementing style changes across multiple pages that refer to a common CSS file.

Within a CSS file, the principles of cascade, selectors, and inheritance all determine how declarations in individual CSS rules can apply to multiple elements within a HTML file, depending on how they are related.

### Cascade Rules

There are two prevailing rules for how cascading style are applied in CSS:

- **Last Rule:** In cases where a CSS file contains two or more identical selectors, the last selector (i.e. the one nearest the bottom of the file) and its attendant declaration takes precedence.
- **Specificity:** If one selector is more specific than another (i.e. targets a more nuanced configuration of HTML elements within the HTML file), the former takes precedence over the latter, _regardless of their absolute positions in the CSS file._

Additionally, the value modifier `!important`, including a preceding space, can be appended to any property value in a selector declaration to indicate that it should take precedence over other rules that apply to the same element.

### Selectors

Type | Meaning
---- | -------
`* {}` (universal) | All elements
`h1, h2, h3 {}` (type) | Elements of indicated type(s)
`.note {}`, `p.note {}` (class) | Groups of elements with the appended `.class` label
`#introduction` (id) | Single elements with the appended `#id` label
`li>a {}` (child) | Elements that are the child of the parent element type
`p a {}` (descendant) | Direct descendant of a specified element type, not just a child
`h1+p {}` (adjacent sibling) | Next sibling element of a specified initial element type
`h1~p {}` (general sibling) | Matches multiple siblings, not just the one directly suceeding the specified initial element type

### Inheritance

Many CSS rules are automatically implictly inherited by child HTML elements if the rule's selector has any. This allows for streamlined rules via the elimination of repetition. Other rules are not inherited by default, but can be made to be inherited by child elements by using the value `inherit` for the desired property.

## Chapter 2 of JavaScript/jQuery

### Statements

Statements are the basic building blocks of a programmatic script. Each statement is an individual instruction that a script executes in order from top to bottom. In the case of JS, each statement should end with a semicolon, which also ends the line.

A statment can be anything from a variable declaration to a complex function call. Moreover, statements can be organized into code blocks which only execute in certain circumstances.

### Variables

Variables are delcared using the keyword `var` at the start of a line, followed by a variable name and the assignnment of a value. For example:

`var favNumber = 2;`

In addition to numeric data as in the example above, variables can also be used to store string data using either single or double quote marks (as long as one or the other is used consistently), or boolean data.

_Note: Single quote marks are universally considered best practice for expressing string data in JavaScript!_

Multiple variables can be declared in one statment, either by:

`var price, quantity, total;`
OR
`var price = 5, quantity = 4;`
`var total = price * quantity;`

#### Naming Rules for Variables

  1. Must start with letter, $, or _ **(NO NUMBERS)**
  2. Can contain letters, numbers, $, or _ **(NO - OR .)**
  3. Cannot use keywords or reserved words
  4. JS is case-sensitive
  5. Be descriptive
  6. Use camel case

### Expressions

Expressions and operators are a basic mechanism of all programming languages, not just JS. There are two types of expressions:

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

## Chapter 4 Part 1 of JavaScript/jQuery

### Programmatic Decision-Making with Conditional Statements

Often in programming, it is necessary to offer divergent code blocks which are conditionally executed depending on how data passing through a script is evaluated. This must be done programmatically using conditional statements. In general terms, conditional statments are expressed as follows:

`if () {function();}`
OR
`if () {function();} else {function2();}`
OR
`if () {function();} else if () {function3();} else {function2();}`

Boolean-evaluable statements are inserted into the parentheses after the `if` and `else if` statements, and these govern which function code block is executed, depending on whether data provided to the conditional statements is evaluated as boolean true or false. Such constructs can be used to provide a variety of outputs to users of a script, depending on the value of data they input.

### Comparison Operators

Comparison operators are the lynchpin of functional conditional statements. Their boolean evaluation is the determining factor for which branch in a  conditional statement code block should be executed. The comparison operators are:

- `==` - "equal to"; checks if two values are identical
- `!=` - "not equal to"; checks if two values are not identical
- `===` - "strictly equal to"; checks if two values and their attendant data types are identical
- `!==` - "strictly not equal to"; checks if two values and their attendant data types are not identical
- `>` - "greater than"; checks if left number is larger than right number
- `<` - "less than"; checks if left number is smaller than right number
- `>=` - "greater than or equal to"; checks if left number is larger than or equal to right number
- `<=` - "less than or equal to"; checks if left number is smaller than or equal to right number

### Logical Operators

Logical operators allow for multiple conditions to be jointly evaluated in boolean. In conjunction with comparison operators, logical operators can be used to create more complex conditional statements that determine which branch should be executed in more precise terms. The logical operators are:

- `&&` - "and"; tests more than one condition, all of which must evaluate as true in order for the whole statement to evaluate as true
- `||` - "or"; tests at least one condition, at least one of which must evaluate as true in order for the whole statement to evaluate as true
- `!` - "not"; tests if a single condition evaluates to true or false based on the inverse of its boolean value (e.g. `!(2 < 1>)` returns true, because the that is the inverse of the statement's actual boolean value)
