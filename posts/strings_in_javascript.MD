# Stringing Along: A Guide to JavaScript Strings

# Overview

To process information, computer programs must store data as a certain type. 
A data type defines the operations that apply to the data. 
For example, a number can be added to another number: ` 1 + 2`, but it is nonsensical to add a number to a text: `1 + two`.
There are seven data types in JavaScript: `number`, `string`, `boolean`, `null`, `undefined`, `symbol`, and `object`. In JavaScript and many programming languages, `string` is the data type used to represent text. This article focuses on the `string` data type.

## What is a string?

A `string` is a sequence of characters.
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
It can be a single character `a`, an empty character containing no characters ` `, your favorite emojis `🤣`, `🎅`, `🎆`, `🎇`, `🎈`, `🎉`, `🎄`, `🍕`, `🍺`, `🍩`, `🍪`, `🍫`, `🍬`, `🍭`, `🍮`, or a whole book.

In JavaScript, a string is a primitive data type. A primitive data type is a data type that is not an object and has no methods. A method is a function that is associated with an object. For example, the `toUpperCase()` method is associated with the `String` object. The `toUpperCase()` method converts a string to uppercase letters. Since a string is a primitive data type, it has no methods. However, there are many built-in functions that can be used to manipulate strings. We will learn more about these functions in this article.

## What can we do with strings?

Strings are used to represent text in computer programs. They are used to store data that is textual in nature. For example, a string can be used to store a person's name, a book title, a movie quote, a song lyric, a poem, a paragraph, a book, a speech, a letter, a recipe, a blog post, a tweet, a comment, a text, an email, a chat message, and so on.

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
- And many more useful things.

## How do we create strings?

Strings can be created as primitives, string literals, or String Objects, using the `String()` constructor.
Let us string along and learn more about each of these methods.

### Primitives

A primitive data type is a data type that is not an object and has no methods.
A method is a function associated with an object.

To create a string primitive, you can use single quotes `' '`, double quotes `" "`, or backticks `` ` ` ``. The following code snippets show how to create strings using each of these methods.

```javascript
'hello world'; // single quotes

"I'm a string"; // double quotes

`${greeting}! I'm a template literal.`; // backticks
```

So, if you wanted to create a string variable called `name` that stores the value `John`, you would write:

```javascript
let name = 'John';
```

A string can be concatenated by joining together two or more strings: ` "hello" + " " + ` to another string, but you cannot concatenate a string to a number.

### String literals

A string literal is a string data value that is written directly into the code. For example, the following code snippet creates a string variable called `name` that stores the value `John`:

```javascript
let name = 'John';
```

A string literal may a sequence of characters enclosed in single quotes `' '`, double quotes `" "`, or backticks `` ` ` ``. The following code snippets show how to create strings using each of these methods.

```javascript
'hello world'; // single quotes

"I'm a string"; // double quotes

`${greeting}! I'm a template literal.`; // backticks
```

A string literal is a sequence of characters enclosed in single quotes `' '`, double quotes `" "`, or backticks `` ` ` ``. The following code snippets show how to create strings using each of these methods.

```javascript
'hello world'; // single quotes

"I'm a string"; // double quotes

`${greeting}! I'm a template literal.`; // backticks
```

So, if you wanted to create a string variable called `name` that stores the value `John`, you would write:

```javascript
let name = 'John';
```

### String objects

The `String` object is a wrapper around the `string` primitive data type. A wrapper is an object that contains a primitive data type. The String object is a built-in object in JavaScript that represents a string of text. It has a number of methods that allow you to manipulate the string, such as:



For example, the `toUpperCase()` method is associated with the `String` object.
The `toUpperCase()` method converts a string to uppercase letters.
Since a string is a primitive data type, it has no methods.
However, there are many built-in functions that can be used to manipulate strings.
We will learn more about these functions in this article.

several ways to create strings in JavaScript. The following terms are used to describe the different ways to create strings:

In JavaScript, strings can be created using the `String` object, string literals, or template literals.

### String object

The `String` object is a wrapper around the `string` primitive data type.
A wrapper is an object that contains a primitive data type.
The String object is a built-in object in JavaScript that represents a string of text.
It has a number of methods that allow you to manipulate the string, such as:



The `String` object can be used to create strings using the `new` keyword. For example, the following code snippet creates a string variable called `name` that stores the value `John`:

```javascript
let name = new String('John'); // String object
```

The `String` object can also be used to create strings using the `String()` constructor. For example, the following code snippet creates a string variable called `name` that stores the value `John`:

```javascript
let name = String('John'); // String constructor
```

#### String object methods

There are many useful methods 

The `String` object can also be used to create strings using the `toString()` method. For example, the following code snippet creates a string variable called `name` that stores the value `John`:

```javascript
let name = (123).toString(); // toString() method
```

The `String` object can also be used to create strings using the `valueOf()` method. For example, the following code snippet creates a string variable called `name` that stores the value `John`:

```javascript
let name = (123).valueOf(); // valueOf() method
```

The `String` object can also be used to create strings using the `String.fromCharCode()` method. For example, the following code snippet creates a string variable called `name` that stores the value `John`:

```javascript
let name = String.fromCharCode(74, 111, 104, 110); // fromCharCode() method
```

The `String` object can also be used to create strings using the `String.fromCodePoint()` method. For example, the following code snippet creates a string variable called `name` that stores the value `John`:

```javascript
let name = String.fromCodePoint(74, 111, 104, 110); // fromCodePoint() method
```



Strings are created by enclosing characters in single quotes `' '`, double quotes `" "`, or backticks `` ` ` ``. The following code snippets show how to create strings using each of these methods.

```javascript
'hello world'; // single quotes

"I'm a string"; // double quotes

`${greeting}! I'm a template literal.`; // backticks
```

So, if you wanted to create a string variable called `name` that stores the value `John`, you would write:

```javascript
let name = 'John';
```

A string can be concatenated by joining together two or more strings: ` "hello" + " " + ` to another string, but you cannot concatenate a string to a number.


## Great... why more than one way to create strings?

The three methods of creating strings are not interchangeable. Each method has its own use case. Let's look at each method in detail.

### Single quotes

Single quotes are the most common way to create strings in JavaScript. They are used to create strings that are short and simple. For example, the following code snippet creates a string variable called `name` that stores the value `John`:

```javascript
let name = 'John';
```

Single quotes are also used to create strings that contain double quotes. For example, the following code snippet creates a string variable called `sentence` that stores the value `He said, "Watch the giant fall."`:

```javascript
let sentence = 'He said, "Watch the giant fall."';

console.log(sentence); // He said, "Watch the giant fall."
```
In the above code snippet, the double quotes `"` are used to enclose the string. The single quotes `'` are used to enclose the string that contains double quotes `"`.


```javascript
let sentence = 'He said, "I\'m a string."';
```

In the above code snippet, the backslash `\ ` is used to escape the double quotes `"` in the string. The backslash `\ ` is used to escape characters that have special meaning in JavaScript.




## Great... how do we access characters in a string?

Strings are immutable, which means that once they are created, their values cannot be changed. In ES6, strings are also iterable, which means that you can access each character in a string individually. We will learn more about immutability and iterability in this article. For now, let's focus on the basics of strings.
