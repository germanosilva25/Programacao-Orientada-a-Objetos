Claro! Aqui estão mais 10 exemplos de funções internas básicas do PHP, cada uma realizando uma tarefa comum e útil:

### 1. **`trim()` - Remover Espaços em Branco de Início e Fim de uma String**

```php
<?php
$string = "   Olá, mundo!   ";
$limpa = trim($string);
echo "String limpa: '" . $limpa . "'"; // Output: 'Olá, mundo!'
?>
```

### 2. **`strlen()` - Retornar o Comprimento de uma String**

```php
<?php
$string = "Hello, world!";
$comprimento = strlen($string);
echo "Comprimento da string: " . $comprimento; // Output: 13
?>
```

### 3. **`explode()` - Dividir uma String em um Array**

```php
<?php
$string = "maçã,banana,laranja";
$array = explode(",", $string);
print_r($array); // Output: Array ( [0] => maçã [1] => banana [2] => laranja )
?>
```

### 4. **`implode()` - Juntar Elementos de um Array em uma String**

```php
<?php
$array = ["maçã", "banana", "laranja"];
$string = implode(", ", $array);
echo $string; // Output: maçã, banana, laranja
?>
```

### 5. **`array_push()` - Adicionar um ou Mais Elementos ao Final de um Array**

```php
<?php
$array = [1, 2, 3];
array_push($array, 4, 5);
print_r($array); // Output: Array ( [0] => 1 [1] => 2 [2] => 3 [3] => 4 [4] => 5 )
?>
```

### 6. **`array_pop()` - Remover e Retornar o Último Elemento de um Array**

```php
<?php
$array = [1, 2, 3, 4];
$ultimoElemento = array_pop($array);
echo "Último elemento removido: " . $ultimoElemento; // Output: 4
print_r($array); // Output: Array ( [0] => 1 [1] => 2 [2] => 3 )
?>
```

### 7. **`in_array()` - Verificar se um Valor Está em um Array**

```php
<?php
$array = [1, 2, 3, 4];
$valor = 3;
if (in_array($valor, $array)) {
    echo "O valor $valor está no array.";
} else {
    echo "O valor $valor não está no array.";
}
?>
```

### 8. **`array_key_exists()` - Verificar se uma Chave Existe em um Array Associativo**

```php
<?php
$array = ["nome" => "João", "idade" => 30];
if (array_key_exists("nome", $array)) {
    echo "A chave 'nome' existe no array.";
} else {
    echo "A chave 'nome' não existe no array.";
}
?>
```

### 9. **`isset()` - Verificar se uma Variável Está Definida e Não é Nula**

```php
<?php
$variavel = "Testando";
if (isset($variavel)) {
    echo "A variável está definida e não é nula.";
} else {
    echo "A variável não está definida ou é nula.";
}
?>
```

### 10. **`rand()` - Gerar um Número Aleatório**

```php
<?php
$numeroAleatorio = rand(1, 100);
echo "Número aleatório entre 1 e 100: " . $numeroAleatorio;
?>
```

### Explicação dos Exemplos

1. **`trim()`**: Remove espaços em branco do início e do fim de uma string.
2. **`strlen()`**: Retorna o comprimento de uma string.
3. **`explode()`**: Divide uma string em um array usando um delimitador.
4. **`implode()`**: Junta os elementos de um array em uma string, separados por um delimitador.
5. **`array_push()`**: Adiciona um ou mais elementos ao final de um array.
6. **`array_pop()`**: Remove e retorna o último elemento de um array.
7. **`in_array()`**: Verifica se um valor está presente em um array.
8. **`array_key_exists()`**: Verifica se uma chave existe em um array associativo.
9. **`isset()`**: Verifica se uma variável está definida e não é nula.
10. **`rand()`**: Gera um número aleatório dentro de um intervalo especificado.

Essas funções são úteis para manipulação de strings, arrays e variáveis, e são amplamente utilizadas em scripts PHP para realizar operações comuns e operações básicas de programação.
