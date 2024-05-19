# 1.  Discuss the concept of dynamic memory allocation in C. How does dynamic memory allocation work, and what are its advantages and disadvantages compared to static memory allocation? Provide examples illustrating the use of dynamic memory allocation in C programming.
---
Dynamic memory allocation in C is the process of allocating memory during runtime instead of during compilation. This means that managing memory resources is now more flexible. The method for dynamic memory allocation in C is through the use of functions like `malloc()`, `calloc()`, `realloc()`, and `free()`, which are defined in the `<stdlib.h>` header.
How dynamic memory allocation works:
- **Allocation** : `malloc()` , `calloc()` or `realloc()` is used to allocate memory.
- **Deallocation** : `free()` is used to free up memory.
Advantages
- **Flexibility** : Code can adapt to unpredictable user inputs
- **Efficiency** : Only the amount of memory needed is allocated which doesnt waste space
Disadvantages
- **Memory Management Overhead** : Managing dynamically allocated memory requires the coder to be careful
Example where dynamic memory allocation is used.
```C
// CREATE A DYNAMIC ARRAY
#include  <stdio.h>
#include  <stdlib.h>
int main(){
	int *arr;
	int i, n;
	
	printf("Enter the size of your array: ");
	scanf("%d", &n);
	
	arr = (int *)malloc(n * sizeof(int));
	
	printf("Enter array elements:\n");
	for(i = 0; i < n; i++){
		scanf("%d", &arr[i]);
	}
	printf("Your array : ");
	for(i = 0; i < n; i++){
		printf("[%d]", arr[i]);
	}
	free(arr);
	return 0;
}
```
# 2.Create a C program to check if a given string is a palindrome using both iterative and recursive methods. Provide examples of palindrome and non-palindrome strings to test the functionality of your program.
---
### ITERATIVE
```C
#include <stdio.h>
int palindromeIterative(char[],int);
int main(){
    char str[100],i;
    printf("Enter string: ");
    gets(str);
    if(palindromeIterative(str))
	    printf("%s is a palindrome",str);
	else
		printf("%s is not a palindrome",str);
    return 0;
}
int palindromeIterative(char arr[]){
    int i,j,flag = 1;
    for(i=0;arr[i]!='\0';i++); // calculate string length
    char rev[i+1];
    for(j=0;arr[j]!='\0';j++){
        rev[j] = arr[i-1];
        i--;
    }
    rev[j] = '\0';
    for(i=0;rev[i]!='\0';i++){
        if(rev[i]!=arr[i]){
            flag = 0;
            break;
        }
    }
    return flag;
}
```
### RECURSIVE
```C
int palindromeRecursive(char[], int, int);
int main(){
    char str[100],i;
    printf("Enter string: ");
    gets(str);
    for(i=0;str[i]!='\0';i++);//calculate length
    if(palindromeRecursive(str, 0, i-1))
	    printf("%s is a palindrome",str);
	else
		printf("%s is not a palindrome",str);
    return 0;
}
int palindromeRecursive(char arr[],int start, int end){
    if(start>=end)
        return 1;
    if(arr[start]!=arr[end])
        return 0;
    return palindromeRecursive(arr, start + 1, end - 1);
}
```
# 3. Point out the errors (if any) from the following problem:
---
## A.
```c
#include  <stdio.h>
int main(){
	//Size of nested arrays must be declared while declaring 2D arrays
	int twod[][] = {2,4,
						6,8};
	printf("%d\n", twod);
	//Array element index not specified while printing
	return 0;
}
```
## B.
```C
#include  <stdio.h>
int main(){
	//Size of nested array not declared
	int three[3][]= 
						{2,4,3,
						6,8,2,
						2,3,1};
	printf("%d\n", three[1][1]);
	return 0;	
}
```
# 4. Write recursive and iterative functions for the following problems:
---
## A. Calculate GCD of two numbers.
```c
#include  <stdio.h>
int gcd(int,int);
int main(){
	int a,b;
	printf("Enter first number:");
	scanf("%d", &a);
	printf("Enter second number:");
	scanf("%d", &b);
	printf("The GCD of %d and %d is %d", a, b, gcd(a,b));
    return 0;
}
int gcd(int a, int b){
    if(b == 0)
        return a;
    return gcd(b, a%b);
}
```
## B. Calculate LCM of two numbers.
```C
#include  <stdio.h>
int lcm(int,int,int,int);
int main(){
	int a,b;
	printf("Enter first number:");
	scanf("%d", &a);
	printf("Enter second number:");
	scanf("%d", &b);
	printf("The LCM of %d and %d is %d", a, b, lcm(a,b,a,b));
    return 0;
}
int lcm(int a, int b,int A,int B){
    // A and B are used to store original values
    if(a==b)
        return a;
    if(a>b)
        return lcm(a,b+B,A,B);
    else
        return lcm(a+A,b,A,B);
}

```
# 5. Complete the following-
---
## A. 
```C
int power_raiser(int base, int power)
{
	int ans;
	if(power==_0_)
		ans = _1_;
	else
		ans = _base_*_power_raiser(base,power-1)_;
	return (ans);
}
```
## B.What is the output of the following program? What does function strange compute when called with a positive integer?
```C
#include <stdio.h>
int strange(int n);
int main(void)
{
	printf("%d\n",strange(7));
}
int strange(int n)
{
	int ans;
	if(n==1)
		ans = 0;
	else
		ans = 1 + strange(n/2);
	return (ans);
}
```
OUTPUT : 2
`int strange()` calculates the number of times `n` can be divided by `2` until `n == 1`;
# 6. What is a common cause of a stack overflow error? The sequence 2, 6, 18, 54, 162, … is geometric because each term divided by its predecessor yields the same result, 3. The number 3 is the common ratio of the sequence. Write the recursive function that can find nth number of values of this series.
---
<u>Example:</u>
Input = 3 ; Output = 54
Input = 4 ; Output = 162

