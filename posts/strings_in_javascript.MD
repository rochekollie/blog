# Strings in JavaScript

## Hmm... what is string?

A `string` is a sequence of characters. Characters are symbols including letters, punctuation, and various other written marks in a language. For example, `a`, `B`, `c`, `1`, `2`, `3`, `@`, `#`, `$`, `🤣`, `❤️`, `🎄` are characters in many European languages like German or Norwegian, romance languages like French or Spanish, African Swahili and Vietnamese.

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
Charles Babbage is considered to be the “father” of the computer. He invented the first mechanical computer in the early 1800s. The computer was called the Analytical Engine. It was designed to perform mathematical calculations. The Analytical Engine was never built, but it was the first design for a computer.
````
As you can see, a string can be as long as you want it to be. It can be a single character, an empty character containing no characters, an emoji, 
or a whole book.

## Okay... why do we need strings?

To process information, computer programs must store data as a certain type. A data type defines the operations that apply to the data. For example, a number can be added to another number: ` 1 + 2`, but it is nonsensical to add a number to a text: `1 + two`. A string can be concatenated by joining together two or more strings: ` "hello" + " " + ` to another string, but you cannot concatenate a string to a number.

There are seven data types in JavaScript: `number`, `string`, `boolean`, `null`, `undefined`, `symbol`, and `object`. In Computer Science, `string` is the data type used to represent text. This article focuses on the `string` data type.


## Sounds good... how do we create strings?

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
