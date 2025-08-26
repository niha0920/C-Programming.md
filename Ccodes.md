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
 if(num > 0)
  printf("Number is Positive");
 else if(num < 0)
  printf("Number is Negative");
 else
  printf("Number is Zero");
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
 else if(m == 0)
  n = 0;
 else
  n = -1;
 printf("Value of n is %d", n);
}
```

## 7. Program to find the largest of three numbers
```c
#include<stdio.h>
int main()
{
 int a, b, c;
 printf("Enter three numbers : ");
 scanf("%d %d %d", &a, &b, &c);
 if(a >= b && a >= c)
  printf("a is the largest number");
 else if(b >= a && b >= c)
  printf("b is the largest number");
 else 
  printf("c is the largest number");
}
```

## 8. Program to check whether a character is a vowel or consonant?
```c
#include<stdio.h>
#include<ctype.h>
int main()
{
 char ch;
 scanf("%c", &ch);
 char fch = tolower(ch);
 if(fch >= 'a' && fch <= 'z')
 {
  if(fch == 'a' || fch == 'e' || fch == 'i' || fch == 'o' || fch == 'u')
   printf("Character is Vowel");
  else 
   printf("Character is Constant");
 }
 else
 {
  printf("Character is not an Alphabet");
 }
}
```

## 9. Program to check whether a character is an alphabet or not?
```c
#include<stdio.h>
#include<ctype.h>
int main()
{
 char ch;
 printf("Enter a Character");
 scanf("%c", &ch);
 char fch = tolower(ch);
 if(fch >= 'a' && fch <= 'z')
 {
  if(fch == 'a' || fch == 'e' || fch == 'i' || fch == 'o' || fch == 'u')
   printf("Character is Vowel");
  else 
   printf("Character is Constant");
 }
 else
 {
  printf("Character is not an Alphabet");
 }
}
```

## 10. Program to find minimum or maximum between two numbers?
```c
#include<stdio.h>
int main()
{
 int a, b, min, max;
 printf("Enter two numbers : ");
 scanf("%d %d", &a, &b);
 if(a > b)
 {
  min = b;
  max = a;
 }
 else
 {
  min = a;
  max = b;
 }
 printf("Minimum : %d, Maximum : %d", min, max);
}
```

## 11. Program to enter week number and print day of week?
```c
#include<stdio.h>
int main()
{
 int num;
 printf("Enter week number : ");
 scanf("%d", &num);
 switch(num)
 {
  case 1 : printf("Sunday");
           break;
  case 2 : printf("Monday");
           break;
  case 3 : printf("Tuesday");
           break; 
  case 4 : printf("Wednesday");
           break;
  case 5 : printf("Thursday");
           break;
  case 6 : printf("Friday");
           break;
  case 7 : printf("Saturday");
           break;
  default : printf("Invalid Input");
 }
}
```
