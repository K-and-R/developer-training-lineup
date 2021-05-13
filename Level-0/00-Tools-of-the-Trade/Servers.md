# Servers

The term "server" can be very confusing to new developers. Even some more experienced developers are a little fuzzy on
the subject. Here, we will try to keep it very simple.

Server: A piece of computer hardware *or* software that provides functionality to other programs or devices.

That definition covers a lot of ground. Let's break it down a little further. A server *serves* a *client*. Think of a
restaurant. The server is the waiter and the diner is the client. The diner orders what he wants to eat and the waiter
goes and gets it for him. Ah, but wait! There's more. What if it was a very fancy restaurant? In this case, you might
have a different waiter for each item you wanted. There might be a wine waiter and dessert waiter and table setting
waiter and so on. Well, that's how it works with computers as well. There can be (and often are) several different types
of servers depending on what you want to do. There can file servers for files and web servers for web pages, and
database servers for databases, etc. Because there can be so many servers of different types and functions, it's much
easier to think with the most basic expression of what a server is. It is a machine or a package of software that does
something for you when you tell it to. It can live on a machine located far away from you or it can live on your machine
itself. A computer can be *both* a client and a server. The server part is the software that gets or does something for
you when you make a request for it to do so. Usually, however, the server is located on a different machine living
somewhere else. Your computer (the client) communicates to the server. The server then responds to your request by
sending you data or performing a task. As a Web Developer, you will work with servers everyday.

## Localhost

As stated above, one computer can operate both as a client and as a server. When using localhost you are using your
computer both as the client and the server. This server does not have access to the rest of the internet. Localhost is
used in the development process when working on a web based project that requires a server component, but you don't want
just anyone on the internet accessing it. You can store your own webpages on your computer and call them up again using
localhost.  You access the localhost by typing "localhost" into the URL window in your browser.

## Virtual Machines

A virtual machine is a computer that is created by your computer. It behaves exactly as though it were a completely
separate computer running on its own. It is not connected in anyway to your computer. It does not have access to any of
your files or applications (unless you let it). Think of a virtual machine as a computer created by your computer that
functions as a separate machine. The virtual machine *does* depend on your computer's CPU and it borrows some memory
from it. This makes sense because memory and the CPU are hardware that a computer cannot function without. Other than
that, a virtual machine is a totally separate machine running on your machine.

These are used when you want to isolate applications from outside access. They are also used for security purposes and
when you want to run a different operating system but don't want to get rid of the operating system you are already
using. You can just install the different OS on the virtual machine. Often, virtual machines are used to run server software.
Several server software applications can be run from a single machine.
The downside of virtual machines is that they do use
CPU and memory resources from your actual machine. As a result of this, you may experience some slow down of your
computer when running one or more virtual machines.

## Client-Server Overview

what is the internet? Just to keep it really simple, it is a network of computers that are all connected together.
Each computer on the network has the ability to send
an receive information to each other. There is a lot going on behind the scenes to make that happen, but at the
end of the day that is what the internet is.

What does "connected" mean?  Right, what does connected really mean? Well, there are two ways to connect a computer.
The first way is by using a physical cable to connect to each computer. Usually, the cable is ethernet. It is similar to
the old phone connectors from days past. However, there is a problem with this method. There are billions (maybe trillions)
of computers and devices connected to the internet. In order to have access to all, or even a tiny fraction, of these you
would need thousands of miles of cabling and a billion connection ports on your computer. So, Ok, that won't work.

There is another way to do it. You could use the existing lines available before there was an internet.
You know, the telephone lines. Even before there was an internet there was a phone line network. You could call anyone
pretty much anywhere. These lines are now used for the transmission of data between computers as well as telephones.
Over the years these lines have been optimized for internet use.

There is a lot to know about the inner workings of the internet. You don't need to know all of it right now.
All we are concerned with here is how the internet is used to send and receive data to and from your webpage. But don't worry
we will get into the details of the internet in a later section. For now, let's focus on how this network works for you.

