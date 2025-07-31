## program to count the number of substrings and print them
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
    char str[20] = "string2025";
    int sum = 0;
    for(int i = 0; str[i] != '\0'; i++)
    {
        if(isdigit(str[i]))
         sum += str[i] - '0';
    }
    printf("Sum of numerics in a string is %d", sum);
}
```
