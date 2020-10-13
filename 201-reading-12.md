# Reading 12: Docs for the HTML \<canvas\> Element & Chart.js

## `<canvas>` Basics

Charts are far better for displaying data visually than tables. They’re easier to look at and convey data quickly, but they’re not always easy to create. A great way to get started with charts is with Chart.js, a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page. It’s a well documented plugin that makes using all kinds of bar charts, line charts, pie charts and more, incredibly easy.

The great things about Chart.js are that it’s simple to use and really very flexible. It's easy to get started with Chart.js. All that's required is the script included in a page along with a single `<canvas>` element to render the chart.

At first sight a `<canvas>` looks like the `<img>` element, with the only clear difference being that it doesn't have the src and alt attributes. Indeed, the `<canvas>` element has only two attributes, width and height. These are both optional and can also be set using DOM properties. When no width and height attributes are specified, the canvas will initially be 300 pixels wide and 150 pixels high. The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout size: if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted. The `<canvas>` element differs from an `<img>` tag in that, like for `<video>`, `<audio>`, or `<picture>` elements, it is easy to define some fallback content, to be displayed in older browsers not supporting it, like versions of Internet Explorer earlier than version 9 or textual browsers. You should always provide fallback content to be displayed by those browsers. As a consequence of the way fallback is provided, unlike the `<img>` element, the `<canvas>` element requires the closing tag (`</canvas>`). If this tag is not present, the rest of the document would be considered the fallback content and wouldn't be displayed.

## Drawing with `<canvas>`

 Normally 1 unit on a `<canvas>` grid corresponds to 1 pixel. The origin of this grid is positioned in the top left corner at coordinate (0,0). All elements are placed relative to this origin. So the position of the top left corner of the blue square becomes x pixels from the left and y pixels from the top, at coordinate (x,y). Unlike SVG, `<canvas>` only supports two primitive shapes: rectangles and paths (lists of points connected by lines). All other shapes must be created by combining one or more paths.
