Aqui estão mais 10 exemplos de funções internas básicas do PHP, que são úteis para diversas tarefas:

### 1. **`isset()` - Verificar se uma Variável Está Definida**

```php
<?php
$variavel = "Olá, PHP!";
if (isset($variavel)) {
    echo "A variável está definida.";
} else {
    echo "A variável não está definida.";
}
?>
```

### 2. **`empty()` - Verificar se uma Variável Está Vazia**

```php
<?php
$variavel = "";
if (empty($variavel)) {
    echo "A variável está vazia.";
} else {
    echo "A variável não está vazia.";
}
?>
```

### 3. **`array_merge()` - Mesclar Dois ou Mais Arrays**

```php
<?php
$array1 = [1, 2, 3];
$array2 = [4, 5, 6];
$arrayMesclado = array_merge($array1, $array2);
print_r($arrayMesclado); // Output: Array ( [0] => 1 [1] => 2 [2] => 3 [3] => 4 [4] => 5 [5] => 6 )
?>
```

### 4. **`array_reverse()` - Reverter a Ordem dos Elementos de um Array**

```php
<?php
$array = [1, 2, 3, 4, 5];
$arrayRevertido = array_reverse($array);
print_r($arrayRevertido); // Output: Array ( [0] => 5 [1] => 4 [2] => 3 [3] => 2 [4] => 1 )
?>
```

### 5. **`array_unique()` - Remover Valores Duplicados de um Array**

```php
<?php
$array = [1, 2, 2, 3, 4, 4, 5];
$arrayUnico = array_unique($array);
print_r($arrayUnico); // Output: Array ( [0] => 1 [1] => 2 [3] => 3 [4] => 4 [6] => 5 )
?>
```

### 6. **`strtolower()` - Converter uma String para Minúsculas**

```php
<?php
$string = "Olá, Mundo!";
$stringMinusculas = strtolower($string);
echo $stringMinusculas; // Output: olá, mundo!
?>
```

### 7. **`strtoupper()` - Converter uma String para Maiúsculas**

```php
<?php
$string = "Olá, Mundo!";
$stringMaiusculas = strtoupper($string);
echo $stringMaiusculas; // Output: OLÁ, MUNDO!
?>
```

### 8. **`preg_match()` - Realizar uma Busca em uma String com Expressão Regular**

```php
<?php
$texto = "O número é 12345";
if (preg_match("/\d+/", $texto, $matches)) {
    echo "Número encontrado: " . $matches[0]; // Output: Número encontrado: 12345
} else {
    echo "Nenhum número encontrado.";
}
?>
```

### 9. **`file_get_contents()` - Ler o Conteúdo de um Arquivo em uma String**

```php
<?php
$conteudo = file_get_contents("exemplo.txt");
echo "Conteúdo do arquivo: " . $conteudo;
?>
```

### 10. **`file_put_contents()` - Escrever Dados em um Arquivo**

```php
<?php
$dados = "Este é um exemplo de escrita em arquivo.";
file_put_contents("exemplo.txt", $dados);
echo "Dados escritos no arquivo com sucesso.";
?>
```

### Explicação dos Exemplos

1. **`isset()`**: Verifica se uma variável está definida e não é nula.
2. **`empty()`**: Verifica se uma variável está vazia (ou seja, é `""`, `0`, `NULL`, `FALSE`, etc.).
3. **`array_merge()`**: Mescla dois ou mais arrays em um único array.
4. **`array_reverse()`**: Reverte a ordem dos elementos em um array.
5. **`array_unique()`**: Remove valores duplicados de um array.
6. **`strtolower()`**: Converte todos os caracteres de uma string para minúsculas.
7. **`strtoupper()`**: Converte todos os caracteres de uma string para maiúsculas.
8. **`preg_match()`**: Realiza uma busca em uma string usando uma expressão regular e retorna os resultados encontrados.
9. **`file_get_contents()`**: Lê o conteúdo de um arquivo e o retorna como uma string.
10. **`file_put_contents()`**: Escreve uma string em um arquivo, substituindo o conteúdo existente.

Essas funções cobrem uma variedade de operações úteis em PHP, desde manipulação de strings e arrays até leitura e escrita de arquivos. Elas são bastante comuns em scripts PHP para realizar tarefas cotidianas.
