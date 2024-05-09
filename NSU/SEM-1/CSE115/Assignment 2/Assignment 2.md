# 1.  Discuss the concept of dynamic memory allocation in C. How does dynamic memory allocation work, and what are its advantages and disadvantages compared to static memory allocation? Provide examples illustrating the use of dynamic memory allocation in C programming.
---
# 2.Create a C program to check if a given string is a palindrome using both iterative and recursive methods. Provide examples of palindrome and non-palindrome strings to test the functionality of your program.
---
# 3. Point out the errors (if any) from the following problem:
---
## A.
```c
#include  <stdio.h>
int main(){
	int twod[][] = {2,4,
						6,8};
	printf("%d\n", twod);
	return 0;
}
```
## B.
```C
#include  <stdio.h>
int main(){
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
## B. Calculate LCM of two numbers.
# 5. Complete the following-
---
## A. 
```C
int power_raiser(int base, int power)
{
	int ans;
	if(power==____)
		ans = ____;
	else
		ans = ____*_____;
	return (ans);
}
```
## B.What is the output of the following program? What does function strange compute when called with a positive integer?
```C
#include  <stdio.h>
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
# 6. What is a common cause of a stack overflow error? The sequence 2, 6, 18, 54, 162, … is geometric because each term divided by its predecessor yields the same result, 3. The number 3 is the common ratio of the sequence. Write the recursive function that can find nth number of values of this series.
---
<u>Example:</u>
Input = 3 ; Output = 54
Input = 4 ; Output = 162

Do this same problem also in non-recursive way. Express your opinion on which solution is better.
# 7. Describe the concept of tail recursion in C programming. Provide a recursive function named "factorial" that calculates the factorial of a given number using recursion. Compare the performance of the recursive approach with the non-recursive approach.
---
# 8. Point out the errors (if any) from the following problem:
---
## A.
```C
#include  <stdio.h>
int main()
{
	int twod[][] = {2, 4,
						6, 8};
	printf("%d\n", twod);
	return 0;
}
```
## B. 
```C
#include  <stdio.h>
int main()
{
	int three[3][] =
						{2,4,3,
						6,8,2,
						2,3,1};
	printf("%d\n", three[1][1]);
	return 0;
}
```
# 9. What is a pointer? What is &, * operators? What is the output of the following program?
---
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
```
# 10. Develop a C program to find the sum of each row and column of the given 2D array and print the results. Use pointers to traverse through the array.
---
# 11.Explain the concept of pass-by-reference in C programming. Provide an example demonstrating how to swap the values of two variables using pass-by-reference and a function. Discuss the advantages of using pass-by-reference compared to pass-by value in certain scenarios.
---
# 12.Suppose an array x [ ] = {16, 12.0, 6.0, 8.0, 2.5, 12.0, 14.0, -54.5} is given. Please fill up the following table with output and explanation.
---

|                                 |                                    |
| ------------------------------- | ---------------------------------- |
| Statement                       | Explanation                        |
| i = 5;                          |                                    |
| printf("%d %.1f\n", 4, x[4]);   | Displays 4 and 2.5 (value of x[4]) |
| printf("%d %.1f\n", i, x[i]);   |                                    |
| printf("%.1f\n", x[i] + 1);     |                                    |
| printf("%.1f\n", x[i] + i);     |                                    |
| printf("%.1f\n", x[i + 1]);     |                                    |
| printf("%.1f\n", x[i + i]);     |                                    |
| printf("%.1f\n", x[2 * i]);     |                                    |
| printf("%.1f\n", x[2 * i - 3]); |                                    |
| printf("%.1f\n", x[(int)x[4]]); |                                    |
| printf("%.1f\n", x[i++]);       |                                    |
| printf("%.1f \n", x[--i]);      |                                    |
| x[i - 1] = x[i];                |                                    |
| x[i] = x[i + 1];                |                                    |
| x[i] - 1 = x[i];                |                                    |
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
		scanf("%d", arr1+1);
	}
	printf("\nThe elements you entered are: \n");
	for(i=0;i<n;i++)
		printf("At Index-%d: %d\n",i, *(arr1+i));
	return 0;
}
```
# 14.Explain the concept of nested structures in C programming. Can a structure be declared inside another structure? Discuss the advantages and potential use cases of nested structures in C. Provide an example demonstrating the declaration and usage of nested structures
---
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
```
# 16. Write a C program to count the number of words and characters present in a file.
---
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
	age = 25;
	salary = 15500.00;
	printf("%s%d%f\n", e.name, age, salary);
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
		return 0;
}
```
# 18.Define a structure named "Employee" to store the name, employee ID, and salary of 50 employees. Design a program that takes input for each employee's details from the user. Then, write a function named "highSalaryEmployees()" to print the names of all employees with a salary greater than $5000.
---
# 19.Discuss the difference between writing data to a file in text mode and binary mode in C. Additionally, explain the significance of using fseek() and ftell() functions when working with file handling in C.
---
# 20. Answer the following:
---
## A. 
While using the following statements in C file,
handlingfp=fopen("myfile.txt", "r");
what happens if 'myfile.txt' does not exist on the disk and when 'myfile.txt' exists on the disk.
## B.
While using the following statement in C file,
fp = fopen("myfile.c","wb");
what happens if 'myfile.c' does not exist on the disk and when 'myfile.c' exists on the disk.