## Program to find the missing element in an array
```c
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
```

## Program that calculates the sums of adjacent elements and print the highest sum
```C
#include<stdio.h>
int main()
{
    int n;
    printf("Enter size of array : ");
    scanf("%d", &n);
    int arr[n];
    printf("Enter array elements : ");
    for(int i = 0; i < n; i++)
    {
        scanf("%d", &arr[i]);
    }
    int sum = 0, maxsum = 0;
    for(int i = 0; i < n - 1; i++)
    {
        sum = arr[i] + arr[i + 1];
        if(sum > maxsum)
         maxsum = sum;
    }
    printf("Highest sum of adjacent elements : %d ", maxsum);
}
```

## Program that reverse an array using recursive function
```C
#include<stdio.h>
void revarr(int arr[], int start, int end)
{
    if(start >= end)
     return;
    int temp = arr[start];
    arr[start] = arr[end];
    arr[end] = temp;
    revarr(arr, start + 1, end - 1);
}
int main()
{
    int n;
    printf("Enter size of an array : ");
    scanf("%d", &n);
    int arr[n];
    printf("Enter array elements : ");
    for(int i = 0; i < n; i++)
    {
        scanf("%d", &arr[i]);
    }
    printf("Original array : ");
    for(int i = 0; i < n; i++)
    {
        printf("%d ", arr[i]);
    }
    printf("\n");
    revarr(arr, 0, n -1);
    printf("Reversed array : ");
    for(int i = 0; i < n; i++)
    {
        printf("%d ", arr[i]);
    }
}
```
