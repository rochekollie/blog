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
romance languages like French or Spanish, African Swahili and Vietnamese.

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

In this article, we will explore many ways to manipulate strings in JavaScript.
However, before we do, we first need to know that there are two types of strings in JavaScript.
A string can be a:

- string primitives, or a
- string objects

In the next section, we will explore the difference between these types.

## String Primitives vs String Objects

Strings can be created using the `String` object or using string literals.
A string literal is a sequence of characters enclosed in single quotes `' '`,
double quotes `" "`, or backticks `` ` ` ``.
For example, the following code snippet creates a string variable called `name` that stores the value `John`:

```javascript
const stringPrimitive = 'I am a string primitive.'; // string literal
```

In the above code snippet, the string `I am a string primitive.` is created using a string literal.
In the following code snippet a string object `I am a string object.` is created using the `String` constructor.

```javascript
const stringObject = new String('I am a String object.'); // String constructor
```

Each method has its own use case, and each method produces a different data type.
If we log the type of each variable to the console, we will see that `stringPrimitive` is a string primitive and that `stringObject` is a string object.

```javascript
console.log(typeof stringPrimitive); // string

console.log(typeof stringObject); // object
```

As shown in the code snippet above, we see that strings can be a primitive data type or an object.
However, it is important to note that the `String` constructor can be used with or without the `new` keyword.
When `String()` is called **with the `new` keyword**, it returns a `String` object.
When `String()` is called **without the `new` keyword**, it returns a string primitive.
We will also cover the difference between these two concepts in the next section.
What is important to know is that there are two types of strings in JavaScript: string primitives and string objects.
String along, as we explore these two string types beginning with the `string` primitive type.

## String Primitives

A [primitive](https://developer.mozilla.org/en-US/docs/Glossary/Primitive) is a data type that is not an object and has
no methods.
When strings are created using string literals, they are primitive data types.
They do not have properties and methods of their own.
This is because primitive data types are not objects.
As we said earlier, there are two ways to create a string primitive in JavaScript:

- Using string literals, or
- Using the `String` constructor

String literals are the most common way to create strings in JavaScript.
The `String` constructor is a built-in global object in JavaScript that represents a string of text.
Although it is rarely used to create strings,
it is important to know that the `String` constructor can be used to create strings.

### Creating String Primitives using String Literals

String primitives can be created using single quotes `' '`, double quotes `" "`, or backticks `` ` ` ``.
This is the most common way to create strings in JavaScript.
Creating a string primitive using single quotes `' '`, double quotes `" "`, or backticks `` ` ` `` has the same result.
The only requirement is that the opening and closing quotes must match.
So, if you use single quotes to create a string, you must use single quotes to close the string.
The same goes for double quotes and backticks.
The following code snippets will produce errors because the opening and closing quotes do not match:

```javascript
const name = 'John"; // beginning single quote, ending double quote
const name = "John'; // beginning double quote, ending single quote
const name = `John'; // beginning backtick, ending single quote
const name = `
John
"; // beginning backtick, ending double quote
const name = String('John"); // String constructor with beginning single quote, ending double quote
```

However, the below code snippets will not produce errors because the opening and closing quotes match:

```javascript
const name = 'John'; // single quotes

const name = "John"; // double quotes

const name = `John`; // backticks

const name = String('John'); // String constructor
```

Whether you use single quotes `' '`, double quotes `" "`,
or backticks `` ` ` `` to create a string primitive is a matter of preference.
However, there are some use cases where one method may be preferred over the other.
Let's look at some use cases where one method may be preferred over the other.

#### Single Quotes (` ' '` )

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
const sentence = 'He said, 'Watch the giant fall.'; // SyntaxError: Unexpected identifier
```
In the above code snippet, the single quotes (`''`) are used to enclose the string.
The single quotes (`''`) are also used to enclose the string that contains single quotes (`'`).
However, the single quotes (`''`) are not escaped.
So,
the JavaScript interpreter thinks that the string ends at the first single quote
(`'`) and the rest of the string is invalid JavaScript code.




#### Double Quotes (` " "` )

A string can also be created using double quotes (`""`).
Double quotes are also used to create strings that are short and readable.
They are used to create strings that contain single quotes.
For example, the following code snippet creates a
string variable called `sentence` that stores the value `He said, "Watch the giant fall."`:

```javascript
const sentence = "I can't believe it's not butter!";
```

There are many reasons you may want to use double quotes to create a string.
The following are some use cases where you may want to use double quotes to create a string: 

- String that contains single quotes: `"I can't wait to see you."`
- String that contains double quotes: `"He said, "Watch the giant fall.""`
- String that contains backticks: `"I'm a template literal."`

In the above code snippet, the double quotes (`""`) are used to enclose the string.
The single quotes (`''`) are used to enclose the string that contains single quotes (`'`).

In the code snippet above, the double quotes (`""`) are used to enclose the string.
The single quotes (`''`) are used to enclose the string that contains single quotes `'`. The backslash `\ ` is used to
escape the single quotes `'` in the string.

#### Escape Characters

To fix this error, you can escape the single quotes (`''`) using the backslash (`\ `):

```javascript
const sentence = 'He said, \'Watch the giant fall.\'';
````

Single quotes are also used to create strings that contain single quotes.
For example, the following code snippet creates a string variable called `sentence` that stores the
value `He said, "I'm a string."`:

```javascript
let sentence = 'He said, "I\'m a string."';

console.log(sentence); // He said, "I'm a string."
```

In the above code snippet, the double quotes (`""`) are used to enclose the string. The single quotes (`''`) are used to
enclose the string that contains double quotes (`""`).

```javascript
let sentence = 'He said, "I\'m a string."';
```

In the above code snippet, the backslash `\ ` is used to escape the double quotes `"` in the string. The backslash `\ `
is used to escape characters that have special meaning in JavaScript.

#### Backticks (` `` `)

Backticks are used to create template literals. Template literals are used to create strings that contain placeholders.
For example, the following code snippet creates a string variable called `sentence` that stores the
value `He said, "Watch the giant fall."`:

```javascript
const sentence = `He said, "Watch the giant fall."`;
```

### Building and Concatenating Strings

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

# START PLACEHOLDER

However, it is important to note that the `String` constructor can be used with or without the `new` keyword.
When `String()` is called **with** the `new` keyword, it returns a `String` object.
When `String()` is called **without** the `new` keyword, it returns a string primitive.

A string primitive is created using single quotes `' '`, double quotes `" "`, or backticks `` ` ` ``.
The following code snippets show how to create strings using each of these methods.

A string primitive is created using single quotes `' '`, double quotes `" "`, or backticks `` ` ` ``.
The following code snippets show how to create strings using each of these methods.

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

const name = 'john';

const sentence = `${greeting}, my name is ${name}.`;

const stringPrimitive = String('I am also a primitive.');
```

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

const name = 'john';

const sentence = `${greeting}, my name is ${
    name.charAt(0).toUpperCase() + name.slice(1)
}.`;
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
However, JavaScript behind the scenes converts string primitives to string objects when a string primitive is used with
a method.
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
