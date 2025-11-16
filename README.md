# Nombres-premiers-
#include <stdio.h>

int main() {
    int N, i, j;
    int est_premier;

    printf("Entrez un nombre : ");
    scanf("%d", &N);

    printf("Les nombres premiers entre 1 et %d sont :\n", N);

    for(i = 2; i <= N; i++) {
        est_premier = 1; // on suppose que i est premier

        // Vérifier si i est divisible par un nombre entre 2 et i-1
        for(j = 2; j * j <= i; j++) {
            if(i % j == 0) {
                est_premier = 0; // pas premier
                break;
            }
        }

        if(est_premier == 1) {
            printf("%d ", i);
        }
    }

    return 0;
}