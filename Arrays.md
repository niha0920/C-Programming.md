## Arrays
## 1. Program to store elements in an array and print them
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter size of array : ");
 scanf("%d", &n);
 int arr[n];
 printf("Enter %d elements : ", n);
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr[i]);
 }
 printf("Array elements : ");
 for(int i = 0; i < n; i++)
 {
  printf("%d ", arr[i]);
 }
}
```

## 2. Program to read n number of values in an array and display them in reverse order
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter number of elements : ");
 scanf("%d", &n);
 int arr[n];
 printf("Enter %d elements : ", n);
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr[i]);
 }
 printf("Array in reverse : ");
 for(int i = n - 1; i >= 0; i--)
 {
  printf("%d ", arr[i]);
 }
}
```

## 3. Program to find the sum of all elements of the array
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter number of elements : ");
 scanf("%d", &n);
 int arr[n];
 printf("Enter %d elements : ", n);
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr[i]);
 }
 int sum = 0;
 for(int i = 0; i < n; i++)
 {
  sum += arr[i];
 }
 printf("Sum of array elements : %d", sum);
}
```

## 4. Program to copy the elements of one array into another array
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter number of elements : ");
 scanf("%d", &n);
 int arr1[n];
 printf("Enter %d elements : ", n);
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr1[i]);
 }
 int arr2[n];
 printf("Elements of arr2 : ");
 for(int i = 0; i < n; i++)
 {
  arr2[i] = arr1[i];
  printf("%d ", arr2[i]);
 }
}
```

## 5. Program to count the total number of duplicate elements in an array
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter number of elements : ");
 scanf("%d", &n);
 int arr[n];
 printf("Enter %d elements : ", n);
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr[i]);
 }
 int count = 0;
 for(int i = 0; i < n; i++)
 {
  for(int j = i + 1; j < n; j++)
  {
   if(arr[i] == arr[j])
   {
    count++;
    break;
   }
  }
 }
 printf("Total duplicate elements : %d", count);
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
