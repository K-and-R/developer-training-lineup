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

### HTML ("Hypertext Markup Language")

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

### CSS ("Cascading Style Sheets")

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
must do with the request it has received.
This is just as if a crew member on our hypothetical spaceship pushed a button to increase the speed. The command input
(maybe a button or something) is sent to the engines.
In order to increase the speed
of the engine, more fuel must be pumped into them. The action pumping the fuel, as well as knowing how much fuel to pump
is handled by the "back end" so to speak. In the case of our particular ship, when the command is executed a signal is
sent back to the control panel confirming it was done.

It is the same with our application. A request is sent via the control panel (webpage). It is handed off to the
instructions stored on the server. The request is
fulfilled, and a response is sent bask to the webpage.

Now you know how the whole thing is supposed to work.
If you work on the control panel, you are working on
the front end. If you are concerned with what the server is supposed to do,you are working on the back end.
The only thing we out was the database.
We will get to that in a second.

### HTTP

HTTP stands for `Hypertext Transfer Protocol`. A `protocol` is a set of rules governing the exchange or transmission of
data between devices. HTTP is a set of rules that govern the way clients and servers communicate to each other.
A `client` is something that makes `requests`.
A `server` is a thing that receives requests and
delivers responses to those requests. A client can be a person, or it can be another device (like a browser). A server can
be a computer that is optimized to send and receive data, or it can be an application that does the same thing.
Because there are so many  different things that can act as a client or a server, it's easier to understand using the above,
very basic, ideas. Servers take requests and give return responses. Clients make requests and receive answers to those
requests. A very common analogy is the diner/waiter analogy. A diner sits down at a table in a restaurant. The waiter comes
to the table and waits for the diner to give him his order.
The waiter then goes and gets what the diner ordered. The waiter either returns with what was ordered or he returns to tell
the diner why he could not bring the order.
The diner is the `client`. The `server` is the waiter.

So, what does this request actually look like?
Well, you have likely seen a request and never knew what it was. Whenever you see `http://somewhere.com/media/cat.jpeg`
you are looking at a request.
This is just an example, but it is valid syntax for
making a request. There is more to this.
Let's break it down.

* `http://`

    - This part specifies which set of rules you want to use for this request. Usually, this rule set (or protocol) is
    HyperText Transfer Protocol. However, there are other rule sets for different types of resources. HTTP or its secured
    version, HTTPS, are the most common.

* `Domain Name`

    - This is the authority that governs the namespace. When you see something like `myWebSite.com` you are looking at
    the domian name. There are things (resources) that
    live in that domain (namespace).
    A `resource` is anything that can be
    accessed. It can be anything, a file, a picture, an application, whatever.

* `:80`
    - This is the port number. It is the "gateway" into the server. This is optional. If you don't specify it, it defaults
    to 80 for http and port 443 for https. However, if there is a different port number than the two above, it must be
    specified in the request.

* `path/to/file.html`

    - This is the file path to the resource. In the past, this was an actual file path to a file on a physical machine.
    Today, it is really just an abstraction, but it does the same thing.

* `Parameters`

    - These are key/value pairs that do extra stuff before returning the resource to the client. There are several of these.

### HTTP Request Methods

Request methods indicate what you want to do with a resource. If you just wanted to see a web page you might use a `GET`
request method. If you were saving data to a database you
might use a `POST` request method. Let's take a look at them:

* `GET`

    - The GET method requests a copy of the resource. GET requests should only retrieve (GET) data.

* `HEAD`

    - This is the same as the GET request, except without the response body

* `POST`

    - This is used to send something to the resource. If you were to log-in to an account, your log-in data would be *posted*
    to the resource (website, for example) on the server.

* `PUT`

    - This method is used to update or create a resource. This is the different than the `POST` request. The entire resource
    is replaced by the contents of the PUT request. The `POST` request adds data to the resource, but does not replace
    or update the resource itself.

* `DELETE`

    - Deletes the resource in the request.

There are a few more of these, but the ones listed above are the most common.

### Ports

Computers connected to the internet use a set of rules (protocol) in order to communicte to each other.
This protocol is called `TCP/IP`. The letters mean `Transmission Control Protocol` and `Internet Protocol` respectively.
There is also `UDP`. These letters mean `User Datagram Protocol`. There is a difference between `TCP` and `UDP`, as you
would imagine. TCP establishes a direct connection between two or more computers. This connection remains for the duration
of the data transfer. It is then closed. UDP is a little different. Instead of a direct transfer of data, the UDP sends
bundles the data into a package. This package is then sent out into the internet and will hopefully arrive where it is
supposed to. The difference her is that UDP does not establish a direct connection to the recieving computer. It relies,
instead, on the devices in between the two computers to
route the data.

