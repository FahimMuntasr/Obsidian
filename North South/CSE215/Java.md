- Computer programs, known as software, are instructions to the computer.
- Machine language is written in binary 
- Assembly Language is written in assembly code and converted to Machine Language
- Interpreters / Compilers convert high level code to machine language
- Interpreters convert one statement and executes it right away, then repeats the process for the next statement
- Compilers convert entire source code into machine-code and then executes it
- OS forms a bridge between software, hardware and the end user
- Java is Compiled first to Java Virtual Machine code and then interpreted 
- byte : 8 bit signed : $-2^7$ to $2^7-1$ 
- short : 16 bit signed : $-2^{15}$ to $2^{15}-1$
- int : 32 bit signed : $-2^{31}$ to $2^{31}-1$
- long : 64 bit signed : $-2^{63}$ to $2^{63}-1$ 
- float : 32 bit : $−3.4×10^{38}$ to $+3.4×10^{38}$
- double : $-1.7 \times 10^{308}$ to $+1.7\times 10^{308}$
- import javax.swing.*
- String input = JOptionPane.showInputDialog( "Enter an input");
- JOptionPane.showMessageDialog(null,"Welcome to Java!","Display Message",JOptionPane.INFORMATION_MESSAGE);  
- int option=JOptionPane.showConfirmDialog(null,"Continue");  

