# The Document Object Model

The Document Object Model is a pattern for organizing an html page into a logical order. This order takes the form of a tree
structure. Each element on this tree is an object containing properties and methods. All of them can be accessed just like
regular JavaScript objects. This is because they are
all regular JavaScript objects.

Attributes such as `class` or `id` are not nodes. Rather they are properties of the elements to which they are appended.
If the attribute is a standard attribute, like the ones
used for `class` or `id` or `href`,they will be added to the element object as a new property. It would look like this:

```javascript

document.div.class

```

The value would be the string given as the identifier. For example, let's say you had an `<a>` tag with an `href` attribute.
The value of the `href` property would be a URL written as a string like this: `'http://myPage.com'`

[The DOM Tree]("./../../../images/The-DOM-Tree.png)

Each block on the tree is called a `node`.
Each of these nodes is a plain old JavaScript object.
That means they can all be accessed
just like any JavaScript object.
The tree shows the heirarchy of the objects contained
within the DOM. So, what we have here is
a series of objects nested inside other objects.
All of the methods and properties of any given
object on the tree can be accessed.

## Why Is This Important?

The Document Object Model gives us a map of a webpage. Each node is listed out in relation to every other node.
We can see at a glance where everything is and what is connected to it and what is not. This is the blueprint the browser
uses to build the page on your screen.

Using Javascript we can manipulate the nodes of the DOM. We can make things disappear or add content, or send data to a
server, or have a slideshow, or.....Well, the possibilities
are only limited by your imagination.
If you can think it, Javascript can probably do it. This is how we make webpages interactive for the user.

## DOM Methods

The way we are able to manipulate the DOM is by use of DOM methods.
With a DOM method we can select what elements we want to work with. There are many, many DOM methods, too many to list out
here. However, there are a few very common methods
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
  font-size : 12px;
}

```

```javascript
document.querySelector('#foo')
```

The querySelector method can select an element by any CSS selector.
In the example above, the element is being selected by its ID, `foo`.
But you can use any selector associated with the element in the querySelector method.

It is more common to see `document.getElementById`
being used to select elements. There is not, unfortunately,
any hard, fast rules regarding this.
We suggest you use `getElementById` rather
then `querySelector` when selecting elements.
