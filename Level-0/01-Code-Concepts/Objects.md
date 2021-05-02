# Objects

An Object is a data structure that contains data and also contains functions to manipulate data. Both are wrapped in a
structure called an Object.

An Object is a data structure that contains data and functions to manipulate data. Both of these things are grouped
into an object. It is called an object because
it copies in the computer the attributes
of a real-world object.

In the real world any object can be broken down into two parts. The first part describes the qualities of the object.
This would be things like its color or its size. The second part is things the object can do. This would be things the object
*does*, like calculations or making copies.

Let's take an ordinary real-world object and break it down into its component parts. For this example we will use a car.
A car has qualities.
It has a color and it has a number of wheels (usually four, but there are exceptions), it also may have a make and model.
All of the qualities of an object are referred to as `Properties`. `Properties` are the data part of the object.
The car wouldn't be much of a car if it didn't do something. It can go forward and it can go backward. You can turn on the
lights and play with the radio. These things are all functions of the car. These actions are referred to a `methods` of the
object. These look a lot like functions. That's because they are. However, when a function is included inside of an object,
it is called a `method`. What is the difference?
Functions included inside an object that are *associated*
with the  object
itself are methods. It is possible to include a
function inside of an object that is not associated
with the object. This is
not a method, it's just incorrect design.

You can think of `properties` as adjectives, and `methods` as verbs.
Let's look at a simple example:

```javascript
const Car = {
    color : 'red',
    make  : 'Ford',
    model : 'Explorer',
    makeAndModel : function(){return this.make + " " + this.model;}
};
```

In the above example, we have `properties` (color, make, and model) and we have some functionality (Placing make and model
together). This is a very simple example, just so you can see the basic layout of the object.

## Key/Value Pairs

A very important concept in OOP (Object Oriented Programming) is the idea of key/value pairs. You will find this idea all
over the place in software development. It is actually pretty simple. If you look at the example you will see a `key`
followed by a " : " and then the `value`. Like this: `color : 'red'`. The idea of assigning a value to a name is very common.
You will find this idea in arrays, variables, and associative arrays.For example, the "keys" of an array would be the index
number. The value would be the value held at that
index location.

```javascript
const array = [1,4,3,2,5];
let myNumber = array[2];
console.log(myNumber);
//Output is 3
```

Or

```javascript
const myObj = {
    myNumber : 3
};
console.log(myObj.myNumber);
//Output is 3
```

In the first example we have an array. The `key` in this case is the index number of the array, `[2]`.
The value at that index location is 3. In the second example, we have an object. The `key` is `myNumber`. The value assigned
to `myNumber` is 3. Even though the values in both examples are accessed with different syntax, the concept is the same.

It is important to remember that the terms `key` and `index` are used for a reason. Conceptually, they are really the same
thing, but a `key` is always a string while an `index` is
always a number. Using `keys` is very helpful for describing what the value is. Arrays are useful when you want to have
several values assigned to a single variable.
They are also useful if you need to have an
ordered list of values. There are many different opinions about when to use an object and when to use an array.
The above is a very basic guideline for their use.

## Accessing Object Values

Once we have our values stored in an object, how do we get them out again? There are two ways to do this. The first is
called `dot notation`. It looks like this:

```javascript
const myObj = {
    name : 'Sam'
};

console.log(myObj.name);
//Output is Sam
```

The second method is by use of `bracket notation`. It looks like this:

```javascript
const myObj = {
    name : 'Sam'
};

console.log(myObject['name']);
//Output is Sam
```

You might be wondering if there are two different ways to access object properties, which one is used when? Good question.
Consider the this example:

```javascript
const myObj = {
    name : 'Bob',
    age : 23,
    job : 'Janitor'
};

console.log(myObj.name);
//Output is Bob
```

The bracket method of accessing properties is a little different. With this method property names can
be assigned to variables so long as they are strings.

```javascript
const myObj = {
    name : 'Bob',
    age : 23,
    job : 'Janitor'
};

let foo = 'name';

console.log(myObj[foo]);
//Output is Bob
```

