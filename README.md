# `JavaScript Dokumentation by Gabriel Aigner`

## Contents

[Data Types](#data-types)

[Variables](#variables)

[Commenting](#commenting)

[Writing to the console](#writing-to-the-console)

[How to work with Strings](#how-to-work-with-strings)

[Mathematic for coding](#mathematic-for-coding)

[Functions](#functions)

[Objects](#objects) 

[Classes](#classes)

## ``Data Types``

### Number

Any number, including numbers with decimals: 4, 8, 1516, 23.42.

### String

' ... ' or double quotes " ... ". \
Though we prefer single quotes.

### Boolean

true or false

### Null

null

### Undefined

undefined

### Symbol

A newer feature to the language, symbols are unique identifiers, useful in more complex coding.

### Object

Collections of related data.

## ``Variables``

The standard convention in JavaScript is `camel casing`.

### `var`

Learn more about `var` [click here (JavaScript Dokumentation)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var).

### `let`

The `let` keyword signals that the variable can be reassigned a different value. \
If you just declare it like this: `let price;` there stands `undefined` in it. \
`(with`**var**`it is the same but you should use`**let**`for this)` \
\
Learn more about `let` [click here (JavaScript Dokumentation)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var).

### `const`

A `const` variable cannot be reassigned because it is _constant_.

## ``Commenting``

### Single line comment

`// Print 5 to the console`

### Multiple line comment

`/* This is all commented console.log(10);` \
`None of this is going to run! console.log(99); */`

## ``Writing to the console``
`console.log();` \

You can put variables or simple text in the  ``()``.


## ``How to work with Strings``
### String Concatenation

Use `+` to concatenate strings.

`console.log('front ' + 'space'); // Prints 'front space'` \
`console.log('back' + ' space'); // Prints 'back space'` \
`console.log('no' + 'space'); // Prints 'nospace'` \
`console.log('middle' + ' ' + 'space'); // Prints 'middle space'`

### String Templates

String templates are better in my opinion, because you cant fortget the \' \' you need for concatenation.

Use `$` and `{}` to put variables in.

As example:

```
var myAnimal = 'Dog';

Code:

`This is my ${myAnimal}`


Output:

This is my Dog

```

### String Properties

`console.log('Hello'.length); // Prints 5`

### String Methods

Some string Methods [click here (JavaScript Dokumentation)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/prototype).

## ``Mathematic for coding``

### Arithmetic Operators

1. Add: `+`
2. Subtract: `-`
3. Multiply: `*`
4. Divide: `/`
5. Remainder: `%`

### Mathematical Assignment Operators

As example `x` is a `let` with the value `100`.

- `+=` : x += 100 = 200 === x = x + 100 => x = 200;
- `-=` : x -= 100 = 0 === x = x - 100 => x = 0;
- `*=` : x \*= 2 = 200 === x = x \* 2 => x = 200;
- `/=` : x /= 5 = 20 === x = x / 5 => x = 20;

### The Increment and Decrement Operator

As example `x` is a `let` with the value `2`.

#### Increment Operator

`x++;` is like `x = x + 1` \
for our example it's `3`;

#### Decrement Operator

`x--;` is like `x = x - 1` \
for our example it's `1`;

### Built-in Objects

- Round: Math.floor()
- Random: Math.random()
  \
  \
   For more `Math` objects [click here (JavaScript Dokumentation)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math).

## ``Functions``

### Declare a funkction

Write `function` infront of your function name.

Add `()` to oyur function name.

Write `{}` after your name and write code into it. Don't forget the closing Brackez `}`

Example:

```
function writeMyName() {
   console.log('Gabriel');
}
```

### Call a function

To call a function just write its name in the code.

```
writeMyName();
```

For this example it will output my name Gabriel.

### Function with parameter

The parameters are specified between the parenthesis, and inside the function body, \
they act just like regular variables. `name` act as placeholder for a value.

```
let name = 'Gabriel A';

writeMyName(name); //this is the call

function writeMyName(name) {
   console.log(name);
}
```

Output:

`Gabriel A`

### Deafault Parameters

- When the code calls greeting('Nick') the value of the argument is passed in and, \
  'Nick', will override the default parameter of 'stranger'.

- When there isn’t an argument passed into greeting(), \
  the default value of 'stranger' is used, and 'Hello, stranger!' is output.

```
function greeting (name = 'stranger') {
  console.log(`Hello, ${name}!`)
}

greeting('Nick') // Output: Hello, Nick!
greeting() // Output: Hello, stranger!
```

### Return

To pass back information from the function call, we use a `return` statement.

As example:

```
function monitorCount(rows, columns) {
  return rows * columns;
}

const numOfMonitors = monitorCount(5, 4);

console.log(numOfMonitors);
```

Output: `20`

### Anonymous function

A function with no name is `anonymous` \

As example:

```
let result = function(numberOne, numberTwo){
   ...
};
```

### Arrow functions

Arrow functions remove the need to type out the keyword function every time you need to create a function. \
Instead, you first include the parameters inside the `( )` and then add an arrow `=>` that points to the function body.

```
const plantNeedsWater = (day) => {
  if (day === 'Wednesday') {
    return true;
  }
};
```

### Concise Body Arrow Functions

The most condensed form of the function is known as concise body.

1. Functions that take only a single parameter don't need that parameter to be enclosed in parentheses. However, at takes zero or multiple parameters, parentheses are required.

2. A single-line block function body does not need `{}`. Without the curly braces, whatever that line evaluates will be automatically returned. The contents should immediately follow the `=>` and the `return` keyword can be removed.

Code: `(before)`

```
const squareNum = (num) => {
  return num * num;
};
```

Code: `(after)`

```
const squareNum = num => num * num;
```

## ``Objects``

### Creating Object Literals

As example:

```
let spaceship = {
  'Fuel Type': 'gasoline',
  color: 'silver'
};
```

### Accessing Properties

#### Dot Notation

As example:

```
let spaceship = {
  homePlanet: 'Earth',
  color: 'silver',
  flightPath: ['Venus', 'Mars', 'Saturn']
};
spaceship.homePlanet; // Returns 'Earth',
spaceship.color; // Returns 'silver',
spaceship.flightPath; // Returns ['Venus', 'Mars', 'Saturn']
spaceship.flightPath.length; // Returns 3
```

#### Bracket Notation

We _must_ use bracket notation when accessing keys that have `numbers`, `spaces`, or `special characters` in them. \
Without bracket notation in these situations, our code would throw an error.
\
\
With bracket notation you can also use a `variable` inside the brackets to select the keys of an object \
This can be especially helpful when working with functions:

```
let returnAnyProp = (objectName, propName) => objectName[propName];

returnAnyProp(spaceship, 'homePlanet'); // Returns 'Earth'
```

If we tried to write our `returnAnyProp()` function with dot notation `(objectName.propName)` \
the computer would look for a `key` of `'propName'` on our object and `not the value` of the `propName` parameter.

### Assign Properties

One of two things can happen with property assignment:

- If the property already exists on the object, whatever value it held before will be replaced with the newly assigned value.
- If there was no property with that name, a new property will be added to the object.

You can delete a property from an object with the `delete` operator.

### Methods

When the data stored on an object is a function we call that a _method_. \
\
For example `console` is a global javascript object and `.log()` is a method on that object. \
`Math` is also a global javascript object and `.floor()` is a method on it. \
\
We can include `methods` in our`object literals` by creating ordinary, comma-separated key-value pairs. \
The key serves as our method’s name, while the value is an `anonymous function` expression. \

```
const alienShip = {
  invade: function () {
    console.log('Hello! We have come to dominate your planet. Instead of Earth, it shall be called New Xaculon.')
  }
};
```

With the new method syntax introduced in ES6 we can omit the colon and the `function` keyword.

```
const alienShip = {
  invade () {
    console.log('Hello! We have come to dominate your planet. Instead of Earth, it shall be called New Xaculon.')
  }
};

```

Object methods are invoked by appending the object’s name with the dot operator followed by the method name and parentheses:

```
alienShip.invade(); // Prints 'Hello! We have come to dominate your planet.
Instead of Earth, it shall be called New Xaculon.'
```

### Nested Objects

As example:

```
let spaceship = {
  passengers: null,
  telescope: {
    yearBuilt: 2018,
    model: "91031-XLT",
    focalLength: 2032
  },
  crew: {
    captain: {
      name: 'Sandra',
      degree: 'Computer Engineering',
      encourageTeam() { console.log('We got this!') },
     'favorite foods': ['cookies', 'cakes', 'candy', 'spinach'] }
  }
};
```

The exercise is to assign the captain‘s favorite food (the element in the 0th index of her 'favorite foods' array) to it to the variable `capFave`.

```
let capFave = spaceship.crew.captain['favorite foods'][0];
```

Next example exercise is to put an array of individual objects into passengers.

```
let spaceship = {
  passengers: [{name: 'Peter'}],
  telescope: {
    ....
```

### Pass By Reference

Objects are passed by reference. This means when we pass a variable assigned to an object into a function as an argument, \
the computer interprets the parameter name as pointing to the space in memory holding that object.

As example:

```
let spaceship = {
  'Fuel Type' : 'Turbo Fuel',
  homePlanet : 'Earth'
};

function greenEnergy(obj) {
  obj['Fuel Type'] = 'avocado oil';
}

function remotelyDisable(obj) {
  obj.disabled = true;
}

greenEnergy(spaceship);
remotelyDisable(spaceship);
console.log(spaceship);
```

Output:

```
{ 'Fuel Type': 'avocado oil',
  homePlanet: 'Earth',
  disabled: true }
```

### Looping Through Objects

Loops are programming tools that repeat a block of code until a condition is met. \
We learned how to iterate through arrays using their numerical indexing, but the key-value pairs in objects aren’t ordered! \
\
[JavaScript has given us alternative solution for iterating through objects with the `for...in` syntax .](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for...in) \
`for...in` will execute a given block of code for each property in an object.

## ``Classes``

### Styling
It is very important for programmer that the variables in the classes have an ``_`` before the name.

### A class
Classes look like this in JavaScript:
````
class Dog {
  constructor(name) {
    this._name = name;
    this._behavior = 0;
  }

  get name() {
    return this._name;
  }
  get behavior() {
    return this._behavior;
  }   

  incrementBehavior() {
    this._behavior ++;
  }
}
````

### The constructor
The one important method is the the _constructor_ method. JavaScript calls the ``constructor()`` method every time it creates a new instance of a class. \
_Tipp: Surgeon means `Chirurg` in German._ 

````
class Surgeon {
  constructor(name, department){
    this._name = name;
    this._department = department;
  }
    ....
}
````

* This constructor() method accepts two arguments, ``name`` and ``department``.

* Inside of the ``constructor()`` method, we use the this keywords. In the context of a class, this refers to an instance of that class. \
In the surgeon class, we use this to set the value of the surgeon instance’s name property to the name argument and the department to the department.

### An instance
An ``instance`` is an object that contains the property names and methods of a class, but with ``unique property values``. \

We create a new variable named ``surgeonPeter`` that will store an instance of our ``Surgeon`` class.

````
let surgeonCurry = new Surgeon('Peter', 'Orthopedics');
````

### Getter
Class method and getter syntax is the same as it is for objects **except you can not include commas between methods.**

This are the ``getter`` for our example.
````
...

get name(){
  return this._name;
}

get department (){
  return this._department;
}
...
````
### Method Calls
The syntax for calling methods and getters on an instance is the same as calling \
them on an object — append the instance with a period, then the property or method name. \
For methods, you must also include opening and closing parentheses.