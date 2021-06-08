# Glossary

* `ACSII`

    - American Standard Code of Information Interexchange. This is a standard for encoding letters and numbers. Computers do
    not understand letters *or* numbers. They understand "1" and "0" only. The ASCII standard assigns each letter and number
    a number. That number is then converted into binary (1's and 0's). Now, the computer understands what the number
    or letter is.

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

* `algorithm`

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
    (whatever name you want to call it). Inside the box is stored a value. We can connect together a series of boxes and put
    values in each box. Then we can give the whole thing a single name. This is an `array`. Each box in our array is
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
    and viewed using a browser. Most browsers are associated with a `search engine`. A search engine is not the same thing as
    a browser. These two different programs are often confused.

* `Binary`

    - A base-2 number system invented by Gottfried Leibnitz. It consists of only two numbers, "1" and "0". Binary works
    very well for writing digital data to a computer.
    Bascially, a computer consists of thousands and thousands of switches. Each switch can either by on ("1") or off
    ("0"). Calculations can be executed using binary,
    referred to as `machine code`. Any computer language used by humans is eventually converted to binary.
    Otherwise, the computer would be unable to execute the instructions received.

* `Back-end`

    - The portion of a computer program that runs out of sight of the user. In web development, the back-end consists of
    writing code that governs how a server send data to users. The back-end handles accessing data from a database as well as
    determining what data is to be sent back as well as the format it should be sent as. None of these operations are
    apparent to the user.

* `bash`

    - Bourne Again SHell. A `shell` is a command interpreter that executes commands from the user. A shell program allows a
    human to give commands to a computer. Executing commands in the shell is not quite the same as writing a computer
    program. These days, most everyone is used to using a mouse to click on icons placed on the computer screen. Alas, there
    was a time before that technology existed. A shell program was needed to execute commands that today would normally be
    done with a mouse. The original shell program was updated in 1989. That update was called the Bourne shell.
    The term Bourne Again Shell is an attempt at humor
    by persons who probably should have just stuck with
    programming.

