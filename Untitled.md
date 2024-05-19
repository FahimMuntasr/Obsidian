```C
#include  <stdio.h>

int main(){
	int length;
	printf("Enter your name length:");
	scanf("%d", &length);
	char str[length+1];
	printf("Enter you name:");
	gets(str);
	printf("Your name is %s", str);
	return 0;
}
```
