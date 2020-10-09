# Reading 10: JS Debugging

## Chapter 10 of JavaScript/jQuery

_Tip: If nothing else, the one toolset that web developers can rely on to help with debugging is built into their internet browsers: the console and dev tools._

Two of the most important things to keep in mind when working on isolating and understanding errors in a program are:

1. **Execution order:** The order in which code in a program is run. This can sometimes be deceptive due to how functions are called. Not everything happense in a straightforward top-to-bottom order.
2. **Variable and function scope:** Different parts of the same program occur in different execution contexts, depending on where and when they are called. A variable declared within a function has local scope that applies only within the function, for instance - and a variable declared at the top of script can be programmatically overwritten further down.

### More Debugging Tips

- Try another browser to see if code works differently in different places.
- Add console log signal messages in order to track how far code gets before it crashes.
- Strip back as much code as possible in order to test a specific section of code.
- Use comments to temporarily remove code if not prepared to delete it.
- Use Stack Overflow and traditional search engines to track down past instances of other developers encountering similar problems.
- Try a code playground (e.g. jsbin.com, jsfiddle.com, dabblet.com, cssdeck.com) if willing to share code.
- Use web-based or browser-based code validation tool (e.g. jslint.com, jsonlint.com).

### Common Error Causes

- Incorrect letter casing
- Missing or extra characters
- Incorrect us of comparison/assignment operators
- Missing or extra closing brackets, braces, and parentheses
- Missing parameters for a function call
- Quote marks that are not matched
- Delcaring variables without `var`
- Reference to HTML id attributes which aren't actually unique
