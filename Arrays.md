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

## 11. Program to sort elements of an array in ascending order
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
 for(int i = 0; i < n - 1; i++)
 {
  for(int j = i + 1; j < n; j++)
  {
   if(arr[i] > arr[j])
   {
    int temp = arr[i];
    arr[i] = arr[j];
    arr[j] = temp;
   }
  }
 }
 printf("Array in ascending order : ");
 for(int i = 0; i < n; i++)
 {
  printf("%d ", arr[i]);
 }
}

```

## 12. Program to sort the elements of the array in descending order
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
 for(int i = 0; i < n - 1; i++)
 {
  for(int j = i + 1; j < n; j++)
  {
   if(arr[i] < arr[j])
   {
    int temp = arr[i];
    arr[i] = arr[j];
    arr[j] = temp;
   }
  }
 }
 printf("Array in descending order : ");
 for(int i = 0; i < n; i++)
 {
  printf("%d ", arr[i]);
 }
}
```

## 13. Program to delete an element at a desired position from an array
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
 int position;
 printf("Enter position to delete : ");
 scanf("%d", &position);
 printf("Array after deletion : ");
 for(int i = 0; i < n; i++)
 {
  if(i != position)
   printf("%d ", arr[i]);
 }
}
```

## 14. Program to find the second largest element in an array
```c
#include<stdio.h>
#include<limits.h>
int main()
{
 int n;
 printf("Enter size of array : ");
 scanf("%d", &n);
 if(n < 2)
 {
  printf("No second largest element");
  return 1;
 }
 int arr[n];
 printf("Enter %d elements : ", n);
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr[i]);
 }
 int max1 = INT_MIN, max2 = INT_MIN;
 if(n > 2)
 {
  for(int i = 0; i < n; i++)
  {
   if(arr[i] > max1)
   {
     max2 = max1;
     max1 = arr[i];
   } 
   else if(arr[i] > max2 && arr[i] != max1)
    max2 = arr[i];
  }
 }
 if(max2 != INT_MIN)
  printf("Second largest element : %d", max2);
 else
  printf("No second largest element");
}
```

## 15. Program to find the second smallest element in an array
```c
#include<stdio.h>
#include<limits.h>
int main()
{
 int n;
 printf("Enter size of array : ");
 scanf("%d", &n);
 if(n < 2)
 {
  printf("No second largest element");
  return 1;
 }
 int arr[n];
 printf("Enter %d elements : ", n);
 for(int i = 0; i < n; i++)
 {
  scanf("%d", &arr[i]);
 }
 int min1 = INT_MAX, min2 = INT_MAX;
 if(n > 2)
 {
  for(int i = 0; i < n; i++)
  {
   if(arr[i] < min1)
   {
     min2 = min1;
     min1 = arr[i];
   } 
   else if(arr[i] < min2 && arr[i] != min1)
    min2 = arr[i];
  }
 }
 if(min2 != INT_MAX)
  printf("Second smallest element : %d", min2);
 else
  printf("No second smallest element");
}
```

## 16. Program for a 2D array of size 3x3 and print the matrix
```c
#include<stdio.h>
int main()
{
 int mat[3][3];
 printf("Enter elements of 3x3 matrix : ");
 for(int i = 0; i < 3; i++)
 {
  for(int j = 0; j < 3; j++)
  {
   scanf("%d", &mat[i][j]);
  }
 }
 printf("Matrix : ");
 for(int i = 0; i < 3; i++)
 {
  for(int j = 0; j < 3; j++)
  {
   printf("%d ", mat[i][j]);
  }
  printf("\n");
 }
}
```

## 17. Program for adding two matrices of the same size
```c
#include<stdio.h>
int main()
{
 int n, m;
 printf("Enter rows and columns : ");
 scanf("%d %d", &n, &m);
 int mat[n][m], mat1[n][m], mat2[n][m];
 printf("Enter elements of first matrix : ");
 for(int i = 0; i < n; i++)
 {
  for(int j = 0; j < m; j++)
  {
   scanf("%d", &mat1[i][j]);
  }
 }
 printf("Enter elements of second matrix : ");
 for(int i = 0; i < n; i++)
 {
  for(int j = 0; j < m; j++)
  {
   scanf("%d", &mat2[i][j]);
  }
 }
 printf("Sum of matrices : ");
 for(int i = 0; i < n; i++)
 {
  for(int j = 0; j < m; j++)
  {
   mat[i][j] = mat1[i][j] + mat2[i][j];
   printf("%d ", mat[i][j]);
  }
  printf("\n");
 }
}
```

## 18. Program for the subtraction of two matrices
```c
#include<stdio.h>
int main()
{
 int n, m;
 printf("Enter rows and columns : ");
 scanf("%d %d", &n, &m);
 int mat[n][m], mat1[n][m], mat2[n][m];
 printf("Enter elements of first matrix : ");
 for(int i = 0; i < n; i++)
 {
  for(int j = 0; j < m; j++)
  {
   scanf("%d", &mat1[i][j]);
  }
 }
 printf("Enter elements of second matrix : ");
 for(int i = 0; i < n; i++)
 {
  for(int j = 0; j < m; j++)
  {
   scanf("%d", &mat2[i][j]);
  }
 }
 printf("Difference of matrices : ");
 for(int i = 0; i < n; i++)
 {
  for(int j = 0; j < m; j++)
  {
   mat[i][j] = mat1[i][j] - mat2[i][j];
   printf("%d ", mat[i][j]);
  }
  printf("\n");
 }
}
```

## 19. Program for the multiplication of two square matrices
```c
#include<stdio.h>
int main()
{
 int r1, c1;
 printf("Enter rows and columns of first matrix : ");
 scanf("%d %d", &r1, &c1);
 int r2, c2;
 printf("Enter rows and columns of second matrix : ");
 scanf("%d %d", &r2, &c2);
 if(c1 != r2)
 {
  printf("Matrix multiplication not possible");
  return 1;
 }
 int mat1[r1][c1];
 printf("Enter first matrix : ");
 for(int i = 0; i < r1; i++)
 {
  for(int j = 0; j < c1; j++)
  {
   scanf("%d", &mat1[i][j]);
  }
 }
 int mat2[r2][c2];
 printf("Enter second matrix : ");
 for(int i = 0; i < r2; i++)
 {
  for(int j = 0; j < c2; j++)
  {
   scanf("%d", &mat2[i][j]);
  }
 }
 int mat[r1][c2];
 for(int i = 0; i < r1; i++)
 {
  for(int j = 0; j < c2; j++)
  {
   mat[i][j] = 0;
  }
 }
 for(int i = 0; i < r1; i++)
 {
  for(int j = 0; j < c2; j++)
  {
   for(int k = 0; k < c1; k++)
   {
    mat[i][j] += mat1[i][k] * mat2[k][j];
   }
  }
 }
 printf("Product of matrices : ");
 for(int i = 0; i < r1; i++)
 {
  for(int j = 0; j < c2; j++)
  {
   printf("%d ", mat[i][j]);
  }
  printf("\n");
 }
}
```

## 20. Program to find the transpose of a given matrix
```c
#include<stdio.h>
int main()
{
 int n, m;
 printf("Enter rows and columns : ");
 scanf("%d %d", &n, &m);
 int mat[n][m];
 printf("Enter elements of matrix : ");
 for(int i = 0; i < n; i++)
 {
  for(int j = 0; j < m; j++)
  {
   scanf("%d", &mat[i][j]);
  }
 } 
 printf("Transpose : ");
 for(int i = 0; i < m; i++)
 {
  for(int j = 0; j < n; j++)
  {
   printf("%d ", mat[j][i]);
  }
  printf("\n");
 }
}
```

## 21. Program to find the sum of the right diagonals of a matrix
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter size of square matrix : ");
 scanf("%d", &n);
 int mat[n][n];
 printf("Enter elements : ");
 for(int i = 0; i < n; i++)
 {
  for(int j = 0; j < n; j++)
  {
   scanf("%d", &mat[i][j]);
  }
 }
 int sum = 0;
 for(int i = 0; i < n; i++)
 {
  for(int j = n - i - 1; j>= 0; j--)
  {
    sum += mat[i][j];
    break;
  }
 }
 printf("Sum of right diagonal : %d", sum);
}
```

