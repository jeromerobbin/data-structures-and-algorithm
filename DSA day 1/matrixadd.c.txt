#include <stdio.h>

void matrixAddition(int rows, int cols, int matrix1[][cols], int matrix2[][cols], int result[][cols]) {
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            result[i][j] = matrix1[i][j] + matrix2[i][j];
        }
    }
}

void displayMatrix(int rows, int cols, int matrix[][cols]) {
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            printf("%d\t", matrix[i][j]);
        }
        printf("\n");
    }
}

int main() {
    int rows = 3;
    int cols = 3;

    int matrix1[][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
    int matrix2[][3] = {{9, 8, 7}, {6, 5, 4}, {3, 2, 1}};
    int result[rows][cols];

    printf("Matrix 1:\n");
    displayMatrix(rows, cols, matrix1);

    printf("\nMatrix 2:\n");
    displayMatrix(rows, cols, matrix2);

    matrixAddition(rows, cols, matrix1, matrix2, result);

    printf("\nResult of Matrix Addition:\n");
    displayMatrix(rows, cols, result);

    return 0;
}
