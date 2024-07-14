A criação de estruturas de dados em C é um conceito fundamental, especialmente quando se deseja organizar e manipular dados complexos. A linguagem C oferece a estrutura `struct`, que permite agrupar diferentes tipos de dados em uma única unidade.

### Exemplo: Estrutura de Dados para Representar um Aluno

Vamos criar uma estrutura para representar um aluno, incluindo informações como nome, idade, matrícula e notas.

#### Definindo a Estrutura

```c
#include <stdio.h>
#include <string.h>

// Definição da estrutura Aluno
struct Aluno {
    char nome[50];
    int idade;
    int matricula;
    float notas[5];
};

int main() {
    // Criando uma instância da estrutura Aluno
    struct Aluno aluno1;

    // Atribuindo valores aos campos da estrutura
    strcpy(aluno1.nome, "João Silva");
    aluno1.idade = 20;
    aluno1.matricula = 123456;
    aluno1.notas[0] = 8.5;
    aluno1.notas[1] = 9.0;
    aluno1.notas[2] = 7.5;
    aluno1.notas[3] = 8.0;
    aluno1.notas[4] = 9.2;

    // Imprimindo os valores dos campos
    printf("Nome: %s\n", aluno1.nome);
    printf("Idade: %d\n", aluno1.idade);
    printf("Matrícula: %d\n", aluno1.matricula);
    for (int i = 0; i < 5; i++) {
        printf("Nota %d: %.2f\n", i + 1, aluno1.notas[i]);
    }

    return 0;
}
```

#### Explicação do Código

1. **Definição da Estrutura**:
   - A estrutura `Aluno` é definida com quatro campos: `nome`, `idade`, `matricula` e `notas`.
   - `nome` é um array de caracteres (string) para armazenar o nome do aluno.
   - `idade` e `matricula` são variáveis inteiras.
   - `notas` é um array de `float` para armazenar cinco notas do aluno.

2. **Criação de uma Instância**:
   - No `main`, uma instância da estrutura `Aluno` chamada `aluno1` é criada.

3. **Atribuição de Valores**:
   - `strcpy` é usado para copiar a string "João Silva" para o campo `nome`.
   - Os campos `idade` e `matricula` recebem valores inteiros diretamente.
   - As notas são atribuídas aos elementos do array `notas`.

4. **Impressão dos Valores**:
   - `printf` é utilizado para imprimir os valores armazenados nos campos da estrutura.
   - Um loop `for` é usado para iterar sobre o array `notas` e imprimir cada nota.

#### Compilação e Execução

Para compilar e executar o programa:

```bash
gcc -o aluno aluno.c
./aluno
```

A saída será:

```
Nome: João Silva
Idade: 20
Matrícula: 123456
Nota 1: 8.50
Nota 2: 9.00
Nota 3: 7.50
Nota 4: 8.00
Nota 5: 9.20
```

### Conclusão

Este exemplo demonstra como definir e utilizar uma estrutura de dados em C. As estruturas são extremamente úteis para agrupar diferentes tipos de dados e são amplamente usadas em programação de sistemas, jogos, bancos de dados e muitas outras áreas onde a organização de dados complexos é necessária.