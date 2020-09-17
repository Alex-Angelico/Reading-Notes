# Class 5: Designing Web Pages with CSS

## Chapter 10

CSS, which stands for Cascading Style Sheets, provides an easy framework for applying stylistic rules to the different structural elements of a HTML-rendered website.

A CSS rule consists of two components:

- **Selector:** Used for selecting what element of HTML a CSS rule applies to. Multiple HTML elements can be selected by a single rule by separating them by a comma.
- **Declaration:** Provides the instructions for how the selected elements should be styled, as indicated by curly brackets. A declaration is itself made up of two components:

- _Property:_ Denotes the part of the element to be changed by a rule. Multiple properties can be targeted in a single declaration.
- _Value:_ Imparts the specific settings desired for a property, which either follow a set pattern, or are preset.

_Examples of CSS rules_
    - `header, p {font-family: Arial;  }`
    - `article {background color: green; border: solid, white, 3px;}`
    - `body {color: white;}`

Although CSS rules can be internal to a HTML file using the `<style>` HTML element within the `<head>` element on a page, it is considered best practice to create external CSS files to ensure appropriate scope of responsibility and separation of concerns. An external CSS file is connected to its corresponding HTML file using the element `<link` with the attributes `href`, `type`, and `rel`.

_Standard composition of HTML &lt;link&gt; element:_
`<link href="css/styles.css" type="text/css" rel="stylesheet" />`

There are three reasons using an external CSS file is considered best practice:

    - Clearer organization for developers when shifting between editing HTML and CSS.
    - Faster page loading for users due to the fact that all relevant CSS can be loaded from a single file rather than repeatedly on every web page that uses it.
    - Ease of implementing style changes across multiple pages that refer to a common CSS file.

Within a CSS file, the principles of cascade, selectors, and inheritance all determine how declarations in individual CSS rules can apply to multiple elements within a HTML file, depending on how they are related.

## Chapter 11

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
