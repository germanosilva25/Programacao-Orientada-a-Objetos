Aqui estão 10 exemplos de funções básicas em PHP, cobrindo uma variedade de operações comuns:

### 1. **Função para Imprimir uma Mensagem**

```php
<?php
function imprimirMensagem($mensagem) {
    echo $mensagem;
}

imprimirMensagem("Olá, mundo!"); // Output: Olá, mundo!
?>
```

### 2. **Função para Somar Dois Números**

```php
<?php
function somar($a, $b) {
    return $a + $b;
}

$resultado = somar(10, 5);
echo $resultado; // Output: 15
?>
```

### 3. **Função para Verificar se um Número é Par**

```php
<?php
function ePar($numero) {
    return $numero % 2 == 0;
}

echo ePar(4) ? 'É par' : 'Não é par'; // Output: É par
?>
```

### 4. **Função para Calcular a Média de um Array**

```php
<?php
function calcularMedia($array) {
    return array_sum($array) / count($array);
}

$notas = [8, 7.5, 9, 6];
echo calcularMedia($notas); // Output: 7.875
?>
```

### 5. **Função para Converter Texto para Maiúsculas**

```php
<?php
function paraMaiusculas($texto) {
    return strtoupper($texto);
}

echo paraMaiusculas("hello world"); // Output: HELLO WORLD
?>
```

### 6. **Função para Validar um Email**

```php
<?php
function validarEmail($email) {
    return filter_var($email, FILTER_VALIDATE_EMAIL) !== false;
}

echo validarEmail("teste@exemplo.com") ? 'Email válido' : 'Email inválido'; // Output: Email válido
?>
```

### 7. **Função para Contar o Número de Caracteres em uma String**

```php
<?php
function contarCaracteres($string) {
    return strlen($string);
}

echo contarCaracteres("Olá"); // Output: 3
?>
```

### 8. **Função para Reverter uma String**

```php
<?php
function reverterString($string) {
    return strrev($string);
}

echo reverterString("PHP"); // Output: PHP
?>
```

### 9. **Função para Criar um Array de Números em um Intervalo**

```php
<?php
function criarArrayIntervalo($inicio, $fim) {
    return range($inicio, $fim);
}

print_r(criarArrayIntervalo(1, 5)); // Output: Array ( [0] => 1 [1] => 2 [2] => 3 [3] => 4 [4] => 5 )
?>
```

### 10. **Função para Encontrar o Maior Valor em um Array**

```php
<?php
function encontrarMaiorValor($array) {
    return max($array);
}

$valores = [3, 5, 7, 2, 8];
echo encontrarMaiorValor($valores); // Output: 8
?>
```

### Explicação dos Exemplos

1. **Imprimir uma Mensagem**: Mostra como criar uma função simples que exibe uma mensagem.
2. **Somar Dois Números**: Demonstra a criação de uma função que retorna a soma de dois valores.
3. **Verificar se um Número é Par**: Verifica se um número é par, usando o operador módulo.
4. **Calcular a Média**: Calcula a média dos valores em um array.
5. **Converter Texto para Maiúsculas**: Converte uma string para maiúsculas usando `strtoupper`.
6. **Validar um Email**: Usa `filter_var` para validar o formato de um e-mail.
7. **Contar Caracteres**: Conta o número de caracteres em uma string usando `strlen`.
8. **Reverter uma String**: Reverte uma string usando `strrev`.
9. **Criar um Array de Números**: Cria um array de números em um intervalo usando `range`.
10. **Encontrar o Maior Valor**: Encontra o maior valor em um array usando `max`.

Essas funções básicas são úteis para uma variedade de tarefas em PHP e formam a base para muitos scripts e aplicações PHP.