`Fahim Muntasir`
# Programming Language I
---
## Contents
- [[#Week 1 Part 1]]
- [[#Week 1 Part 2]]
---
## Week 1 Part 1
#### Types of number systems
##### Decimal (base 10) : 
- 0,1,2,3,4,5,6,7,8,9
- used by ***HUMANS***
##### Binary (base 2) : 
- 0,1
- used by ***COMPUTERS***
##### Octal (base 8) :
- 0,1,2,3,4,5,6,7
- used to ***REPRESENT*** large binary digits
##### Hexadecimal (base 16) :
- 0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F
- used to ***REPRESENT*** large binary digits
#### Bits and Bytes
A **single** binary digit is called a bit
A **collection** of 8 bits is called a byte
One byte is the standard **unit** of measurement of data

#### Conversion between types of number systems
##### Binary to decimal 
(101001)<sub>2</sub> ---> ( ? )<sub>10</sub>
> keep adding the product of 2<sup>n</sup> and the nth number (n starts from 0 on the far right side)

1 x 2<sup>0</sup> =   1
0 x 2<sup>1</sup> =  0
0 x 2<sup>2</sup> =  0
1 x 2<sup>3</sup> =   8
0 x 2<sup>4</sup> =  0
<u>1 x 2<sup>5</sup> =   32</u>
        41 

(101001)<sub>2</sub> ---> (41)<sub>10</sub>
##### Octal to decimal
(724)<sub>8</sub> ---> ( ? )<sub>10</sub>
> keep adding the product of 8<sup>n</sup> and the nth number (n starts from 0 on the far right side)

4 x 8<sup>0</sup> =    4
2 x 8<sup>1</sup> =   16
<u>7 x 8<sup>2</sup> =  448</u>
        468

(724)<sub>8</sub> ---> (468)<sub>10</sub>

##### Hexadecimal to decimal 
(ABC)<sub>16</sub> ---> ( ? )<sub>10</sub>
> keep adding the product of 16<sup>n</sup> and the nth number (n starts from 0 on the far right side)

C x 16<sup>0</sup> = 12 x 1 =           12
B x 16<sup>1</sup> = 11 x 16 =        176   
<u>A x 16<sup>2</sup> = 10 x 256 = 2560</u>
			    2748

(ABC)<sub>16</sub> ---> (2748)<sub>10</sub>

##### Decimal to binary
(41)<sub>10</sub> ---> ( ? )<sub>2</sub>
> Keep dividing the number by 2 until the number becomes 0, after that join the remainders from top to bottom

41 / 2 => 20      (1) 
20 / 2 => 10      (0)
10 / 2 => 5        (0)
5 / 2 => 2          (1)
2 / 2 => 1          (0)
1 / 2 => 0          (1)
join numbers from top to bottom,
(41)<sub>10</sub> ---> (101001)<sub>2</sub>

##### Decimal to octal
(1234)<sub>10</sub> ---> ( ? )<sub>8</sub>
> Keep dividing the number by 8 until the number becomes 0, after that join the remainders from top to bottom 

1234 / 8 => 154  (2) 
154 / 8 => 19      (2)
19 / 8 => 2          (3)
2 / 8 => 0            (2)
join numbers from top to bottom,
(1234)<sub>10</sub> ---> (2322)<sub>8</sub>
##### Decimal to hexadecimal 
(1234)<sub>10</sub> ---> ( ? )<sub>16</sub>
> Keep dividing the number by 16 until the number becomes 0, after that join the remainders from top to bottom 

1234 / 16 => 77         (2) 
77/ 16 => 4      (13 => D)
4 / 16 => 0                 (4)
join numbers from top to bottom,
(1234)<sub>10</sub> ---> (4D2)<sub>16</sub>

##### Octal to binary
(705)<sub>8</sub> ---> ( ? )<sub>2</sub>
> Convert each digit to a 3 bit binary number and then join them up

5 => 101
0 => 000
7 => 111
joining the digits,
(705)<sub>8</sub> ---> (111000101)<sub>2</sub>
##### Binary to octal 
(1011010111)<sub>2</sub> ---> ( ? )<sub>8</sub>
> Split the number into 3 bits starting from the right and then convert, add 0 to the front if the number cannot be evenly split into 3

111 => 7
010 => 2
011 => 3
001 => 1
joining numbers,
(1011010111)<sub>2</sub> ---> (1327)<sub>8</sub>
##### Hexadecimal to binary
(10AF)<sub>16</sub> ---> ( ? )<sub>2</sub>
> convert each symbol to a 4bit binary number, if the symbol is an alphabet then convert the value of that alphabet to binary

F = 15 => 1111
A = 10 => 1010
0 => 0000
1 => 0001
joining the numbers,
(10AF)<sub>16</sub> ---> (0001000010101111)<sub>2</sub>

##### Binary to hexadecimal
(1010111011)<sub>2</sub> ---> ( ? )<sub>16</sub>
> split into 4 bits and then convert the values

1011 => B
1011 => B
0010 => 2
joining the numbers,
(1010111011)<sub>2</sub> ---> (2BB)<sub>16</sub>
##### Octal to hexadecimal
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

##### Hexadecimal to octal
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
## Week 1 Part 2
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
#### The anatomy of memory
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

####