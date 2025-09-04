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

## 6. Program to print all unique elements in an array
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter number of elemets : ");
 scanf("%d", &n);
 int arr[n];
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr[i]);
 }
 printf("Unique elements : ");
 for(int i = 0; i < n; i++)
 {
  int unique = 1;
  for(int j = 0; j < n; j++)
  {
   if(i != j && arr[i] == arr[j])
   {
    unique = 0;
    break;
   }
  }
  if(unique)
   printf("%d ", arr[i]);
 }
}
```

## 7. Program to merge two arrays of the same size sorted in descending order
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter size of each array : ");
 scanf("%d", &n);
 int arr1[n];
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr1[i]);
 }
 int arr2[n];
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr2[i]);
 }
 int merged[2 * n];
 for(int i = 0 ; i < n ;i++)
 {
  merged[i] = arr1[i];
 }
 for(int i = 0; i < n; i++)
 {
  merged[n + i] = arr2[i];
 }
 for(int i = 0; i < 2 * n - 1; i++)
 {
  for(int j = 0; j < 2 * n - 1 - i; j++)
  {
   if(merged[j] < merged[j + 1])
   {
    int temp = merged[j];
    merged[j] = merged[j + 1];
    merged[j + 1] = temp;
   }
  }
 }
 printf("Merged array in descending order : ");
 for(int i = 0; i < 2 * n; i++)
 {
  printf("%d ", merged[i]);
 }
}
```

## 8. Program to count the frequency of each element of an array
```c
#include<stdio.h
int main()
{
 int n;
 printf("Enter size of array : ");
 scanf("%d", &n);
 int arr[n];
 printf("Enter elements : ");
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr[i]);
 }
 
 printf("Element : Frequency\n");
 for(int i = 0; i < n; i++)
 {
  int isvisited = 0;
  for(int k = i; k > 0; k--)
  {
   if(arr[i] == arr[k - 1])
   {
    isvisited = 1;
    break;
   }  
  }
  if(isvisited)
   continue;
  int count = 0;
  for(int j = 0; j < n; j++)
  {
   if(arr[i] == arr[j])
    count++;
  }
  printf("%d : %d\n", arr[i], count);
 }
}
```

## 9. Program to find the maximum and minimum elements in an array
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter number of elements : ");
 scanf("%d", &n);
 int arr[n];
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr[i]);
 }
 int min = arr[0], max = arr[0];
 for(int  i = 0; i < n ; i++)
 {
  if(arr[i] < min)
   min = arr[i];
  if(arr[i] > max)
   max= arr[i];
 }
 printf("Minimun : %d\nMaximum : %d", min, max);
}
```

## 10. Program to seperate odd and even integers into separate arrays
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter number of elements : ");
 scanf("%d", &n);
 int arr[n];
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr[i]);
 }
 int even[n], odd[n];
 int evencount = 0, oddcount = 0;
 for(int i = 0; i < n; i++)
 {
  if(arr[i] % 2 == 0)
   even[evencount++] = arr[i];
  else
   odd[oddcount++] = arr[i];
 }
 printf("Even elements : ");
 for(int i = 0; i < evencount; i++)
 {
  printf("%d ", even[i]);
 }
 printf("\nOdd elements : ");
 for(int i = 0; i < oddcount; i++)
 {
  printf("%d ", odd[i]);
 }
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
