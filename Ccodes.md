## CONTROL STATEMENTS
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
 int week;
 printf("Enter week number : ");
 scanf("%d", &week);
 switch(week)
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

## 12. Program to check whether a character is uppercase or lowecase?
```c
#include<stdio.h>
int main()
{
 char ch;
 printf("Enter a character : ");
 scanf("%c", &ch);
 if(ch >= 'A' && ch <= 'Z')
  printf("Character is in Uppercase");
 else if(ch >= 'a' && ch <= 'z')
  printf("Character is in Lowercase"); 
 else
  printf("Character is not an alphabet");
}
```

## 13. Program to find number of days in month?
```c
#include<stdio.h>
int main()
{
 int month;
 printf("Enter month number : ");
 scanf("%d", &month);
 switch(month)
 {
  case 1 : 
  case 3 :
  case 5 : 
  case 7 : 
  case 8 : 
  case 10 : 
  case 12 : printf("31 Days");
           break;
  case 2 : printf("28 or 29 Days");
           break;
  case 4 : 
  case 6 : 
  case 9 :
  case 11 : printf("30 Days");
           break;
  default : printf("Invalid Input");
 }
}
```

## 14. Program to find maximum between two numbers using swicth case?
```c
#include<stdio.h>
int main()
{
 int a, b;
 printf("Enter two numbers : ");
 scanf("%d %d", &a, &b);
 switch(a > b)
 {
  case 1 : printf("Maximun : %d", a);
           break;
  case 0 : switch(b > a)
           {
            case 1 : printf("Maximum : %d", b);
                     break;
            case 0 : printf("Both are equal");
           }
 } 
}
```

## 15. Program to print even numbers between 1 to 20 using a for loop?
```c
#include<stdio.h>
int main()
{
 printf("Even numbers from 1-20 : ");
 for(int i = 0; i <= 20; i++)
 {
  if((i % 2) == 0)
   printf("%d ", i);
 }
}
```

## 16. Program to calculate the sum of numbers from 1 to 100 using a while loop?
```c
#include<stdio.h>
int main()
{
 int i = 1, sum = 0;
 while(i <= 100)
 {
  sum += i;
  i++;
 }
 printf("Sum of numbers from 1 to 100 : %d", sum);
}
```

## 17. Program to find the factorial of a given number using a for loop?
```c
#include<stdio.h>
int main()
{
 int num, fact = 1;
 printf("Enter a number : ");
 scanf("%d", &num);
 for(int i = num; i > 0; i--)
 {
  fact *= i;
 }
 printf("Factorial : %d", fact);
}
```

## 18. Program to check whether a given number is prime or not using a while loop?
```c
#include<stdio.h>
int main()
{
 int num, i = 2, isprime = 1;
 printf("Enter a number : ");
 scanf("%d", &num);
 if(i <= 1)
 {
  isprime = 0;
 }
 else
 {
  while(i <= (num / 2))
  {
   if(num % i == 0)
   {
    isprime = 0;
    break;
   }
   i++;
  }
 }
 if(isprime)
  printf("%d is Prime", num);
 else
  printf("%d is not Prime", num);
}
```

## 19. Program to find the sum of digits of a number using a while loop?
```c
#include<stdio.h>
int main()
{
 int num, sum = 0;
 printf("Enter a number : ");
 scanf("%d", &num);
 while(num > 0)
 { 
  int rem = num % 10;
  sum += rem;
  num = num / 10;
 }
 printf("Sum of digits of a number : %d", sum);
}
```

## 20. Program to print fibonacci series up to n terms using a for loop?
```c
#include<stdio.h>
int main()
{
 int n, temp1 = 0, temp2 = 1, nextTerm;
 printf("Enter a number : ");
 scanf("%d", &n);
 for(int i = 1; i <= n; i++)
 {
  printf("%d ", temp1);
  nextTerm = temp1 + temp2;
  temp1 = temp2;
  temp2 = nextTerm;
 }
}
```

## 21. Program to reverse a given number using a while loop?
```c
#include<stdio.h>
int main()
{
 int num, rev = 0;
 printf("Enter a number : ");
 scanf("%d", &num);
 int n = num;
 while(n > 0)
 {
  int rem = n % 10;
  rev = rev * 10 + rem;
  n = n / 10;
 } 
 printf("Reverse of %d is %d", num, rev);
}
```

## 22. Program to find the largest element in an array using a for loop?
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter size of an array : ");
 scanf("%d", &n);
 int arr[n];
 printf("Enter the elements of an array : ");
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr[i]);
 }
 int max = arr[0];
 for(int i = 0; i < n; i++)
 {
  if(arr[i] > max)
   max = arr[i];
 }
 printf("Largest element in an array is : %d", max);
}
```

## 23. Program to find the smallest element in an array using a while loop?
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter the size of array : ");
 scanf("%d", &n);
 int arr[n];
 printf("Enter elements of an array : ");
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr[i]);
 }
 int i = 0, min = arr[0];
 while(i < n)
 {
  if(arr[i] < min)
   min = arr[i];
  i++;
 }
 printf("Smallest element in an array : %d", min);
}
```

## 24. Program to print all the elements of an array using a for loop?
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter the size of array : ");
 scanf("%d", &n);
 int arr[n];
 printf("Enter elements of an array : ");
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr[i]);
 }
 printf("Elements of an array are ");
 for(int i = 0; i < n; i++)
 {
  printf("%d ", arr[i]);
 }
}
```

## 25. Program to find the sum of elements in an array using a while loop?
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter the size of array : ");
 scanf("%d", &n);
 int arr[n];
 printf("Enter elements of an array : ");
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr[i]);
 }
 int i = 0, sum = 0;
 while(i < n)
 {
  sum+=arr[i];
  i++;
 }
 printf("Sum of elements in an array : %d", sum);
}
```

