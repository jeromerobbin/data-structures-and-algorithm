#include <stdio.h>

void matrixMultiplication(int rows1, int cols1, int matrix1[][cols1], int rows2, int cols2, int matrix2[][cols2], int result[][cols2]) {
    for (int i = 0; i < rows1; i++) {
        for (int j = 0; j < cols2; j++) {
            result[i][j] = 0;
            for (int k = 0; k < cols1; k++) {
                result[i][j] += matrix1[i][k] * matrix2[k][j];
            }
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
    int rows1 = 3;
    int cols1 = 2;

    int rows2 = 2;
    int cols2 = 3;

    int matrix1[][2] = {{1, 2}, {3, 4}, {5, 6}};
    int matrix2[][3] = {{7, 8, 9}, {10, 11, 12}};
    int result[rows1][cols2];

    printf("Matrix 1:\n");
    displayMatrix(rows1, cols1, matrix1);

    printf("\nMatrix 2:\n");
    displayMatrix(rows2, cols2, matrix2);

    matrixMultiplication(rows1, cols1, matrix1, rows2, cols2, matrix2, result);

    printf("\nResult of Matrix Multiplication:\n");
    displayMatrix(rows1, cols2, result);

    return 0;
}
