# Glossary

* `ACSII`

    - American Standard Code of Information Interexchange.
    This is a standard for encoding letters and numbers. Computers do not understand letters *or* numbers.
    They understand "1" and "0" only.
    The ASCII standard assigns each letter and number
    a number. That number is then converted into binary
    (1's and 0's). Now, the computer understands what the
    number or letter is.

    Here is an example:  The ACSII numerical code of the letter "h" is 104. 104 translates in binary code to 01101000. The
    computer doesn't understand "h" or even "104". But it *does* understand 01101000. It knows that is the letter "h".
    A capital "H" has a different ACSII code.

* `Address`

    - A specific location in memory. A memory address is a location where data is stored. It has a alpha-numeric code.
    - In networking, an Internet Protocol address. This is an address that tells the computer where a resource is located
    on the internet.

* `AJAX`

    - Asynchronus JavaScript and XML. This is a set of web development techniques to create asynchronus web
    applications. Computers do not understand time. To the computer everything takes as long as it takes.
    When executing a series of instructions, the computer begins at the top and works its way down. Should the computer come
    across an instruction that may take some time to do, it will keep working on that insruction until it is done.
    Nothing else can occur until this instruction is complete.
    In other words, the computer can't "multi-task", at least not on its own.
    When a computer can only execute one instruction at a time, it is referred to as `single-threaded`.
    JavaScript is single-threaded. By using certain programming techniques, instructions that take longer to execute
    can be executed without interrupting the rest of the program. This is referred to as "asynchronus" programming.
    It is required because it can take some time to
    retrieve data from a server. If the code wasn't asynchronus, everything would just stop until the data retrieval process
    was complete. AJAX refers to the different technologies that allow that to happen.

* `Algorithm`

    - A list of instructions, procedures, or a formula that solves a problem. Even a recipe could be considered a algorithm.
    If you do so-and-so, then do this-and-that, you get a thingamabob. This would be an algorithm.
    Now, those instructions have to be consistent.
    In other words, if you always, always get a
    thingamabob if you do so-and-so and this-and-that,
    you have an algorithm for making a thingamabob. Algorithms are very common in mathematics. But, they are also very useful
    for creating computer programs. You could think of
    them as a set of rules for solving a specific problem.

* `Alpha`

    - An early test version of a piece of software or hardware.

* `Apache Server`

    - A popular brand of HTTP server. A very large number of HTTP servers are made by Apache. The technology is
    open-source, supported by ASF (Apache Software Foundation). It runs on Linux or other Unix based operating systems.

* `App`

    - Short for `application`. It is a program developed for phones or tablets. The term was popularized by Apple in
    conjuction with the release of the first iPhone.
    There is no difference between a computer program and an application. In reality, the term was introduced as a
    marketing scheme for iPhone. Today, the term `app`
    refers to a program that runs on a phone or a tablet,
    while a `program` runs on a computer.
    However, the truth is there is no difference
    between the two.

* `Argument`

    - Sometimes abbreviated to `arg`. It is a value that is passed into a command, function, or routine.
    Here is an eample of an argument:

```javascript
const addNumbers = (num1, num2) => {
    return num1 + num2;
};

addNumbers(3, 5);
```

The numbers 3 and 5 are the `arguments`. They are the actual values we want the function to add together. `num1` and `num2`
are just place holders. They tell the computer to expect the function to receive 2 values. They are called `parameters`.

* `Array`

    - A group of values defined by a single identifer.
    A `variable` is like a single box. The box has a name
    (whatever name you want to call it).
    Inside the box is stored a value. We can connect together a series of boxes and put values in each box.
    Then we can give the whole thing a single name.
    This is an `array`. Each box in our array is
    labeled with a number beginning with "0".
    It looks like this:

```javascript
var myArray = [3,6,12,23,48];
console.log(myArray[0]);
//Output will be "3".
```

* `Associative Array`

    - An array that utilizes strings instead of numbers to designate individual elements of the array.
    This arrangement is referred to as a `key/value pair`.
    Instead of having just a number to designate the location of a value, we use a string. This gives context to the value
    we have stored at that location. Different computer languages call this structure different things, but all of them use
    a string for the "key" and then a value of one kind or another.

* `Asynchronous`

    - An approach to writing computer programs that permit actions to occur outside of the normal program flow. Such programs
    are "non-blocking". This means that successive instructions can be executed even though a previous instruction has
    not completed. The code is not "blocked" (stopped from execution). see `AJAX`.