Do this same problem also in non-recursive way. Express your opinion on which solution is better.

A common cause of stack overflow is when there is no base case or the base case is never reached due to some logical error.
#### Recursive solution
```C
#include <stdio.h>
int nthTerm(int,int,int);
int main(){
    // nth term --> n = ar^(n-1)
    int n;
    printf("Enter n: ");
    scanf("%d", &n);
    printf("%d\n", nthTerm(2,3,n));
    return 0;
}
int nthTerm(int a,int r,int n){
    if(n == 0)
        return a;
    return nthTerm(a*r, r, n-1);
}
```
#### Iterative solution
```C
#include <stdio.h>
int nTerm(int,int,int);
int main(){
    // nth term --> n = ar^(n-1)
    int n;
    printf("Enter n: ");
    scanf("%d", &n);
    printf("%d\n", nTerm(2,3,n));
    return 0;
}
int nTerm(int a, int r, int n){
    int i,answer=1;
    for(i=0;i<n;i++){
        answer *= r;
    }
    return a * answer;
}
```
Recursive solution is better as the code is smaller and more readable
# 7. Describe the concept of tail recursion in C programming. Provide a recursive function named "factorial" that calculates the factorial of a given number using recursion. Compare the performance of the recursive approach with the non-recursive approach.
---
Tail recursion is a form of recursion where the recursive call is the last operation in the function. This optimizes the performance and prevents stack overflow errors.
#### Recursive
```C
#include <stdio.h>
int factorial(int);
int main(){
	int n;
	printf("Enter n:");
	scanf("%d",&n);
	printf("%d! = %d", n, factorial(n));
	return 0;
}
int factorial(int n){
	if(n==1)
		return 1;
	else if(n==0)
		return 1;
	else
		return n * factorial(n-1);
}
```
#### Iterative
```C
#include <stdio.h>
int factorial(int);
int main(){
	int n;
	printf("Enter n:");
	scanf("%d",&n);
	printf("%d! = %d", n, factorial(n));
	return 0;
}
int factorial(int n){
	int ans = 1;
	while(n>0){
		ans *= n;
		n--;
	}
}
```
# 8. Point out the errors (if any) from the following problem:
---
## A.
```C
#include  <stdio.h>
int main(){
	//Size of nested arrays must be declared while declaring 2D arrays
	int twod[][] = {2,4,
						6,8};
	printf("%d\n", twod);
	//Array element index not specified while printing
	return 0;
}

```
## B. 
```C
#include  <stdio.h>
int main(){
	//Size of nested array not declared
	int three[3][]= 
						{2,4,3,
						6,8,2,
						2,3,1};
	printf("%d\n", three[1][1]);
	return 0;	
}
```
# 9. What is a pointer? What is &, * operators? What is the output of the following program?
---
A pointer is a variable which contains the address of another variable.`&` is the 'address of' operator, this returns the address of a variable.`*` is the 'dereference' operator, this returns the value at the address specified.  
## A.
```C
#include  <stdio.h>
int main()
{
	float a = 13.5;
	float *b, *c;
	b = &a ; /*suppose address of a is 1006*/
	c = b;
	printf("%u %u %u\n",&a, b, c);
	printf("%f%f%f%f%f\n", a, *(&a), *&a, *b, *c);
	return 0;
}
/*
1006 1006 1006
13.513.513.513.513.5
*/
```
## B.
```C
#include  <stdio.h>
void function (int *);
int main()
{
	int i = 35, *z;
	z = function(&i);
	printf("%d\n", z);
	return 0;
}
void function(int *m)
{
	return(m+2);
}
/*
37
*/
```
# 10. Develop a C program to find the sum of each row and column of the given 2D array and print the results. Use pointers to traverse through the array.
---
```C
#include <stdio.h>

int generateNum(){
	return rand(NULL) % 100;
}
int main(){
	int arr[3][3], row[3], col[3];
	int i,j,k,sum;
	//randomly Initialize a 2D array and print it
	printf("Input array\n");
	for(i=0;i<3;i++){
		for(j=0;j<3;j++){
			*(*(arr+i)+j) = generateNum();
			printf("[%d]", *(*(arr+i)+j));
		}
		printf("\n");
	}
	for(k=0;k<3;k++){
		*(row+k) = 0;
		*(col+k) = 0;
		for(i=0;i<3;i++){
			*(row+k)+=*(*(arr+k)+i);
			*(col+k)+=*(*(arr+i)+k);
		}
	}
	printf("Sum of rows\n");
	for(i=0;i<3;i++){
		printf("[%d]\n",*(row+i));
	}
	printf("Sum of columns\n");
	for(i=0;i<3;i++){
		printf("[%d]",*(col+i));
	}
	return 0;
}
```
# 11.Explain the concept of pass-by-reference in C programming. Provide an example demonstrating how to swap the values of two variables using pass-by-reference and a function. Discuss the advantages of using pass-by-reference compared to pass-by value in certain scenarios.
---
Pass-by-reference allows a function to modify the actual variables instead of the copies. 
```C
#include <stdio.h>
void swap(int*,int*);
int main(){
	int x = 10;
	int y = 20;
	printf("Before swap: x = %d, y = %d\n", x, y);
	swap(&x, &y);
	printf("After swap: x = %d, y = %d\n", x, y);
	return 0;
}
void swap(int *a, int *b){
	int temp = *a;
	*a = *b;
	*b = temp;
}
```
Pass-by-reference reduces the memory usage since only the address of the variable is passed, rather than creating a copy of the variable itself. 
# 12.Suppose an array x [ ] = {16, 12.0, 6.0, 8.0, 2.5, 12.0, 14.0, -54.5} is given. Please fill up the following table with output and explanation.
---

