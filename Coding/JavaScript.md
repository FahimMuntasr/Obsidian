#JavaScript
#WebDev
#Coding
[[Web Development]]
# Arithmetic operators
| Operator       | Syntax     |
| -------------- | ---------- |
| Addition       | x = x + y  |
| Subtraction    | x = x - y  |
| Multiplication | x = x * y  |
| Division       | x = x / y  |
| Exponents      | x = x ** y |
| Modulus        | x = x % y  |
| Increment      | x++        |
| Decrement      | x--        |
# Operator Precedence
From left to right:
- Parantheses`()`
- Exponents `**`
- Multiplication`*` and Division`/`
- Addition `+` and Subtraction `-`
# User Input
---
Two ways of taking user input: Window prompt OR HTML textbox
### Window Prompts
```JavaScript
let input;

input = window.prompt("Enter input");
```
### HTML textbox
```HTML
<body>
	<label> Input: </label>
	<input id="userTxt">
	<button id="submitBtn">Submit</button>
</body>
```

```JavaScript
const button = document.getElementById("submitBtn");
const inputText = document.getElementById("userTxt");

let input;

button.onclick = function(){
	input = inputText.value;
	console.log(input)
}
```
# Type conversion
---
To check the type of a variable `typeof variable` is used.
To change a variable to a int/float data type, `Number(variable)` is used.
To change a variable to a string data type, `String(variable)` is used.
To change a variable to a boolean data type, `Boolean(variable)` is used.

# Practice Problem
---
Create a program with a text display and 3 buttons which have functionality of decreasing,increasing and resetting the display. CSS not needed
```HTML
<body>
	<p id="countDisplay">0</p>
	<button id="decreaseBtn">Decrease</button>
	<button id="resetBtn">Reset</button>
	<button id="increaseBtn">Increase</button>
</body>
```

```JavaScript
const display = document.getElementById("counterTxt");
const decrease = document.getElementById("decreaseBtn");
const reset = document.getElementById("resetBtn");
const increase = document.getElementById("increaseBtn");

let count = 0;

decrease.onclick = function(){
	count--;
	display.textContent = count;
}
reset.onclick = function(){
	count = 0;
	display.textContent = count;
}
increase.onclick = function(){
	count++;
	display.textContent = count;
}
```
# Math functions
---
### Constants

| Syntax       | Returns                 |
| ------------ | ----------------------- |
| Math.E       | Euler's number          |
| Math.PI      | pi                      |
| Math.SQRT2   | square root of 2        |
| Math.SQRT1_2 | square root of 1/2      |
| Math.LN2     | natural logarithm of 2  |
| Math.LN10    | natural logarithm of 10 |
| Math.LOG2E   | base 2 logarithm of E   |
| Math.LOG10E  | base 10 logarithm of E  |
### Functions (aka Methods)

| Syntax                | Returns                                 | Example                  |
| --------------------- | --------------------------------------- | ------------------------ |
| Math.round(x)         | x rounded to nearest integer            | Math.round(4.6) = 5      |
| Math.ceil(x)          | x rounded UP to nearest integer         | Math.ceil(3.1) = 4       |
| Math.floor(x)         | x rounded DOWN to nearest integer       | Math.floor(4.9) = 4      |
| Math.trunc(x)         | only the integer part of x              | Math.trunc(3.4) = 3      |
| Math.sign(x)          | if x is negative, positive or null      | Math.sign(-4.3) = -1     |
| Math.pow(x, y)        | x to the power y                        | Math.pow(8, 2) = 64      |
| Math.sqrt(x)          | square root of x                        | Math.sqrt(64) = 8        |
| Math.abs(x)           | absolute value of x                     | Math.abs(-4.7) = 4.7     |
| Math.sin(x)           | sine of x (in radians)                  | Math.sin(Math.PI) = 0    |
| Math.cos(x)           | cosine of x (in radians)                | Math.cos(Math.PI) = -1   |
| Math.tan(x)           | tangent of x (in radians)               | Math.tan(Math.PI) = 0    |
| Math.cbrt(x)          | cubic root of x                         | Math.cbrt(8) = 2         |
| Math.exp(x)           | E to the power of x                     | Math.exp(1) = e          |
| Math.log(x)           | natural log of x                        | Math.log(Math.E) = e     |
| Math.random()         | returns random number between 0 - 1     | Math.random() = 0.345    |
| Math.max(x,y,z,...,n) | returns max number                      | Math.max(1,2,3) = 3      |
| Math.min(x,y,z,...,n) | returns min number                      | Math.min(1,2,3) = 1      |
| --------------------  | --------------------------------------- | ------------------------ |
# String functions
---

| Function                   | What it does                                                                      |
| -------------------------- | --------------------------------------------------------------------------------- |
| text.length                | Returns length of the "text" string                                               |
| text.charAt(n)             | Returns the character at `n` index of `text`                                      |
| text.charCharAt(n)         | Returns UTF-16 code of the character at `n` index of `text`                       |
| text.at(n)                 | Returns the character at `n` index of `text`                                      |
| text[n]                    | Returns the character at `n` index of `text`                                      |
| text.slice(start,end)      | Returns the substring starting at `start` and ending at `end`                     |
| text.substring(start,end)  | Returns the substring starting at `start` and ending at `end`                     |
| text.substr(start, length) | Returns the substring starting at `start` with a length of `length`               |
| text.toUpperCase()         | Returns the string converted to upper case                                        |
| text.toLowerCase()         | Returns the string converted to lower case                                        |
| text.concat()              | Joins two or more strings to the end of a string                                  |
| text.trim()                | Removes whitespace from both sides of a string                                    |
| text.trimStart()           | Removes whitespace from the start of a string                                     |
| text.trimEnd()             | Removes whitespace from the end of a string                                       |
| text.padStart(4,character) | Pads the start of a string with `character` until the length is 4 characters long |
| text.padEnd(4,character)   | Pads the end of a string with `character` until the length is 4 characters long   |
| text.repeat(n)             | Returns `n` number of copies of the string                                        |
| text.replace(key, str)     | Searchs for the first occurence of `key` and replaces it with `str`               |
| text.split(char)           | Split the string into an array, you can specify what char to split it on          |
| text.indexOf(char)         | Returns the index of the first occurence of `char` in the string                  |
| text.lastIndexOf(char)     | Returns the index of the last occurence of `char` in the string                   |
| text.includes(string)      | Returns true if the text contains the search string                               |
| text.startsWith(string)    | Returns true if the text starts with the search string                            |
| text.endsWith(string)      | Returns true if the text ends with the search string                              |
