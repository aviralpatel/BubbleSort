# Bubble Sort in C

This repository contains an implementation of the Bubble Sort algorithm in C. Bubble Sort is a simple sorting algorithm that repeatedly steps through the list, compares adjacent elements and swaps them if they are in the wrong order. The algorithm continues iterating through the list until no swaps are needed, which indicates that the list is sorted.

## Getting Started

To use the Bubble Sort implementation in your project, copy and paste the code below into a new C file.

```c
#include <stdio.h>

void bubble_sort(int arr[], int n) {
    int i, j, temp;
    for (i = 0; i < n - 1; i++) {
        for (j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}

void print_array(int arr[], int size) {
    int i;
    for (i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");
}

int main() {
    int arr[] = {64, 34, 25, 12, 22, 11, 90};
    int n = sizeof(arr) / sizeof(arr[0]);
    
    printf("Original array:\n");
    print_array(arr, n);

    bubble_sort(arr, n);

    printf("Sorted array:\n");
    print_array(arr, n);
    
    return 0;
}
```
## Sample Usage and Output

```c
int main() {
    int arr[] = {64, 34, 25, 12, 22, 11, 90};
    int n = sizeof(arr) / sizeof(arr[0]);

    printf("Original array:\n");
    print_array(arr, n);

    bubble_sort(arr, n);

    printf("Sorted array:\n");
    print_array(arr, n);

    return 0;
}
```
When you run the program with the sample usage above, the output should look like

```c
Original array:
64 34 25 12 22 11 90
Sorted array:
11 12 22 25 34 64 90
```