Using UDP there is no quarantee that the data will arrive where it is supposed to go. However, it has a low overhead, and
the likelyhood is pretty good that you will get the data.
But sometimes, maybe, you won't.

### TCP and UDP Ports

Every device connected to the internet has a unique identifier. This is known a s an IP address. It is a number that is
associated with a particular device. In the past, it was pretty much only computers that had IP addresses. These days
*anything* that uses the internet for anything has an IP address. Printer, cameras, phones, and a whole host of other things
can connect to the internet. All of them have IP addresses.
Without an IP address, there is no way of knowing which
device is which. Hence, the server will not know where to
send the data that has been requested.

Each IP address has a series of "channels" that send and receive data. These channels are called `ports`. There are *a lot*
of them. 65,535 for both TCP and UDP to be exact.

When you send a request to a web server (a server that has a webpage(s) stored on it) your computer will send the request
from a random port (any one of the 65,535 ports available).
The server, if it is using the HTTP protocol, will be "listening" for incoming connections on port 80. When the request is
received and the response returned, the connection closes. That means for every request made to the server a connection
is established, a request is received, request response sent,
and the connection is closed. Your computer ends the request from any old port available. However, the server
(when using HTTP) is listening for the request on port 80.
Not to beat this to death or anything, but remember the
server is bound to port 80. The connection is established,
data is transferred, and the connection is closed each
and every time a request is made.

### HTTP vs. TCP/IP

There are several different sets of rules (protocols) that exist for the purpose of allowing computers the communicate to
each other. HTTP is a set of rules that tell the computer
how to transfer *information* from one place to another.
TCP/IP is the set of rules that determines how the *connections* are made between computers. When we are talking about TCP/IP
we might include the subject of ports. However, when discussing HTTP, we really don't care about the port. We are just
talking about the information that moves through the connection. You could think of TCP/IP as the road, and HTTP as the
thing transported on that road.

### HTTPS

HTTPS means `HyperText Transfer Protocol Secure`. While HTTP uses port 80 to listen for requests, HTTPS uses port 443. The
difference is security. HTTPS encrypts the data that is
sent over the connection.

In order to use HTTPS instead of HTTP, you need to get an SSL Certficate. SSL means `Secure Socket Layer`.
The certificate is actually a small data file that binds a cryptographic key to an organizations details.
This makes your website secured. This is necessary
to protect visitors to your website personal information, including financial data that may be needed for transactions over
the internet. There are several different kinds of SSL Certifcates. Each provides a different type or different degree of
security. SSL Certifcates can be obtained for free, but larger oganizations will pay for certs that provide greater security.
If your website handles personal information you will need
to use HTTPS instead of HTTP.

### Databases

A database is an organized collection of information stored in a computer system. A database is usually accessed using a
database management system (DBMS). Let's translate that.
A database is a giant bucket. It contains sets of
smaller buckets that hold data. The buckets are organized in a logical way. If you want to get, add, change, or
otherwise mainpulate the data in a database you have to use a
tool called a `database management system`.
Because of the computer worlds' love of acronyms,
you will often see a database management
system referred to like this, `DBMS`.

Why use a database? If there is data that you want to hold on to and access later, a database is the way to go.
Things like passwords, account information, names, birthday, anything that you want to keep for a long time  all
things stored in a database.

A database organizes the data stored in it in a logical way.  This allows for the best efficiency when storing or retrieving the data from it.  The database is organized into 'tables'.  A 'table' is a rectangular configuration of 'cells'.  You could think of it as a sheet of graph paper.  A column of cells of a particular data type (text, number, date, etc.) is referred to as a 'field', typically given some meaningful label, such as: 'FirstName', and will be referred to as the 'FirstName field'.  Other such fields may be 'LastName', 'DateOfBirth', etc.  Each cell is then filled with a 'value' that corresponds to that 'field'.  Each row is called a 'record'.  Information is typically entered one record (row) at a time, field by field.  The value in a cell is simply that, the 'value'.  A database can have more that one 'table'.

Each database table has a 'key field' which is meant to be unique (think serial number or identification number). In this case, let us suppose an 'ID_Number' field.  For example, I may have the information of many people (think 'records') in my database and I want to know when Bob's birthday is.  If I make a request to my database to search the 'FirstName' field (the column labeled as 'FirstName') for the cell containing value 'Bob' and then to search that record (go across the row) and tell me the value of the cell in the 'DateOfBirth' field (column) for that record, I will get a list of the dates of birth for all people in my database with the first name 'Bob', which could be many (go to http://howmanyofme.com to see how many people have your same name).  But if I know that particular Bob's ID_Number (suppose 123456), then I can make a request to my database to search the 'ID_Number' field (the 'key field' in this example which is unique for every record) for the value '123456' and to tell me the value found in the 'DateOfBirth' field of that record, I will be given one and only one answer.

