# Class 6: Dynamic Web Pages with JavaScript

## Chapters 1c and 2 part 1 of JavaScript/jQuery

If HTML is the skeleton of a website, and CSS its skin along with other external features, JavaScript (JS) is the muscle that allows a website and its constituent pages to act dynamically and interact with users. Together, these three langauges are the pillars of building a modern website. HTML, CSS, and JS can alternatively be thought of as the content layer, presentation layer, and behavior layer, respectively.

_Note: While JS plays a powerful role in making websites accessible and appealing to users, many users disable the execution of JS code in their browsers. Thus, it is important that sites are designed to be functional even if their JS component is discluded._

As with CSS, while it is possible to write JS within a HTML file (in this case using the `<script>` element), it is considered best practice to create external JS files to ensure appropriate scope of responsibility and separation of concerns. An external JS file is connected to its corresponding HTML file using the element `<script>` with the attribute `src`.

_Standard composition of HTML `<script>` element for JS file refernce:_
`<script src="js/javascript.js"></script>`

JS that provides dyanmic presentation outputs on a webpage will generate them in the area corresponding to where the `<script>` reference is placed in the HTML file (e.g. in `<header>`, or at the bottom of `<body>`).

There are three reasons using an external JS file is considered best practice:

- Clearer organization for developers when shifting between editing HTML and JS.
- Faster page loading for users due to the fact that all relevant CJSSS can be loaded from a single file rather than repeatedly on every web page that uses it.
- Ease of implementing dynamic function changes across multiple pages that refer to a common JS file.