You can't do that with dot notation. You *can* assign a property to a variable using dot notation. Like this:

```javascript
const myObj = {
    name : 'Bob',
    age : 23,
    job : 'Janitor'
};

let foo = myObj.name;
console.log(foo);
//Output is Bob
```

So, the difference here is you can use a variable in place of a property name *if* the variable evaluates to a string
The string is the property name in the object.

## Object Destructuring

The most common way of accessing properties in an object is to use dot notation. However, there is a drawback to this method.
What if the property you need to access is nested inside of another object, that is nested inside another object,
that is nested inside another object........ That would make your dot notation a bit long. It might look something like this:

```javascript
const myObj = {
    obj1 : {
        obj2 : {
            obj3 : {
                name : 'Bill'
            }
        }
    }
};

let foo = myObj.obj1.obj2.obj3.name;

console.log(foo);
//Output is Bill
```

That's a bit long. There is another method that simply extracts properties from the object and makes them into variables.
This is called `destructuring`. It looks like this:

```javascript
const myObj = {
    obj1 : {
        obj2 : {
            obj3 : {
                name : 'Bill'
            }
        }
    }
};

const {name} = myObj.obj1.obj2.obj3;

console.log(name);
//Output is Bill
```

Each nested object contains only the next object, except the last one. That's just to keep things simple.
You can destructure several object properties all in one go if needed. It looks like this:

```javascript
const myObj = {
    obj1 : {
        obj2 : {
            obj3 : {
                name : 'Bill',
                age: 34
            }
        }
    }
};

const {name,age} = myObj.obj1.obj2.obj3;

console.log(name, age);
//Output is Bill 34
```

This is really the same as using dot notation. It is just easier to read and requires less typing. It also
makes extracting properties from objects much easier. As you can see, using destructuring, I don't have to create a
variable then assign my object property to it. I only have to say, "Hey, this property name is now a variable in its
own right, deal with it." Then I can use the property just like a variable, because that's what it is now.

You *can* assign a different value to your new variable, but that *will not* change the value inside the object.
It only changes the value of the variable itself. The object property will not change to your assigned value.

## Classes

There is another way to create an object. You can create a 'blueprint' of your object. This is a set of instructions
that tell the computer how you want your objects
to behave and what data they should have. Once have your 'blueprint' written, you can create as many objects as you need.
The 'blueprint' is called a `class`. It looks like this:

```javascript
class Person {
    constructor(firstName, lastName){
        this._firstName = firstName;
        this._lastName = lastName;
    }
};

const bill = new Person('Bill', 'Smith');

console.log(bill._firstName);
//Output is Bill
```

Let's break this down. On line 1 we are using the keyword `class`. This tells the computer we want to write a
blueprint for an object. The name of our class is `Person`. Names of classes are always capitalized.
This is not for the computer, its for the humans.
By making class names capitalized, it's easy to tell you are looking at a class. After the class name there is a
curly brace, just like any other code block would have.

On line 2, we have our `constructor function`. This tells the class how to build our object. Let's cover this a little
more closely.

### Constructor Function

A `constructor function` is a function that creates an object. If we wanted to create a new object we might write
something like this:

```javascript
const makeAnObject = function(name, age){
    let bar = {};
    bar.name = name;
    bar.age = age;
  return bar;
};

let newObject = makeAnObject('Bill', 34);

console.log(newObject.name);
//Output is Bill
```

In the above example we have written a function that does the following:

1. Takes in two arguments, `name` and `age`.
2. Declares and empty object, `let bar = {};`
3. Adds a property to object `bar` called `name`.
4. Adds the parameter `name` as the value of property `name`.
5. Adds a property to object `bar` called `age`.
6. Adds the parameter `age` as the value of property `age`.
7. Finally, the object `bar` is returned.

On the next line after the function, variable `newObject` is set equal to our function. Lastly, we log `newObject.name`
to print `Bill` on the screen.

Wow, that's a lot of stuff to do just to get an new object created! And there aren't even all that many properties in
the object. What a pain in the ass, right? Well, here's some good news! You don't have to do that every time you want to
create a new object. The `constructor` function does all of that *for* you.

