#include <stdio.h>

int findSmallestElement(int arr[], int size) {
    int smallest = arr[0]; // Initialize the smallest element to the first element of the array

    for (int i = 1; i < size; i++) {
        if (arr[i] < smallest) {
            smallest = arr[i]; // Update the smallest element if a smaller element is found
        }
    }

    return smallest;
}

int main() {
    int arr[] = {12, 45, 3, 67, 9, 23, 10};
    int size = sizeof(arr) / sizeof(arr[0]);

    int smallestElement = findSmallestElement(arr, size);

    printf("The smallest element in the array is: %d\n", smallestElement);

    return 0;
}
