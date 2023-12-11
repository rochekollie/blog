# String Along with JavaScript Strings

To process information, computer programs must store data as a type.
A data type defines how the data is stored in memory,
which operations can be applied to the data, and how to execute those operations.
In computer science, `string` is the data type used to represent text.
Strings are a fundamental part of JavaScript.
They are used to store data that is textual in nature.
For example, a string can be used to store a person's name, a book title, a movie quote, a song lyric, a poem, a
paragraph, a book, a speech, a letter, a recipe, a blog post, a tweet, a comment, a text, an email, a chat message, and
so on.

## What is a JavaScript string?

In JavaScript, a `string` is a sequence of characters.
Characters are symbols including letters, punctuation, and various other written marks in a language.
For example, `a`, `B`, `c`, `1`, `2`, `3`, `@`, `#`, `$`
are characters in many European languages like German or Norwegian,
romance languages like French or Spanish, African Swahili, and Vietnamese.

A string can be a word:

```text
hello
```

A string can also be a sentence:

```text
The computer was invented in order to automate mathematical calculations that were previously completed by people.
```

Or a string can be a paragraph from an article:

```text
Babbage is considered by some to be "father of the computer".
Babbage is credited with inventing the first mechanical computer, the Difference Engine, that eventually led to more complex electronic designs, though all the essential ideas of modern computers are to be found in Babbage's Analytical Engine, programmed using a principle openly borrowed from the Jacquard loom.
Babbage had a broad range of interests in addition to his work on computers covered in his 1832 book Economy of Manufactures and Machinery. His varied work in other fields has led him to be described as "pre-eminent" among the many polymaths of his century.
```

As you can see, a string can be as long as you want it to be.
It can be a single character (`a`), an empty character containing no characters (` `), your favorite
emojis `🤣`, `🎅`, `🎆`, `🎇`, `🎈`, `🎉`, `🎄`, `🍕`, `🍺`, `🍩`, `🍪`, `🍫`, `🍬`, `🍭`, `🍮`, or a whole book.

As a JavaScript developer, you will often need to create strings, manipulate strings, and compare strings.
You may need to create strings to store textual data, convert strings to uppercase, lowercase, or title case, split a
string into an array of substrings, concatenate two or more strings, search for a substring, replace a substring,
reverse a string, trim a string, sort a string, compare two strings, and so on.