Front-End vs. Back-End
There is sooooo much bullshit tossed around about this subject. I have seen guys give lectures that go on for hours.
And worse than that,every second is coma-indicuing boredom.
So, no lectures, or verbose descriptions, and I won't even discuss the deep philosophical ramifications of world-wide
connectivity. Nope. I am going to just tell you what
it is and what it does and why you care.

## Front-End

The front-end is the end used by the user. When you check your bank balance on your phone, you are using the front-end.
When you are binge watching YouTube, you are using the front-end. Any user interaction with the webpage is front end.
The front-end can be broken down into three separate parts.
These are HTML, CSS, and JavaScript. Let's briefly look at each.

### HTML

This is not really a programming language.
It is more of a set of instructions to tell the browser how to display information. It does have some features that make
it seem like it is a programming language and it does use some "logic" to help you lay out your page,but it isn't
really a language for telling the computer what to do. We have a section on HTML. It is mentioned here in a simplified
context as it relates to the over-all front-end.
Think of HTML as giving the page its
structure. It will put things where you tell it to put them.

```html
<!-- The div is a block designated as a separate portion of the page -->
<div>
  <p> This is a paragraph block that lives inside the div.</p>
<!-- This paragraph element is a separate block that lives inside the div block -->
</div>

```

### CSS

This is code used to make the data on your page pretty. It handles fonts, and colors, and positions on the page of your data.
HTML puts the blocks of data on the page. That's about it. CSS lets you more precisely craft how you want that data to look.
You will find that there is a certain amount of bleed over between HTML and CSS. You can sometimes do the same thing using
HTML or CSS. This lack of definition can be confusing for some. How do you know which one to use? CSS is for styling.
Styling means "a distinctive apppearance, typically determined by the principles according to which something is designed.
Think of HTML are the scaffolding and CSS as adding the pretty details.

```css

#section {
width : 100px;
height : 200px;
background-color : red;
color : green;

}
```

In the example above the CSS directs that the element id `section` should be 100 pixels by 200 pixels in size, that the
background color of the element should be red, and the
font color should be green.That's all styling of the page. CSS can do other things, but basically this is what it does.

### JavaScript

JavaScript is a coding language. It allows the user
to interact with the webpage. When the user pushes a button or clicks on a link or logs into their account JavaScript handles
the logic to make that happen. Way back when, there was no JavaScript.Webpages could not be interacted with.
There were no buttons to click and no log ins,and no comments section. There was only a page of information.
You could request to look at the page, but you couldn't really interact with the page in any significant way.
JavaScript was invented for the purpose of allowing users to interact with a webpage.

```javascript
var pageElement= document.getElementById('page');

pageElement.addEventListener('click', () => {
  pageElement.style.color = green;
});
```

In the above example we have captured an element of the webpage. We then assign an event listener to it.
Done correctly, when the element is clicked any text
in the element will turn green. Granted, that's not
super useful or even particualrly intelligent.
But it is a example of allowing the user to interact
with the web page.

Ok, that's the front end. There is quite a lot you can do
with the front end. So much, in fact, that you could have
a long, successful career just working with the front end. But wait! There's more!

## Back End

The whole point of the internet is to be able to send and receive data from multiple computers all over the world.
Browsers were made for the purpose of requesting data and displaying that data to the user. The back end is the code
that makes that happen. You could think of the front end as the control panel of a vehicle. The operator of the vehicle can
give "commands" to the vehicle by turning a wheel or pushing a pedal. But what happens after that? There is a whole network
of linkages that go to work to execute the command input from the user. This could be thought of as the back end.

While it is possible to code the back end using JavaScript,
it is usually done in a different coding language.
PHP, Ruby, or Python are examples languages that are
commonly used for back end coding.

### Parts of the Back End

The first part of the back end is the `server`. What is a server? It is a computer that is optimized to "listen" for requests
from clients. Your computer could be used as a server. The difference is, you have all kinds of different apps,
pictures, music, personal files, etc. The server does not have these things. It only has the application you are contacting.
They arw called `servers` because they serve client (user) requests. It should be taken into consideration that it is not
only users that are clients of servers. *Any* request from anything is considered a `client`. Sometimes other
can make requests of servers. Whatever, or whoever, is making the request is the `client`. Anything that responds to requests
is a `server`. Sometimes the server is not necessarily
a physical machine. It's not important to distinguish between each of the various types of servers right now. The main point
here is `clients` make requests. `Servers` respond to requests.