# String Methods
| Method                                                                                     | Description                                                                                                          | Return Type  |
| ------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------- | ------------ |
| [charAt()](https://www.w3schools.com/java/ref_string_charat.asp)                           | Returns the character at the specified index (position)                                                              | char         |
| [compareTo()](https://www.w3schools.com/java/ref_string_compareto.asp)                     | Compares two strings lexicographically                                                                               | int          |
| [compareToIgnoreCase()](https://www.w3schools.com/java/ref_string_comparetoignorecase.asp) | Compares two strings lexicographically, ignoring case differences                                                    | int          |
| [concat()](https://www.w3schools.com/java/ref_string_concat.asp)                           | Appends a string to the end of another string                                                                        | String       |
| [contains()](https://www.w3schools.com/java/ref_string_contains.asp)                       | Checks whether a string contains a sequence of characters                                                            | boolean      |
| [contentEquals()](https://www.w3schools.com/java/ref_string_contentequals.asp)             | Checks whether a string contains the exact same sequence of characters of the specified CharSequence or StringBuffer | boolean      |
| [copyValueOf()](https://www.w3schools.com/java/ref_string_copyvalueof.asp)                 | Returns a String that represents the characters of the character array                                               | String       |
| [equalsIgnoreCase()](https://www.w3schools.com/java/ref_string_equalsignorecase.asp)       | Compares two strings, ignoring case considerations                                                                   | boolean      |
| [getChars()](https://www.w3schools.com/java/ref_string_getchars.asp)                       | Copies characters from a string to an array of chars                                                                 | void         |
| [indexOf()](https://www.w3schools.com/java/ref_string_indexof.asp)                         | Returns the position of the first found occurrence of specified characters in a string                               | int          |
| [isEmpty()](https://www.w3schools.com/java/ref_string_isempty.asp)                         | Checks whether a string is empty or not                                                                              | boolean      |
| [lastIndexOf()](https://www.w3schools.com/java/ref_string_lastindexof.asp)                 | Returns the position of the last found occurrence of specified characters in a string                                | int          |
| [length()](https://www.w3schools.com/java/ref_string_length.asp)                           | Returns the length of a specified string                                                                             | int          |
| [replaceAll()](https://www.w3schools.com/java/ref_string_replaceall.asp)                   | Replaces each substring of this string that matches the given regular expression with the given replacement          | String       |
| [replace()](https://www.w3schools.com/java/ref_string_replace.asp)                         | Searches a string for a specified value, and returns a new string where the specified values are replaced            | String       |
| [replaceFirst()](https://www.w3schools.com/java/ref_string_replacefirst.asp)               | Replaces the first occurrence of a substring that matches the given regular expression with the given replacement    | String       |
| [split()](https://www.w3schools.com/java/ref_string_split.asp)                             | Splits a string into an array of substrings                                                                          | String[]     |
| [startsWith()](https://www.w3schools.com/java/ref_string_startswith.asp)                   | Checks whether a string starts with specified characters                                                             | boolean      |
| [subSequence()](https://www.w3schools.com/java/ref_string_subsequence.asp)                 | Returns a new character sequence that is a subsequence of this sequence                                              | CharSequence |
| [substring()](https://www.w3schools.com/java/ref_string_substring.asp)                     | Returns a new string which is the substring of a specified string                                                    | String       |
| [toCharArray()](https://www.w3schools.com/java/ref_string_tochararray.asp)                 | Converts this string to a new character array                                                                        | char[]       |
| [toLowerCase()](https://www.w3schools.com/java/ref_string_tolowercase.asp)                 | Converts a string to lower case letters                                                                              | String       |
| [toString()](https://www.w3schools.com/java/ref_string_tostring.asp)                       | Returns the value of a String object                                                                                 | String       |
| [toUpperCase()](https://www.w3schools.com/java/ref_string_touppercase.asp)                 | Converts a string to upper case letters                                                                              | String       |
| [trim()](https://www.w3schools.com/java/ref_string_trim.asp)                               | Removes whitespace from both ends of a string                                                                        | String       |
# Math Methods
| Method                                                         | Description                                                | Return Type              |
| -------------------------------------------------------------- | ---------------------------------------------------------- | ------------------------ |
| [abs(x)](https://www.w3schools.com/java/ref_math_abs.asp)      | Returns the absolute value of x                            | double\|float\|int\|long |
| [ceil(x)](https://www.w3schools.com/java/ref_math_ceil.asp)    | Returns the value of x rounded up to its nearest integer   | double                   |
| [exp(x)](https://www.w3schools.com/java/ref_math_exp.asp)      | Returns the value of Ex                                    | double                   |
| [floor(x)](https://www.w3schools.com/java/ref_math_floor.asp)  | Returns the value of x rounded down to its nearest integer | double                   |
| [log(x)](https://www.w3schools.com/java/ref_math_log.asp)      | Returns the natural logarithm (base E) of x                | double                   |
| [log10(x)](https://www.w3schools.com/java/ref_math_log10.asp)  | Returns the base 10 logarithm of x                         | double                   |
| [max(x, y)](https://www.w3schools.com/java/ref_math_max.asp)   | Returns the number with the highest value                  | double\|float\|int\|long |
| [min(x, y)](https://www.w3schools.com/java/ref_math_min.asp)   | Returns the number with the lowest value                   | double\|float\|int\|long |
| [pow(x, y)](https://www.w3schools.com/java/ref_math_pow.asp)   | Returns the value of x to the power of y                   | double                   |
| [random()](https://www.w3schools.com/java/ref_math_random.asp) | Returns a random number between 0 and 1                    | double                   |
| [round(x)](https://www.w3schools.com/java/ref_math_round.asp)  | Returns the value of x rounded to its nearest integer      | long\|int                |
| [sqrt(x)](https://www.w3schools.com/java/ref_math_sqrt.asp)    | Returns the square root of x                               | double                   |
| [cbrt(x)](https://www.w3schools.com/java/ref_math_cbrt.asp)    | Returns the cube root of x                                 | double                   |
| [sin(x)](https://www.w3schools.com/java/ref_math_sin.asp)      | Returns the sine of x (x is in radians)                    | double                   |
| [cos(x)](https://www.w3schools.com/java/ref_math_cos.asp)      | Returns the cosine of x (x is in radians)                  | double                   |
| [tan(x)](https://www.w3schools.com/java/ref_math_tan.asp)      | Returns the tangent of an angle                            | double                   |
| [tanh(x)](https://www.w3schools.com/java/ref_math_tanh.asp)    | Returns the hyperbolic tangent of a double value           | double                   |

# Array Methods
| Method                                                             | Description                                                                               |
| ------------------------------------------------------------------ | ----------------------------------------------------------------------------------------- |
| [compare()](https://www.w3schools.com/java/ref_arrays_compare.asp) | Compares two arrays                                                                       |
| copyOf()                                                           | Creates a copy of an array with a new length                                              |
| deepEquals()                                                       | Compares two multidimensional arrays to check whether they are deeply equal to each other |
| [equals()](https://www.w3schools.com/java/ref_arrays_equals.asp)   | Checks if two arays are equal                                                             |
| [fill()](https://www.w3schools.com/java/ref_arrays_fill.asp)       | Fills an array with a specified value                                                     |
| mismatch()                                                         | Returns the index position of the first mismatch/conflict between two arrays              |
| [sort()](https://www.w3schools.com/java/ref_arrays_sort.asp)       | Sorts an array in ascending order                                                         |