![DatabaseGraphicFinal5x7](https://user-images.githubusercontent.com/99445778/154956332-10d9cf7c-23d0-4ed9-aa3e-d97825e5bbe5.png)

A database will usually have many tables stored in it. These different tables are related to each other.
For example, you might have a table that holds customer data. That might include a name, an address, an account number, etc.
There can be (and often are) several different tables all holding data. These tables contain data that are related to each
other. By accessing these different tables all kinds of different reports, analysis, and other combinations of the data
can be formed. This type of database that uses tables is called a `relational database`. This is the most common type of
database. There are several other ways to organize data in a database. These are all referred to as
`non-relational databases`.

### SQL

The database is a thing in itself. It is just a storage structure. So, how do we manipulate the data in the database?
We use `Structured Query Language` or `SQL`.
This is a language that is part of the `RDBMS`
or `Relational Data Base Management System`.
Just to avoid any confusion, there are three parts here.
There is the database entity itself, there is the RDBMS,
and there is SQL. SQL is a *part* of the RDMS. It helps to have a lay of the land with this stuff. You will use SQL.
It is part of the RDBMS used to manipulate data stored in
the database. That is the relationship between these different things. This section will focus on basic SQL.

### Clauses

A `clause` is text that the database recognizes as something it needs to do. `Clauses` ALWAYS end with a `;`. Pay very
close attention to the semi-colon at the end of clauses.
If you forget, trouble ensues. I say this from painful experience. Here is what a clause looks like:

```sql
SELECT * FROM my_database
```

SQL clauses are always capitalized. This clause says, *"Select everything from the database called "my_database"*.
The "everything" part is designated by the `*`.
The asterisk is referred to as a "wild-card".
It means "everything" or "give me whatever you got".

All data in a database has a `data type`. A `data type` is a certain kind of data. Some types are words, or `strings`.
Some are numbers, or `integers` etc. There are many data types. Here are some of the more common ones:

* `INTEGER`

    - Any positive or negative whole number.

* `TEXT`

    - A text string

* `DATE`

    - The data formatted as YYYY-MM-DD

* `REAL`

    - A decimal value

Statements can have `parameters`. This is similar to function parameters. It looks like this:

```sql
CREATE TABLE table_name (
  column_1 data_type,
  column_2 data_type,
  column_3 data_type
);
```

This clause includes a list of parameters. Parameters are a list of columns, data types, or values that are passed to a
clause like arguments to a function.

If we want to create a new table, we use the clause
`CREATE TABLE`.
This clause tells the database that we want to make a new
table rom the beginning. Remember, our new table has
no data in it yet. It is just an empty table. We need
to give this new table a name and we need to tell
the database what the columns are going to be.
It looks like this:

```sql

CREATE TABLE persons (  idnum INTEGER,
                        moniker TEXT,
                        age INTEGER
                    );

```

In the above example, we see the parameters give the column headings (id, name, and age). We then specify what *type* of
data the column will hold (INTEGER, TEXT, and INTEGER).

We now have our table created. But is has no data in it.
We will use the INSERT statement to accomplish this.
The clause we will use is pretty straight-forward.
It looks like this:

```sql

INSERT INTO persons (idnum, moniker, age);
```

Now, we must provide the values that we want stored in the new record. Looks like this:

```sql
INSERT INTO persons (idnum, moniker, age)
VALUES (1, 'Bill Smith', 22);

```

Now that we have some data in our table, we can access that data using the `SELECT` statement. Looks like this:

```sql
SELECT moniker FROM persons;
```

This will give all of the data from the 'moniker' column. If we wanted *all* of the data in the table we would use the
'wildcard' character like this:

```sql
SELECT * FROM persons;
```

SECTION INCOMPLETE

Why do we care about this? Webpages are designed to be interactive. "Interactive" means that clients can request information
from the website. They can also store information on the website (actually, it is stored on a database associated with the
website.). In the past, only textual information could be requested and returned. But that was quite a long time ago. Today,
anything that can be stored on a server can be requested and returned or sent to be stored. That includes applications,
images, videos, whatever. Collectively, anything that can be stored on a server is referred to as a `resource`. You will
often hear the term `web resource`. It just means a thing stored on a server that can be accessed. We care about this because
we want our website to have the ability to send information and to receive information. This is what makes them useful.
Without this ability, a website is really just an electronic bulletin board. If we want our website to do anything
more than display data, we need to make it interactive.