## 26. Program to count the number of vowels in a given string using for loop?
```c
#include<stdio.h>
#include<ctype.h>
int main()
{
 char str[10];
 printf("Enter a string : ");
 scanf("%s", str);
 int count = 0;
 for(int i = 0; str[i] != '\0'; i++)
 {
  char ch = tolower(str[i]); 
  if(ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u')
   count++;
  }
  printf("Number of vowels in %s are %d", str, count);
}
```

## 27. Program to count the number of words in a given string using a while loop?
```c
#include<stdio.h>
int main()
{
 char str[200];
 printf("Enter a string : ");
 fgets(str, sizeof(str), stdin);
 int i = 0, count = 0;
 while(str[i] != '\0')
 {
  if(str[i] == ' ' || str[i] == '\n' || str[i] == '\t')
   count++;
  i++;
 }
 printf("Number of words in string : %d", count);
}
```

## 28. Program to check whether a given string is a palindrome or not using a for loop?
```c
#include<stdio.h>
#include<string.h>
int main()
{
 char str[20];
 printf("Enter a string : ");
 scanf("%s", str);
 int len = strlen(str);
 if(str[len - 1] == '\n')
  str[len - 1] = '\0';
 len = strlen(str);
 int flag = 1;
 for(int i = 0; str[i] != '\0'; i++)
 { 
  for(int j = len - 1 - i; j > 0; j--)
  {
   if(str[i] != str[j])
    flag = 0;
    break;
  }
 }
 if(flag)
  printf("String is a Palindrome");
 else
  printf("String is not a Palindrome");
}
```

## 29. program to concatenate two strings without using library functions using a while loop?
```c
#include<stdio.h>
int main()
{
 char str1[10];
 char str2[10];
 printf("Enter two strings : ");
 scanf("%s %s", str1, str2);
 char str[25];
 int i = 0, j = 0;
 while(str1[i] != '\0')
 {
  if(str1[i] == '\n')
  {
   str1[i] = '\0';
   break;
  }
  i++;
 }
 i = 0;
 while(str1[i] != '\0')
 {
  i++;
 }
 while(str2[j] != '\0' && str2[j] != '\n')
 { 
  str1[i] = str2[j];
  i++;
  j++;
 }
 str1[i] = '\0';
 printf("Concatinated String : %s", str1);
}
```

## 30. Program to find the length of a string using a for loop?
```c
#include<stdio.h>
int main()
{
 char str[20];
 printf("Enter a string : ");
 scanf("%s", str);
 int count = 0;
 for(int i = 0; str[i] != '\0'; i++)
 {
  count++;
 }
 printf("Length of string %s : %d", str, count);
}
```

## 31. Program to convert a string to uppercase using a while loop?
```c
#include<stdio.h>
int main()
{
 char str[10];
 printf("Enter a string : ");
 scanf("%s", str);
 int i = 0;
 while(str[i] != '\0')
 {
  if(str[i] >= 'a' && str[i] <= 'z')
   str[i] = str[i] - 32;
  i++;
 }
 printf("Uppercase string : %s", str);
}
```

## 32. Program to find the power a number using a for loop?
```c
#include<stdio.h>
int main()
{
 int base, exponent;
 printf("Enter base : ");
 scanf("%d", &base);
 printf("Enter Exponent : ");
 scanf("%d", &exponent);
 long res = 1;
 for(int i = 1; i <= exponent; i++)
 {
  res *= base;
 }
 printf("%d to the power %d : %ld", base, exponent, res);
}
```

## 33. Program to find the factorial of a number using a while loop?
```c
#include<stdio.h>
int main()
{
 int num;
 printf("Enter a number : ");
 scanf("%d", &num);
 int i = num;
 unsigned long long fact = 1;
 while(i > 0)
 {
  fact *= i;
  i--;
 }
 printf("Factorial : %llu", fact);
}
```

## 34. Program to find the gcd of two numbers using a while loop?
```c
#include<stdio.h>
int main()
{
 int num1, num2, gcd;
 printf("Enter two numbers : ");
 scanf("%d %d", &num1, &num2);
 int x = num1, y = num2;
 while(y != 0)
 {
  int temp = y;
  y = x % y;
  x = temp;
 }
 gcd = x;
 printf("GCD of %d and %d is %d", num1, num2, gcd);
}
```

## 35. Program to find the lcm of two numbers using for loop?
```c
#include<stdio.h>
int main()
{
 int num1, num2, lcm;
 printf("Enter two numbers : ");
 scanf("%d %d", &num1, &num2);
 int temp;
 if(num1 > num2)
  temp = num1;
 else
  temp = num2;
 for(lcm = temp; ; lcm++)
 {
  if(lcm % num1 == 0 && lcm % num2 == 0)
  {
   printf("LCM of %d and %d is %d", num1, num2, lcm);
   break;
  }
 }
}
```

## 36. Program to print the multiplication table of a given number using a for loop?
```c
#include<stdio.h>
int main()
{
 int num;
 printf("Enter a number : ");
 scanf("%d", &num);
 for(int i = 1; i <= 10; i++)
 {
  printf("%d x %d : %d\n", num, i, num * i);
 }
}
```
