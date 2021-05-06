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

