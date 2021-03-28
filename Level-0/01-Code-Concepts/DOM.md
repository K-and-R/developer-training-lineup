# The Document Object Model

The Document Object Model is a pattern for organizing an html page into a logical order. This order takes the form of a tree
structure. Each element on this tree is an object containing properties and methods. This structure allows for computer
languages to interact with an HTML page.
Any language can interact with the DOM.
However, usually the language used is JavaScript.

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

## DOM Events

DOM events are actions taken by either the user or the browser that initiate changes to the DOM. Clicking on an element,
moving the mouse over an element, or pressing a key on
the keyboard are examples of events.

There are a couple of different ways to tell the browser you want to create an event. The first method is to use
`addEventListener`. This method listens for an event to occur. It is often used in conjuction with the DOM methods above.
It looks like this:

```javascript

let title = document.getElementById('title');

title.addEventListener('click', someFunction);
```

In the above example `document.getElementById('title')` selects an element with the attribute `id = 'title'`.
This element is stored in the variable `title`. This variable then has another method called on it,`addEventListener`.
This method tells the browser that the element stored
in the variable `title`should "listen" for an event to occur. The method takes two arguments. The first one indicates what
type of event to listen for. In the example, this event
is a `click` event. The second argument tells the browser
which function to call when a click is detected.
Let's look at the whole thing together:

```javascript

let title = document.getElementById('title');

let someFunction = function(){
  document.getElementById('title').innerHTML = "new title";
}

title.addEventListener('click', someFunction);
```

The first line stores the element in a variable called `title`.\
The next line is a function that changes the title element's
text to read "new title". The last line adds the event
listener to the element and specifies that the event to
listen for is a click of the mouse and the function to
fire is called `someFunction`.

When a user clicks on the `title` element the text will change to read "new title".

The above is just one way to add interactivity to your webpage. You can also register an event this way:

```javascript
document.getElementById('title').onclick = function(e){
  document.getElementById('title').innerHTML = "new title";
};
```

You can also use the `.on` method to do much the same thing as above. It looks like this:

```javascript
let button - getElementById('button');

let changeColor = function(){
  button.style.backgroundColor = 'red';
};

button.onclick = changeColor;
```

You are not required to write named function for either of these methods. You can use an anonymous function instead.
It looks like this:

```javascript
button.onclick = function(){
  button.style.backgroundColor = 'red';
};
```

or

```javascript
button.addEventListener('click', () => {button.style.backgroundColor = 'red'});
```

There is one big difference between using `.on` and `addEventListener`. If you are using the `.on` method you can only
register one event to the target element.
By using `addEventListener` you can add as many
events as you want to a single target element.
In the examples above only one event handler was
added using both methods.
If more than one function needed to be fired in
response to the event you would need to use
the `addEventListener` method. If it doesn't matter,
using the `.on` method works.

## Propagation and Bubbling

When an event is fired it is not just fired in the element where it lives. It is fired in *all* elements associated with that
element. The event travels outward to the outermost
element or it starts from the outermost element and moves inward.
All along the way it looks to see if there is an event
handler to call. If there is, it initiates the event handler.
If not, it moves on until it finds an event handler
that matches the event. In most modern browsers the
event takes a round trip, moving outward then
moving back inward. When the event travels *down* the
DOM tree it is referred to as `propagation`.
When the event travels*up* the DOM tree it is
referred to as `bubbling`.

Because the event travels firing any event handler
that matches the event, you can have multiple events
all fire at the same time. That may not be what is wanted.
`Propagation` and `bubbling` can be interrupted by using the method
`.stopPropagation()`. It looks like this:

```javascript
let textElement = document.getElementById('text');

let changeColor = function(){
  textElement.style.backgroundColor = 'red';
  e.stopPropagation();
};

textElement.addEventListener('click', changeColor);
```

In the example above, we have and element stored in the variable `textElement`. Next we have a function that changes the
background color of the target element.
It also has the `.stopPropagation()`. This will prevent
the event from traveling up and down the DOM tree.

Finally, an event listener is added to `textElement`.
When the element is clicked, the function fires and
the `.stopPropagation()` is called.  

## The Event Object

When an event is occurs and the function associated with the event is fired, an object is passed as an argument to the
event handler function. This object is called the `event object`.
It contains information about the event that has just occurred.

It looks like this:

```javascript
let changeColor = function(){

  event.target.style.backgroundColor = 'red';

  };
```

The event object contains all of the data about the event itself.
This object is the thing that does the traveling when the event propagates. 