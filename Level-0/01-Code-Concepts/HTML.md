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
on a particular element. 