#include <stdio.h>

// Function to delete an element at a specific position in the array
void deleteElement(int arr[], int size, int position) {
    if (position < 0 || position >= size) {
        printf("Invalid position to delete.\n");
        return;
    }

    // Shift elements to the left to fill the gap
    for (int i = position; i < size - 1; i++) {
        arr[i] = arr[i + 1];
    }

    // Reduce the size of the array
    size--;

    printf("Element at position %d deleted successfully.\n", position);
}

int main() {
    int arr[] = {10, 20, 30, 40, 50};
    int size = sizeof(arr) / sizeof(arr[0]);

    int positionToDelete = 2; // Delete element at position 2 (30)

    printf("Original array: ");
    for (int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    deleteElement(arr, size, positionToDelete);

    printf("Array after deletion: ");
    for (int i = 0; i < size; i++) {
        printf("%d ", arr[i]);
    }
    printf("\n");

    return 0;
}