Let's refactor the last example using a constructor function:

```javascript
class AnObject {
    constructor(name, age){
        this._name = name;
        this._age = age;
    }
};

let myObject = new AnObject('Jim', 34);
```

Above we have created a class called `AnObject`.
We tell the class how to build an instance of the class
(an object) by using a function.
This function is called the `constructor`. This function has two parameters, `name` and `age`. When we create a new instance
of the class, as we did on the last line of the example
above, we give the constructor function the information `name`
and `age`. The constructor then creates a new object with the
properties we gave it. In this case, `'Jim'` and `34`.
The keyword, `new`, invokes the constructor function.

An object also contains functionality. We can add
functionality like this:

```javascript
class AnObject{

    constructor(name, age){
      this._name = name;
      this._age = age;
      }

    get printName() {console.log(this._name)}

    changeName(name){this._name = name;}

};

let myObject = new AnObject('Jim', 54);

myObject.changeName('Bill');

myObject.printName;

};
```

In the class definition above some methods have been added. The first method is a `getter method`. This method is used to
retrieve data from the object. The second method allows the user to change the value of the `name` property. At the bottom
of the code block you can see where both methods have
been called using `dot notation`.

## The 4 Principles of OOP

There are four basic ideas regarding Object Oriented Programming.
That means that there are four different concepts that
up the paradigm of OOP. As mentioned earlier,
there are a few different ways one can go about writing computer programs. Each "way" is referred to a paradigm.
The word `paradigm` means "*A typical example or pattern
of something; a model.*" -Definitions from Oxford Languages.
One can write a program that uses one instruction at a time in
a long list of instructions. Each one of these
instructions is executed in order, one at a time.
This is a `Procedural` paradigm. Grouping code into
reuseable blocks is a `Functional` paradigm.

`Object Oriented Programming` is a paradigm that uses
Objects and Classes to accomplish the tasks required
in a computer program. This paradigm is achieved by use of the four principles of OOP (Object Oriented Programming).

### Encapsulation

The first of the four core principles in object-oriented programming is encapsulation.
The idea of encapsulation is that the data and code (like in a method definition) defined in the class  should not be visible
to end users. For example, let’s say you have a class.
Implementing the principle of encapsulation would mean that all
properties of this class are private, hidden from other classes.

The only way to access these class properties would be
through public accessor methods (sometimes referred to
as `getter` and `setter` methods) of that class.
An Accessor method is a method created for the purpose
of accessing specific class property. This practice of hiding
information or data about implementation is called “data hiding”.

To implement encapsulation in JavaScript, we create new class.
Inside it, we declare two new properties,
also called fields and members. We make all of them private.
This will ensure all these properties are hidden.
They will be inaccessible from the outside of the class.
From now, the only way to access them is through methods
inside that class.

This is the next thing we will do. We will create public setter and getter methods for each private property.
These methods will allow us to view and modify
values of these properties.

```javascript
class Animal{
  constructor(name, breed, origin){
    this._name = name;
    this._breed = breed;
    this._origin = origin;
    }

    getName(){
      return this._name;
      }

    getBreed(){
      return this._breed;
      }

    getOrigin(){
      return this._origin;
      }

    setName(name){
      this._name = name;
      return name;
      }
};

let gabby = new Animal('Gabby', 'Tabby', 'Scotland');
console.log(gabby.getOrigin());
console.log(gabby.getName());
console.log(gabby.getBreed());
```

### Inheritance

Inheritance is the most used principle of object-oriented programming. This makes sense. Real world objects can very similar
to each other. A lot of objects are *almost* identical, but not quite.
For example, a dog and a cat are both animals.
They both have four legs. They both can walk and make sounds.
They both have fur. They are similar, but not the same.

Inheritance allows you to create similar classes from a parent class. The parent class would hold all of the properties and
methods common to both dogs and cats. This helps you avoid writing the same code over again and again.
Instead, you can let your dog and cat classes “inherit” from this separate class.
The main class that holds all of the common properties of both dogs and cats is called a `parent class` or `super-class`.
The `dog` class and the `cat` class *inherit* all of the properties and methods from the `super-class`.

