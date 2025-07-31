## program to count the number of substrings and print them
```
c
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
