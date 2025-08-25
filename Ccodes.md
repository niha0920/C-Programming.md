## Program to accept two integers and check whether they are equal or not
```c
#include<stdio.h>
int main()
{
 int a, b;
 printf("Enter two integers : ");
 scanf("%d %d", &a, &b);
 if(a == b)
  printf("a and b are equal"); 
 else
  printf("a and b are not equal");
}
```

##  Program to check whether a given number is even or odd?
```c
#include<stdio.h>
int main()
{
 int num;
 printf("Enter a number : ");
 scanf("%d", &num);
 if((num % 2) == 0)
  printf("Number is even");
 else
  printf("Number id odd");
}
```
