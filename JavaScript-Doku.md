# `JavaScript Dokumentation by Gabriel Aigner`

## Writing to console

`Console.log();`

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

## String Concatenation with Variables

`let myPet = 'armadillo';` \
`console.log('I own a pet ' + myPet + '.');` \
`// Output: 'I own a pet armadillo.'`

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
