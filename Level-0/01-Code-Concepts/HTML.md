# HTML

HTML means HyperText Markup Language. It is the rules used to dictate how the computer should display information.
Conversely, it is also the framework by which new web pages are made. Think of HTML as a set of rules or instructions about
how to display information to and from the internet.

When you search for information on the internet, most of the time you just type in what you are looking for into the
search window of your favorite search engine. The engine then looks for anything that might match your request and returns
it to you, usually as a list. You then select the specific page you would like to view. The browser sends a request to
a server asking for the page you have requested. The browser then returns the page to you view. But how does the browser
know what information to display and in what format it should display it? That's where HTML comes in.

HTML is the instruction manual that tells the browser how to build a web page to be displayed on your computer.
It is similar (but is not) to a coding language. A sinlge page of data is divided into discrete sections.
These sections are then arranged in the way the author wishes for them to be displayed.
Text and images are placed inside these sections. You could think of it as very similar to the layout of a newspaper,
but with some added features.

## HTML Tags

The means by which different sections of a page are divded is the use of tags. These tags surround the contents of one
chunk of data or text or image. It looks like this:

```html
<div>This is a division of a page</div>
```

Notice in the example there is a beginning marker `<div>` and an ending marker, `</div>`. These markers are called `tags`.
The entire section desiginated inside a set of tags is called an `element`. `<div></div>` are the tags.
The whole thing, `<div>This is a division of a page</div>`, is an `element`.

There are several types of tags. Usually, they follow the open/closed format, but not always. There are a few that
only have one tag. We will cover those later.

### Boxes in boxes

In its simplest form, a web page consists of boxes (elements) inside boxes (bigger elements). It looks like this:

```html
<div>
  <p>This is a paragraph element</p>
</div>
```

In the example we have a paragraph element (so designated by the `<p></p>` tags) nested inside of a larger div tag.
The entire web page consists of these nested tags
laid out in a specific order.

### Attributes

An attribute is used to specify a particular property of an element. Different element tags have different attributes.
These are used to more specifically define properties
on a particular element. It looks like this:

```html
<img alt = "banana" />
```

The above is a tag used for images. It contains and attribute called `alt`. This is short for "alternate".
It is used to descibe what the image is to visually
challenged users or in the event the image is not viewable.

You could say that the element puts a thing on the page. The attribute further describes the thing you put there or
gives a command to the browser regarding what it
should do with the element. In the example above
we put an image there.
We then added an attribute to give a
alternative description to the image. We could have (and probably *should* have)
also put the width and height of the image.
It should look like this:

```html
<img alt = "banana" height = "100px" width = "100px"/>

```

We now have three attributes added to our image tag.
This tells the browser that there is an alternate description for the image, that the image is 100 pixels high,
and the image is 100 pixels wide. Attributes are placed inside the opening tag of the element.

There are hundreds, maybe thousands, of different attributes.
It would be impossible (and unnecessary) to try to learn them all. A better way to go about it is to understand
what an attribute is, then look up the one you need.
Of course, there are a few that you will use all the time.
Just for your own convenience, you will probably want
to commit those to memory.

### The Form

Forms are used when you want to collect information from a user. For example, say you want to have users log into your
web site. In order to collect their data you
would use a form. It looks like this:

```html
<form>
  <label for="username">Username:</label>
  <input type="text" name="username" id="username">
</form>
```

This bit of HTML will produce an input box with a label called "Username:". Let's break this down:

1. Line one is the opening tag `<form>`.

2. Next tag is `<label>`. This tag gives the textbox a label of "Username:" The opening `<label>` tag has one attribute.

3. The attribute in the `<label>` tag is `for`. This designates where the label needs to be placed.

4. The next tag is `<input>`. This tag tells the browser that there needs to be a input field placed inside the form.

5. The `<input>` tag has three attributes.

6. The `type="text"` attribute tells the browser what kind of input field should be there.
  In this case, it is a single line text field.

7. The `name` attribute gives the input element a name for the browser to refer to.
  Different input elements can have different names.

8. Last we have the `id` attribute. This gives the element a unique identifier.

The above is a common way that data can be
gathered from a user. It is not the only
way to do it, but it's a good place to start.

### ID's and Classes

Elements of an HTML page can be identified by either an ID or a Class, or both. It looks like this :

```html
<div id = "div1" class = "line1">
This is a div</div>
```

The `id` attribute is a unique identifier. That means that you can have only one `id` on an element. The `id` identifies
that specific element, and only that element. When you need to refer to the element, you can do so easily by using the `id`.

The `class` attribute is an identifer for multiple elements. You can have the same class on several different elements.
If you need to refer to a group of elements, you can do that by using a `class` name. Because an `id` identifies a single
element, and a `class` identifies a group of elements, it is possible to have both as attributes on a single element.
See the example above.

### Why Do We Need ID's and Classes

Classes and ID's are used for a few things. First, they are used in styling the page. By listing the ID's and Classes in the
CSS file, the browser can understand what element(s) you are referring to. (We will go over what a CSS file is later) ID's
and Classes are also used in your Javascript files. When manipulating elements using Javascript, the browser
needs to know which elements you are referring to.

ID's are also used in URL's to direct the user to a specific section of a page.

### Some Common Tags

You can use any name inside of a tag that you want. The name does not have to designate any particular type of element.
If you use a word other than the designated tag names,
the browser will simply interpret the element as a `<div>` element. Even so, there are some standard types of
elements that have standard attributes.
It's a good idea to know what these are.
We will cover a few here.

```html
<a href="http://www.webPage.com">
This is a link</a>
```

This is an anchor tag. It tells the browser that the element is a link to another web page or file or even a section of the
same page. There is an attribute here as well, `href`. This stands for "hypertext reference". The `href` atrributes specifies
what you want to link to. The `href` value is a file path or URL.
This tag is used when you want to connect to another web page or if you want to link different parts of your own page.
It for *connecting* things to other things. You will always see this attribute inside of an anchor, `<a></a>`, tag.

```html
<img src="./pic.jpeg"/>
```

This is an image, `<img/>`, tag. It is used to embed an image into your page. It does not have an opening and closing tag.
It is called a self-closing tag. Self-closing tags are known as "void" tags. This is because they may not have any content.
This is different from a regular tag that may, but does not have to, have content inserted between the opening
and closing tag. The `<img/>` tag has an attribute called `src`. This stands for "source".
It tells the browser where to find the image you want to embed. The value is a file path or URL.

`href` and `src` are sometimes confused. They both seem to do the same thing. However, there is a difference.
The attribute `src` tells the browser where to find the resource to embed into the page. The attribute `href` tells the
browser to link two pages together, or a section of the same page. So, one *embeds* a resource. The other *links* pages
together. The confusion can happen because both use either a file path or URL.

```html
<ul>
  <li>One</li>
  <li>Two</li>
  <li>Three</li>
</ul>
```

These tags are for an `unordered list`. The "ul" in `<ul></ul>` means "unordered list". It is "unordered" because it
will not render list numbers. Instead, it renders a bullet point.
The other tag `<li></li>` designates a "list item". List items are nested inside unordered list tags.

These tags can have `class` and `id` tags for identification and styling purposes.
