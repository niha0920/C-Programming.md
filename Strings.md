## program that count the number of substrings and print them
```C
#include<stdio.h>
#include<string.h>
int main()
{
    char str[5];
    printf("Enter the string : ");
    scanf("%s", str);
    int i = 0, len = 0;
    while(str[i] != '\0')   // without using strlen()
    {
        len++;
        i++;
    }
    //int len = strlen(arr);   //with using strlen()
    int sub = (len * (len + 1)) / 2;
    printf("Number of substrings possible : %d\n", sub);
    printf("Substrings : ");
    for(int i = 0; i < len; i++)
    {
        for(int j = i; j < len; j++)
        {
            for(int k = i; k <= j ; k++)
            {
                printf("%c", str[k]);
            }
            printf("\n");
        }
    }
}
```

## Program that calculates sum of numerics in a string
```C
#include<stdio.h>
#include<ctype.h>
int main()
{
    char str[20];
    printf("Enter the string : ");
    scanf("%s", str);
    int sum = 0;
    for(int i = 0; str[i] != '\0'; i++)
    {
        if(isdigit(str[i]))
         sum += str[i] - '0';
    }
    printf("Sum of numerics in a string is %d", sum);
}
```

## program that count the number of vowels in a string
```C
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
    printf("Number of vowels in string are %d", count);
}
```

## Program that check if the second string is present anywhere within the first string (i.e., as a substring)
```C
#include<stdio.h>
#include<string.h>
int main()
{
 char str1[100];
 printf("Enter 1st string : ");
 fgets(str1, sizeof(str1), stdin);
 str1[strcspn(str1, "\n")] = '\0';
 char str2[100];
 printf("Enter 2nd string : ");
 fgets(str2, sizeof(str2), stdin);
 str2[strcspn(str2, "\n")] = '\0';
 /*
 if((strstr(str1, str2) != NULL))
  printf("%s is present in %s", str2, str1);
 else
  printf("%s is not present in %s", str2, str1);
  */
 int l1 = strlen(str1);
 int l2 = strlen(str2);
 int f = 0, j;
 for(int i = 0; i <= l1 - l2; i++)
 {
  for(j = 0; j < l2; j++)
  {
   if(str1[i + j] != str2[j])
   {
    break;
   } 
  }
  if(j == l2)
  {
   f = 1;
   break;
  } 
 }
 if(f)
  printf("%s is present in %s", str2, str1);
 else
  printf("%s is not present in %s", str2, str1);
}
```
