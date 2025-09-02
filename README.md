#include <stdio.h>

/*
  Desafio Super Trunfo — Movimentação (Nível Novato)
  ---------------------------------------------------
  Movimentos:
    - Bispo:  P_Bispo casas na diagonal superior direita (Cima + Direita)
    - Torre:  P_Torre casas para a Direita
    - Rainha: P_Rainha casas para a Esquerda

  Estruturas usadas:
    - Bispo  -> for
    - Torre  -> while
    - Rainha -> do...while
*/

int main(void) {
    // Constantes (quantidade de casas que cada peça vai andar)
    int P_Bispo  = 5;  // diagonal superior direita
    int P_Torre  = 5;  // direita
    int P_Rainha = 8;  // esquerda

    printf("=== Super Trunfo - Movimentacao (Nivel Novato) ===\n\n");

    /* ================================
       1) BISPO — usando for
       Cada passo diagonal = Cima + Direita
    ================================= */
    printf("[Bispo] %d casas na diagonal superior direita (Cima + Direita)\n", P_Bispo);
    for (int i = 1; i <= P_Bispo; i++) {
        printf("Cima\n");
        printf("Direita\n");
    }
    printf("(Total de casas diagonais executadas: %d)\n\n", P_Bispo);

    /* ================================
       2) TORRE — usando while
       Movendo para a direita
    ================================= */
    printf("[Torre] %d casas para a direita\n", P_Torre);
    int contador_torre = 0;
    while (contador_torre < P_Torre) {
        printf("Direita\n");
        contador_torre++;
    }
    printf("(Total de casas executadas: %d)\n\n", contador_torre);

    /* ================================
       3) RAINHA — usando do...while
       Movendo para a esquerda
    ================================= */
    printf("[Rainha] %d casas para a esquerda\n", P_Rainha);
    int contador_rainha = 0;
    if (P_Rainha > 0) {
        do {
            printf("Esquerda\n");
            contador_rainha++;
        } while (contador_rainha < P_Rainha);
    }
    printf("(Total de casas executadas: %d)\n\n", contador_rainha);

    /* ================================
       4) Resumo final
    ================================= */
    printf("=== Resumo de Execucao ===\n");
    printf("Bispo : %d casas diagonais (cada uma = Cima + Direita)\n", P_Bispo);
    printf("Torre : %d casas para a Direita\n", P_Torre);
    printf("Rainha: %d casas para a Esquerda\n", P_Rainha);
    printf("=================================\n");

    return 0;
}
