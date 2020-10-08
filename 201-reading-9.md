# Reading 9: Forms and Events

## Chapter 7 of HTML/CSS

The `<form>` element is the key to all form-based user interactions in HTML. Forms may have several different control which gather different kinds of information from users. For example, a username and password combination.

HTML5 has introduced many new subsidiary elements to form which make it easier for users to fill in forms in different ways. Among the most versatile of these is `<input>`, which in its basic implementation allows users to enter email addresses and URLs. Beyond that, appending the attribute 'type' to an `<input>` element, with the value "search", creates a text box for executing search queries.

Much as when manipulating data in JavaScript, data provided to a form is translated into key/value pairs for processing.

## Chapter 14 of HTML/CSS

There are a number of CSS properties which were designed speciifcally to work with lists, tables, and forms. For example, using the 'list-style-type' and 'list-style-image' properties, list markers (aka bullet points) can be given different appearances.

Other properties can be used to ensure tables have consistent borders and spacing. This is importnat because these things can appear differently in different browsers otherwise.

Generally speaking, forms benefit from considered styling, both to make them more organized on the one hand, and interactive on the other. This can be done by lining up form controls so they are all easy for a user to see, for instance, or by creating visual elements within form fields.

## Chapter 6 of JavaScript/jQuery

Using the EVENT object's 'target' property, it can be determined which HTML element on a page an event occurred on.

The EVENT object can tell where a user's cursor was positioned when an event was triggered.

- The 'screenX' and 'screenY' properties indicate the position of the curosr within the dimensions of the physical monitor, rather than the browser window.
- The 'pageX' and 'pageY' properties indicate the position of the curosr within the dimensions of the web page itself--though if the top of the page is out of view, this will create coordinate discrepancies which are solved by the next pair of properties.
- The 'clientX' and 'clientY' properties indicate the position of the cursor within the dimensions of the browser window, rather than the web page within it. This means coordinates will not be affected by the top of the page being out of view.
