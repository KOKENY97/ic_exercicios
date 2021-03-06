# Arrays e apontadores

1 - Completa o código da seguinte função, cujo objectivo é fazer uma soma de
dois _arrays_, guardando o resultado no primeiro _array_. A variável `tamanho`
representa o tamanho dos _arrays_.

```c
void soma_arrays(int *array1, int *array2, int tamanho) {
    /* Inserir codigo aqui */
}
```

> [Soluções](../solucoes/11_arrays/01.md)

2 - No código seguinte as duas primeiras instruções definem três variáveis: um
_array_ e dois apontadores. As instruções seguintes representam várias
operações sobre essas variáveis. Indica quais dessas instruções são inválidas e
justifica a tua resposta.

```c
/* Variaveis */
unsigned char a[5] = {10, 20, 30, 40, 50};
int *puc;
void *pg;

/* Instrucoes a verificar: */
puc = a;
pg = a;
puc[3]++;
pg = puc;
pg[2] = 0;
puc[2] = 0;
a[5] = 60;
--puc;
pg++;
puc = pg;
a = puc;
*(puc + 2) = 31;
*(a + 3) = 41;
*(pug + 1) = 21;
```

> [Soluções](../solucoes/11_arrays/02.md)

3 - A variável `p` é um apontador para `long`, apontando inicialmente para o
endereço de memória 0x9F88. Qual o valor de `p` após a operação `p += 2`
assumindo que variáveis do tipo `long` têm 64 bits? Explica o teu raciocínio.

> [Soluções](../solucoes/11_arrays/03.md)

4 - A variável `p` é um apontador para `short`, apontando inicialmente para o
endereço de memória 0xEF02. Qual o valor de `p` após a operação `p -= 4`
assumindo que variáveis do tipo `short` têm 16 bits? Explica o teu raciocínio.

> [Soluções](../solucoes/11_arrays/04.md)

5 - Indica o que é impresso no ecrã pelo seguinte programa, explicando o que
fazem cada uma das instruções entre os comentários `START` e `END`:

```c
#include <stdio.h>
#include <stdlib.h>
#define ARRSIZE 5
int main() {

    int a[ARRSIZE] = {4, 2, 1, 5, 1};
    int b[ARRSIZE] = {-1, -2, 0, -4, -3};
    int *pa = a;
    int *pb = b;

    /* START */
    *(pa + 2) *= 2;
    pb[1] = *a * 3;
    *(a + 1) &= pb[3];
    *(b + 4) <<= *(pa + 4);
    *pa %= pa[3];
    pb++;
    pb[0] *= b[1];
    /* END */

    for (int i = 0; i < ARRSIZE; i++) {
        printf("%d %d\n", a[i], b[i]);
    }

    return 0;
}
```

> [Soluções](../solucoes/11_arrays/05.md)

6 - Completa o código da seguinte função, cujo objectivo é fazer uma soma de
prefixos de um array, isto é, cada elemento do array passa a ser igual a ele
próprio mais o anterior. Por exemplo, o array |2|3|1|0|4| seria transformado em
`|2|5|6|6|10|`. A variável tamanho representa o tamanho do array.

```c
void somaprefixos(int *array, int tamanho) {
    /* Inserir codigo aqui */
}
```

> [Soluções](../solucoes/11_arrays/06.md)

7 - Escreve um programa em C que peça ao utilizador para preencher um array
bidimensional de inteiros com dimensões 3x2, e depois solicite as coordenadas
de um dos elementos do array e o imprima no ecrã. Se as coordenadas inseridas
estiverem fora dos limites do array, o programa deve terminar com uma mensagem
de erro.

> [Soluções](../solucoes/11_arrays/07.md)

8 - Escreve as instruções C que fazem o seguinte:

1. Declara um apontador para inteiro e inicializa-o a `NULL`.
2. Declara um apontador para apontador para inteiro e inicializa-o com o
   endereço de memória do apontador declarado na instrução anterior.
3. Declara uma variável do tipo _double_.
4. Declara um apontador constante para _double_ e inicializa-o com o endereço
   de memória da variável do tipo _double_ declarada na instrução anterior.

Pergunta: é possível modificar o valor referenciado (apontado) pelo apontador
constante declarado na alínea 4?

> [Soluções](../solucoes/11_arrays/08.md)

9 - Transforma o seguinte código de modo a que apenas use notação de arrays e
manipulação de índices:

```c
short as[10] = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9};
short *ps = &as[0];
while (ps <= &as[9]) {
    printf("ps aponta para %d\n", *ps);
    ++ps;
}
```

> [Soluções](../solucoes/11_arrays/09.md)

10 - Escreve um programa em C que converte os argumentos passados na linha de
comandos em _doubles_, obtém a respetiva média, e mostra-a no ecrã.

> [Soluções](../solucoes/11_arrays/10.md)