|                                 |                                                                        |
| ------------------------------- | ---------------------------------------------------------------------- |
| Statement                       | Explanation                                                            |
| i = 5;                          |                                                                        |
| printf("%d %.1f\n", 4, x[4]);   | Displays 4 and 2.5 (value of x[4])                                     |
| printf("%d %.1f\n", i, x[i]);   | Displays 5 and 12.0 (value of x[5])                                    |
| printf("%.1f\n", x[i] + 1);     | Displays 13.0 (value of x[5] + 1 = 12.0 + 1)                           |
| printf("%.1f\n", x[i] + i);     | Displays 17.0 (value of x[5] + 5 = 12.0 + 5)                           |
| printf("%.1f\n", x[i + 1]);     | Displays 14.0 (value of x[5+1]) = x[6]                                 |
| printf("%.1f\n", x[i + i]);     | Displays 0.0 as x[10] is a NULL value                                  |
| printf("%.1f\n", x[2 * i]);     | Displays 0.0 as x[10] is a NULL value                                  |
| printf("%.1f\n", x[2 * i - 3]); | Displays -54.5 (value of x[7])                                         |
| printf("%.1f\n", x[(int)x[4]]); | Displays 6.0 as (x[4] = 2.5, (int)2.5 = 2,x[2] = 6.0)                  |
| printf("%.1f\n", x[i++]);       | Displays 12.0 as x[5] is first printed than i is increased by 1, i = 6 |
| printf("%.1f \n", x[--i]);      | Displays 2.5 as i is first decreased by once than x[4] is printed      |
| x[i - 1] = x[i];                | x[] = {16, 12.0, 6.0, 8.0, 12.0, 12.0, 14.0, -54.5}                    |
| x[i] = x[i + 1];                | x[] = {16, 12.0, 6.0, 8.0, 2.5, 14.0, 14.0, -54.5}                     |
| x[i] - 1 = x[i];                | Incorrect syntax, it should be x[i] = x[i] - 1                         |
# 13. Debug and Explain what the following program is doing:
---
```C
#include  <stdio.h>
int main(){
	int arr1[25], i, n;
	printf("Input the number of elements for the array:");
	scanf("%d", &n);
	printf("Enter the %d elements of the Array:\n",n);
	for(i=0;i<n;i++){
		printf("At Index-%d: ",i);
		scanf("%d", arr1+1); //syntax error, it should be arr1 + i;
	}
	printf("\nThe elements you entered are: \n");
	for(i=0;i<n;i++)
		printf("At Index-%d: %d\n",i, *(arr1+i));
	return 0;
}
```
This program takes integers as input for an array and then prints it

