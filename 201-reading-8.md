# Reading 8: More CSS Layout

## Chapter 15 Selection of HTML/CSS

### Further Positioning Techniques

- **Overlapping:** By using relative, fixed, or absolute positioning, HTML eleaments can be made to sit on top of each other. If further control of how they overlap is needed, developers can use the CSS property called `z-index`. Its value is a simple interger, and the higher that value, the more elements a given HTML element will sit on top of.
- **Float:** The `float` property simply allows a HTML element to be removed from normal page flow, and placed as far to the left or right of its containing element as possible. All other elements inside the same containing element will hence "flow" around it like a river around a rock. Generally, the `width` property should be used in any CSS rule where `float` is applied in order to control the element's box size. Otherwise, it may take up the entire width of the element and interfere with other formatting.

### Screen Sizes

With the proliferation of so many different kinds of consumer computer technology, screen sizes and resolutions have come to vary very widely. Because of this, a page **width of 960-1000 pixels** has become the conventionally accepted range for web design. _This page width range strongly favors users on mobile devices, who are likely browsing the web in a tall screen orientation._ However, there is a somewhat popular trend of developing adaptive or responsive designs which change to fit a specific user's screen size.

Additionally, usability studies have shown that users are generally capable of assessing the value of a website or page in about one second. What this means is that they don't have to scroll to do so. In response to this, conventions of web design favor concentrating a page's value proposition in the **top 570-600 pixels**, which can be seen as soon as a page loads.

### Layouts

- **Fixed Width:** Fixed width layouts offer designers the most control over design, and the easiest reference for how assets will appear on a page (because positions are matched exactly the pixel counts). However, they can leave big gaps on the sides of screens in wide orientation, and they can break or look unappealing depending on a user's hardware and software preferences.
- **Liquid:** Liquid layouts expand to fill a browser window, regardless of screen orintation and resolution. However, various elements of such pages can behave unpredictably--for example, a liquid layout page in wide orientation may have blocks of text that are visually too long in one direciton.
- **Grid:** Grid layouts are surprisingly versatile for creating differt styles of appearance. They also set consistent proportions and spacing for elements on a page. Furthermore, they can help organize information and features in a very user-friendly way.

### Multiple Style Sheets

It is often good organizational practice to create multiple style sheets to manage the styling of a website, or even a single webpage. A HTML page can point to multiple style sheets in one of two ways.

1. `@import`: This is used on a CSS sheet that a HTML page is pointing to; generally the core 'style.css' sheet. On the sheet, the `@import` rule can be used in the following notation: `@import url("tables.css"); @import url("typography.css");`.
2. `<link>`: Alternatively a HTML page can simply link to multiple CSS sheets using the standard notation for the `<link>` element.