## 22. Program to find the sum of the left diagonals of a matrix
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter size of square matrix : ");
 scanf("%d", &n);
 int mat[n][n];
 printf("Enter elements : ");
 for(int i = 0; i < n; i++)
 {
  for(int j = 0; j < n; j++)
  {
   scanf("%d", &mat[i][j]);
  }
 }
 int sum = 0;
 for(int i = 0; i < n; i++)
 {
  for(int j = 0; j < n; j++)
  {
   if( i == j)
    sum += mat[i][j];
  }
 }
 printf("Sum of left diagonal : %d", sum);
}
```

## 23. Program to find the sum of rows and columns of a matrix
```c
#include<stdio.h>
int main()
{
 int n, m;
 printf("Enter rows and columns : ");
 scanf("%d %d", &n, &m);
 int mat[n][m];
 printf("Enter elements : ");
 for(int i = 0; i < n; i++)
 {
  for(int j = 0; j < m; j++)
  {
   scanf("%d", &mat[i][j]);
  }
 }
 for(int i = 0; i < n ; i++)
 {
  int rowsum = 0;
  for(int j = 0; j < m; j++)
  {
   rowsum += mat[i][j];
  }
  printf("Sum of row %d : %d\n", i + 1, rowsum);
 }
 for(int i = 0; i < m ; i++)
 {
  int colsum = 0;
  for(int j = 0; j < n; j++)
  {
   colsum += mat[j][i];
  }
  printf("Sum of column %d : %d\n", i + 1, colsum);
 }
}
```

## 24. Program to print or display the lower triangular of a given matrix
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter size of square matrix : ");
 scanf("%d", &n);
 int mat[n][n];
 printf("Enter elements : ");
 for(int i = 0; i < n; i++)
 {
  for(int j = 0; j < n; j++)
  {
   scanf("%d", &mat[i][j]);
  }
 }
 printf("Lower triangular matrix : \n");
 for(int i = 0; i < n; i++)
 {
  for(int j = 0; j <= i; j++)
  {
   printf("%d ", mat[i][j]);
  }
  printf("\n");
 }
}
```

