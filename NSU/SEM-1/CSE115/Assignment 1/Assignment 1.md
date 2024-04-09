# 1.Given the value of coefficients a, b and c, write a C program to find the value of x.The equation is given by: ax^2+bx+c=0
---
 ```c
#include <stdio.h>
#include <math.h>

main(){
    float a, b, c, det, x1, x2;
    
    printf("Enter a b c:");
    scanf("%f%f%f", &a, &b, &c);
    
    det = (b*b)-(4*a*c);
    
    if(a == 0){
        printf("Invalid input (a cannot be zero)");
    }else if(det < 0){
        printf("NO ROOTS");
    } else if (det == 0){
        printf("x=%.2f",(-((b)/(2*a))));
    } else {
        printf("x1=%.2f\nx2=%.2f", ((-b+sqrt(det))/2*a), ((-b-sqrt(det))/2*a));
    }
}
```
# 2. If d, w, and l are given, find out the area of the green portion.
---
![[Pasted image 20240317180727.png]]
```c
#include <stdio.h>
#define PI 3.142

main(){
    float w, l, d;
    
    printf("Enter d w l:");
    scanf("%f%f%f", &d, &w, &l);
    
    printf("Area of green portion = %f", ((w * l)-(PI * (d/2) * (d/2))));
}
```
# 3.Write a program to print Pascal’s triangle as follows:
---
![[Pasted image 20240317183045.png]]
```c
#include <stdio.h>
int factorial(int x){
    int result = 1, copy;
    copy = x;
    while(copy>0){
        result *= copy;
        copy--;
    }
    return result;
}
int nCr(int n, int r){
    int result;
    
    result = (factorial(n))/((factorial(r))*(factorial(n-r)));
    
    return result;
}
main(){
    int rows, i, j, k;
    
    printf("Enter number of rows:");
    scanf("%d", &rows);
    
    for(i=0;i<rows;i++){
        for(k=(rows-i)-1;k>0;k--){
            printf(" ");
        }
        for(j=0;j<=i;j++){
            printf("%d ", nCr(i,j));
        }
        printf("\n");
    }
}
```
# 4.Calculate the sum of the following series, where x and n are given by the user. n is the number of terms in the series.
---
![[Pasted image 20240327235007.png]]
```C
#include <stdio.h>
#include <math.h>

main(){
    int i, x, n;
    float term, result;
    printf("Enter x and n");
    scanf("%d%d", &x, &n);
    
    for(result = 0.0;n>0;n--){
        if(n % 2 == 0){
            term = -((pow(x, n))/(n));
        } else {
            term = ((pow(x, n))/(n));
        }
        result += term;
    }
    printf("Result: %.3f", result);
}
```
# 5. What is a function in C? Solve a self-chosen problem with function and without function and compare them. Discuss the benefits of using functions.
---
A function is a piece of code that performs a specific task. One function can be called in another function. This makes writing code easier as rewriting code is not needed.

