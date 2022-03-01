# The Browser

A browser is a piece of software on your computer. It allows you to make requests for information from the World Wide
Web. When that information is returned to the browser it will assemble the information into the format specified by
instructions from the webpage itself. We will cover the parts of the browser and how to use it to view web pages on the
internet.

## Internet Protocol Address (IP)

Your specific machine has an identification number unique to it. This is called an IP address. This is your "home"
address. Data that you request from the internet is delivered to you using this address. It is usually a set of four
groups of numbers each separated by ".". As the internet has grown the number of IP addresses has also increased. Such
was the increase that we ran out of four unit sets of numbers. To solve this problem a new standard for IP addresses has
come into use. This one uses a larger set of numbers. You may see both of these written as IPv4 and IPv6 respectively.
All it means is *Internet Protocol version 4* or *Internet Protocol version 6*. You can find the IP address of your
machine by opening a terminal window and typing: hostname -I. You can also open your browser and type "What is my ip" in
the search bar. The browser will tell you your IP addess.

## Domain Names

A domain name is an actual name of something substituted for the IP address. IP addresses are just sets of numbers. You
can think of a domain name as an alias for the IP address number. Instead of saying. "I would like to connect with
172.16.254.1, please" you can say, "Connect me to Bobby's house." Bobby's house and the IP address number is the same
thing. One is a human readable name and the other is the number associated with it. Domain names are organized in a
heirarchy starting with regions and going down to individual machines and locations on the internet. Suffixes like .com
or .edu are known as top-level domain names. These govern regions of types of locations. A suffix like .gov is concerned
with goverenment information. A suffix of .edu is concerned with the subject of education. This is used to keep things
organized. The most common Top Level Domain name is .com. This means "commercial". It is used by websites that are doing
business online. However, any website can use the .com TLD name. The Top Level Domain is concerned with grouping areas
of the internet together based on the type of content the website has. So, if you had a URL like My_Page.com, the ".com"
means the website is out there on the public internet. The "My_Page" part is the alias for the IP address of your
website.

## Uniform Resource Locator

* Every web page on the internet has a specific location where it can be found.

* This location, or "address", is called a Uniform Resource Locator, or URL. It tells the browser where to look for a
  particular web page.

* The browser is often confused with a search engine. These are actually different things.  A search engine is a
  website that lists the locations of other websites. Once you find what you are looking for, you still have to tell
  your browser use the URL to request the data. This is a little deceptive because in order to "use the URL to locate
  the data" is really just clicking on the listing in the search engine. Even though it is deceptively simple, it is
  important to understand that the simple click on a search engine listing is, actually, a request from the browser for
  information located at a specific address (URL).

* If you know the URL of the resource you wish to view, you can skip the search engine altogether. All you need to do
  is enter the URL in the window at the very top of browser window. The information will be requested, returned, and
  assembled for you just as if you had clicked on a search result. And it's faster using the search engine.

* Search engine pages are often displayed as the first thing you see when you open your browser. This is partially the
  reason why there has been some confusion between the two.

* The URL address has parts to it just like the address for your house. It is a good idea to know what each of these
  parts are when using a URL. Here they are:

    * `http` or `https`
        - This means Hyper Text Transfer Protocol or Hyper Text Transfer Protocol Secure. A Protocol is a set of rules to be
        used by the browser when requesting and receiving information.

    * `:`
        - This comes right after the HTTP or HTTPS. It has a purpose, but getting into it will confuse you. For now,
        just know it is needed and where it goes.

    * `//`
        - This is a double-slash. Again, there's reasons for it, but it will confuse you. The specifics of these
        symbols will be covered in later modules. For now, just know its needed, and it comes after the :.

    * `www.domain-name`
        - This is the actual address of where your website is located.

After the domain name you may see additional / marks and names of things. This is a file path. It is the road to travel
to arrive at the specific file you are requesting.  There are quite a few other symbols in there too. We will cover
these in a later module. For now, the basic form of the URL is all you need.

The URL window is located at the very top of the browser screen. Usually just below it is the search window. The search
window is for searching for a website. The URL window is for times when you already know where you want to go (In other
words, you already have a URL available to you).