There are many
built-in [methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#constructor)
that can be used to work with strings.
In this article, we will explore some useful string methods.
However, before we do, we first need to know that there are two types of strings in JavaScript:
string primitives and string objects.
Let's jump right in and explore these two types of string.

## String Primitives vs String Objects

A string [primitive](https://developer.mozilla.org/en-US/docs/Glossary/Primitive) is a string that is not an object and
has
no methods.
A method is a function associated with an object.
A string [object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object) is a wrapper
around the string primitive data type.
To understand these two types of strings, take a look at the following code snippet:

```javascript
const stringPrimitive = 'I am a string primitive.'; // string literal

const anotherStringPrimitive = String('I am also a string primitive.'); // String constructor

const stringObject = new String('But I am a string object.'); // String constructor

// check the type of each variable
console.log(typeof stringPrimitive); // string

console.log(typeof anotherStringPrimitive); // string

console.log(typeof stringObject); // object
```

In the code above, `stringPrimitive` and `anotherStringPrimitive` variables are string primitives.
The only difference between the two is that `stringPrimitive` was created
using a string literal and `anotherStringPrimitive` was created using the `String` constructor.
Our last variable, `stringObject`, is a string object also created using the `String` constructor.
Do not worry if you are not familiar with the `String` constructor.
I will explain it in more detail in this article.
Meanwhile, let's take a look at the difference between string primitives and string objects.

## String Primitives

As seen in the code above, there are two ways to create primitive strings.
You can create primitive strings using string literals or the `String` constructor.

String literals are the most common way to create strings in JavaScript.
To create a string literal, you enclose the string in single quotes `' '`, double quotes `" "`, or backticks `` ` ` ``.

The following are valid string primitives using the string literals:

```javascript
'I am a string primitive.'; // string literal

"I am also a string primitive."; // string literal

`I am a template literal.`; // template literal
```

The second way to create primitive strings in JavaScript is to use the `String` constructor.
The `String` constructor is a built-in global object in JavaScript that represents a string of text.

The following are valid strings primitives using the `String` constructor:

```javascript
String('I am a string primitive.'); // String constructor with single quotes

String("I am also a string primitive."); // String constructor with double quotes

String('I am also a string primitive.'); // String constructor
```

Note that in the above code snippet, the `String()` constructor is called without the `new` keyword.
There is a difference between calling the `String()` constructor with or without the `new` keyword.
We will cover this difference in our next section, string objects.

## String Objects

String objects are created using the `String` constructor.
To create a string object, you use the `new` keyword with the `String` constructor.

The following are valid string objects using the `String` constructor:

```javascript
new String('I am a String object.'); // String constructor with single quotes

new String("I am also a String object."); // String constructor with double quotes

new String(`I am also a String object.`); // String constructor with backticks
```

Note that this time the `String()` constructor is called with the `new` keyword.
This is evident that the `String` constructor can be used with or without the `new` keyword.
When the `String()` constructor is called without the `new` keyword,
it returns a string primitive.
However, when the `String()` constructor is called with the `new` keyword, it returns a `String` object.

Take a look at the flowing code snippet:

```javascript
const stringObject = new String('Hello, world'); // string object
console.log(typeof stringObject); // object

const stringPrimitive = String('Hello, world'); // String primitive
console.log(typeof stringPrimitive); // string
```

Although it is rarely used to create strings,
it is important to know
that the `String` constructor can be used to create string primitives and string objects.
What you need to know is that regardless of how a string is primitive is created,
it is still a string primitive type and has no methods of its own.
On the other hand, a string object is an instance of the `String` object and has many methods of its own.
With this fact in mind, we may be tempted to think that from the code above, `stringPrimitive` has no methods at all.
However, this is not the case.
As they say, the devil is in the details.
Let's take a look at the details:

```javascript
console.log(stringPrimitive.toUpperCase()); // HELLO, WORLD
````

Wait a mousy minute!
The `toUpperCase()` method is used to convert the string primitive to uppercase.
Why does the `toUpperCase()` method work on a string primitive
when string primitives have no methods of their own?
The answer is coercion.
JavaScript behind the scenes converts string primitives to string objects
when a string primitive is used with a method.
For this reason, you can use the `String` constructor methods such as `toUpperCase()`,
`toLowerCase()`, `charAt()`, and so on as if they were string objects.
This is because JavaScript automatically coerces a string primitive to a string object if the `new` keyword is not used.

In summary, there are two types of strings in JavaScript: string primitives and string objects.
Primitive strings can be created as string literals using single quotes `' '`,
double quotes `" "`, or backticks `` ` ` ``.
Primitive strings can also be created using the `String` constructor without the `new` keyword.
When the `String` constructor is called with the `new` keyword, it returns a string object.
JavaScript converts string primitives to string objects behind the scene when a string primitive is used with a method.
For this reason, you can use methods on string primitives as if they were string objects.
Now, are you ready to have fun working with strings?

## Working with Strings

As we said earlier, although primitive strings and string objects are different data types,
they can be used in the same way.
That is, you can use the same methods on both string primitives and string objects.

Let's see this in action using the `toUpperCase()` and `slice()` methods:

```javascript
const greeting = 'Hello, world';

const name = 'john';

const sentence = `${greeting}, my name is ${name.charAt(0).toUpperCase() + name.slice(1)}.`;
```

In the above code snippet, the `toUpperCase()` method is used to convert the first letter of `name` to uppercase.
The `slice()` method is used to extract the rest of the string after the first letter.
The `+` operator is used to concatenate the uppercase letter with the rest of the string.
So, the output of `sentence` is `Hello, world, my name is John.`.
If you do not understand the above code snippet, don't worry.
String along,
as we work with string methods in the upcoming sections.
Before we do, let's take cover two key concepts about strings: immutability and iterability.
Let's start with immutability.

## String Immutability

Strings are immutable, which means that once they are created, their values cannot be changed.
String immutability is a property of strings in JavaScript that prevents them from being changed once they are created.
This means that once you create a string, you cannot change its contents, length, or any of its properties.

There are a few ways to work around this limitation.
One way is to create a new string with the modified contents.
Another way is to use a string object that implements the `.replace()` method. We will learn about the `.replace()`
method when we cover string methods.

Another way to work around this limitation is to use the `String` constructor. Recall that the `String` constructor can
be used to create string primitives and string objects. When the `String` constructor is called with the `new` keyword,
it returns a string object. String objects are mutable. They can be changed. For example, the following code snippet
creates a string object called `name` that stores the value `John`:

```javascript
const name = new String('John');
```

The `name` variable stores a string object that can be changed. For example, the following code snippet changes the
value of the `name` variable from `John` to `Jane`:

```javascript
let name = new String('John');
name = 'Jane'; // name is now changed to a string primitive

console.log(name); // Jane
```

Here is an example of how to use the `.replace()` method to modify a string:

```javascript
const str = "Hello, world!";
const newStr = str.replace("world", "universe");
console.log(newStr); // "Hello, universe!"
```

Take a look at the following code snippet:

```javascript
let name = 'John';

name = 'Jane';

console.log(name); // Jane
```

In the above code snippet, the `name` variable is declared using the `let` keyword. The `let` keyword is used to declare
a variable that can be reassigned a new value. The `name` variable is assigned the value `John`. The `name` variable is
then reassigned the value `Jane`. The output of `console.log(name)` is `Jane`. Looking at the code above, one might
think that the `name` variable was changed from `John` to `Jane`. However, this is not the case. The `name` variable was
not changed from `John` to `Jane`. The `name` variable was reassigned a new value. The `name` variable was reassigned
the value `Jane`. This is because, as we said earlier, strings are immutable. They cannot be changed once they are
created.

For example, the `toUpperCase()` method is used to convert a string to uppercase.
The `toUpperCase()` method is attached to the `String` object.
It is used to perform an action on the `String` object.
The `toUpperCase()` method is called on a string and returns a new string with the uppercase letters.
For example, the following code snippet calls the `toUpperCase()` method on the `String` object instance `name`:

```javascript
const name = new String('John');
name.toUpperCase(); // JOHN
```

In the above code snippet, the `toUpperCase()` method is called on the `String` object instance `name`.
The `toUpperCase()` method converts the string `John` to uppercase and returns a new string with the uppercase letters.
The `toUpperCase()` method does not change the original string.
It returns a new string with the uppercase letters.
The original string is unchanged.
This is known as immutability.
Strings are immutable.
They cannot be changed once they are created. With this in mind, let's take a look at string iterability.

## String Iterability

First, let's recognize that the word "iterability" is not a real word. It is a made-up word to describe the ability to
be iterated over. When we say that strings are iterable, we mean that you can access each character in a string
individually using loops.

For example, the following
code snippet iterates over the characters in the string primitive `name` and logs each character to the console:

```javascript
const name = 'John';

for (const character of name) {
    console.log(character);
}
```

The output of the above will look something like this:

```text
J
o
h
n
```

String iterability is a property of strings in JavaScript that was introduced in ES6. In the previous code snippet, we
used the `for...of` loop to iterate over the characters in the string primitive `name`. The `for...of` loop is used to
iterate over the characters in the string primitive `name`. Now, with this added knowledge, let's learn about creating
strings.

## Creating Strings

To create primitive strings using string literals,
you enclose the string in single quotes `' '`, double quotes `" "`, or backticks `` ` ` ``.

The following are valid string literals:

```javascript
const greeting = 'Hello, world'; // single quotes

const name = "John"; // double quotes

const sentence = `Hello, my name is ${name}.`; // backticks
```

Creating a string primitive using single quotes `' '`, double quotes `" "`, or backticks `` ` ` `` is a matter of
preference.
The only requirement is that the opening and closing quotes must match.

The following are invalid string literals:

```javascript
const greeting = 'Hello, world"; // SyntaxError: Unexpected identifier

const name = "John'; // SyntaxError: Unexpected identifier

const sentence = `Hello, my name is ${name}.'; // SyntaxError: Unexpected identifier

const name = String('John"); // SyntaxError: Unexpected identifier
```

If you use single quotes to create a string, you must use single quotes to close the string.
The same goes for double quotes and backticks.
Single quotes and double quotes are interchangeable.
However, backticks are not interchangeable with single quotes or double quotes.
Backticks are used to create template literals.
We will learn about template literals in this article.

Using single quotes `' '` or double quotes `" "`,
or backticks `` ` ` `` to create a string primitive is a matter of preference.
However, there are some use cases where one method may be preferred over the other.
Let's look at some use cases where one method may be preferred over the other.

### Single Quotes (`' '`)

Single quotes are the most common way to create strings in JavaScript.
They are used to create strings that are short
and readable.
Single quotes are also used to create strings that contain double quotes.
For example, the following code snippet
creates a string variable called `sentence` that stores the value `He said, "Watch the giant fall."`:

```javascript
const sentence = 'He said, "Watch the giant fall."';

console.log(sentence); // He said, "Watch the giant fall."
```

In the above code snippet, the single quotes (`''`) are used to enclose the string.
The double quotes (`""`) are used to enclose the string that contains double quotes (`""`).
However, if you try to create a string that contains single quotes using single quotes, you will get an error:

```javascript
const sentence = 'He said, '
Watch
the
giant
fall.
'; // SyntaxError: Unexpected identifier
```

In the above code snippet, the single quotes (`''`) are used to enclose the string.
The single quotes (`''`) are also used to enclose the string that contains single quotes (`'`).
However, the single quotes (`''`) are not escaped.
So,
the JavaScript interpreter thinks that the string ends at the first single quote
(`'`) and the rest of the string is invalid JavaScript code.

### Double Quotes (`" "`)

Double quotes (`""`) are also used to create strings that are short and readable.
They are used to create strings that contain single quotes:

```javascript
const sentence = "I can't believe it's not butter!";
```

In the above code snippet,
the double quotes (`""`) are needed to enclose the string because the string contains words that contain single quotes
(`'`).
Because an apostrophe is used in the words `can't` and `it's`, the string must be enclosed in double quotes (`""`).
Enclosing the string in single quotes (`''`) would result in a syntax error:

```javascript
const sentence = 'I can'
t
believe
it
's not butter!'; // SyntaxError: Unexpected identifier
```

In the above code snippet, the single quotes (`''`) are used to enclose the string.
Because an apostrophe is the same as a single quote (`'`),
the JavaScript interpreter thinks that the string ends at the first single quote
(`'`) and the rest of the string is invalid JavaScript code.

Double quotes (`""`) are also used to create strings that contain double quotes:

```javascript
const sentence = "He said, \"Watch the giant fall.\"";
```

### Backticks (` `` `)

Backticks are used to create template literals.
Template literals are used to create strings that contain placeholders.
This is known as string interpolation.
String interpolation is a process of evaluating a string literal containing one or more placeholders.
It is a feature of ES6 that allows you to insert variables into a string.

Let's take a look at an example of string interpolation:

```javascript
const sentence = `He said, "Watch the giant fall."`;
```

While the above code snippet works, it is not the ideal way to create a string that contains placeholders.
That is, when using template literals, you should use placeholders instead of hard-coding the values.
Your string should contain placeholders that will be replaced with the actual values.
Your placeholders can be variables, expressions, or functions.

The follow code snippet demonstrates how to use placeholders in a template literal:

```javascript
const noun = 'giant';
const sentence = `He said, "Watch the ${noun} fall."`;
console.log(sentence); // He said, "Watch the giant fall."

const number = 100;
const sentence = `He said, "Watch the ${number} foot ${noun} fall."`;
console.log(sentence); // He said, "Watch the 100 foot giant fall."

const getNoun = () => 'giant';

const sentence = `He said, "Watch the ${getNoun()} fall."`;
console.log(sentence); // He said, "Watch the giant fall."
```

In the above code snippet, the placeholders are indicated by the dollar sign and curly braces `${}`.
The placeholders are replaced with the value of the variables, expressions, or functions.
For example, the placeholder
`${noun}` is replaced with the value of the variable `noun`, which is `giant`.
The placeholder `${number}` is replaced with the value of the variable `number`, which is `100`.
The placeholder
`${getNoun()}` is replaced with the value of the function `getNoun()`, which is `giant`.
The output of first `console.log(sentence)` is `He said, "Watch the giant fall."`.
The next output is `He said, "Watch the 100 foot giant fall."`.
And the last output is `He said, "Watch the giant fall."`.

### Escape Sequences

In computer science,
escape sequences are character combinations that have a different meaning than the characters they contain.
They are used to represent characters that are difficult or impossible to represent directly.

Escape sequences are used to represent:

- A newline character
- A single quotation mark
- Certain other characters in a character constant
- Special characters, such as tabs, carriage returns, and quotation marks

Here are some examples of escape sequences in most programming languages:

- `\n` - newline
- `\t` - tab
- `\r` - carriage return
- `\b` - backspace
- `\'` - single quote
- `\"` - double quote
- `\\` - backslash

In JavaScript, the backslash (`\ `) is used as an escape character.
An escape character is a character that has a special meaning in JavaScript.
For example, the single quote (`'`) is a special character in JavaScript.
It is used to enclose strings.
However, if you want to use a single quote (`'`) in a string that is enclosed in single quotes (`''`),
you must escape it using the backslash (`\ `).

Let's go back to one of our earlier examples:

```javascript
const sentence = "I can't believe it's not butter!";
```

Because an apostrophe is used in the words `can't` and `it's`, the string must be enclosed in double quotes (`""`).
However, if you still wanted to enclose the string in single quotes (`''`), you would have to escape the single quotes
(`''`) using the backslash (`\ `):

```javascript
const sentence = 'I can\'t believe it\'s not butter!';
```

In the above code snippet, the backslash (`\ `) is used to escape the single quotes (`''`) in the string.
The escape character (`\ `) can also be used to escape double quotes
(`""`) in a string that is enclosed in double quotes
(`""`).
For example,
the following code snippet creates a string variable called `sentence` that stores the
value `He said, "Watch the giant fall."`:

```javascript
const sentence = "He said, \"Watch the giant fall.\"";
```

In the above code snippet, the backslash (`\ `) is used to escape the double quotes (`""`) in the string.

### Concatenating Strings

Sometimes you may need to build a string by concatenating two or more strings together.
A string can be concatenated by joining together two or more strings.
The `+` operator is used to concatenate strings.
As we said earlier, a data type defines the operations that apply to the data.
The `+` operator is used to add numbers together.
However, when the `+` operator is used with strings, it is used to concatenate strings together.
For example, the following code snippet concatenates the strings `hello` and `world` together:

```javascript
'hello' + 'world'; // helloworld
```

As stated, we can also build strings by interpolating variables, expressions, or functions into a string using template
literals.

```javascript
const greeting = 'Hello';
console.log(`${greeting}! I'm a template literal.`); // Hello! I'm a template literal.
```

### String `length` Property

The `String` data type has a special property called `length` that returns the length of a string. The length of a
string is the number of characters in the string. A property is the value of an object. A property has a name and a
value. You may think of it as a variable attached to an object. It can be a primitive value, like a number or string, or
it can be a function, known as a method which we will cover next. A property is accessed by using the dot (`.`)
notation. The dot notation is used to access the properties and methods of an object. You have seen this throughout this
article when we used the `console.log()` method to log a value to the console.

```javascript
console.log('Hello world.'); // Hello world.
```

In the above code snippet, the `console` object has a method called `log` that is used to log a value to the console. We
can access `log` method by using the dot (`.`) notation as in `console.log()`.

String indexing starts at zero. Therefore, JavaScript indexes the first character in a string at zero as in `0`, `1`,
`2`, `3`, and so on. Please note that this does not mean that the first character in a string is zero. This also does
not mean that when we count the length of a string like `John`, we start counting at zero and say that the length
of `John` is `3` as in `0`, `1`, `2`, `3`. When we count the characters in a string, we start counting at `1` as
in `1`, `2`, `3`, `4`, and so on. Therefore, the length of `John` is `4`. However, when we index the characters in a
string, we start indexing at zero as in `0`, `1`, `2`, `3`, and so on. Indexing and counting are two different things. A
string's length is the number of characters in the string. A string's index is the position of a character in the
string. Indexing starts at zero. Counting starts at one. For example, the following code snippet returns the length of
the string `John` and the index of the first character in the string `John`:

```javascript
const name = 'John';
console.log(name.length); // 4

console.log(name.charAt(0)); // J
```

In the above code snippet, the `length` property is used to get the length of the string `John`. The `length` property
is accessed by using the dot (`.`) notation as in `name.length`. The `length` property returns the length of the
string `John`, which is `4`. The `charAt()` method is used to get the character at index `0` in the string `John`.
The `charAt()` method is accessed by using the dot (`.`) notation as in `name.charAt(0)`. The `charAt()` method returns
the character at index `0` in the string `John`, which is `J`.

Note that the `length` property returns the number of characters in a string, and not only the numbers of letters. As we
said earlier, characters are symbols including letters, punctuation, and various other written marks in a language.
Therefore, the `length` will return the total number of characters in a string, including letters, punctuation,
whitespaces, and so on. The `lenght` property does count an escape sequence (one or more special characters) as one
character because it has a special meaning in JavaScript.

```javascript
const name = 'John' + '\t' + 'Doe';
console.log(name); // John  Doe
console.log(name.length); // 8
```

In the above code snippet, the `name` variable stores the string `John` concatenated with the tab escape sequence
(`\t`) and the string `Doe`. The tab escape sequence (`\t`) is used to insert a tab in a string. The `name` variable is
then logged to the console. The output of `console.log(name)` is `John  Doe`. The `length` property is then used to get
the length of the string `John  Doe`. The `length` property returns the length of the string `John  Doe`, which is `8`.
The `length` property returns `8` because the tab escape sequence (`\t`) is counted as one character.

Note that an empty string has a length of `0`. This is because the empty string contains no characters.

```javascript
const emptyString = '';
console.log(emptyString.length); // 0
```

However, the empty string is not the same as a string that contains a space. A string that contains a space is not an
empty string. It is a string that contains a space, which is a character.

```javascript
const space = ' ';
console.log(space.length); // 1
```

As seen in the code snippet above, the `space` variable stores a string that contains a space. So if you created a
string that stores a sentence that contains multiple whitespaces and other characters, the `length` property will return the
total number of characters in the string, including these whitespaces and other characters.

```javascript
const sentence = 'The quick brown fox jumps over the lazy dog.';

console.log(sentence.length); // 44
```

The `length` property is the only property of the String data type. It is a commonly used property of the `String`
object. Also, indexing is a commonly used technique when working with strings. Therefore, it is important to understand
the difference between indexing and counting. Now we are ready to learn about string methods.

## String Methods

Methods are functions that are attached to an object. They are used to perform an action on the object. While strings
methods do not change the original string, however, they return a new string with the changes. Some methods take
arguments and some do not. Arguments are values that are passed to a function. Arguments are used to customize the
behavior of a function.

For example, the`toUpperCase()` method is used to convert a string to uppercase.The`toUpperCase()` method is attached to
the`String` object. It is used to perform an action on the`String` object. The`toUpperCase()` method is called on a
string and returns a new string with the uppercase letters. For example, the following code snippet calls
the`toUpperCase()` method on the`String` object instance`name`:

```javascript
const name = 'john';

console.log(name.charAt(0).toUpperCase() + name.slice(1)); // John
```

In the code snippet above, `charAt(0)` is used to get the first character of the string `name`. The `toUpperCase()`
method is used to convert the first letter of `name` to uppercase. The `slice()` method is used to extract the rest of
the string after the first letter. The `+` operator is used to concatenate the uppercase letter with the rest of the
string. So, the output of `console.log(name.charAt(0).toUpperCase() + name.slice(1))` is `John`. Again, if you do not
understand the code above, by the end of
this article, you will learn how to use some of the most commonly used string methods.

The `String` object has a number of methods that allow you to manipulate the string.
There are two types of methods available on the `String` object: static methods and prototype methods.
Static methods are called directly on the `String` object.
Prototype methods are called on an instance of the `String` object.
Let's cover these two types of methods next.

### Static Methods

When we say that static methods are called directly on the `String` object,
we mean that they are called directly on the `String` object without creating an instance of the `String` object.
That is, they are called on the `String` object itself.
You do not need to create an instance of the `String` object to call a static method.

For example, the following code snippet calls the `String.fromCharCode()` static method on the `String` object:

```javascript
String.fromCharCode(74, 111, 104, 110); // John
```

In the above code snippet, the `String.fromCharCode()` static method is called directly on the `String` object.
We did not need to create an instance of the `String` object to call the `String.fromCharCode()` static method as in the
following code snippet:

```javascript
const name = new String('John');
name.fromCharCode(74, 111, 104, 110); // TypeError: name.fromCharCode is not a function
```

The code above will throw an error because the `String.fromCharCode()` static method is not a prototype method.
It is a static method.
If the concept of static methods is new to you,
the easier way to think about static methods is to think of them as functions that are attached to the `String` object.
You may have seen this before when working with the `Math` or `Array` objects.
For example, the following code uses static methods on the `Math` and `Array` objects:

```javascript
Math.random(); // 0.12345678910111213

Math.ceil(1.1); // 2

Math.floor(1.9); // 1

Math.round(1.5); // 2

Array.isArray([1, 2, 3]); // true

Array.from('John'); // ['J', 'o', 'h', 'n']

Array.of(1, 2, 3); // [1, 2, 3]
```

As demonstrated in the code above, static methods are called directly on the `Math` and `Array` objects.
We did not need to create an instance of the `Math` or `Array` object to call the static methods.
We just called the static methods directly on the `Math` and `Array` objects.
The same goes for the `String` object.
What you need to know when using static methods is
that the name of the object is used to call the static method as in `Math.random()`,
`Math.ceil()`, `Math.floor()`, `Math.round()`, `Array.isArray()`,
`Array.from()`, `Array.of()`, and `String.fromCharCode()`.

### Prototype Methods

When we say that prototype methods are called on an instance of the `String` object,
we mean that they are called on an instance of the `String` object.
That is, they are called on the `String` object instance itself. You need to create an instance of the `String` object
to call a prototype method.

For example,
the following code snippet calls the `toUpperCase()` prototype method on the `String` object instance `name`:

```javascript
const name = new String('John');
name.toUpperCase(); // JOHN
```

In the above code snippet, the `toUpperCase()` prototype method is called on the `String` object instance `name`.
We cannot call the `toUpperCase()` prototype method directly on the `String` object as in the following code snippet:

```javascript
String.toUpperCase(); // TypeError: String.toUpperCase is not a function
```

The code above will throw an error because the `toUpperCase()` is not a static method.
It is a prototype method.

Whether using static or prototype methods, recall that JavaScript is case-sensitive.
Therefore, the object name must be capitalized and spelled exactly as it is in the documentation.
Therefore, `String.fromCharCode()` is not the same as `string.fromCharCode()`.
The same is true that `name.toUpperCase()` is not the same as `name.toUppercase()`.

Now that we've covered the two types of methods available on the `String` object,
it is time to learn about some of the most commonly used string methods.
Please note that this is not an exhaustive list of all the methods available on the `String` object.
There are many more methods available on the `String` object.
You can find a complete list of methods on
the [MDN web docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String#constructor).
With no further ado, let's get stringing with our first string method.

### `at(index)`

The `at(index)` method returns the character at the specified index in a string. Indexing starts at zero. For example,
the following code snippet returns the character at index 0 in the string `John`:

```javascript
const name = 'John';
console.log(name.at(0)); // J
```

### `charAt()`

The `charAt()` method returns the character at the specified index in a string. Indexing starts at zero. For example,
the following code snippet returns the character at index 0 in the string `John`:

```javascript
const name = 'John';
console.log(name.charAt(0)); // J
```

### `charCodeAt()`

## Useful String Methods

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
- `valueOf()` - returns the primitive value of a `String` object.
- `toString()` - returns a string representing the specified object.
- `fromCharCode()` - converts Unicode values to characters.
- `fromCodePoint()` - returns a string created by using the specified sequence of code points.
- `toUpperCase()` - converts a string to uppercase letters.
- `toLowerCase()` - converts a string to lowercase letters.
- `includes()` - determines whether a string contains the characters of a specified string.
- `endsWith()` - determines whether a string ends with the characters of a specified string.
- `startsWith()` - determines whether a string begins with the characters of a specified string.
- `repeat()` - returns a new string with a specified number of copies of an existing string.
- `padEnd()` - pads the current string with a given string (repeated, if needed) so that the resulting string reaches
  a given length.
- `padStart()` - pads the current string with another string (multiple times, if needed) until the resulting string
  reaches the given length.
- `match()` - searches a string for a match against a regular expression, and returns the matches, as an Array object.
- `matchAll()` - returns an iterator of all results matching a string against a regular expression, including
  capturing groups.
- `normalize()` - returns the Unicode Normalization Form of a given string.
- `repeat()` - returns a new string with a specified number of copies of an existing string.
- `replace()` - searches a string for a specified value, or a regular expression, and returns a new string where the
  specified values are replaced.
- `replaceAll()` - returns a new string with all matches of a pattern replaced by a replacement.