Classes that inherit from this “parent” class are called “child classes”, “subclasses” or “derived” classes.
When some class (child class) inherits from another class (parent class), it inherits all of the parent’s properties and
methods. One exception are private properties and methods.

Another exception is the constructor method. The constructor is not a normal class method and is not inherited by child classes.
When you instantiate the parent class, the constructor method of the parent class will be called.
When you want to let one class inherit from another use the `extends` keyword followed by the parent’s class name.
It looks like this:

```javascript
class Shape{
    constructor(){
      this._name = name;
      this._numOfSides = numOfSides;
      this._sideLength = sideLength;
      }

    calcArea(height, width){
      return height * width;
    }

    calcPerimeter(sides){
      return sides + sides;
    }
}

class Square extends Shape{

  super()

}

  calcPerimeter(side1, side2, side3, side4){
    return side1 + side2 + side3 + side4;
  }

  calcArea(height, width){
    return height * width;
  }
}
```

### Polymorphism

Polymorphism is the third of principle of object-oriented programming.
The word “polymorphism” means having “more than one form”.
You know about the principle of inheritance and how it works.
Let’s say you have a couple of classes related to each other
through inheritance, parent class and child classes.

In order for polymorphism to occur two things have to happen.
First, one of these child classes creates its own method.
Second, this method in some way overrides a method with the same name that is declared in parent’s class.
For example, let’s say you have a class `Dog` and `Cat`. Both inherit from the `Animal` class.

The Animal class has `speak()` method.
Both child classes `Dog` and `Cat` also has their own implementation of `speak()` method. In both cases, this method returns
a different result.

### Abstraction

In computer science the word "abstraction" means to get
rid of the pesky details and then examine a problem
in its most basic parts. Any problem can be broken
down into a series of fundamental statements.
These statements do not require any details or
reference to a specific problem.

Abstraction can be illistrated using a series of
statements about a thing.
Like this:

1. Humans have two eyes.
2. Many living things have eyes.
3. Many living things can percieve electromagnetic waves

The problem being solved in this example is how do living
things percieve their environments visually. An "eye" is a
organ that detects electromagnetic waves in the
environment. We can abstract this fact into "Some living
things have the ability to detect electromagnetic waves."

This idea can also be applied to a concept of "data hiding".
The idea is that the user of an application does not need to know the
underlying code that executes the task directed by the user.
In other words, you don't need to know how your car works
in order to drive it. All you need is access to the parts
that allow you to interact with the car. These would be
things like the ignition or the gearshifter or the
steering wheel, etc. The inner workings of the car itself
is something most of us don't care about.

### Abstract Classses and Interfaces

An `abstract class` is a class that cannot be instantiated
and contains at least one `abstract method`. Now, what does that
mean? Think of an `abstract class` as a *very* generalized
blueprint. It contains the raw materials that will be used
in sub-classes that are derived from it. But it does not
specifically define anything. The details are left to the sub-class.
An `abstract class` would say, "Build a house".
It does not say what kind of house or where to build the
house or how many stories the house is supposed to have.
It just says "Build it!".

From this general order, we can create a sub-class that
more specifically defines how we are going to build our house.
There can be several of these, each one concerned with
some specific aspect of building the house. The `abstract class`
contains the very basic properties and methods that are then
inherited by the sub-class. We can add, change, or remove
properties and methods from the abstract class in our sub-class.
This also allows us to hide the implementation details as
base class (abstract class) cannot be directly accessed.

Let's review these four ideas and try to break them down to their essential parts.

* `Encapsulation`

    - The guts of your class cannot not be accessed directly.
    - You have to use a `getter` method. It is done to keep your code
    from being altered by another. Someone also cannot
    change anything you don't want changed. If you do allow someone to
    change something, they have to use a `setter` function to do it. Otherwise, no one can change anything.

