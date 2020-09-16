# Class 5: Designing Web Pages with CSS

## Chapter 10

CSS, which stands for Cascading Style Sheets, provides an easy framework for applying stylistic rules to the different structural elements of a HTML-rendered website.

A CSS rule consists of two components:

- **Selector:** Used for selecting what element of HTML a CSS rule applies to. Multiple HTML elements can be selected by a single rule by separating them by a comma.
- **Declaration:** Provides the instructions for how the selected elements should be styled, as indicated by curly brackets. A declaration is itself made up of two components:
    - _Property:_ Denotes the part of the element to be changed by a rule. Multiple properties can be targeted in a single declaration.
    - _Value:_ Imparts the specific settings desired for a property, which either follow a set pattern, or are preset.

    #### Examples of CSS rules
    - header, p {  
        font-family: Arial;  
    }  
    - article {  
        background color: green; border: solid, white, 3px;  
    }  
    - body {  
        color: white;  
    }  

Although CSS rules can be internal to a HTML file using the &lt;style&gt; HTML element within the &lt;head&gt; element on a page, it is considered best practice to create external CSS files to ensure appropriate scope of responsibility and separation of concerns. An external CSS file is connected to its corresponding HTML file using the element &lt;link&gt; with the attributes 'href', 'type', and 'rel'.