* `Attribute`

    - Name/value pairs that further define an HTML element. Different attributes can be applied to different elements.
    Some attributes are specific to a certain type of element. Others can be applied to a variety of different
    elements. Attributes provide information to the browser
    about an element.

* `Browser`

    - A piece of software that permits users to locate and view internet content. Data stored on remote servers can be accessed
    and viewed using a browser. Most browsers are associated
    with a `search engine`. A search engine is not the same
    thing as a browser. These two different programs are often confused.

* `Binary`

    - A base-2 number system invented by Gottfried Leibnitz. It consists of only two numbers, "1" and "0". Binary works
    very well for writing digital data to a computer.
    Bascially, a computer consists of thousands and thousands of switches. Each switch can either by on ("1") or off
    ("0"). Calculations can be executed using binary,
    referred to as `machine code`. Any computer language used by humans is eventually converted to binary.
    Otherwise, the computer would be unable to execute the instructions received.

* `Back-end`

    - The portion of a computer program that runs out of
    sight of the user. In web development, the back-end
    consists of writing code that governs how a server send
    data to users. The back-end handles accessing data from a database as well as determining what data is to be sent
    back as well as the format it should be sent as.
    None of these operations are
    apparent to the user.

* `Bash`

    - Bourne Again SHell. A `shell` is a command interpreter
    that executes commands from the user.
    A shell program allows a human to give commands to
    a computer. Executing commands in the shell is not quite the same as writing a computer program. These days, most
    everyone is used to using a mouse to click on icons placed on the computer screen. Alas, there
    was a time before that technology existed. A shell program was needed to execute commands that today would normally be
    done with a mouse. The original shell program was updated in 1989. That update was called the Bourne shell.
    The term Bourne Again Shell is an attempt at humor
    by persons who probably should have just stuck with
    programming.

* `Binding`

    - To create a connection between two or more programming object for a specified period of time.

* `Bit`

    - Short for `binary digit`. It is a single unit of information of either the value 1 or the value 0. Eight of these
    grouped together form a `byte`. Two `bytes` joined
    together form a `word`, or a total of 16 `bits`. All of these units allow the computer to store data in memory, and
    retrieve the data when needed. One bit is too small to store any useful information. For this reason, bits are grouped
    into bytes, and bytes into words. The smallest unit of
    memory is the `byte`.

* `Bitmap`

    - A type of file that stores graphics information (pictures). They can be identified by the file extension `.bmp` or
    `.dib`. These types of graphics files tend to be larger than similar types of graphics files. Therefore, their use
    outside of a Microsoft Windows environment is not
    recommended.

* `Boolean`

    - A data type that consists of two possible values, 0 and 1. The 0
    value is referred to as `false`
    and the 1 value as `true`.
    It is named for English mathematician, George Boole. His book, The Mathematical Analysis of Logic, laid out the
    principles of applying mathematics to decision-making. His ideas were very influential in computer programming and design.

* `Boot`

    - Sometimes referred to `boot up` or `start-up`, `boot` is the various actions a computers performs to prepare for
    operation. These begin whenever power is supplied to the
    system (When you turn it on).
    The computer will perform a self-
    diagnostic to ensure everything is operating properly.
    It will then load the operating system. Once the operating system is running, any additonal programs configured
    to run on start-up are loaded. Sometimes it is required that the computer `boot` again after software is added to
    its memory, or to handle a irregularity in its operation.
    You can `boot` the computer at any time. This is called `re-booting`.

* `Broadband Internet`

    - A telecommunications technology that provides high-speed internet access using multiple channels of digital signals
    all running at the same time. `Broadband Internet` provides fast interchange of data between devices present on
    the internet.

* `Bubble sort`

    - A type of sort that compares two adjacent values in a list. The values are either swapped in position or left
    alone depending on the condition of the sort. Each pair of adjacent values are compared until no further swaps are required.

* `Buffer`

    - A temporary storage area used to hold data while the computer is processing other data.

* `Bug`

    - A general term used to describe a error in the
    execution of a computer program or a malfunction in a hardware component. If a program has `bugs` it means
    there are errors in the code that prevent the program from functioning as intended. `De-bugging` is the term used
    to describe the action of finding and correcting `bugs`.
    This is a very large step in the program development process.

* `Bug-tracking`

    - The action of reporting bugs when they are found. The error and its resolution is recorded for future reference.
    There are several spftware programs that perform this acition. By keeping a central repository documenting bugs,
    developers can keep track of errors in the development
    process.

