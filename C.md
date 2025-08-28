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
