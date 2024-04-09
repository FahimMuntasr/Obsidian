`Fahim Muntasir`
# Contents
- [[#Computer Architecture]]
- [[#Introduction to C]]
- [[#General syntax]]
- [[#Data types and variables]]
- [[#Operators]]
- [[#*if...else* statements]]
- [[#Switch case statements]]
- [[#Loops]]
- [[#Arrays]]
- [[#Strings]]
- [[#User input]]
- [[#Memory addresses]]
# Computer Architecture
#### Types of number systems
###### Decimal (base 10) : 
- 0,1,2,3,4,5,6,7,8,9
- used by ***HUMANS***
###### Binary (base 2) : 
- 0,1
- used by ***COMPUTERS***
###### Octal (base 8) :
- 0,1,2,3,4,5,6,7
- used to ***REPRESENT*** large binary digits
###### Hexadecimal (base 16) :
- 0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F
- used to ***REPRESENT*** large binary digits
#### Bits and Bytes
A **single** binary digit is called a bit
A **collection** of 8 bits is called a byte
One byte is the standard **unit** of measurement of data

#### Conversion between types of number systems
###### Binary to decimal 
(101001)<sub>2</sub> ---> ( ? )<sub>10</sub>
> keep adding the product of 2<sup>n</sup> and the nth number (n starts from 0 on the far right side)

1 x 2<sup>0</sup> =  1
0 x 2<sup>1</sup> =  0
0 x 2<sup>2</sup> =  0
1 x 2<sup>3</sup> =  8
0 x 2<sup>4</sup> =  0
<u>1 x 2<sup>5</sup> =  32</u>
1+0+0+8+0+32 = 41 

(101001)<sub>2</sub> ---> (41)<sub>10</sub>
###### Octal to decimal
(724)<sub>8</sub> ---> ( ? )<sub>10</sub>
> keep adding the product of 8<sup>n</sup> and the nth number (n starts from 0 on the far right side)

4 x 8<sup>0</sup> =  4
2 x 8<sup>1</sup> = 16
<u>7 x 8<sup>2</sup> =  448</u>
    468

(724)<sub>8</sub> ---> (468)<sub>10</sub>
###### Hexadecimal to decimal 
(ABC)<sub>16</sub> ---> ( ? )<sub>10</sub>
> keep adding the product of 16<sup>n</sup> and the nth number (n starts from 0 on the far right side)

C x 16<sup>0</sup> = 12 x 1 =      12
B x 16<sup>1</sup> = 11 x 16 =    176   
<u>A x 16<sup>2</sup> = 10 x 256 = 2560</u>
12+176+2560 = 2748

(ABC)<sub>16</sub> ---> (2748)<sub>10</sub>
###### Decimal to binary
(41)<sub>10</sub> ---> ( ? )<sub>2</sub>
> Keep dividing the number by 2 until the number becomes 0, after that join the remainders from top to bottom

41 / 2 => 20      (1) 
20 / 2 => 10      (0)
10 / 2 => 5        (0)
5 / 2 => 2          (1)
2 / 2 => 1          (0)
1 / 2 => 0          (1)
Join numbers from top to bottom,

(41)<sub>10</sub> ---> (101001)<sub>2</sub>
###### Decimal to octal
(1234)<sub>10</sub> ---> ( ? )<sub>8</sub>
> Keep dividing the number by 8 until the number becomes 0, after that join the remainders from top to bottom 

1234 / 8 => 154  (2) 
154 / 8 => 19      (2)
19 / 8 => 2          (3)
2 / 8 => 0            (2)
Join numbers from top to bottom,

(1234)<sub>10</sub> ---> (2322)<sub>8</sub>
###### Decimal to hexadecimal 
(1234)<sub>10</sub> ---> ( ? )<sub>16</sub>
> Keep dividing the number by 16 until the number becomes 0, after that join the remainders from top to bottom 

1234 / 16 => 77         (2) 
77/ 16 => 4      (13 => D)
4 / 16 => 0                 (4)
Join numbers from top to bottom,

(1234)<sub>10</sub> ---> (4D2)<sub>16</sub>
###### Octal to binary
(705)<sub>8</sub> ---> ( ? )<sub>2</sub>
> Convert each digit to a 3 bit binary number and then join them up

5 => 101
0 => 000
7 => 111
joining the digits,
(705)<sub>8</sub> ---> (111000101)<sub>2</sub>
###### Binary to octal 
(1011010111)<sub>2</sub> ---> ( ? )<sub>8</sub>
> Split the number into 3 bits starting from the right and then convert, add 0 to the front if the number cannot be evenly split into 3

111 => 7
010 => 2
011 => 3
001 => 1
joining numbers,
(1011010111)<sub>2</sub> ---> (1327)<sub>8</sub>
###### Hexadecimal to binary
(10AF)<sub>16</sub> ---> ( ? )<sub>2</sub>
> convert each symbol to a 4bit binary number, if the symbol is an alphabet then convert the value of that alphabet to binary

F = 15 => 1111
A = 10 => 1010
0 => 0000
1 => 0001
Joining the numbers,

(10AF)<sub>16</sub> ---> (0001000010101111)<sub>2</sub>

###### Binary to hexadecimal
(1010111011)<sub>2</sub> ---> ( ? )<sub>16</sub>
> split into 4 bits and then convert the values

1011 => B
1011 => B
0010 => 2
joining the numbers,
(1010111011)<sub>2</sub> ---> (2BB)<sub>16</sub>
###### Octal to hexadecimal
(1076)<sub>8</sub> ---> ( ? )<sub>16</sub>
> convert to binary first and then convert to hexadecimal

6 => 110
7 => 111
0 => 000
1 => 001
joining numbers,

(1076)<sub>8</sub> ---> (001000111110)<sub>2</sub>

1110 => 14 = E
0011 => 3
0010 => 2
joining numbers,

(001000111110)<sub>2</sub> ---> (23E)<sub>16</sub>

(1076)<sub>8</sub> ---> (001000111110)<sub>2</sub> ---> (23E)<sub>16</sub>
###### Hexadecimal to octal
(1F0C)<sub>16</sub> ---> ( ? )<sub>8</sub>
> convert to binary then convert to hexadecimal

C = 12 => 1100
0 => 0000
F = 15 => 1111
1 => 0001
joining numbers,

(1F0C)<sub>16</sub> ---> (0001111100001100)<sub>2</sub>

100 => 4
001 => 1
100 => 4
111 => 7
001 => 1
joining numbers,

(00001111100001100)<sub>2</sub> ---> (17414)<sub>8</sub>

(1F0C)<sub>16</sub> ---> (0001111100001100)<sub>2</sub> ---> (17414)<sub>8</sub>
#### Complements 
##### Types of Complements
For a number of base r, two types of complements can be found
- r's complement
- (r-1)'s complement
If N is a number of base r having n digits then
- r's complement of N = r<sup>n</sup> - N
- (r-1)'s complement of N = r<sup>n</sup> - N - 1
##### Shortcut to find complements
let r=> 10
(r - 1) => 9
9 - 5 = 4
9 - 7 = 2
9 - 6 = 3
9 - 3 = 6
(r-1)'s complement of 3675 is 6324

To find r's complement, add 1 to (r-1)'s complement

##### 2's complements
Finding the 2's complement for any binary number is simple; keep leading zeros and first one as is  and flip everything after that.

Example:
The 2's complement for 00001010 = 11110110

---

#### The software development pipeline
1. Source code first written 
2. Compiler converts code to machine language
3. Library files are linked to the code with a linker 
4. Linker then converts the code to an executable file
#### Types of memory
- ROM (Read only memory)
	- Non-volatile memory with persistence. This means that the data inside stays the same even after rebooting the computer.
	- Extremely high storage (~Terabytes) but at the cost of low speed.
	- Used to store BIOS settings (which contains information on how to start the computer) and save large user files.
- RAM (Random access memory)
	 - Volatile memory without persistence. This means that turning off the computer will erase all data inside.
	 - Compared to ROM, storage is very limited (~Gigabytes) but with very high read/write speeds.
	 - Contains instructions and data needed for currently opened programs.
- CPU cache
	- Also volatile memory
	- Storage is extremely minimal (~Kilobytes) but the read/write speed is extremely fast
	- Also contains instructions and data needed for currently opened programs, but the data stored in cache is used much more frequently 
##### The anatomy of memory
Computer memory is made up of individual memory cells. Each cell has two relevant values, the address and the data. The unit of measurement of digital data is Bytes and Bits.
One Byte contains 8 bits. One bit is one binary digit
#### The central processing unit (CPU)
There are three main parts in a CPU:
- Control Unit: Fetches instructions from main memory and puts them into the register(CPU cache)
- ALU (arithmetic logic unit): Executes all arithmetic and logical operations
- Register: Also known as the CPU cache (covered in the previous section)
#### Computer software
There are two types of software
- Operating system (OS): Provides a user-interface for the user to interact with the computer
- Applications: Specific software used for specific tasks
A software is a combination of relevant data files and programs. A program is a series of instructions.
#### Hierarchy of Programming languages
- Low level - Machine language 
	- Binary code
	- Only language that a computer can understand.
	- All code has to be converted to machine language using a compiler
	- Extremely fast as nothing has to be compiled
	- Machine code is processor architecture dependent
- Mid level - Assembly language 
	-  Mnemonic code that is understandable by humans and can be easily converted to Machine language
	- Assembly language is processor architecture dependent
	- Also fast is it just a representation of machine code
- High level - C, Java, Python, JavaScript, Rust 
	- Combination of arithmetic expressions and English characters. Very easy for humans to read
	- High level languages are processor architecture independent
	- Slower than lower level languages as the code has to be compiled first


# Introduction to C

#### What is C?
C is a general purpose programming language developed in 1972. Almost all modern day languages are inspired by C or built WITH C (the compiler used for python was built in C).
#### Advantages of C
- **High performance and efficiency**
- **Small footprint**
- **Access to Low-Level System Resources**
#### Disadvantages of C
- **High complexity**
- **Manual memory management**
- **Slower development time**
#### How human written code is read by a computer
Computers only understand binary instructions, so humans write code in a **readable** language like **C** which is converted to machine code (binary code) by a **compiler**
# General syntax 
#### Example code snippet
Take a look at this piece of code, it outputs the sentence "Hello World".
```C
#include <stdio.h>

int main(){
	printf("Hello World");
	return 0;
}
// OUTPUT : Hello World
```
Line by line explanation :
1. `#include <stdio.h>` : This tells the compiler to **include** the *stdio.h* file. This file contains most general functions needed to perform actions in C. Almost all C programs start with this line.
2. `BLANK LINE` : The second line is blank, this line is ignored by the compiler . People include blank lines to make code more readable so this is optional.
3. `int main(){` : Another thing that always appear in a C program is `main()`. This is called a **function**. Any code inside its curly brackets `{}` will be executed.
4. `printf("Hello World");` : The **printf** function is used to output values to the screen. Anything inside the brackets is shown on the output terminal. The semicolon shows that the command ends there. All lines in C must end with a semicolon.
5. `return 0` : This line is at the end of the function. This is used to check  if the code had any issues or not. If the code did not have any problems then it will output 0.
6. `}` : The closing bracket shows that the function has ended.
7. `// Terminal : Hello World` : This is called a **comment** , comments are ignored by the computer as they are only there to make the code easier to understand for someone else other than the programmer. All comments start with a `//` or a `/**/` if you want a multi line comment. Here the comment is just used to show what the output would have been if it were run in a compiler.
Each line inside a function is called a **statement**, all statements need to end with a semicolon. The computer executes the statements line by line, so the statement at the top is executed first.
#### Escape sequences
| **Escape Sequence** | **Purpose/ Description**                                                                 | **HEX Value in ASCII** | **Syntax**                      |
| ------------------- | ---------------------------------------------------------------------------------------- | ---------------------- | ------------------------------- |
| \a                  | _Alert or bell:_ Produces an audible alert or bell sound.                                | 0x07                   | printf("Hello \a World");       |
| \b                  | _Backspace:_ Moves the cursor back by one position.                                      | 0x08                   | printf("Hello\bWorld");         |
| \f                  | _Form feed:_ Advances the printer to the next logical page.                              | 0x0C                   | printf("Hello\fWorld");         |
| \n                  | _Newline:_ Moves the cursor to the beginning of the next line.                           | 0x0A                   | printf("Hello\nWorld");         |
| \r                  | _Carriage return:_ Moves the cursor to the beginning of the current line.                | 0x0D                   | printf("Hello\rWorld");         |
| \t                  | _Horizontal tab:_ Moves the cursor to the next horizontal tab stop.                      | 0x09                   | printf("Hello\tWorld");         |
| \v                  | _Vertical tab:_ Moves the cursor to the next vertical tab stop.                          | 0x0B                   | printf("Hello\vWorld");         |
| \\                  | _Backslash:_ Inserts a backslash character.                                              | 0x5C                   | printf("Hello\World");          |
| \’                  | _Single quote:_ Inserts a single quote character.                                        | 0x27                   | printf("Hello'World");          |
| \”                  | _Double quote:_ Inserts a double quote character.                                        | 0x22                   | printf("Hello"World");          |
| \?                  | _Question mark:_ Inserts a question mark character.                                      | 0x3F                   | printf("Hello?World");          |
| \0                  | _Null character:_ Inserts a null character.                                              | 0x00                   | char str[] = "Hello\0World";    |
| \nnn                | _Octal value:_ Inserts the character represented by the octal value nnn.                 | 0x00 to 0xFF           | printf("Hello \072 World");     |
| \xhh                | _Hexadecimal value:_ Inserts the character represented by the hexadecimal value hh.      | 0x00 to 0xFF           | printf("Hello\x41World");       |
| \uhhhh              | _Universal character name:_ Inserts the character represented by the Unicode value hhhh. | None                   | printf("Hello\u03A9World");<br> |

# Preprocessor keywords
#### Use of #include
`#include` is used to import libraries with pre-programmed functions that are essential for c , a common library is `<stdio.h>` which contains functions like `printf()` and `scanf()`  
#### Use of #define
`#define` is used to define constant values outside the main function. This is done to decrease compiler time by defining values outside of the code instead of declaring it inside.
For example
# Data types and variables
#### Types of Data
The main 3 types of variables used in C are:
- `int` - stores integers (whole numbers) // 4 bytes // -2<sup>32</sup> ~ 2<sup>32</sup> 
- `float` - stores floating point numbers// 4 bytes // 1.2E-38 ~ 3.4E+38
- `double` - stores floating point numbers with higher precision // 8 bytes // 2.3E-308 ~ 1.7E+308
- `char` - stores a single character // 1 byte // -128 ~ 127 OR 0 ~ 255
- `bool` - `true` or `false` values only (must use `#include <stdbool.h>` in the top of the code to use booleans) // 1 byte
- `char string[] = "Hello World"` : Arrays store a collection of variables/constants. Here an array is used to store a collection of `char` type variables
The 7th data type is a constant which is denoted with the `const` variable. Once you state a constant variable you cannot change it
#### Declaration and Initialization 
Before we can use a variable we must do two things, **declaration** and **initialization**.
You HAVE to declare ALL variables before any statements in the code.
1. Declaration : First we need to ***declare*** to the compiler the **name** of the variable and the **type** of the variable. The variable currently has a value of **undefined** as we haven't stored a value for it yet. 
2. Initialization : After declaration we need to initialize the value of the variable. This stores a user-defined value for the variable.
```c
// Declaration
int myNumber; // Declares a integer variable with the name myNumber
float myFloat; // Declares a floating variable with the name myFloat
char myChar; // Declares a character variable with the name myChar
char myWord[]; // Declares a string variable with the name myWord
// Initialization
myNumber = 7; // Assigns a integer value to the variable
myFloat = 9.11; // Assigns a floating value to the variable
myChar = 'c'; // Assigns a single character to the variable
myWord = "Hello World"; // Assigns a word to the array
```
The Declaration and initialization step can be merged into one step
```c
int myNumber = 7; // Declares and assigns a value to the variable called myNumber
```
You can also declare multiple variables of the same type in the same line
```c
int x = 1, y = 2, z = 3;
```
You can also change the value of a variable as many times as you want, or assign the value of one variable to another variable
```c
int x = 1; // Declares and assigns a value
int y = 2; // Declares and assigns a value

x = 3; // Changes value of x from 1 to 3
x = y; // Changes value of x from 3 to value of y (2)
printf("%d", x);
//OUTPUT: 2
```
The `%d` is called a format specifier and it is used to print the values of variables.
#### Format specifiers
This is how to print variables
```c
int myNum = 7
float myFloat = 7.23
char myChar = 'n'
printf("%d %f %c", myNum, myFloat, myChar);
// OUTPUT : 7 7.23 n
```
Here the `%d` is a **format specifier** , this specifies that the variable to output is a integer.
Each variable type has a unique format specifier.
- `%d` - int, bool
- `%u` - unsigned int
- `%o` - unsigned octal
- `%x / %X` - unsigned hexadecimal
- `%f` - float
- `%e` - floating point with E notation
- `%c` - char
- `%s` - string
the order of appearance of the format specifier should match the order of appearance of the variable name inside the `printf()` function.


#### Real life example
The following snippet of code is an example of the cases where declaring, initializing and then printing the variable with format specifiers is useful.
```c
//Student data
int studentID = 2411371042;
int studentAge = 18;
char studentDept[] = "CSE";
char studentName[] = "Fahim Muntasir";
//Print the data
printf("Name: %s\nAge: %d\nID: %d\nDepartment: %s\n", studentName, studentAge, studentID, studentDept);
/*
OUTPUT: Name: Fahim Muntasir
		Age: 18
		ID: 2411371042
		Department: CSE
*/
// Each line is on the next line because of the usage of the \n escape sequence
```

# Operators
#### Arithmetic Operators
| Operator | Type | Function | Example |
| ---- | ---- | ---- | ---- |
| `+` | Addition | Add two values | `x + y` |
| `-` | Subtraction | Subtract two values | `x - y` |
| `*` | Multiplication | Multiply two values | `x * y` |
| `/` | Division | Divide two values | `x / y` |
| `%` | Modulus | Returns the division remainder | `x % y` |
| `++`  | Increment | Increase value by 1 | `++x` |
| `--` | Decrement | Decrease value by 1 | `--x` |
#### Assignment Operators
| Operator | Syntax | Explained |
| ---- | ---- | ---- |
| `=` | `x = 5` | `x = 5` |
| `+=` | `x += 5` | `x = x + 5` |
| `-=` | `x -= 5` | `x = x - 5` |
| `*=` | `x *= 5` | `x = x * 5` |
| `/=` | `x /= 5` | `x = x / 5` |
| `%=` | `x %= 5` | `x = x % 5` |
#### Comparison Operators
| Operator | Type |
| ---- | ---- |
| `==` | Equal to |
| `!=` | Not equal to |
| `>` | Greater than |
| `<` | Lesser than |
| `>=` | Greater than or equal to |
| `<=` | Lesser than or equal to  |
Comparison operators output `1` if true and `0` if false
#### Bitwise Operators
| Operator | Type        |
| -------- | ----------- |
| `&`      | bitwise AND |
| \|       | bitwise OR  |
| `~`      | bitwise NOT |
| `^`      | bitwise XOR |
| `<<`     | shift left  |
| `>>`     | shift right |
#### Logical Operators
| Operator | Type |
| -------- | ---- |
| `&&`     | AND  |
| \|\|     | OR   |
| `!`      | NOT  |
#### Operator precedence
Example
```c
#include <stdio.h> 
int main() { 
	int result = 5 + 3 * 2 - 4 / 2; 
	printf("Result: %d\n", result);
	return 0; 
}
```
1. `3 * 2` is evaluated first, resulting in `6`.
2. `4 / 2` is evaluated next, resulting in `2`.
3. Then, the result of the multiplication (`6`) is added to `5`, resulting in `11`.
4. Finally, `11` is subtracted by `2`, resulting in a final `9`.

Order of operators
1. Function calls (printf(), scanf(), etc.)
2. !, ++, --
3. * , /, %
4. +, -
5. == , >= , <= , >, <, !=
6. &&
7. | |
8. =
# *if...else* statements
#### If statements
If statements are useful for decision making. 
Format for an if statement:
```PseudoCode
if (condition){
	code that will execute only if the condition is true
}
```
Example 
```c
int age = 26;
if (age > 18){
	printf("You are a %d year old adult", age);
}
// OUTPUT: You are a 26 year old adult
```
#### Else statements
Else statements are used when the condition in the if statement is not true
Formant for an else statement:
```PseudoCode
if(condition){
	code that will execute if condition is true
} else {
	code that will execute if condition is false
}
```
Example
```c
int age = 16;
if (age > 18){
	printf("You are an adult");
} else {
	printf("You are not an adult);
}
// OUTPUT: You are not an adult
```
#### Else if statements
Else if statements are used to check for another condition if the previous condition was false
Format for else if statements:
```PseudoCode
if(condtion 1){
	code that will execute if condtion 1 is true
} else if(condtion 2){
	code that will execute if condtion 2 is true
} else {
	code that will execute when all conditions are false
}
```
Example
```C
int age = -2;
if(age > 18){
	printf("You are an adult");
} else if(age < 0){
	printf("Invalid age, age cannot be negative");
} else {
	printf("You are not an adult);
}
// OUTPUT: Invalid age, age cannot be negative
```

#### Shorthand if statement
This method is used for small and simple statements that can be written in a single line
Format for shorthand if statements
```PseudoCode
(condtion) ? code that will execute if true : code that will execute if false;
```
Example
```c
int age = 21;
(age > 18) ? printf("You are an adult") : printf("You are not an adult");
```

# Switch case statements
Switch case statements are used instead of using many lines of if statements. Using it is optional, If statements and switch case statements have the same function
Format
```PseudoCode
switch(variable/expression){
	case a:
		//code
		break;
	case b:
		//code
		break;
	default:
		//code
}
```
The default block can be though of as an else statement 
# Loops
#### While loop
The while loop repeats a piece of code as long as a condition is true
Format:
```PseudoCode
while(condition){
	//code to be executed
}
```
Example
```C
int i = 0; // this variable is declared so that it can be used to count the loops
while(i < 5){
	printf("%d\n", i); // outputs the current value of i
	i++; // every loop i is increase by one so that the code is not looped forver
}
/*
OUTPUT : 
0
1
2
3
4
*/
```
#### Do/While loop
Do while loop is almost the exact same thing as the while loop, the only difference is that the loop first executes code then checks the condition
Format:
```PseudoCode
do {
	// code to be executed
} while (condition);
```
#### For loop
For loops repeat code a fixed amount of times unlike the while loop which can loop forever;
Format:
```PseudoCode
for (expression 1; expression 2; expression 3){
	//code to be executed
}
```
Expression 1 : code that is executed one time before the loop
Expression 2 : condition for running the loop
Expression 3 : code that is executed after every loop

Example:
```C
for(int i = 0; i < 5; i++){
	printf("%d\n", i);
}
```
#### Break/Continue
The `break` statement is used to break out of a loop;
Example:
```C
for(int i = 0; i < 10; i++){
	if(i == 4){
		break;
	}
	printf("%d\n", i);
}
/*
OUTPUT:
0
1
2
3
*/
// loop stops when i = 4
```
The `continue` statement is used to skip one iteration of the loop;
Example:
```C
for(int i = 0; i < 10; i++){
	if(i == 4){
		continue;
	}
	printf("%d\n", i);
}
/*
OUTPUT: 
0
1
2
3
5
6
7
8
9
*/
// loop skips the step of printing 4 and goes onto the next iteration
```

# Arrays
Arrays are used to store a collection of variables of the same type
The declaration and initialization of arrays is identical to variables ;
```C
int myArray[] = {25, 62, 91, 11};
```
Each element of an array has an index, the first element of an array has an index of 0.
```c
int myArray[] = {25, 62, 91, 11};
printf("%d", myArray[2])
// OUTPUT : 91
```
You can use loops to list all elements of an array ;
```C
int myArray[] = {25, 62, 91, 11};
for(int i = 0; i < 4; i++){
	printf("%d ", myArray[i]);
}
// OUTPUT: 25 62 91 11 
```
To know the size of an array we can use the `sizeof()` method. This outputs the number of bytes of memory that is being used by the array.
```C
int myNumbers[] = {10,25,50,75,100};
int size = sizeof(myNumbers);

printf("%lu", size);
// OUTPUT : 20 (20 bytes)
```
When we want to know the number of elements in an array we can divide the (total memory taken by the array ) by (the memory taken by one element).
```C
int myNumbers[] = {10,25,50,75,100};
int length = sizeof(myNumbers)/sizeof(myNumbers[0]);

printf("%d", length);
//OUTPUT : 5
```


# Strings
To use string functions you need to include the strings header file by using `#include <string.h>`
Some common functions:
- `strlen()` = returns length of string
- `strcat(str1, str2)` = adds str2 to the end of str1 and the result is stored in str1
- `strcpy(str2, str1)` = copies value of str1 to str2
- `strcmp(str1, str2)` = compares two st1 and str2 ; returns 0 if same

# User input
`printf()` is used to show output. Similarly, `scanf()` is used to take user input.
Format:
```C
int myNum;
scanf("%d", &myNum);
// use a format specifier to define type of input and then declare the variable that will be assigned to that value
```
# Memory addresses
Preceding any variable with the `&` sign gives the memory address of the variable. Format specifier for addresses is `%p` 


# Functions
#### What is a function?
A function is a piece of code that is used to complete a specific task. Functions are useful because they only need to be written once and can be reused without writing the same code over and over again.
#### Types of functions
Pre-defined
- Built-in functions provided by C that are used by programmers without having to write any code for them.  ex. printf( ), scanf( ), etc.
User-defined
- Functions written by the programmer

####