* `Computer`

    - A programmable device that stores, retrieves, and manipulates data. Computers recieve the input of data, manipulates
    that data, outputs the data, and stores data. Computers in modern times come all manner of sizes and
    configurations. Everything from a desktop computer to the microprocessor in an autonomous drone.
    If the device inputs, outputs, manipulates, and stores
    data, it is considered a computer.

* `CPU`

    - Central Processing Unit. The computers' CPU handles all of the instructions it receives from hardware and software.
    It is the "brain" of the computer.

* `Cache`

    - To store away in hiding or for later use. The name of the place where something is stored for hiding or later use.

    - A high speed access area reserved in memory. Data is stored in the cache for faster access to the CPU. The idea of
    storing information that might be needed again can be applied to anything that might need it. The idea is to make
    the processing of data faster. computers cache data that it uses frequently rather having to access that data from
    where it is stored in memory. In web browsers, data received from a server can be kept in the browsers cache.
    In this way the browser does not need to continually make requests of the server.

* `Callback`

    - A function that is passed as an argument in another function. It is called a `callback` because it is not executed
    until the function that receives it as an argument is, itself, invoked. The callback function may never be called.
    It depends on whether the parent function is ever invoked.
    If it is, the interpreter must go back, or *callback* to the argument function and execute that.

