# String Along with JavaScript Strings

## Overview

To process information, computer programs must store data as a data type.
A data type defines the operations that apply to the data.
For example, `number` is a data type that allows us to add two numbers:
` 1 + 2`.
However, it would be nonsensical to add a number to a text: `1 + two` because `two` is not a number.
`two` is a text.
In JavaScript and many programming languages, `string` is the data type used to represent text.
There are seven data types in JavaScript: `number`, `string`, `boolean`, `null`, `undefined`, `symbol`, and `object`.
This article focuses on the `string` data type.

## What is a JavaScript string?

In JavaScript, a `string` is a sequence of characters.
Characters are symbols including letters, punctuation, and various other written marks in a language.
For example, `a`, `B`, `c`, `1`, `2`, `3`, `@`, `#`, `$`
are characters in many European languages like German or Norwegian,
romance languages like French or Spanish, African Swahili and Vietnamese.

A string can be a word:

```text
hello
```

A string can also be a sentence:

```text
The computer was invented in order to automate mathematical calculations that were previously completed by people.
```

Or a string can be a paragraph:

```text
Charles Babbage is considered to be the “father” of the computer. He invented the first mechanical computer in the early 1800s.
The computer was called the Analytical Engine. It was designed to perform mathematical calculations.
The Analytical Engine was never built, but it was the first design for a computer.
````

As you can see, a string can be as long as you want it to be.
It can be a single character `a`, an empty character containing no characters ` `, your favorite
emojis `🤣`, `🎅`, `🎆`, `🎇`, `🎈`, `🎉`, `🎄`, `🍕`, `🍺`, `🍩`, `🍪`, `🍫`, `🍬`, `🍭`, `🍮`, or a whole book.

## What can we do with strings?

Strings are used to represent text in computer programs. They are used to store data that is textual in nature. For
example, a string can be used to store a person's name, a book title, a movie quote, a song lyric, a poem, a paragraph,
a book, a speech, a letter, a recipe, a blog post, a tweet, a comment, a text, an email, a chat message, and so on.

As a programmer, you will often need to manipulate strings in many useful ways:

- A string can be converted to uppercase letters, lowercase letters, or title case.
- A string can be split into an array of substrings.
- A string can be concatenated by joining together two or more strings.
- A string can be searched for a substring.
- A string can be replaced with another string.
- A string can be reversed.
- A string can be trimmed.
- A string can be sorted.
- A string can be compared to another string.
- And hopefully many more useful stringing along with strings.

There are two ways to create strings in JavaScript:

- Using the `String` object
- Using string literals

We can create strings using the `String` object or using string literals as shown in the following code snippet:

```javascript
const stringObject = new String('Hello, world'); // String object

const stringLiteral = 'Hello, world'; // string literal
```

Using `console.log` and the `typeof` operator to output the data type of each variable, we get:

```javascript
console.log(typeof stringObject); // object

console.log(typeof stringLiteral); // string
```

As you can see, a `String` object is a different data type than a `string` primitive.
Of the seven data types in JavaScript, `string`, `number`, `boolean`,
`null`, `undefined`, and `symbol` are primitive data types.
This is important to know
because a string can be a primitive data type or an object.
String along,
and let us explore the difference between these two concepts beginning with the `string` primitive data type.

## String primitives

A primitive is a data type that is not an object and has no methods.
A method is a function associated with an object.
A string primitive is created using single quotes `' '`, double quotes `" "`, or backticks `` ` ` ``.
The following code snippets show how to create strings using each of these methods.

```javascript
'hello world'; // single quotes

"I'm a string"; // double quotes

`I'm a template literal.`; // backticks
```

We can also create a string primitive using the `String` constructor:

```javascript
const stringPrimitive = String('Hello, world'); // String constructor
```

Note that in the above code snippet, `String()` is called without the `new` keyword.
`String()` can be called with or without the `new` keyword.
When `String()` is called **with** the `new` keyword, it returns a `String` object.
When `String()` is called **without** the `new` keyword, it returns a string primitive.
This is
because JavaScript automatically coerces a string
created using the `String` constructor to a string primitive if the `new` keyword is not used.


Take a look at the following code snippet:

```javascript
const stringObject = new String('Hello, world'); // String object

const stringPrimitive = String('Hello, world'); // string primitive
```

In the above code snippet, `stringObject`
is a `String` object
and `stringPrimitive` is a string primitive
because the `new` keyword is used with `String()` in the first line and omitted in the second line.


The following are valid string primitive variables:

```javascript
const greeting = 'Hello, world';

const name = "john";

const sentence = `${greeting}, my name is ${name}.`;

const stringPrimitive = String('I am also a primitive.');
```

As you can see, a string primitive can be created using single quotes `' '`,
double quotes `" "`, or backticks `` ` ` ``, or using the `String` constructor.
Each method has its own use case.
Let's look at each
method in detail.

Single quotes are the most common way to create strings in JavaScript.
They are used to create strings that are short
and simple. For example, the following code snippet creates a string variable called `name` that stores the
value `John`:

```javascript
let name = 'John';
```

Single quotes are also used to create strings that contain double quotes. For example, the following code snippet
creates a string variable called `sentence` that stores the value `He said, "Watch the giant fall."`:

```javascript
let sentence = 'He said, "Watch the giant fall."';

console.log(sentence); // He said, "Watch the giant fall."
```

In the above code snippet, the double quotes `"` are used to enclose the string. The single quotes `'` are used to
enclose the string that contains double quotes `"`.

```javascript
let sentence = 'He said, "I\'m a string."';
```

