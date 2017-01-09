# Intro to HTML

![HTML5](https://www.w3.org/html/logo/downloads/HTML5_Logo_512.png)

| Lesson Objectives - SWBAT (Students Will Be Able To) |
| :--------------------------------------------------- |
| Structure a basic HTML page using a "doctype" and the `<html>`,`<head>`, and `<body>` elements. |
| List and explain the role of HTML `<head>` elements, including `<title>`, `<link>`, `<script>`, and `<meta>`. |
| List and give use cases for common HTML elements: `<img>`, `<h1>`...`<h6>`, `<p>`, `<span>`, `<a>`, `<ul>` & `<ol>`, `<li>`, `<!--…-->`, and `<div>`. |
| List the most important structural HTML5 semantic elements: `<footer>`, `<header>`, `<nav>`, `<main>`, and `<section>`. |
| Explain the purpose and benefits of using HTML5 semantic elements. |
| Explain the purpose of HTML attributes as opposed to their content. |
| Identify the parts of an HTML element (tagname/type, attributes and values, content, and closing tag). |
| Assign attributes to HTML elements using the correct format. |

## What is HTML?

In short: HyperText Markup Language.

HTML is the essential building blocks of website. It is the steel beams of your soon to be impressive, awe-inspiring, skyscraping website. Because it is so essential to every website, people often have a difficult time explaining what exactly the language does. In order to avoid any confusion, let's break down that garbled, unabbreviated title.

*Hypertext* - The method by which you move around on the web — by clicking on special text called **hyperlinks** which bring you to the next page. The fact that it is *hyper* just means it is not linear — i.e. you can go to any place on the Internet whenever you want by clicking on links — there is no set order to do things in.

*Markup*  - This is what **HTML tags** do to the text inside them. They mark it as a certain type of text (*italicised* text, for example).

*Language* - This one is pretty straightforward. HTML has its own syntax and structure like any other language, programmatic or human.

For the most part, tags have an opening, and a closing tag with the content sandwiched in the middle. Some tags are *self-closing*, which means there is only one tag and it doesn't require a separate closing tag. We'll discuss those when we get to them!

## The Doctype, `<head>` and `<body>`

> Why do I need to use `<!DOCTYPE html>`? Doesn't seem to do anything...
>
> — Some poor sap

Let's talk about the major pillars of every HTML Page:

``` html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>Intro to HTML</title>
    <!-- Link to other files here! -->
  </head>
  <body>
    <!-- Put all your site stuff in here! -->
  </body>
</html>
```

Sublime makes it easy for us to get this skeleton.  Let's open up Sublime and create a file called `index.html`.  Inside this file let's type `html` and hit *tab*.

You should see this appear:
```html
<!DOCTYPE html>
<html>
<head>
	<title></title>
</head>
<body>

</body>
</html>
```

#### Doctype

`<!DOCTYPE html>` belongs at the top of each of your html pages. This informs the browser that this file is written in HTML.

It's important to include this despite the fact that the browser will **PROBABLY** understand you anyway.

Don't take chances with your code! Programming is all about being exact. You don't want your code to fail for some simple reason like you forget to put `<!DOCTYPE html>` at the top of the page.

After this, the remainder of the document should be enclosed within an `<html>` tag. Only two tags are directly inside the `<html>` tag.

#### `<head>`

The `<head>` tag provides all general information (metadata) for the webpage. For instance, in the bit of code above, we're setting the character encoding to 'utf-8' (the dominant character encoding for the internet, made to be backwards compatible with ASCII), telling the browser if it supports the page, and setting our title.

Other common parts of the `<head>` are attaching stylesheets (`<link>`), libraries, and scripts (`<script>`).

#### `<body>`

The `<body>` tag contains all our content. It contains the majority of what we see on the page.

## Structural HTML Tags

Once we're inside the `<body>` of our document, we can actually begin building out our content.

First, let's look at the structure of any given html tag.

![html tag structure](http://tutorial.techaltum.com/images/element.png)

We see that each tag is built from a tag, an attribute, and content. Let's look at each part in detail.

- Tag names define what kind of html element is being used
- Attributes provide additional information about HTML elements
- Content is the stuff that gets rendered in the browser

#### Content Tags

Let's go over some content tags:

#####`<h1>...<h6>`

Headers, going from biggest(`<h1>`) to smallest (`<h6>`).

#####`<p>`

Paragraph tag. Put your prose in the `<p>` tag!

#####`<span>`

The span tag is unique in that it's generally used to highlight a small section of writing (a generic inline container). This is most commonly used in regards to CSS, which we'll discuss in more deatil tomorrow, but to see what I mean:

``` html
<p>Isn't this <span>interesting?</span></p>
```

#####`<div>`

Div tags are probably the most commonly seen tags. A div is a generic container for content. It's often used to group things together for styling purposes.

#####`<ul>`, `<ol>`, & `<li>`

Unordered and Ordered Lists. Unordered come with bullets, ordered come with numbers. The lists within them must be made of `<li>` (list item) tags. For example:

``` html
<ul>
    <li>Thing 1</li>
    <li>Thing 2</li>
</ul>
```

#####`<!--…-->`

HTML comment tag. Anything between these double hyphens will be ignored by the browser. So... what's the point?

Comments are useful to developers, because they allow us to add information that the user doesn't need to see, but developers can use.

Comments can provide context (describe what some code does) or save code that we don't want to display, but don't want to delete.

### Semantic Tags

Certain tags tell you exactly what they are in their naming. These are great to use when other developers will be using your code, as anyone seeing these tags will be well aware what you're trying to make with them.

Again, an important rule in programming is clarity! These assist in that. Examples are `<footer>`, `<header>`, `<code>`, `<em>`, `<strong>`, `<nav>`, `<main>`, and `<section>`.

## Tags with Distinct Attributes

Some tags are very specific in nature.  They contain attributes, or additional metadata, in order to work. Let's look at some and see how to use them in our HTML documents.

#####`<a>`

Anchor tag. I'm sure you've used these before - they link us to other pages. Within them are the special attribute `href` (hypertext reference). You set the `href` to a url using an `=`, then surround a word in the `<a>`. For example:

``` html
<a href="http://www.google.com">Google</a>
```

The above tag will navigate to Google when clicked.

#####`<img>`

The image tag is a *self-closing tag*. That means you do not need a closing tag! It uses `src` (or source) to find the required image. The url can be local (on your computer) or online. `<img>` also uses `alt` which can be filled by text if the image is not found, and read by page readers. For instance:

``` html
<img src="http://images.ftw.usatoday.com/wp-content/uploads/2013/05/freehugs.jpg" alt="Tim wants a hug">
```

If the image is not found, the text "Tim wants a hug" will appear on the page instead.

#####`<form>` & `<input>`

We use these a ton in WDI when we have data we want to persist, but for now, just understand that they have their own attributes, such as `for`, `value`, and `type`.

Additionally, `<input>` is also a self-closing tag, but `<form>` is not.

##Attributes

#####`class`

`class` is an attribute used when you want to target several elements at once for styling or functional purposes.  The class attribute can be used on any HTML element.

```html
<h1 class="pink">Hello!</h1>
<p class="pink">This is a paragraph.</p>
```

For the above tags, any style you assign to the `pink` class in your CSS file will be applied to both the `h1` and `p` tag, because they both have the `pink` class.

#####`id`

`id` is an attribute that can be used in a number of ways (with any html tag with content, aka non-`<head>` elements). While it's often used as a very specific selector for CSS, it can also be used as a place to point to for site navigation and as a great locator for JavaScript. **Each id may only be assigned to one HTML element.**

```html
<h1 id="myHeader">Hello!</h1>
<p id="paragraph1">This is a paragraph.</p>
```

## Conclusion

We've now covered the basics of an HTML page. Below are some references beyond this markdown if you need any additional resources.

Let's review a bit before moving on to building a couple of pages!

1. Explain the roles of the following in an html document: tag, attribute, and content.
2. What does the `alt` attribute do for us in an `<img>` tag?
3. What is a self-closing tag and name an example?

### References

[MDN HTML Element Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

[MDN HTML Attribute Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes)