* `C:`

    - The designation for the first primary hard drive on IBM compatible computers (PC's). This disk drive is also
    sometimes referred to as `Local Disk` or `Primary Drive`.

* `char`

    - A data type used in some programming languages. It refers to `character`. A `char` data type holds one character.
    The character could be any character on the keyboard. JavaScript does not have a `char` data type
    (It doesn't require any sort of type declarations).
    However, it does have methods that act on characters. Methods like `charAt()` or `charCodeAt()` are used in JavaScript
    to return values related to the characters in a string.

* `chmod`

    - In a Unix-type operating system, this command is
    used to grant or restrict file permissions.
    It is laid out like this:
    `chmod options permissions file name`. `Options` refers to modifiers telling the computer how the command should
    be executed. `Permission` refers to what sort of permission should be associated with the file. `File name` is the name
    of the file to which permission should be applied.

* `Chrome`

    - A free internet browser offered by Google. It is very widely used throughout the internet community.

* `CLI`

    - Command Line Interface. An interface for interacting with a computer. Often CLI is used to refer to accessing
    network computers. This is correct, but incomplete.
    Any computer can be controlled using the CLI. When you are giving commands in the terminal you are suing the
    Command Line. The place you are giving the commands is
    the interface.

* `Click`

    - The action of activating the buttons on a mouse.
    `Click` also refers to a DOM event that fires a callback function when the 'click' event is detected.

* `Client`

    - A device connected to the internet that uses the resources of another device likewise connected. In the past, a client
    was a computer that connected to a server (another
    computer at a remote location). If a computer
    is the reciever of a server resource, it is the `client`. Today, there are all sorts of different types of
    devices that utilize internet resources. All of these could correctly be referred to as `clients`. These days, a server
    is often not a physical machine. More likely, the server is merely another computer program performing the actions
    of a server. Several of these servers may be living on
    the same physical machine.

* `Cloud`

    - Services provided over a network by a collection of many different remote servers. The data in this collection
    is distributed over the whole of the collection, thus the term "cloud". Applications running in the cloud can be accessed
    by clients and used just as if the software had been downloaded to the users machine without the clients machine having
    to store the application in its own memory.

* `COBOL`

    - Common Business Oriented Language. COBOL is a very early computer programming language. Introduce in 1959,
    COBOL was created to provide a means for programming
    business applications. It is still in use in many businesses.

* `Code`

    - Short for `source code`. Code is the text written to give instructions to a computer. There are many types of
    computer languages used for writing code.

* `Coder`

    - One who writes code.

* `Color codes`

    - Hexidecimal or decimal number codes used to describe
    various colors on a computer screen. Millions of different colors can be rendered using combinations of the colors
    red, green, and blue. The amount of each of these are determined by a numeric code. This code can be either
    numeric or hexidecimal. The color purple would have the
    color code of rgb(39, 34, 166). Each number represents the amount of red, green, and blue present in the color purple.

* `CAPTCHA`

    - `Completely Automated Public Turing test to tell Computers and Humans Apart.` A CAPTCHA is usually a image that has
    been purposely distorted in such a way that humans can figure out what the image is supposed to represent, but a
    computer cannot. Distorted images are the most prevalent types of CAPTCHA, but any image designed to be interpreted by
    a human, but is unintelligible to a computer is a CAPTCHA. They are used to ensure that an actual human being is
    requesting access to a webpage, web application, etc. There are several pieces of software referred to as `bots`.
    These bots are designed to perform common tasks, such
    as submit forms, autonomously. To protect against this, some websites use CAPTCHAS.

* `Capture`

    - To obtain information and placing it in a storage device for future reference. Anytime a variable is initialized,
    a `capture` has taken place. When a value is assigned to a memory location, that data has been `captured`.

* `Carbonite`

    - A liquid substance made from carbon. By use of a rapid freezing process, carbonite can be made solid.
    Once frozen, carbonite becomes a stable solid. The process of carbon freezing has been used for thousands of years
    to encapsulate volatile materials for safer transport. When applied to living organisms, carbon freezing provides a
    unique protective quality. After undergoing the carbon
    freezing process, an organism is placed in a hibernate state, provided the life form survives the initial freezing
    process. The encasing outer shell of carbonite serves
    as a very durable protective shell. Smuggler Han Solo is, perhaps, the most famous example of an individual
    undergoing carbon freezing. He was subsequently freed some several months later. However, had he not been so liberated,
    it is possible he would have remained encased, alive, for centuries.

* `Caret`

    - Sometimes referred to as a `circumflex`, the caret symbol,
    `(^)`, is used in some computer languages to represent
    exponents. `5^3` represents `5 x 5 x 5`. The symbol is
    also used to represent `Ctrl`. It is also used by some
    computer languages in `regular expressions`.

* `Case-sensitive`

    - Refers to the quality of discerning whether the case of a statement or character is recognized by the computer.
    Some computer languages discern between upper and lower case letters. Others do not. If a language is `case-sensitive`,
    the capital letters matter. If the language is not, it
    does not matter whether the letters are capitalized or not.
    It should be noted that there are some coding conventions
    used by programmers that dictate the use of capital letters, even though the language itself is not
    case-sensitive. Conventions such as the capitalization
    of class names is an example of this.

* `Checksum`

    - A number or string of text generated when data is sent from one place to another. By verifying the file `check-sum`
    the receiver of the data can be certain the data delivered is uncorrupted. This is done by checking the `checksum` of
    the received data to the `checksum` of the data before
    it was sent. If the numbers match, the data has been
    deivered uncorrupted.

* `Compile`

    - The process by which a source file is converted into an executable file. When a source file is compiled,
    there are several actions that occur "under the hood".
    The final product is to translate source files into
    data the computer understands.

* `Compiled-language`

    - A language that must be compiled before execution. Some languages do not require compilation instead relying
    on an interpreter to execute code.

* `Configuration`

    - Setting up a piece of software for use. Many programs have options that determine how it is intended to operate when
    in use. `Configuration` is the process of setting any available options for a piece of software. When you change the
    settings on your profile page, you are `configuring` your profile. Some of these options are required to be set in
    a specific manner, depending on what the program is going
    to be used for. Many programs have no options selected when first loaded into memory. Consequently, configuration
    is required in order for the program to function at all.

* `Collision`

    - The condition of two or more computers or network devices sending data at the same time. when this occurrs a message
    is sent requesting the data be sent again.

    - When two pieces of data are identical to each other. Everything in the computer must have a unique
    identifier. Variables must have unique names to be valid within the same scope, namespace, or environment.
    Hash numbers generated for security or transfer verification must be unique. When they are not, the computer
    tell which variable or hash is being referred to. Identical identifers will cause the program to crash.
    Great lengths are gone to in an effort to avoid collisions. Variables naming must ensure each value can be
    uniquely identified.

* `Connectivity`

    - The quality of being able to be connected to hardware or software. If something is said to have good `connectivity`,
    it means the thing can connect to a large number of different devices or software programs.

* `Console`

    - Alternately referred to as a `computer console`, `root console`, `system console`, or `terminal`. The console is really
    just the computer, the shell, a monitor, and a keyboard. Often, you will see backgrounds and icons all over the
    computer screen. There may also be toolbars across the top of the screen, and maybe even a background image or
    "wallpaper". All of these are layered on top of the terminal. Were all of these graphics stripped away, you would see
    just a cursor and a blank screen. This is the console.

* `Constant`

    - A value that does not change. The value of pi is a constant. The speed of light is a constant. Values within a program
    that the programmer does not wish to be altered in the running of the program. The keyword `const` is used to designate

* `Container`

    - Similar to a virtual machine, a container is a encapsulated computer environment. It has its own file system (separate
    from the file system of the host computer). A container is like a virtual machine, but much simpler.

* `Cookie`

    - A small amount of text data saved on the computer when a website is visited. This data helps the computer either
    create custom pages whenever that computer visits the website in the future. It is also used to save session information,
    so the data is available when you return to the same site. A `cookie` is the means by which a website "remembers" you
    when you visit a website.

* `Copy`

    - The action of duplicating data from a file.
    The process was invented by Larry Tesler. Whole files can be duplicated or only segments of a given file.
    This data can then be placed into another file location (paste). On the keyboard, the command `Ctrl+C` will copy a file
    or a selection of a file.

* `CPU`

    - Central Processing Unit. A computer's CPU handles all instructions from the computer hardware or software. It is
    the "brain" of the computer.

* `Crash`

    - A software or hardware problem that results in the operation of the program or the even the computer system itself.
    When something has `crashed` it has ceased to operate
    completely.

* `Crash Dump`

    - When a piece of software experiences an error that
    terminates its operation, raw data from the softwares
    written to the filesystem. This data can then be
    analyized by developers to determine the cause of
    the crash.

* `Create`

    - Create means to make something new. When a new file or directory or just about anything that can be saved on
    a computer is brought into existence, it has been created.

* `CSS`

    - Cascading Style Sheet. CSS is a language that allows developers to alter the layout and change the appearance of
    an HTML page. It looks like this:

    ```CSS
    body {
        font : normal 100% "Arial";
    }
    ```

    This changes the font of the text in the body of the HTML page.

* `CSV`

    - Comma Separated Values. CSV is a plaintext file that
    stores data in table form. CSV is used to store data.
    Because they are plaintext files they can be easily
    viewed by spreadsheet applications or transferred to
    a database.

* `Ctrl`

    - Short for `control`. The `Ctrl` key is used to modify the actions of other keys on the keyboard. `Ctrl+C` is
    used for copying. `Ctrl+V` is used to paste content. There are many, many more such commands.

* `Cursor`

    - A visual representation on the computer screen that shows where the next symbol will be placed. On a mouse, the cursor
    is usually an arrow or a finger. It allows a user to move elements of the GUI or desginate where something has
    been selected on the screen.

* `Cut`

    - The action of removing an item from its location and placing it temporarily in another location called the `clipboard`.
    It can then be copied to another location.

* `Cyber`

    - Relating to or characteristic of the culture of computers. The word is derived from the Greek "kubernetes" which means
    "A pilot or steersman" from the word "kubernesis" meaning "the gift of governance".

* `Download`

    - To copy data from one computer to another via a network. Whenever a browser connects to a website, data is transferred,
    or `downloaded`. Downloading refers to receiving data. `Uploading` is the opposite of `downloading`.

* `Data`

    - Any set of characters that is gathered and translated for some purpose. Data can be subdivided in various catagories.
    If the characters in a computer convey an idea to a human, it is data.

* `Desktop`

    - If you think of your computer as a desk, the desktop is all of the stuff that is laying on your desk when you sit down
    in the morning. Some things are always on you desk, like a pencil holder or a stapler. The icons on the screen are
    just like those things, except they are graphical images. If you click on one these graphical icons, programs or files
    can be opened. You can open files and leave them open. They are on the desktop.

* `Device driver`

    - A group of files that allow hardware to communicate with computer's operating system. Without drivers, a computer
    would be unable to send an receive data from hardware like a printer or keyboard.

* `Daemon`

    - In Unix and Linux, a daemon is a program that runs in the background without user interaction.

* `Dashboard`

    - A collection of data displayed together. A dashboard is called a dashboard because it is very much like the
    dashboard of a car. It allows the user to interact with vehicle as well as give commands to the vehicle. A computer
    dashboard does much the same thing. It allows a user to see relevant information as well as interact with the program.

* `Database`

    - A storage repository for data. Databases store data in an organized manner. Data can be grouped, stored, and
    retrieved using a database. Most databases organize data according its relationship to other data. This type of
    database is called a `relational database`. While relational databases are the most common type of database, there are
    other types of databases that organize data in a
    different way.

* `Database server`

    - A computer system that provides other computers with
    services related to accessing and retrieving data from a database. You can access a database server either from
    the "front-end" running locally on a users machine or
    from the "back-end" running on the database server itself.

* `Data breach`

    - The action of unauthorized persons gaining access to restricted area of a computer or portion of a network.
    It is a bad thing. Computer security is a BIG DEAL. When writing software, programmers should pay very close
    attention to proper security for their software.

* `Data center`

    - A facility used to store computers


