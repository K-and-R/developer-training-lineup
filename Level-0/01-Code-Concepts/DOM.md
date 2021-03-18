# The Document Object Model

The Document Object Model is a pattern for organizing an html page into a logical order. This order takes the form of a tree
structure similar to the file structure of a Linux file system. It looks like this:

[The DOM Tree]("./../../../images/DOM-Tree.png)

Each block on the tree is called a `node`. A node is any point on a network that sends, receives, or contains data.
The terms `node` and `element` are often used interchangeably,
but they are not necessarily the same thing.
The first node is the Document element itself.
All other nodes are contained within the
Document node. Below the Document node there is the HTML element node.
Everything below this node is contained within the HTML node.

Any element will, of course, be contained inside the HTML node. However, notice that the `<body>` element is not contained
inside the `<head>` element. But both are contained inside the `<html>` element.

The `<a>` element has a a node extending from it that contains an attribute. It also has a text node extending from it as
well. These are called "leaf nodes". They are called this because they are at the end of the node tree just like a leaf
would be on a real tree.

## Why Is This Important?

The Document Object Model gives us a map of a webpage. Each node is listed out in relation to every other node.
We can see at a glance where everything is and what is connected to it and what is not. This is the blueprint the browser
uses to build the page on your screen.

Using Javascript we can manipulate the nodes of the DOM. We can make things disappear or add content, or send data to a
server, or have a slideshow, or.....Well, the possibilities
are only limited by your imagination.
If you can think it, Javascript can probably do it. This is how we make webpages interactive for ther user.

## DOM Methods

The way we are able to manipulate the DOM is by use of DOM methods.
With a DOM method we can select what elements we want to work with. There are many, many DOM methods, too many to list out
here. However. there are a few very common methods
that are used all the time. Let's cover those first.

```html
<div id = 'first'>

  <h1 class = 'title'>This is the title</h1>

    <p id = 'firstPara' class = 'para'> This is the first paragraph of the page</p>

    <p id='secondPara' class='para'>This is the second paragraph</p>
</div>
```

Above is a section of a webpage. It's a pretty simple layout.
We will refer to this section when descibing the following DOM methods.

If we wanted to select just one, specific element we would use:

```javascript
document.getElementById('first')
```

This method selects the element with the id attribute of "first".
In this case, the element selected would be the
`<div>` element. Usually, this method would be
assigned to a variable like this:

```javascript
var firstDiv = document.getElementById('first')
```

Now, instead of having to write out the whole
method we can just refer to it as `firstDiv`.
This is makes the code easier to read.

If we wnated to select a group of elements we could use this:

```javascript
document.getElementsByClassName('para')
```

This will select *every* element with a class name of `para`. You can also use:

```javascript
document.getElementsByTagName('div')
```

This will select every element with a `<div>` tag name.
We can also select elements by using a CSS selector:

```javascript
document.querySelector('#foo')
```

This selects the first element with a CSS id of "foo".
This can be a little confusing because the `id`
attribute is used for selecting an element using
a method *as well as* defining
CSS rules for the element. It looks like this:

```css
#foo {
  color : red;
  fonct-size : 12px;
}

```

```javascript
document.querySelector('#foo')
```

The `#` refers to the CSS Selector id, `#foo`. Now look at this:

```javascript
document.getElementById('foo')
```

This refers to the element id, `foo`.
Yes, I know, the id `foo` is used for both.
But for one, `#foo`, you are referring to
the CSS selector. The other one refers to the element attribute, `id='foo'`. When you use `document.querySelector()` the
first element with the specified CSS selector is selected.
