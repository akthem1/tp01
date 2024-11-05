#include <stdio.h>

int main() {
    char matrix[5][5] = {
        {'1', '2', '3', '4', '5'},
        {'7', 'a', 'c', '8', 'd'},
        {'c', '9', '4', 'z', '8'},
        {'5', '6', 'p', 'n', '3'},
        {'2', '9', 't', 'm', 'k'}
    };
    printf("Affichage complet:\n");
    for (int i = 0; i < 5; i++) {
        for (int j = 0; j < 5; j++) {
            printf("%c ", matrix[i][j]);
        }
        printf("\n");
    }
    printf("indice pair:\n");
    for (int i = 0; i < 5; i += 2) { 
        for (int j = 0; j < 5; j++) {
            printf("%c ", matrix[i][j]);
        }
        printf("\n");
    }
    printf("indice impair:\n");
    for (int i = 0; i < 5; i++) {
        for (int j = 1; j < 5; j += 2) { 
            printf("%c ", matrix[i][j]);
        }
        printf("\n");
    }
    printf("Premiere diagonale :\n");
    for (int i = 0; i < 5; i++) {
        printf("%c ", matrix[i][i]);
    }
    printf("\n");
    
    printf("Deuxieme diagonale:\n");
    for (int i = 0; i < 5; i++) {
        printf("%c ", matrix[i][4 - i]);
    }
    printf("\n");

    return 0;
}



---------------------------------------------------
---------------------------------------------------
#include <stdio.h>

int main() {
    int matrix[4][4] = {
        {1, 2, 3, 4},
        {5, 6, 7, 8},
        {9, 10, 11, 12},
        {13, 14, 15, 16}
    };
    printf("Matrice :\n");
    for (int i = 0; i < 4; i++) {
        for (int j = 0; j < 4; j++) {
            printf("%d\t", matrix[i][j]);
        }
        printf("\n");
    }
    // نبديل المثلثين
    for (int i = 0; i < 4; i++) {
        for (int j = 0; j < i; j++) { 
            // تبديل العناصر
            int a = matrix[i][j];
            matrix[i][j] = matrix[j][i];
            matrix[j][i] = a ;
        }
    }
    printf("Matrice:\n");
    for (int i = 0; i < 4; i++) {
        for (int j = 0; j < 4; j++) {
            printf("%d\t", matrix[i][j]);
        }
        printf("\n");
    }
    

    return 0;
}