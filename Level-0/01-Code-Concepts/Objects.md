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
