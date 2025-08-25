## Program to accept two integers and check whether they are equal or not
```c
#include<stdio.h>
int main()
{
 int a, b;
 printf("Enter two integers : ");
 scanf("%d %d", &a, &b);
 if(a == b)
  printf("a and b are Equal"); 
 else
  printf("a and b are not Equal");
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
  printf("Number is Even");
 else
  printf("Number id Odd");
}
```

## Program to check whether a given number is positive or negative?
```c
#include<stdio.h>
int main()
{
 int num;
 printf("Enter a number : ");
 scanf("%d", &num);
 if(num >= 0)
  printf("Number is Positive");
 else
  printf("Number is Negative");
}
```

## Program to find whether a given year is a leap year or not?
```c
#include<stdio.h>
int main()
{
 int year;
 scanf("%d", &year);
 if(year % 400 == 0 || year % 4 == 0 && year % 100 != 0)
  printf("%d is a Leap year", year);
 else  
  printf("%d is not a Leap year",year);
}
```
