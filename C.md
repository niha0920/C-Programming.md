## 1. Program to find the ceiling and floor of the numbers 0 to 10 and check the floor and ceiling are part of the sorted array [1, 3, 5, 7, 9]. If the floor or ceiling is found in the array, use that.If not found but within the range (0 to 10), return the number itself and If not found and not in range (0-10), return null
```c
#include <stdio.h>
#define SIZE 5
#define RANGE_MIN 0
#define RANGE_MAX 10
int findFloor(int arr[], int size, int num) {
    int res = -1;
    for (int i = 0; i < size; i++) {
        if (arr[i] <= num) {
            res = arr[i];
        } else {
            break;
        }
    }
    return res;
}
int findCeiling(int arr[], int size, int num) {
    for (int i = 0; i < size; i++) {
        if (arr[i] >= num) {
            return arr[i];
        }
    }
    return -1;
}
int isarray(int arr[], int size, int num) {
    for (int i = 0; i < size; i++) {
        if (arr[i] == num) {
            return 1;
        }
    }
    return 0;
}
int main() {
    int array[SIZE] = {1, 3, 5, 7, 9};
    for (int num = 0; num <= 10; num++) {
        int floor = findFloor(array, SIZE, num);
        int ceiling = findCeiling(array, SIZE, num);
        if (!isarray(array, SIZE, floor)) {
            if (floor >= RANGE_MIN && floor <= RANGE_MAX)
                floor = num; 
            else
                floor = -1;
        }
        if (!isarray(array, SIZE, ceiling)) {
            if (ceiling >= RANGE_MIN && ceiling <= RANGE_MAX)
                ceiling = num;
            else
                ceiling = 11;
        }
        printf("%d, %s, %s\n",
               num,
               floor == -1 ? "null" : (char[4]){floor+ '0'},
               ceiling == 11 ? "null" : (char[4]){ceiling+ '0'}
        );
    }
    return 0;
}
```

## Program that interleaves words from two files (file1.txt and file2.txt) and writes the output to a third file (file3.txt) 
```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
int main() {
    FILE *f1, *f2, *f3;
    char w1[100], w2[100];
    f1 = fopen("file_1.txt", "r");
    f2 = fopen("file_2.txt", "r");
    f3 = fopen("file_3.txt", "w");
    if (f1 == NULL || f2 == NULL || f3 == NULL) {
        printf("Error opening files.");
        return 1;
    }
    int r1, r2;
    while (1) {
        r1 = fscanf(f1, "%s", w1);
        r2 = fscanf(f2, "%s", w2);
        if (r1 == EOF && r2 == EOF)
            break;
        if (r1 != EOF)
            fprintf(f3, "%s ", w1);
        if (r2 != EOF)
            fprintf(f3, "%s ", w2);
    }
    fclose(f1);
    fclose(f2);
    fclose(f3);
    printf("file_3.txt.");
    return 0;
}
```