## 25. Program to print or display an upper triangular matrix
```c
#include<stdio.h>
int main()
{
 int n;
 printf("Enter size of square matrix : ");
 scanf("%d", &n);
 int mat[n][n];
 printf("Enter elements : ");
 for(int i = 0; i < n; i++)
 {
  for(int j = 0; j < n; j++)
  {
   scanf("%d", &mat[i][j]);
  }
 }
 printf("Upper triangular matrix : \n");
 for(int i = 0; i < n; i++)
 {
  for(int j = 0; j < n ; j++)
  {
   if(i <= j)
    printf("%d ", mat[i][j]);
   else
    printf("0 ");
  }
  printf("\n");
 }
}
```

## 26. Program to calculate the determinant of a 3 x 3 matrix
```c
#include<stdio.h>
int main()
{
 int mat[3][3];
 printf("Enter elements : ");
 for(int i = 0; i < 3; i++)
 {
  for(int j = 0; j < 3; j++)
  {
   scanf("%d", &mat[i][j]);
  }
 }
 int det = mat[0][0] * (mat[1][1] * mat[2][2] - mat[1][2] * mat[2][1]) - mat[0][1] * (mat[1][0] * mat[2][2] - mat[1][2] * mat[2][0]) + mat[0][2] * (mat[1][0] * mat[2][1] - mat[1][1] * mat[2][0]);
 printf("%d", det);
}
```

## 27. 
```c

```

## 28. 
```c

```

## 29. 
```c

```

## 30. 
```c

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
