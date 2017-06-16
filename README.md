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

This is possibly the best part of web development is the Developer Tools. Chrome in particular has great developer tools. They let you look at the **Element Tree** (aka the **DOM**), the full hierarchy of all the elements on a web page. In addition to tags, you'll see attributes and styles.

**Exercise:** Right-click on the header element you see in the output window and choose **Inspect** from the context menu. This will open up the Chrome Developer Tools, and you should see highlighted an `<h1>` element.

Next we'll load up the [English language main page of Wikipedia](http://en.wikipedia.org/wiki/Main_Page). Open the Developer Tools, and hover over the various elements of the page. What gets highlighted?

Each element on the page has a **margin**, **border**, **padding**, and **content**. What do those mean?

**Exercise**: Notice that many elements have `class` and `id` attributes. What do those mean? Look them up. How many elements can have the same `class` attribute? The same `id` attribute?

**Research Question**: is the HTML source code of the file always the same as the element tree? 

### CSS

CSS is the styling information for the web. If HTML is the blueprint, CSS is the paint colors, window trim, and tile in the kitchen.

CSS style rules consist of a **selector** that says which elements the rule applies to, and a collection of **declarations** that give actual style information. For example:

```css
h1 {
  color: blue;
}
```

This rule selects all elements with tag name **h1** and sets their color to blue. Try it in codepen, and you should see the color of your header element change.

**Exercise**: Explore the following CSS attributes by setting them individually in the `h1` rule you created above:

 * `background: white;`
 * `font-size: 200%;`
 * `margin: 25%;`
 * `padding: 20px 20px 20px 20px;`
 * `border: 3px;`
 * `border-radius: 10px;`
 * `width: 50%;`
 * `font-family: sans-serif;`
 * `text-transform: capitalize;`
 * `text-align: center;`
 
There's a [full list](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference) on the web, of course. **Exercise**: Pick an attribute, read the documentation, and ask someone what it means!

Beyond tag names, you can also **select** using the `class` or `id` attributes:

```css
h1.big {
  font-size: 200%;
}

h1#main {
  font-weight: bold;
}
```

Use the `.classname` syntax to select all elements with a given class. `tagname.classname` selects only elements of the given tag with the given class. Use `#id` to select the element with the given id.

Classes let you create consistent styling that you can apply to many different elements across the page. Tag names are set by the HTML standard, but classes are defined by you, the developer. For example, you could use a single class to indicate something like a warning box; each box might have a pastel red background and red bolded text with a red border:

```css
.warningBox {
  background: #fdb;
  color: red;
  font-weight: bold;
  border: 2px solid red;
  border-radius: 5px;
}
```

Then, creating a warning box is as easy as including `warningBox` in the `class` attribute of any element.

**Exercise**: Define a new class in CSS with a bunch of attributes. Create a new paragraph tag, and set its class attribute to the class you just created.

**Research Question**: What happens if you give an element more than one CSS class?

### Layout

CSS also lets you specify layout rules. You saw the `width` property above. 
