# A quick workshop covering HTML, CSS, JavaScript

Enacted at CCA, June 16 & 21, 2017.

## Day 1

In which we uncover the basics of HTML and CSS, using [codepen.io](codepen.io) as a platform for experimentation.

### Basic HTML

HTML provides a blueprint, the base structure of a webpage. It's made up of a hierarchy of elements, including headers, paragraphs, bullet points, boxes with text ("div" tags), images, links, etc.

Browsers provide a default "interior decorator", or style, for these types of elements, but we can modify the appearance of these elements using CSS, which we'll talk about later.

Elements are declared using a **&lt;body&gt;** *some stuff, including other elements* **&lt;/body&gt;** syntax. To create an element, enclose its **tag** in `< >` characters, followed by any content you want within the element, and terminated by its **tag** in `</ >`. For example, this creates a first-level header element: `<h1>Hello1</h1>`.

**Exercise:** Open up [codepen.io](codepen.io) and create an `<h1>` header tag in the "HTML" section. Examine the output. Add a `<small>` element inside the `<h1>` element.

**Exercise:** Create an [&lt;img&gt;](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/img) tag; the `<img>` tag uses a `src=` attribute to incidte the URL (web address) of the image to be included in the page. Next, create an [anchor (`<a>`)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a) tag (a link!) that points to http://en.wikipedia.org/wiki/Main_Page -- the English language main page of Wikipedia.

**Exercise:** Read through the [full list of HTML elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element); create a `<p>` tag, a `<ul>` tag (with a two or three `<li>` tags inside it), and a `<span>` tag. Pick three new tags from the list of all elements to create in your codepen sketch. Put some of those tags inside other tags.

#### The Inspector

This is possibly the best part of web development is the Developer Tools. Chrome in particular has great developer tools. They let you look at the **Element Tree**, the full hierarchy of all the elements on a web page. In addition to tags, you'll see attributes and styles.

**Exercise:** Right-click on the header element you see in the output window and choose **Inspect** from the context menu. This will open up the Chrome Developer Tools, and you should see highlighted an `<h1>` element.