The next part of the back-end is the application itself. This is the actual computer program that is running on the server.
It listens for client requests, retrieves information from a database, and sends a response back to the client.

Lastly, there is the database. A data base is a structured set of data held in a computer. It is a big storage facility that
lives on a computer somewhere. It stores information in an organized system. Anything that you want your app to
"remember" would be stored on a database. The database is a separate thing from the server. It might live on the server,
but it exists as its own entity.

Understanding the relationships between the server, application, and database is important. Understanding what these things
are and how they relate to each other helps a lot when you start digging deeper into them. The server contains the
application. The database may, or may not, live on the server.
The app listens for requests. When a request is received, the app will likely make a request to the database for data.
Then the database returns the data to the app. The app takes that data and prepares it to send. It will then send the data
back to the client who made the request (This is not the user, but rather the users' browser ).
The browser takes the data it has received and displays it to the user.

This is ony intended to give a very broad overview of how the system works. Wherever it has been mentioned that a
component *does* this or that it must be remembered that a developer had to write the code to enable that to happen.
So when I say, *"...and then the thingamabob does this"* it means a human wrote instructions for the computer to carry out
that task. None of this is automatic. There is code for sending a request. There is code to ask the database for data.
There is code to formulate and send the data back. Computers can't do anything on their own.
It requires a human to tell the computer what to do.

### An Analogy

All of this front/back end stuff can get confusing really fast. What goes where? How do I write that so it does what I want?
How do I even know what it is I want it to do?

It can be helpful to have something to compare to the thing you are having trouble with.
Analogies are good for this type of thing.

Think of the whole system of HTML, CSS, JavaScript, and Ruby as a single entity, like a, oh, I don't know, like a spaceship.
A spaceship has a variety of different systems that all do different things. You have engines and life support and
navigation and maybe even weapons, etc.
Each of these systems exist in their own right, but at the same time, must be integrated to some degree.
And all of these systems must be controlled, preferrably from a central location if possible. A computer application
shares many of these same attributes.
Let's compare some of them.

#### The Control Panel

You could think of the front end of an application as the control panel of the ship. The control panel allows us to give
commands, but it also supplies us with data we need to
operate the ship. It is the interface between the crew
member and the vessel itself. The front end of our application does very much the same thing. The user can "flip switches"
and "push buttons" and the page responds. Data can be sent, received and displayed on our control panel.

When a button is pushed on the control panel, a block of code is executed. This code is JavaScript. The request or command
that is sent from our control panel button then goes to the
system we want to control or get data from.

Once that request or command is sent another thing takes over. At this point in the process, the action of getting the data
or executing the command must be done.
This action, out of the view of the user, is performed by another language. Could be PHP, Python, Ruby,
or even C++.

Whatever language is used it is important to remember that we are no longer dealing with the control panel
(Our HTML page). We are now dealing with the computer
itself, not an application running on the computer
like a browser. The language used is not really all that important. They all basically do the same thing. They provide a
means to give the server instructions about what it
must do with the request it has received. This is just as if a crew member on our hypothetical spaceship pushed a button to
increase the speed. The command input (maybe a button or something) is sent to the engines. In order to increase the speed
of the engine, more fuel must be pumped into them. The action pumping the fuel, as well as knowing how much fuel to pump
is handled by the "back end" so to speak. In the case of our particular ship, when the command is executed a signal is
sent back to the control panel confirming it was done.

It is the same with our application. A request is sent via the control panel (webpage). It is handed off to the
instructions stored on the server. The request is
fulfilled, and a response is sent bask to the webpage.

Now you know how the whole thing is supposed to work. If you work on the control panel, you are working on the front end. If
you are concerned with what the server is supposed to do,
you are working on the back end. The only thing we
 out was the database. We will get to that in a second.