# 14.Explain the concept of nested structures in C programming. Can a structure be declared inside another structure? Discuss the advantages and potential use cases of nested structures in C. Provide an example demonstrating the declaration and usage of nested structures
---
Nested structures are used to create complex data types by including one structure within another. 
A structure can be declared inside another structure which is called nested structures.
Advantages:
- Reusability: Enables reusability of individual structures in different contexts.
- Organization of Related Data: Nested structures allow grouping related data together in a hierarchical manner, making the code more organized and readable.
Potential use cases:
- Database Records: Nested structures can represent complex records in databases, where each record may contain multiple related fields.
- Configuration Files: Complex configuration data with multiple levels of settings can be represented using nested structures.
Example:
```C
#include <stdio.h>
// Define the inner structure
struct Date {
    int day;
    int month;
    int year;
};
// Define the outer structure containing the inner structure
struct Student {
    char name[50];
    int roll_number;
    struct Date birthdate; // Nested structure
};
int main() {
    // Declare and initialize an instance of the outer structure
    struct Student student1 = {"John Doe", 12345, {15, 8, 2000}};
    // Access and print the nested structure's members
    printf("Student Name: %s\n", student1.name);
    printf("Roll Number: %d\n", student1.roll_number);
    printf("Birth Date: %02d/%02d/%d\n", student1.birthdate.day, student1.birthdate.month, student1.birthdate.year);
    // Modify the nested structure's members
    student1.birthdate.day = 16;
    student1.birthdate.month = 9;
    student1.birthdate.year = 2001;
    // Print the modified nested structure's members
    printf("Updated Birth Date: %02d/%02d/%d\n", student1.birthdate.day, student1.birthdate.month, student1.birthdate.year);
    return 0;
}
```
# 15.What will be the output of the following codes:
---
## A.
```c
#include  <stdio.h>
#include  <string.h>
int main()
{
	struct part{
		char carname[20];
		int carnumber;
	};
	struct part p, *ptrp;
	ptrp = &p;
	strcpy(p.carname, "Mercedes");
	p.carnumber = 102133;
	printf("%s%d\n", p.carname, p.carnumber);
	printf("%s%d\n", (*ptrp).carname, (*ptrp).carnumber);
	printf("%s%d\n", ptrp->carname, ptrp->carnumber);
	return 0;
}
/*
Mercedes102133
Mercedes102133
Mercedes102133
*/
```
## B. 
```c
#include  <stdio.h>
struct randomStruct{
	int number;
	char message1[50];
	char message2[50];
	
} m1 = {22, "This is Message 1", "& this is Message 2"};
int main()
{
	struct randomStruct m2, m3;
	m2 = m1;
	m3 = m2;
	printf("%d %s %s\n", m1.number, m2.message1, m3.message2);
	return 0;
}
/*
22 This is Message 1 & this is Message 2
*/
```
# 16. Write a C program to count the number of words and characters present in a file.
---
```C
```
# 17. Point out the errors (if any) from the following codes:
---
## A. 
```c
#include  <stdio.h>
#include  <string.h>
int main(){
	struct employee {
		char name[30];
		int age;
		float salary;
	};
	struct employee e;
	strcpy(e.name, "Shailesh");
	age = 25;// this should refer to the struct it is from, e.age = 25
	salary = 15500.00;// e.salary = 15500.00
	printf("%s%d%f\n", e.name, age, salary); // e.age, e.salary should be used to print
	return 0;
}
```
## B.
```c
#include  <stdio.h>
struct virus{
	char name[20];
	char type[30];
	int serial;
}v[2] = {"Corona", "Deadly", 2019, "HIV", "Killer", 1999};
int main()
{
	int i;
	for(i=0;i<=1;i++)
		printf("%s%s\n", v.name, v.type[]);
		// As v is an array of structures it should have an index number during printing
		// Also there should be no third brackets after v.type
		// This is the correct version 
		// printf("%s%s\n", v[i].name, v[i].type)
		return 0;
}
```
# 18.Define a structure named "Employee" to store the name, employee ID, and salary of 50 employees. Design a program that takes input for each employee's details from the user. Then, write a function named "highSalaryEmployees()" to print the names of all employees with a salary greater than $5000.
---
```C
/*
Define a structure named "Employee" to store the name, employee ID,
and salary of 50 employees. Design a program that takes input for
each employee's details from the user. Then, write a function named
"highSalaryEmployees()" to print the names of all employees with a
salary greater than $5000.
*/
#include <stdio.h>
#include <stdlib.h>
struct Employee{
    char name[50];
    int ID;
    int salary;
}e[50];
void highSalaryEmployees(struct Employee *data){
    printf("%s\n%d\n%d\n\n", data->name,data->ID,data->salary);
}
int main(){
    int i;
    //Take input
    for(i=0;i<50;i++){
        printf("Name: ");
        scanf("%s", e[i].name);
        printf("Id: ");
        scanf("%d", &e[i].ID);
        printf("Salary: ");
        scanf("%d", &e[i].salary);
    }
    for(i=0;i<50;i++){
        if(e[i].salary>5000){
            highSalaryEmployees(&e[i]);
        }
    }
    return 0;
}
```
# 19.Discuss the difference between writing data to a file in text mode and binary mode in C. Additionally, explain the significance of using fseek() and ftell() functions when working with file handling in C.
---
#### Difference between text mode and binary mode
- Text mode has EOF (end-of-file) marker at the end of the file, binary mode does not have the EOF marker
- All data is interpreted as characters in text mode. All data in binary mode is read as it its
#### fseek()
- It is used to move the file pointer to a specified location
- `int fseek(File *filename, int distance, int start)`
- the distance parameter is the number of bytes to move the file pointer
- the start parameter is the location from where the pointer will start moving
#### ftell()
- returns the current location of the file pointer
- `int fseek(FILE *filename)`
# 20. Answer the following:
---
## A. 
While using the following statements in C file,
handlingfp=fopen("myfile.txt", "r");
what happens if 'myfile.txt' does not exist on the disk and when 'myfile.txt' exists on the disk.
#### When `myfile.txt` Does Not Exist on the Disk
- **Return Value**: If "myfile.txt" does not exist, `fopen` will return `NULL`.
- **Error Handling**: It's essential to check the return value of `fopen` to handle this scenario correctly.
- **No File Created**: The file will not be created since the mode is `"r"` (read mode), which only allows opening an existing file for reading
#### When `myfile.txt` Exists on the Disk

