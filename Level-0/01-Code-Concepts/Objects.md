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
    constructor(name, numOfSides, sideLength){
      this._name = name;
      this._numOfSides = numOfSides;
      this._sideLength = sideLength;
      }

        getName(){
          console.log(this._name)
        }
        getNumOfSides(){
          console.log(this._numOfSides)
        }

        getSideLength(){
          console.log(this._sideLength)
        }

        setName(newName){
          this._name = newName
        }

        setNumOfSides(numSides){
          this._numOfSides = numSides
        }

        setSideLength(side){
          this._sideLength = side
        }
}
```

### Polymorphism

Polymorphism is the third of principles of object-oriented programming.
The word “polymorphism” means having “more than one form”.
You know about the principle of inheritance and how it works.
About polymorphism. Let’s say you have a couple of classes related to each other
through inheritance, parent class and child classes.

In order for polymorphism to occur two things have to happen.
First, one of these child classes creates its own method.
Second, this method in some way overrides a method with the same name that is declared in parent’s class.
For example, let’s say you have a class Dog and Cat. Both inherit from the Animal class.

The Animal class has speak() method. Both child classes Dog and Cat also has their own implementation of speak() method.
In both cases, this method returns a different result.
