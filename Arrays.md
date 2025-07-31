## Program to find the missing element in an array
'''C
#include<stdio.h>
int main()
{
    int n;
    printf("Enter the size of array : ");
    scanf("%d", &n);
    int arr[n];
    printf("Enter the elements of an array : ");
    for(int i = 0; i < n; i++)
    {
        scanf("%d", &arr[i]);
    }
    int m = n + 1;
    int sumofn = (m * (m + 1)) / 2;
    int sum = 0;
    for(int i = 0; i < n; i++)
    {
        sum += arr[i];
    }
    printf("Missing number is %d", sumofn - sum);
}
'''