- **Return Value**: If "myfile.txt" exists, `fopen` will return a pointer to the `FILE` object associated with the file.
- **File Pointer**: The file pointer will be positioned at the beginning of the file, ready for reading.
- **Read Operations**: You can proceed to perform read operations on the file using functions like `fgetc`, `fgets`, `fread`, etc.
## B.
While using the following statement in C file,
fp = fopen("myfile.c","wb");
what happens if 'myfile.c' does not exist on the disk and when 'myfile.c' exists on the disk.
#### When `myfile.c` Does Not Exist on the Disk

- **File Creation**: If "myfile.c" does not exist, `fopen` will create a new file named "myfile.c".
- **Return Value**: `fopen` will return a pointer to the `FILE` object associated with the new file.
- **File Pointer**: The file pointer will be positioned at the beginning of the newly created file.
- **File Mode**: Since the file is opened in "wb" (write binary) mode, the file is intended for binary data. The file will be empty initially.
#### When `myfile.c` Exists on the Disk

- **File Truncation**: If "myfile.c" already exists, `fopen` will open the existing file but truncate it to zero length. This means any existing data in the file will be lost.
- **Return Value**: `fopen` will return a pointer to the `FILE` object associated with the file.
- **File Pointer**: The file pointer will be positioned at the beginning of the file.
- **File Mode**: The file is opened in "wb" mode, ready for binary writing.