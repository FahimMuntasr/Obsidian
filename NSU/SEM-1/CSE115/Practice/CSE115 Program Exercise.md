# Contents
---
- [[#Selection]]
- [[#Loops]]
# Selection
---
##### 1
```c
/*
Write a C program that takes an integer input and determines whether it's positive, negative, or zero.
Input: -5
Output: The entered number is negative.
*/
#include <stdio.h>
int main(){
    int x;
    
    printf("Enter your integer:");
    scanf("%d", &x);
    
    if(x == 0){
        printf("The entered number is zero");
    } else if(x > 0){
        printf("The entered number (%d) is positive", x);
    } else if(x < 0){
        printf("The entered number (%d) is negative", x);
    }
    return 0;
}
```
##### 2
```c
/*
2. Create a program that reads two integers and prints the larger one using a conditional statement (if-else).
Input:
Enter the first integer: 24
Enter the second integer: 37
Output: The larger integer is 37.
*/
#include <stdio.h>
int main(){
    int x, y;
    
    printf("Enter your first integer:");
    scanf("%d", &x);
    printf("Enter your second integer:");
    scanf("%d", &y);
    
    if(x > y){
        printf("The larger integer is %d", x);
    } else if(x == y){
        printf("Both numbers are equal");
    } else if(x < y){
        printf("The larger integer is %d", y);
    }
    return 0;
}
```
##### 3
```c
/*
3. Develop a C program that calculates the roots of a quadratic equation given the coefficients a, b, and c.
Input:
Enter the coefficient a: 2
Enter the coefficient b: -5
Enter the coefficient c: -3
Output: Roots of the quadratic equation are: 3.00 and -0.50
*/
#include <stdio.h>
#include <math.h>
int main(){
    int a, b, c;
    float r1, r2;
    
    printf("Enter the value of a:");
    scanf("%d", &a);
    printf("Enter the value of b:");
    scanf("%d", &b);
    printf("Enter the value of c:");
    scanf("%d", &c);
    
    r1 = (((-b)+(sqrt((pow(b,2))- (4 * a * c))))/(2*a));
    r2 = (((-b)-(sqrt((pow(b,2))- (4 * a * c))))/(2*a));
    printf("The roots of %dx^2 + %dx + %d are %f and %f", a, b, c, r1, r2);
    return 0;
}
```
##### 4
```c
/*
4. Write a program to find the maximum of three numbers using nested if statements.
Input:
Enter the first number: 18
Enter the second number: 27
Enter the third number: 22
Output: The maximum number is 27.
*/
#include <stdio.h>
int main(){
    int num1, num2, num3;
    
    printf("Enter the first number:");
    scanf("%d", &num1);
    printf("Enter the second number:");
    scanf("%d", &num2);
    printf("Enter the third number:");
    scanf("%d", &num3);
    
    if(num1 > num2){
	    if(num1 > num3){
			printf("The maximum number is %d", num1);
		} else {
			printf("The maximum number is %d", num3);
		}
    } else {
	    if(num2 > num3){
		    printf("The maximum number is %d", num2);
	    } else {
		    printf("The maximum number is %d", num3);
	    }
    }
    return 0;
}
```
##### 5
```c
/*
5. Implement a C program that reads a character and determines whether it's a vowel or a consonant using a switch statement.
Input:
Enter a character: e
Output: The entered character 'e' is a vowel.
*/
#include <stdio.h>
int main(){
    char inputChar;
    
    printf("Enter the a character:");
    scanf("%c", &inputChar);
    
    switch (inputChar){
        case 'a':
            printf("The entered character '%c' is a vowel", inputChar);
            break;
        case 'e':
            printf("The entered character '%c' is a vowel", inputChar);
            break;
        case 'i':
            printf("The entered character '%c' is a vowel", inputChar);
            break;
        case 'o':
            printf("The entered character '%c' is a vowel", inputChar);
            break;
        case 'u':
            printf("The entered character '%c' is a vowel", inputChar);
            break;
        default:
            printf("The entered character '%c' is a consonant", inputChar);
    }
    return 0;
}
```
##### 6
```c
/*
6. Write a C program to determine the greatest of three numbers using nested ternary operators.
Input:
Enter three numbers: 7 12 5
Output: The greatest number is 12
*/
#include <stdio.h>
int main(){
    int num1, num2, num3;
    
    printf("Enter three numbers:");
    scanf("%d", &num1);
    scanf("%d", &num2);
    scanf("%d", &num3);
    
    (num1>num2)?((num1 > num3)?printf("The greatest number is %d",num1):printf("The greatest number is %d", num3)):((num2 > num3)?printf("The greatest number is %d", num2):printf("The greatest number is %d", num3));
    return 0;
}
```
##### 7
```c
/*
7. Develop a program that calculates the total cost of a car rental.
   The cost depends on the number of days the car is rented and the type
   of car chosen (economy, standard, luxury). The cost per day for each
   type of car is different. The program should ask the user for the number
   of days and the car type, then calculate and display the total cost.
   Car Type Pricing:
   - Economy: $30 per day
   - Standard: $50 per day
   - Luxury: $100 per day
Input: Enter the number of days: 5
Enter car type (1=economy, 2=standard, 3=luxury): 2
Output: Total cost: $250
*/
#include <stdio.h>
int main(){
    int days, type;
    
    printf("Enter the number of days:");
    scanf("%d", &days);
    printf("Enter car type (1=economy, 2=standard, 3=luxury):");
    scanf("%d", &type);
    
    switch(type){
        case 1:
            printf("Total cost: %d", (30*days));
            break;
        case 2:
            printf("Total cost: %d", (50*days));
            break;
        case 3:
            printf("Total cost: %d", (100*days));
            break;
        default:
            printf("Invalid input type");
    }
    return 0;
}
```
##### 8
```c
/*
8. Develop a C program to classify a given year as a leap year or not.
Sample Input:
Enter a year: 2024
Sample Output: 2024 is a leap year.
*/
#include <stdio.h>
int main(){
    int year;
    
    printf("Enter a year:");
    scanf("%d", &year);
    
    if(year % 4 == 0){
        if(year % 100 == 0){
            if(year % 400 == 0){
                printf("%d is a leap year", year);
            } else {
                printf("%d is not a leap year", year);
            }
        } else {
            printf("%d is a leap year", year);
        }
    } else {
        printf("%d is not a leap year", year);
    }
    return 0;
}

```
##### 9
```c
/*
9. Write a program that takes a character input and determines whether it's an uppercase letter, lowercase letter, digit, or special character.
Input:
Enter a character: G
Sample Output: G is an uppercase letter.
*/
#include <stdio.h>
int main(){
    char userInput;
    
    printf("Enter a character:");
    scanf("%c", &userInput);
    
    if(userInput == '0' || userInput == '1' || userInput == '2'|| userInput == '3'|| userInput == '4'|| userInput == '5'|| userInput == '6'|| userInput == '7'|| userInput == '8'|| userInput == '9'){
        printf("%c is a digit",userInput);
    } else if (userInput=='a'||userInput=='b'||userInput=='c'||userInput=='d'||userInput=='e'||userInput=='f'||userInput=='g'||userInput=='h'||userInput=='i'||userInput=='j'||userInput=='k'||userInput=='l'||userInput=='m'||userInput=='n'||userInput=='o'||userInput=='p'||userInput=='q'||userInput=='r'||userInput=='s'||userInput=='t'||userInput=='u'||userInput=='v'||userInput=='w'||userInput=='x'||userInput=='y'||userInput=='z'){
        printf("%c is a lowercase letter",userInput);
    } else if (userInput=='A'||userInput=='B'||userInput=='C'||userInput=='D'||userInput=='E'||userInput=='F'||userInput=='G'||userInput=='H'||userInput=='I'||userInput=='J'||userInput=='K'||userInput=='L'||userInput=='M'||userInput=='N'||userInput=='O'||userInput=='P'||userInput=='Q'||userInput=='R'||userInput=='S'||userInput=='T'||userInput=='U'||userInput=='V'||userInput=='W'||userInput=='X'||userInput=='Y'||userInput=='Z'){
        printf("%c is a uppercase letter",userInput);
    } else {
        printf("%c is a special character",userInput);
    }
    return 0;
}
```
##### 10
```c
/*
10. Implement a C program that calculates the final grade for a student based on their exam score and attendance percentage.
Input:
Enter exam score: 89
Enter attendance percentage: 92
Sample Output: Final grade: A
*/
#include <stdio.h>
int main(){
    int score, attendance;
    float grade;
    char letter;
    
    printf("Enter exam score:");
    scanf("%d", &score);
    printf("Enter attendance percentage:");
    scanf("%d", &attendance);
    
    grade = (((75*score)+(25*attendance))/100);
    if(grade >= 90){
        letter = 'A';
    } else if(grade >= 80){
        letter = 'B';
    } else if(grade >= 70){
        letter = 'C';
    } else if(grade >= 60){
        letter = 'D';
    } else if(grade >= 50){
        letter = 'E';
    } else {
        letter = 'F';
    }
    
    printf("Final Grade: %c", letter);
    return 0;
}
```
# Loops
---
##### 1
```c
/*
1. Write a program that calculates the sum of the first N even numbers using a
single while loop.
Input: 5
Output: Sum of first 5 even numbers: 30
*/
#include <stdio.h>

int main() {
    int count, index=0, nextNum = 2, result=0;
    printf("Input:");  
    scanf("%d", &count);
    while(index < count){
        result += nextNum;
        nextNum += 2;
        index++;
    }
    printf("Sum of first %d even numbers: %d", count, result);
    return 0;
}
```
##### 2
```c
/*
2. Write a program to calculate the sum of the squares of the first N natural
numbers using a single while loop.
Input: 4
Output: Sum of squares: 30
*/
#include <stdio.h>
#include <math.h>
int main() {
	int count, nextNum = 1, result=0;
	printf("Input:");
	scanf("%d", &count);
	while(0 < count){
		result += pow(nextNum, 2);
		nextNum = nextNum + 1;
		count--;
	}
	printf("Sum of squares: %d", result);
	return 0;
}
```
##### 3
```c
/*
3. Implement a program to calculate the factorial of a number using a do-while
loop.
Input:
Enter a number: 4
Output: The factorial of 4 is 24
*/
#include <stdio.h>

int main() {
	int count, result=1, index;
	printf("Input:");
	scanf("%d", &count);
	index = count;
	while(0 < count){
		result *= count;
		count--;
	}
	printf("The factorial of %d is %d", index, result);
	return 0;
}
```
##### 4
```c
/*
4. Write a program that reads positive integers until a negative integer is entered
and then calculates the sum of the positive integers.
Input:
Enter positive integers: 10 5 8 -1
Output: Sum of positive integers: 23
*/
#include <stdio.h>

int main() {
	int inputNum , result=0;
	printf("Enter positive integer:");
	scanf("%d", &inputNum);
	if(inputNum > 0){
		while(inputNum > 0){
			result += inputNum;
			printf("Enter positive integer:");
			scanf("%d", &inputNum);            
		}
	}
	printf("Sum of positive integers: %d", result);
	return 0;
}
```
##### 5
```c
/*
5. Develop a C program that prints the terms of the Fibonacci series that are less than a given limit using a single loop.
Sample Input:
Enter the limit: 100
Output: Fibonacci series terms less than 100: 0 1 1 2 3 5 8 13 21 34 55 89
*/
#include <stdio.h>

int main() {
	int limit, fibNum = 0, nextFibNum = 1, reduntant = 0;
	printf("Enter the limit:");
	scanf("%d", &limit);
	printf("Fibonacci series terms less than %d: 0 1", limit);
	while(reduntant < limit){
		printf(" %d", reduntant);
		reduntant = fibNum + nextFibNum;
		fibNum = nextFibNum;
		nextFibNum = reduntant;
	}
	printf("\n");
	return 0;
}
```
##### 6
```c


```