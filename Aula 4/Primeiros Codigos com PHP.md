Ao começar a aprender PHP, é útil começar com alguns comandos básicos que ajudam a familiarizar-se com a linguagem e suas funcionalidades principais. Abaixo estão alguns dos comandos iniciais mais comuns que você pode explorar:

### 1. Comentários

Os comentários são úteis para documentar seu código e são ignorados durante a execução.

```php
// Este é um comentário de uma linha

/*
   Este é um comentário de várias linhas
   Ideal para documentar seções de código
*/
```

### 2. Variáveis

As variáveis são usadas para armazenar dados. PHP é fracamente tipado, então você não precisa declarar explicitamente o tipo da variável.

```php
$nome = "João"; // Variável do tipo string
$idade = 30;     // Variável do tipo inteiro
$altura = 1.75;  // Variável do tipo float
$temFilhos = false; // Variável do tipo boolean
```

### 3. Saída de Dados

Para imprimir conteúdo na tela ou retornar dados de uma função, você pode usar `echo` ou `print`.

```php
echo "Olá, Mundo!"; // Imprime na tela
```

### 4. Operadores Aritméticos

PHP suporta os operadores aritméticos básicos para realizar operações matemáticas.

```php
$a = 10;
$b = 5;

$soma = $a + $b;   // Soma
$subtracao = $a - $b; // Subtração
$multiplicacao = $a * $b; // Multiplicação
$divisao = $a / $b; // Divisão
$resto = $a % $b; // Resto da divisão
```

### 5. Estruturas de Controle: Condicional IF

O condicional `if` é usado para executar blocos de código com base em condições.

```php
$idade = 25;

if ($idade >= 18) {
    echo "Você é maior de idade.";
} else {
    echo "Você é menor de idade.";
}
```

### 6. Estruturas de Controle: Loop WHILE

O loop `while` é usado para executar repetidamente um bloco de código enquanto uma condição for verdadeira.

```php
$i = 1;

while ($i <= 5) {
    echo "Número: " . $i . "<br>";
    $i++;
}
```

### 7. Funções

As funções permitem agrupar blocos de código para reutilização em diferentes partes do programa.

```php
function calcularSoma($a, $b) {
    return $a + $b;
}

$resultado = calcularSoma(10, 20); // Chama a função e atribui o resultado a $resultado
echo "A soma é: " . $resultado;
```

### 8. Arrays

Arrays são estruturas de dados que permitem armazenar múltiplos valores em uma única variável.

```php
$cores = array("vermelho", "verde", "azul");

echo "A segunda cor é: " . $cores[1]; // Saída: verde
```

### 9. Superglobais

As superglobais são variáveis predefinidas que estão sempre disponíveis em todos os escopos.

```php
echo $_SERVER['PHP_SELF']; // Retorna o nome do arquivo do script atual
echo $_GET['nome']; // Obtém o valor do parâmetro 'nome' passado pela URL
```

### 10. Manipulação de Strings

PHP oferece uma variedade de funções para manipulação de strings, como concatenação, busca, substituição, etc.

```php
$nome = "Maria";
$sobrenome = "Silva";

$nomeCompleto = $nome . " " . $sobrenome; // Concatenação de strings

echo strlen($nomeCompleto); // Retorna o comprimento da string (número de caracteres)
```

### Conclusão

Esses são alguns dos comandos básicos iniciais que você pode explorar ao começar com PHP. À medida que você avança, pode explorar recursos mais avançados da linguagem, como funções de banco de dados, manipulação de formulários, classes e objetos, entre outros. A prática contínua e a experimentação são fundamentais para dominar eficazmente a linguagem PHP.