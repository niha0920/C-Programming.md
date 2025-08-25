## 1. Program to accept two integers and check whether they are equal or not
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

##  2. Program to check whether a given number is even or odd?
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

## 3. Program to check whether a given number is positive or negative?
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

## 4. Program to find whether a given year is a leap year or not?
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

## 5. Program to read the age of a candidate and determine whether he is eligible to cast his/her own vote
```c
#include<stdio.h>
int main()
{
 int age;
 printf("Enter age : ");
 scanf("%d", &age);
 if(age >= 18)
  printf("He/She is eligible to cast his/her own Vote");
 else 
  printf("He/She is not eligible to cast his/her own Vote");
}
```

## 6. Program to read the value of an integer m and display the value of n is 1 when m is larger than 0, 0 when m is 0 and -1 when m is less than 0
```c
#include<stdio.h>
int main()
{
 int m, n;
 printf("Enter value of m : ");
 scanf("%d", &m);
 if(m > 0)
  n = 1;
 else 
  n = 0;
 printf("Value of n is %d", n);
}
```
