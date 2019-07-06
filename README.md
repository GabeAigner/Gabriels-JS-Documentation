# `JavaScript Dokumentation by Gabriel Aigner`

## Writing to the console

`console.log();`

## Commenting

### Single line comment

`// Print 5 to the console`

### Multiple line comment

`/* This is all commented console.log(10);` \
`None of this is going to run! console.log(99); */`

## Data Types

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

## Variables

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

## Arithmetic Operators

1. Add: `+`
2. Subtract: `-`
3. Multiply: `*`
4. Divide: `/`
5. Remainder: `%`

## String Concatenation

Use `+` to concatenate strings.

`console.log('front ' + 'space'); // Prints 'front space'` \
`console.log('back' + ' space'); // Prints 'back space'` \
`console.log('no' + 'space'); // Prints 'nospace'` \
`console.log('middle' + ' ' + 'space'); // Prints 'middle space'`

## String Templates

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

## Properties

`console.log('Hello'.length); // Prints 5`

## Methods

Some string Methods [click here (JavaScript Dokumentation)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/prototype).

## Built-in Objects

- Round: Math.floor()
- Random: Math.random()
  \
  \
   For more `Math` objects [click here (JavaScript Dokumentation)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math).

## Mathematical Assignment Operators

As example `x` is a `let` with the value `100`.

- `+=` : x += 100 = 200 === x = x + 100 => x = 200;
- `-=` : x -= 100 = 0 === x = x - 100 => x = 0;
- `*=` : x \*= 2 = 200 === x = x \* 2 => x = 200;
- `/=` : x /= 5 = 20 === x = x / 5 => x = 20;

## The Increment and Decrement Operator

As example `x` is a `let` with the value `2`.

### Increment Operator

`x++;` is like `x = x + 1` \
for our example it's `3`;

### Decrement Operator

`x--;` is like `x = x - 1` \
for our example it's `1`;

## Functions

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

As Example:

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
