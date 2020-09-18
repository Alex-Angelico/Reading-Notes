# Class 8: Operators and Loops

## Chapter 4 of JavaScript/jQuery

### Comparison Operators

Comparison operators are the lynchpin of functional loop constructs. Their boolean evaluation is the determining factor for whether or not a loop should continue to iterate after each execution of its code block. The comparison operators are:

- `==` - "equal to"; checks if two values are identical
- `!=` - "not equal to"; checks if two values are not identical
- `===` - "strictly equal to"; checks if two values and their attendant data types are identical
- `!==` - "strictly not equal to"; checks if two values and their attendant data types are not identical
- `>` - "greater than"; checks if left number is larger than right number
- `<` - "less than"; checks if left number is smaller than right number
- `>=` - "greater than or equal to"; checks if left number is larger than or equal to right number
- `<=` - "less than or equal to"; checks if left number is smaller than or equal to right number

### Logical Operators

Logical operators allow for multiple conditions to be jointly evaluated in boolean. In conjunction with comparison operators, logical operators can be used to establish complex conditional statements for instructing loops how often to run. The logical operators are:

- `&&` - "and"; tests more than one condition, all of which must evaluate as true in order for the whole statement to evaluate as true
- `||` - "or"; tests at least one condition, at least one of which must evaluate as true in order for the whole statement to evaluate as true
- `!` - "not"; tests if a single condition evaluates to true or false based on the inverse of its boolean value (e.g. `!(2 < 1>)` returns true, because the that is the inverse of the statement's actual boolean value)

### For Loops and While Loops

In general terms, loops are code constructs which reiterate themselves subject to a boolean evaluated condition or series of conditions (often based on a numerical counter). This allows for a subsidiary code block to be repeatedly executed.

#### Types of Loops

There are three common types of loops employed in JavaScript:

- **for:** runs a specific number of times based on a bounded counting condition
- **while:** runs an indefinite or definite number of times, depending on if a bounded counting condition is used, or some other kind of boolean evaluation
- **do while:** similar to the while loop, except that its subsidiary code block will run at least once, even if its condition evaluates to false.

_Note: Standard practice for variables used as counters in loop conditions is that they are named 'i' or 'j'. One or both may be used._
