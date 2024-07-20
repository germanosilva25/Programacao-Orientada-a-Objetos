Aqui estão 10 exemplos de funções internas do PHP que são bastante úteis para tarefas básicas:

### 1. **`strlen()` - Comprimento de uma String**

```php
<?php
$string = "Hello, world!";
$comprimento = strlen($string);
echo "Comprimento da string: " . $comprimento; // Output: 13
?>
```

### 2. **`strpos()` - Encontrar a Posição da Primeira Ocorrência de uma Substring**

```php
<?php
$texto = "Olá, mundo!";
$posicao = strpos($texto, "mundo");
echo "A palavra 'mundo' começa na posição: " . $posicao; // Output: 6
?>
```

### 3. **`substr()` - Extrair uma Substring**

```php
<?php
$texto = "Olá, mundo!";
$subtexto = substr($texto, 0, 5);
echo "Substring: " . $subtexto; // Output: Olá, 
?>
```

### 4. **`str_replace()` - Substituir Texto em uma String**

```php
<?php
$texto = "Olá, mundo!";
$novoTexto = str_replace("mundo", "PHP", $texto);
echo $novoTexto; // Output: Olá, PHP!
?>
```

### 5. **`array_sum()` - Somar Todos os Valores de um Array**

```php
<?php
$array = [1, 2, 3, 4, 5];
$soma = array_sum($array);
echo "Soma dos valores do array: " . $soma; // Output: 15
?>
```

### 6. **`count()` - Contar o Número de Elementos em um Array**

```php
<?php
$array = [1, 2, 3, 4, 5];
$numeroDeElementos = count($array);
echo "Número de elementos no array: " . $numeroDeElementos; // Output: 5
?>
```

### 7. **`date()` - Formatar Data e Hora**

```php
<?php
$dataAtual = date("Y-m-d H:i:s");
echo "Data e hora atual: " . $dataAtual; // Output: Data e hora no formato: 2024-07-20 10:30:00
?>
```

### 8. **`number_format()` - Formatando Números**

```php
<?php
$numero = 1234567.891;
$numeroFormatado = number_format($numero, 2, ',', '.');
echo "Número formatado: " . $numeroFormatado; // Output: 1.234.567,89
?>
```

### 9. **`isset()` - Verificar se uma Variável Está Definida**

```php
<?php
$variavel = "Teste";
if (isset($variavel)) {
    echo "A variável está definida.";
} else {
    echo "A variável não está definida.";
}
?>
```

### 10. **`json_encode()` - Codificar Dados em JSON**

```php
<?php
$array = ["nome" => "João", "idade" => 30];
$json = json_encode($array);
echo "Dados em JSON: " . $json; // Output: {"nome":"João","idade":30}
?>
```

### Explicação dos Exemplos

1. **`strlen()`**: Retorna o comprimento de uma string.
2. **`strpos()`**: Encontra a posição da primeira ocorrência de uma substring dentro de uma string.
3. **`substr()`**: Extrai uma parte de uma string com base na posição inicial e no comprimento.
4. **`str_replace()`**: Substitui todas as ocorrências de uma substring por outra dentro de uma string.
5. **`array_sum()`**: Soma todos os valores numéricos em um array.
6. **`count()`**: Conta o número de elementos em um array.
7. **`date()`**: Formata e retorna a data e hora atuais.
8. **`number_format()`**: Formata um número com casas decimais e separadores de milhar.
9. **`isset()`**: Verifica se uma variável está definida e não é nula.
10. **`json_encode()`**: Codifica um array ou objeto PHP para uma representação JSON.

Essas funções são básicas e essenciais para trabalhar com strings, arrays, datas e formatação de dados em PHP. Elas ajudam a realizar operações comuns de forma eficiente e simplificada.