# Class 4: Structuring Web Pages With HTML

## Chapter 18

The fundamental utility of HTML for creating the underlying structure of modern webpages is deeply important to determining how successful a website is at attracting the users it was built to serve, retaining their interest once they arrive, and keeping them coming back in the future--however frequently or infrequently they may need to.

Although the elements of HTML which are critical to creating a page's structure are relatively simple in nature, they can be used in complex ways to create diverse structural designs which are attractive to all kinds of different users. For this reason, it is important for web developers to have a good understanding of who their users are for the site they are designing.

While it isn't feasible to create a website that has perfect appeal to the full set of intended users. A few practices can go a long way to making the site very appealing to the majority of intended users:

- Articulating why people come to the site, what they do when they are on it, and how often they come.
- Creating fictitious model users as examples of how one would expect different types of people to behave on different pages.
- Establishing a site map that organizes pages and groups of pages by relevancy to each other.

With regards to the third practice in particular, it is also necessary to build user-friendly side navigation using HTML. Concision, clarity, and consistency of this element of a site goes a long way to making it a success among users.

Lastly, with these elements of structure established, they can be used to amplify design choice concerning size, color, style, and grouping of various content elements on a page in ways that reflect information priority to users. This will make the experience seamless, and users more likely to return.

## Chapter 1

HTML provides structure to webpages in the same way that formatting does to documents written in word processors, and assorted print elements do to newspapers. In other words, HTML is primarily concerned with ensuring overall legibility of information presented on a webpage to its users. This is managed through numerous kinds of tags which demarcate text and images into discreet groups. These tags can further be customized with attributes that make them more versatile.

## Chapter 17

The newest version of HTML, HTML5, clarifies the purpose of some existing HTML elements while also introducing new ones, which are collectively easier for developers to use, while providing better structural design to web pages.

HTML Element | Strucutral Purpose
------------ | ------------------
&lt;header&gt; | Containing important information at the top of every page (i.e. &lt;body&gt;), &lt;article&gt;, or &lt;section&gt;.
&lt;footer&gt; | Containing important information at the bottom of every page (i.e. &lt;body&gt;), &lt;article&gt;, or &lt;section&gt;.
&lt;nav&gt; | Holds major navigational blocks that correspond to different parts of a website's sitemap.
&lt;article&gt; | A generic container for any part of a page that is a coherent unit, and might be reproduced elsewhere.
&lt;aside&gt; | Alternatively used in articles to hold related but non-essential information, or at the page level to hold page-related content and functions.
&lt;section&gt; | A generic container that holds multiple articles on a page.
&lt;hgroup&gt; | Holds multiple heading tags together
&lt;figure&gt; | A special container for special, predominantly visual assets referenced by an article (e.g. images) that is not integral to overall flow of a page.
&lt;figcaption&gt; | Provides captioning to a figure asset.
&lt;div&gt; | A container that is used where no other suitable element (mainly &lt;section&gt; or &lt;article&gt;) exists to contain a group of sub-elements.
&lt;a&gt; | Used to convert a block element and child elements into a link.

## Chapter 8

Further elements of HTML code provide both essential and more nuanced control of site functionality and presentation.

HTML Element | Strucutral Purpose
------------ | ------------------
&lt;!DOCTYPE html&gt; | Used to initialize a web page in HTML
&lt;!-- --&gt; | This format can be used either to insert non-programmtic comments into a HTML file for reference by developers, or to prevent otherwise executable HTML code from running, by placing the relevant text or code between the two sets of hyphens.
id attribute | Provides a unique identifier to a HTML element (e.g. &lt;p id="intro paragraph"&gt;) that CSS uses as a reference for specific formatting.
class attribute | Functions similarly to the id attribute, except is applied to groups of HTML elements instead of a single one. Additionally a class attribute can point to multiple classes by simple putting a space between class names (e.g. class="important fancy")
&lt;span&gt; | An inline generic container for text where no other containing element is suitable (e.g. &lt;a&gt;). Can be used with the ID or class attribute.
&lt;iframe&gt; | Creates a window within your webpage onto another page or entirely different site, using the attributes 'src', 'height', and 'width'.
&lt;meta&gt; | Contains information that is not visible on a webpage but provides critical information about the page's design--and whether or not it is indexed by search engines, using the attribute 'robots'. It is used inside a &lt;head&gt; element.