Problem: Given two user-inputs n and r, find nPr using the formula :$$^nP_r = \frac{n!}{(n-r)!}$$
WITHOUT FUNCTIONS:
```c
#include <stdio.h>

main(){
    int n, r, i;
    int nFact = 1, nrFact = 1;
    printf("Enter n and r:");
    scanf("%d%d", &n, &r);
    for(i=n;i>0;i--)
        nFact *= i;
    for(i=(n-r);i>0;i--)
        nrFact *= i;
    printf("%dP%d = %d", n, r, (nFact/nrFact));
}

```
WITH FUNCTIONS:
```c
#include <stdio.h>
int factorial(int x){
    int i, result = 1;
    for(i=x;i>0;i--)
        result *= i;
    return result;
}
main(){
    int n, r;
    printf("Enter n and r:");
    scanf("%d%d", &n, &r);
    printf("%dP%d = %d", n, r, (factorial(n)/factorial(n-r)));
}
```
The benefit of using functions is that the same code doesnt have to be written everytime, instead the code is written only one time and after that the function is just called in one line. This makes the code easier to maintain.
# 6. Point out the error(s), if any, in the following programs and provide solutions as well:
---
### a.
```c
# include <stdio.h>

int addmult(int, int)

int main(){
    int i = 3, j = 4, k, l;
    k = addmult(i, j);
    l = addmult(i, j);
    printf("%d %d\n", k, l);
    return 0;
}
int addmult(int i, int j){
    int kk, ll;
    kk = ii + jj;
    ll = ii * jj;
    return (kk, ll);
}
```
Errors: 
- The program only outputs the product of two numbers.
- Returning multiple variables.
- incorrect syntax (ii and jj instead of i and j).
Solution:
```c
#include <stdio.h>
int add(int, int)
int mult(int, int)
int main(){
	int i = 3, j = 4, k, l;
	k = add(i, j);
	l = mult(i ,j);
	printf("%d %d\n", k, l);
	return 0;
}
int add(int i, int j){
	int  kk;
	kk = i + j;
	return kk;
}
int mult(int i, int j){
	int ll;
	ll = i * j;
	return ll;
}
```
## b.
```C
# include <stdio.h>

int main( ){
	int a = 15.5;
	char ch = 'C';
	print(a, ch);
	return 0;
}
printf(a, ch){
	print("%f %c\n", a, ch);
}
```
Errors: 
- Function 'print' is not defined.
- variable declaration in defined function does not have variable types.
- variable a is int type but %f is used to print it.
- Function defined after main
Solution:
```C
# include <stdio.h>
void print(int, char)
int main(){
	int a = 15.5;
	char ch = 'C';
	print(a, ch);
	return 0;
}
void print(int a, char ch){
	printf("%d %c\n", a, ch);
	return void
}
```
## c.
```C
#include <stdio.h>

void message( );
int main( ){
	message(message( ));
	return 0;
} 
void message( ){
	printf ("It's a small world after all...\n");
}
```
Errors: 
- function is called as another functions argument but the return type is void.
Solution:
```C
#include <stdio.h>

void message( );
int main( ){
	message();
	return 0;
}
void message( ){
	printf ("It's a small world after all...\n");
}
```
## d. 
**![](https://lh7-us.googleusercontent.com/GNpDXMXFSL4emBhwiSuwtr72vYOWJRtiMF51af1DyiiTjWf_GLgPZaWZti8nkByPYdYicfMFoPFRKlyNgGY5rrPZCa0-E-04Y4I7r9wdnF-MS9o7tRgFLQoSVKXCv_Zht-RKA2ikmMq6fPT2m8AdRQ)
Errors: 
- No `break` statements.
Solution
``` C
#include <stdio.h>

int main(){
    int i = 0;
    switch (i){
        case 0:
            printf("i is zero\n");
            break;
        case 1:
            printf("i is one\n");
            break;
        default:
            printf("It is something else\n");
            break;
    }
    return 0;
}
```
## e.
![](https://lh7-us.googleusercontent.com/nJskMne1ctfoxgRLlDjZ3mW5QoS0DW3WlTr2kZSSrCMK2JJoba9fnSAxO7IAc7VCMJqaJ8fkEyX3WB2xiv8sPcndwprgVN8IdaBX921Nmzlp4tT0qA62Mhtm82aAjlj_Op4qFvGoPBIFeYVlSOCKPg)
Errors:
- Syntax error - code inside if statement not inside brackets.
Solution:
```C
#include <stdio.h>

int main(){
    int x = 10;
    if (x>5){
        printf("x is greater than 5\n");
        x *= 2;
    }else
        printf("x is not greater than 5\n");
    printf("New value of x:%d\n", x);
    return 0;
}
```
# 7. Write a C program to find out the Bitwise OR, Bitwise AND & Bitwise XOR value of the given X, Y input. X and Y will be given as decimal values. Your output also should be in Decimal. Constraint, 0≤X,Y<63
---
```C
#include <stdio.h>

int main(){
    int x, y;
    printf("Enter x and y:");
    scanf("%d%d", &x, &y);
    if(x<0||x>=63||y<0||y>=63){
        printf("Input must be between 0 and 63");
        return 1;
    }
    printf("Bitwise Or: %d\nBitwise And: %d\nBitwise XOR: %d", x|y, x&y, x^y);
    return 0;
}
```
# 8.Write a C Program to print the following according to their GPA. Also, print the amount of semester fees they have to pay.
---
```C
#include <stdio.h>

int main(){
    int fee, scholarship, deducted, amount;
    float cgpa;
    printf("Enter your CGPA:");
    scanf("%f", &cgpa);
    printf("Enter semester fee:");
    scanf("%d", &fee);
    if(cgpa == 4.0){
        scholarship = 100;
        amount = 0;
    } else if(cgpa <= 3.75){
        scholarship = 75;
        amount = fee/4;
    } else if(cgpa <= 3.50){
        scholarship = 50;
        amount = fee/2;
    } else if(cgpa <= 3.30){
        scholarship = 25;
        amount = (3*fee)/4;
    } else {
        scholarship = 0;
        amount = fee;
    }
    printf("You got %d %% scholarship on your CGPA.\nYour payable amount is %d BDT", scholarship, amount);
}
```
# 9. Take a year as user input. Write a function checkLeapYear(int year) to determine whether the year is a leap year
---
```C
#include <stdio.h>
int checkLeapYear(int);
int main(){
    int year, leap;
    printf("Enter year:");
    scanf("%d", &year);
    leap = checkLeapYear(year);
    if(leap == 0){
        printf("%d is not a leap year", year);
    } else {
        printf("%d is a leap year", year);
    }
}
int checkLeapYear(int year){
    if(year % 4 == 0){
        if(year % 100 == 0){
            if(year % 400 == 0){
                return 1;
            } else {
                return 0;
            }
        } else {
            return 1;
        }
    } else {
        return 0;
    }
}
```
# 10. What is an array? How do you declare and initialize an array in C? How many types of arrays are there?
---
An array is a collection of values with the same data types. The address of each value is denoted through its location in the array. 
Declaring an array ;
```C
int myArray[arraySize];
```
Initializing an array;
```C
myArray[5] = {1,2,3,4,5};
```
An array can be any type a variable can be.
# 11. Suppose you have given n size array. Each contains the height of a student in your class. Use another array to store their names sequentially. Now write a program that finds the names of the tallest students (assuming there could be more than one tallest student).
---
```C
#include <stdio.h>
#include <string.h>

int main() {
    int i, n, k = 0, tallest = 0;
    printf("Enter number of students: ");
    scanf("%d", &n);
    
    int height[n];
    char name[n][20]; // Assuming maximum name length is 19 characters
    char nameList[n][20]; // Initialized to store names
    
    for (i = 0; i < n; i++) {
        printf("Enter student name: ");
        scanf("%19s", name[i]); // Limiting input length to 19 characters
        printf("Enter student height(cm): ");
        scanf("%d", &height[i]);
    }
    
    for (i = 0; i < n; i++) {
        if (height[i] >= tallest) {
            tallest = height[i];
        }
    }
    
    for (i = 0; i < n; i++) {
        if (height[i] == tallest) {
            strcpy(nameList[k], name[i]); // Copying name to nameList
            k++;
        }
    }
    
    printf("Name(s) of the tallest student(s): ");
    for (i = 0; i < k; i++) {
        printf("%s ", nameList[i]);
    }
    return 0;
}
```
# 12. Write a C program to read the number of minutes talked on the phone and to calculate the total bill according to the given conditions:
---
- For the first 5 minutes Tk. 0.45/min,
- For the next 30 minutes Tk. 0.60/min,
- For the next 1 hour Tk. 0.85/min,
- After that, Tk. 1.00/min.
- An additional VAT of 18% is added to the bill.
```C
#include <stdio.h>

main(){
    int min;
    float bill = 0;
    
    printf("Enter number of minutes talked:");
    scanf("%d", &min);
    
    if(min < 0){
        printf("Duration cannot be negative");
    }else{
        printf("Duration: %d min\n", min);
        if(min <= 5){
            bill = (min * 0.45);
        }else if(min <=35){
            min -= 5;
            bill = 2.25 + (min * 0.60);
        }else if(min <= 95){
            min -= 35;
            bill = 20.25 + (min * 0.85);
        }else if(min > 95){
            min -= 95;
            bill = 71.25 + (min * 1.0);
        }
        printf("Bill(includes 18%% VAT): TK. %.2f", 1.18 * bill);
    }
}
```
# 13. What will be the outputs of the following programs:
---
### A. 
```C
# include <stdio.h>

int main(){
	int num[26], temp;  
	num[0] = 100;
	num[25] = 200;
	temp = num[25];
	num[25] = num[0];
	num[0] = temp;
	printf("%d %d\n", num[0], num[25]);
	return 0;
}
```
OUTPUT
```
200 100
```
### B.
```C
#include <stdio.h>

int main(){
	int array[10], i;
	for(i = 0; i <10; i++){
		array[i] = 'A' + i;
		printf("%d %c\n", array[i], array[i]);
	}
	return 0;
}
```
OUTPUT
```
65 A
66 B
67 C
68 D
69 E
70 F
71 G
72 H
73 I
74 J                                                                           
```
# 14. Point out the errors in the following code segment if any:
---
### A.
```C

#include <stdio.h>

int int mixed[100]; \\ variable type declared twice
  
int main( ){
	int a[10], i;
	for (i = 1; i <= 10; i++){
		scanf("%f", a[i]); \\ %f used for int array, &a[i] should be used to store value
		printf("%f\n", a[i]); \\ %f used for int array
	}
	return 0;
}
```
### B.
```C
#include <stdio.h>

int main(){
	int size;
	scanf ("%d", &size);
	int arr[size];
	\\ i not declared beforehand
	for (i = 1; i <= size; i++)
	{ 
		scanf("%d", &arr[i]);
		printf("%d\n", arr[i]);
	}
	return 0;
}
```
### C.
```C
#include <stdio.h>

int main( ){
	int i, a = 2, b = 3;
	int arr[2 + 3];
	for (i = 0; i < a + b; i++){
		scanf("%d", &arr[i]);
		printf("%d\n", arr[i]);
	}
	return 0;
}
\\ NO ERRORS
```
# 15.  Write a C program to find the summation of n size array excluding second largest element in a given array
---
```C
#include <stdio.h>

int main() {
    int n, i, k = 0, sum = 0, largest;
    printf("Enter array size: ");
    scanf("%d", &n);
    int array[n];
    for (i = 0; i < n; i++) {
        printf("Enter element: ");
        scanf("%d", &array[i]);
    }
    largest = array[0];
    for (i = 1; i < n; i++) {
        if (array[i] > largest) {
            largest = array[i];
            k = i;
        }
    }
    sum += largest;
    array[k] = 0;
    largest = array[0];
    for (i = 1; i < n; i++) {
        if (array[i] > largest) {
            largest = array[i];
            k = i;
        }
    }
    array[k] = 0;
    for (i = 0; i < n; i++) {
        sum += array[i];
    }
    printf("Sum: %d", sum);
    return 0;
}
```
# 16. Write a function sumEven(int arr[], int length) which returns the summation of all the even elements of the array. And write another function sumOdd(int arr[], int length) which returns the summation of all the odds elements of the array. Print the difference between the sum of even and the sum of odd numbers.
---
```C
#include <stdio.h>
int sumEven(int arr[], int length){
    int i, sum = 0;
    for(i = 0;i<length;i++){
        if(arr[i] % 2 == 0){
            sum += arr[i];
        }
    }
    return sum;
}
int sumOdd(int arr[], int length){
    int i, sum = 0;
    for(i = 0;i<length;i++){
        if(arr[i] % 2 != 0){
            sum += arr[i];
        }
    }
    return sum;
}
int main() {
    int i, length;
    printf("Enter array size:");
    scanf("%d", &length);
    int arr[length];
    for(i=0;i<length;i++){
        printf("Enter element:");
        scanf("%d", &arr[i]);
    }
    printf("Difference = %d", abs(sumEven(arr, length)-sumOdd(arr, length)));
    return 0;
}
```
# 17.
---
### A. What are Strings in C? Why is a ‘\\0’ necessary at the end of the string?
Ans) A string is an array of characters. All strings have to end in a \\0 character to show the end of the string, '\\0' is called a NULL character;
### B. What are preprocessor directives? Why it is necessary to include them at the beginning of  any C code file?
Ans) Preprocessor directives are commands for the compiler to execute before compilation. For example, If a programmer wants to use a library in their code they need to use the `#include` directive. Or if they want to define a constant before the compilation they need to use `#define`.
# 18. Write a C program that counts the total number of letters, numbers or special character/symbols in a string
---
```C
#include <stdio.h>

int main() {
    int i, count = 0;
    char str[101];
    
    printf("Enter string (Max 100 characters): ");
    gets(str);
    
    // Count the number of non-null, non-whitespace characters
    for (i = 0; str[i] != '\0'; i++) {
        if (str[i] != ' ') {
            count++;
        }
    }
    
    printf("Number of characters: %d", count);
    
    return 0;
}
```
# 19. What would be the output of the following program:
--- 
```C
#include <stdio.h>

void main(){
	int i=14>>2, j=11<<2;
	printf("i=%d, j=%d\n",i,j);
	if(i > 2){
		i=i|16;
		printf("i=%d, j=%d\n",i,j);
	}
	int k=0;
	k=j|16;
	printf("i=%d, k=%d\n",i,k);
	
	if(j%2){
		j=j&16;
		printf("i=%d, j=%d\n",i,j);
	}
	
	if(i>j)
		printf("i=%d, j=%d\n",++i,--j);
	else
		printf("i=%d, j=%d\n",--i,++j);
	printf("Done");
}
```
OUTPUT:
```
i=3, j=44
i=19, j=44
i=19, k=60
i=18, j=45
Done
```
# 20. Write a C program to check whether a string is a palindrome or not.
---
```C
#include <stdio.h>

main(){
    int i, j=0,result = 0, count=0;
    char input[100];
	printf("Enter string:");
	gets(input);
	
	for (i = 0; input[i] != '\0'; i++) {
        if (input[i] != ' ') {
            count++;
        }
    }
    char str[count], rev[count];
    for(i=0;input[i] != '\0';i++){
        if(input[i] == ' '){
            str[j] = input[i];
            j++;
        }
    }
    j=0;
    for(i=count-1;i>=0;i--){
        rev[j] = str[i];
        j++;
    }
    for(i=0;i<count;i++){
        if(rev[i] != str[i]){
            result++;
        }
    }
	if(result == 0){
        printf("%Is not a palindrome");
	} else {
        printf("Is a palindrome");
	}
}
```