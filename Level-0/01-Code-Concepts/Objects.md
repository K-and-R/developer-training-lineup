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
index location. In an associative array the
"index" is a string instead of
just a number. It too is an example of a key/value pair.
