#include <stdio.h>

int findSumOfElements(int arr[], int size) {
    int sum = 0;

    for (int i = 0; i < size; i++) {
        sum += arr[i];
    }

    return sum;
}

int main() {
    int arr[] = {10, 20, 30, 40, 50};
    int size = sizeof(arr) / sizeof(arr[0]);

    int sumOfElements = findSumOfElements(arr, size);

    printf("The sum of elements in the array is: %d\n", sumOfElements);

    return 0;
}