In the above code snippet, the backslash `\ ` is used to escape the double quotes `"` in the string. The backslash `\ `
is used to escape characters that have special meaning in JavaScript.

Double quotes are used to create strings that contain single quotes. For example, the following code snippet creates a string variable called `sentence` that stores the value `He said, "Watch the giant fall."`:

```javascript
const sentence = "I can't believe it's not butter!";
```

In the code snippet above, the double quotes `"` are used to enclose the string.
The single quotes `'` are used to enclose the string that contains single quotes `'`. The backslash `\ ` is used to escape the single quotes `'` in the string.

Backticks are used to create template literals. Template literals are used to create strings that contain placeholders. For example, the following code snippet creates a string variable called `sentence` that stores the value `He said, "Watch the giant fall."`:

```javascript
const sentence = `He said, "Watch the giant fall."`;
```
A string can be concatenated by joining together two or more strings:

```javascript
'hello' + ' ' + 'world'; // hello world
```

A string can also be interpolated using template literals:

```javascript
const greeting = 'Hello';
console.log(`${greeting}! I'm a template literal.`); // Hello! I'm a template literal.
```

String interpolation is a process of evaluating a string literal containing one or more placeholders.
It is a feature of ES6 that allows you to insert variables into a string.
The placeholders are indicated by the dollar sign and curly braces `${}`.
The placeholders are replaced with the value of the variables.

Regardless of how a string primitive is created, it is a primitive data type and has no methods of its own.
However, there are many built-in functions that can be used to manipulate strings.
We will learn more about these functions in this article.
Before we do, let's take a look at the `String` object.

## String Objects

The `String` object is a wrapper around the `string` primitive data type.
A wrapper is an object that contains a primitive data type
and has methods that can be used to manipulate the primitive data type.
The `String` object can be used to create strings using the `new` keyword.

For example, the following code snippet creates a string object:

```javascript
let stringObject = new String('This is a string object.'); // String object
```

In the above code snippet, the `String` object is used to create a string object called `stringObject`.
The `String` object is a built-in global object in JavaScript that represents a string of text.
It has a number of methods that allow you to manipulate the string, such as:

- `charAt()` - returns the character at the specified index.
- `charCodeAt()` - returns the Unicode of the character at the specified index.
- `concat()` - joins two or more strings.
- `indexOf()` - returns the index of the first occurrence of a specified value in a string.
- `lastIndexOf()` - returns the index of the last occurrence of a specified value in a string.
- `length` - returns the length of a string.
- `replace()` - replaces a specified value in a string with another value.
- `search()` - searches a string for a specified value and returns the position of the match.
- `slice()` - extracts a part of a string and returns the extracted part in a new string.
- `split()` - splits a string into an array of substrings.
- `substr()` - returns the characters in a string beginning at the specified location through the specified number of
  characters.
- `substring()` - returns the characters in a string between two specified indices.
- `toLocaleLowerCase()` - converts a string to lowercase letters, according to the host's current locale.
- `toLocaleUpperCase()` - converts a string to uppercase letters, according to the host's current locale.
- `trim()` - removes whitespace from both ends of a string.

As you can see,
the `String` object has many useful methods
that can be used to manipulate strings while the string primitive has no methods of its own.
However, JavaScript behind the scenes converts string primitives to string objects
when a string primitive is used with a method.
For this reason, you can use methods on string primitives as if they were string objects.
For example, the `toUpperCase()` method is associated with the `String` object.
If we go back to our code snippet,
can change the first letter of `name` to uppercase using the methods associated with the `String` object:

```javascript
const greeting = 'Hello, world';

const name = "john";

const sentence = `${greeting}, my name is ${name.charAt(0).toUpperCase() + name.slice(1)}.`;
```

In the above code snippet, the `toUpperCase()` method is used to convert the first letter of `name` to uppercase.
The `slice()` method is used to extract the rest of the string after the first letter.
The `+` operator is used to concatenate the uppercase letter with the rest of the string.
So, the output of `sentence` is `Hello, world, my name is John.`.
If you do not understand the above code snippet, don't worry.
String along, and you will understand it soon enough as we explore our next section, string methods.

## String methods

A string method is a function associated with a string object.
Going back to string primitive vs a string object, we stated that a string primitive has no methods of its own.
Therefore, a string primitive cannot be used with a method.
However, JavaScript behind the scenes converts string primitives to string objects when a string primitive is used with a method.
For this reason, you can use methods on string primitives as if they were string objects.
For example, the `toUpperCase()` method is associated with the `String` object.

Strings are immutable, which means that once they are created, their values cannot be changed. In ES6, strings are also
iterable, which means that you can access each character in a string individually. We will learn more about immutability
and iterability in this article. For now, let's focus on the basics of strings.

### Methods:

The `String` object can also be used to create strings using the `toString()` method. For example, the following code
snippet creates a string variable called `name` that stores the value `John`:

```javascript
let name = (123).toString(); // toString() method
```

The `String` object can also be used to create strings using the `valueOf()` method. For example, the following code
snippet creates a string variable called `name` that stores the value `John`:

```javascript
let name = (123).valueOf(); // valueOf() method
```

The `String` object can also be used to create strings using the `String.fromCharCode()` method. For example, the
following code snippet creates a string variable called `name` that stores the value `John`:

```javascript
let name = String.fromCharCode(74, 111, 104, 110); // fromCharCode() method
```

The `String` object can also be used to create strings using the `String.fromCodePoint()` method. For example, the
following code snippet creates a string variable called `name` that stores the value `John`:

```javascript
let name = String.fromCodePoint(74, 111, 104, 110); // fromCodePoint() method
```