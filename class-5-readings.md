# Class 5: Designing Web Pages with CSS

## Chapter 10 of HTML/CSS

CSS, which stands for Cascading Style Sheets, provides an easy framework for applying stylistic rules to the different structural elements of a HTML-rendered website.

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

## Chapter 11 of HTML/CSS

One of the basic and most versatile building blocks of CSS is color. The two most common color properties in CSS are:

- `color`: determines text color
- `background-color`: determines background

Color can be adjusted through several different value types:

- RGB(A) (Red, Green, Blue, (Alpha))
- HSL(A) (Hue, Saturation, Lightness, (Alpha))
- Hex code
- Color names

In the above examples, the Alpha value is a secondary, optional value which is not directly tied to color, but rather determines opacity. It is expressed as a percentage.

What is most imporatnat in considering color schemes within CSS is to use combinations of colors for backgrounds and text that provide sufficient but not excessive contrast, ensuring maximum readability for users.