* `Inheritance`

    - Stuff from a super-class can be passed down to a
    derived class without having to re-write anything.
    So, if you write a class then you want to have another
    class that is pretty close, *but not exactly the same*
    you can use `inheritance`.
    Using the keyword `extends`, you can create a class
    based off of the previous class. All of the properties
    and methods in the super-class are now in the child-class.
    You do not have to write them again. You can also add any
    methods you need in your new class that may not be in
    the super-class. In this way you can save yourself a
    lot of typing and at the same time customize your class
    to do exactly what you need.

    - Do not forget that you must call the parents' constructor function like this `super();`. This is required if you want
    your class to inherit from the super-class.

* `Polymorphism`

    - When you inherit a method from a parent class you can alter it in your child class to better fit what you need it to
    do. The name of the method is the same as it is in the parent class, but the implementation in the child class is
    different. So, you can have many different classes
    that all are changed a bit. Or, you might say,
    "many forms" of the same thing.

* `Abstraction`

    - Taking something complicated and breaking it down into its basic parts, getting rid of all the details.
    A cat has whiskers and a tail, and a supple spine,
    vertical pupils, and pointy ears. If it does not have
    these things it may or may not be a cat.
    So, let's take a specific example of a cat, like
    *your* cat. It has specific details that make
    it recognizable to you as *your* cat.
    It might have a particular physical attribute such as
    a tear in its ear or kink in its tail that is specific to that individual cat. In contrast to that, we can have a
    broad definition of the actions and properties of any
    and all cats. That generalization of this thing
    called a 'cat' is `abstraction`.

    - There is another aspect of `abstraction`.
    This is the idea that we do not want the end user of our program to have to know *how* the code does what it does.
    All they need to know is that it does that thing. You do not need to know how a
    internal combustion engine works in order to operate your car. You only need to know to put your key in the little slot,
    turn it, and like magic the engine starts. By hiding the details we make the user experience easier and at the same time
    protect our data. This is sometimes referred to as `data-hiding`. It is similar to the section above in that we are
    taking something that might be very complicated and breaking it down in to something easy and simple to use.
    Again, we have this idea of taking something complex and breaking it down into its fundamental parts. This is also `abstraction`.

### Practical Uses of OOP

There are countless ways to use OOP in designing and implementing software. There are even defined "design patterns" to help
solve specific types of coding problems.
These are beyond the current scope of this section. For now, the simplest way to think about OOP could be summed up as
"Bigger, broader first, then more and more details as you go down." But be warned, that is only the most general of
guidelines. The implementation of OOP really depends on the specifics of the problem you are trying to solve. Often, you
will experience a trial and error phase of your project.
A lot of developers operate on the basis of "get the code
on the page and make it work. Then refine it as needed."
This is a good place to start.

Another point to consider is the use of functional programming. In theory, anything that can be build using OOP can also be
built using only a series of functions. The only difference between functional programming and OOP is organization. In OOP,
functions (called `methods` when contained in an object) are grouped together in a structure called an `object`. However, a
function that does not live inside of an object still works
as a function. And there was a time when there was no such thing as an `object`. What should be taken from this is that
understanding how data is stored (`variables`) and how that data is then manipulated (`function`) comes before how either of
these things are organized. OOP is covered here because it is very prevalent in software development. It has some advantages,
but is not the be all and end all of writing code.

```javascript
//Define variables here
let name = 'Joe';
let age = 34;
let job = 'Janitor';

//Define function here
let description = function(name, age, job){
    console.log(`My name is ${name}. I am ${age} years old.
    I work as a ${job}.`);
    };
    
//Invoke function here 
description(name, age, job);
    
//Define a class here    
class Person{
    constructor(name, age, job){
        this._name = name;
        this._age = age;
        this._job = job;
        }
    
    description(){
        console.log(`My name is ${this._name}. 
        I am ${this._age} years old. I work 
        as a ${this._job}`);
        }
}
//End class definition here

//Instantiate new Object
let joe = new Person('Joe', 34, 'Janitor');


//Invoke method 
joe.description();
```

Above is an example of handling a task first with only variables and functions, then by using OOP principles. The output for
both the functional approach and the OOP approach is identical. This example is written there so that you can compare the two
different versions. It is understood that the task itself
is sort of dumb. It's just an example to keep things simple.
