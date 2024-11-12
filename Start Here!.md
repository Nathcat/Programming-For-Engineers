# Variables and data types
```c
int main() {
	int a = 0;
	float b = 2.54f;
}
```

Know what this does? It's fine if you don't, that's what we're here to fix :)

Let's break this down shall we.

## What is a _variable_?
A variable is a _very_ important thing in programming of any language. They are a location in memory which can be used to store data _which may change during the course of a program_.

Conversely a _constant_ is a location in memory which can be used to store data _which will **not** change during the course of a program_.

When we talk about memory here, we're talking about a computer's _**RAM**_, or _primary memory_, not your hard drive, that's a whole different ball game.

So, ignoring the whole `int main` bits in the code for now, lets look at the rest of it:
```c
int a = 0;
```
This is the syntax for declaring variables in C, here we are _declaring_ a variable called `a`, and then _assigning_ it the value `0`, we also specify the _data type_ of the variable as `int`.

An `int` is a data type, the primitive data types in C are:
- `int` - A whole number (integer)
- `float` - A decimal number
- `double` - A more accurate decimal number (allows more digits after the decimal point)
- `char` - A single character.
Each represents a piece of data, there are different rules for how you can use and manipulate each of these data types.

So in our program above:
```c
int a = 0;
float b = 0.54f;
```
We define two variables, an integer `a`, and a decimal number `b`, and assign the values `0` and `0.54f`. Now you might be thinking, _why is there an "f" after the decimal number?????_ Well my friend, we put the `f` there to explicitly tell C that this number is a float. If we just had `0.54`, C would _assume_ that it is a double, the `f` tells it that that number is a float. This brings us nicely onto the topic of _literals_.

## Literals
A literal is an actual value in your code, in our code above we are assigning values to the variables using literals, `0` is an integer literal, and `0.54f` is a float literal, while `0.54` is a double literal.

There are other kinds of literals, `'a'` is a character literal, note that `'ab'` would be invalid since the `char` type can only contain a _single character_. A string literal is enclosed by `""`, like: `"Hello world"`. But what is a string? I hear you ask.

A string is an _array of characters_, although they are very commonly used, strings are not technically primitive types like `int` or `char`, they are a _collection_ of primitive types, namely `char`s.

```c
int i = 0;
float f = 0.54f;
double d = 0.36;
char c = 'a';
```

So what is an array?
## Arrays
An array is a fixed length collection of values, all of which are of the same type. i.e. you can have an array of `int`s, and a separate array of `char`s, but you cannot have a single array which contains _both_ `int`s and `char`s.

You can declare an array like so:
```c
int a[20];
```
Where the `a` is the name of the variable containing the array, `int` is the type of each value in the array, and the number inside the square brackets is the length of the array, or the number of items it can store.

Declaring an array like that will initialise all the values stored by the array to be nothing (technically they would be whatever value was left in memory but this is meaningless to your program).

If you want to specify the actual values in the array, you can declare it like this:

```c
int a[] = {1, 2, 3, 4, 5, 6};
```

Here we declare an array `a` containing the integer values 1 through 6. Note we no longer have the number inside the square brackets, and we use curly braces to bound the values of the array.

You can reference a particular value in an array like so:
```c
a[3]
```
Where `a` is the name of the array, and the value inside the square brackets is the index of the value you want. Note that array indices are zero-based, meaning the first element in the array is at index 0, and the last is at `a.length - 1`.

You can also use this syntax to assign values to indices in an array:
```c
a[2] = 4;
```
This assigns the value `4` to the 3rd element in the array `a`.


Next go to functions.