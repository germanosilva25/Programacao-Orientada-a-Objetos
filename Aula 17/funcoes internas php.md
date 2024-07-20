Claro! Aqui estão 10 exemplos de funções internas do PHP em um nível intermediário. Essas funções são úteis para tarefas mais complexas e operações avançadas.

### 1. **`array_filter()` - Filtrar Elementos de um Array com Base em uma Função de Callback**

```php
<?php
$numeros = [1, 2, 3, 4, 5];
$pares = array_filter($numeros, function($numero) {
    return $numero % 2 == 0;
});
print_r($pares); // Output: Array ( [1] => 2 [3] => 4 )
?>
```

### 2. **`array_map()` - Aplicar uma Função a Todos os Elementos de um Array**

```php
<?php
$numeros = [1, 2, 3, 4];
$dobrados = array_map(function($numero) {
    return $numero * 2;
}, $numeros);
print_r($dobrados); // Output: Array ( [0] => 2 [1] => 4 [2] => 6 [3] => 8 )
?>
```

### 3. **`array_reduce()` - Reduz um Array a um Único Valor Usando uma Função de Callback**

```php
<?php
$numeros = [1, 2, 3, 4];
$soma = array_reduce($numeros, function($carry, $item) {
    return $carry + $item;
});
echo "Soma: " . $soma; // Output: Soma: 10
?>
```

### 4. **`strtotime()` - Converter uma Data e Hora em Timestamp**

```php
<?php
$data = "2024-07-20 10:30:00";
$timestamp = strtotime($data);
echo "Timestamp: " . $timestamp; // Output: Timestamp para a data especificada
?>
```

### 5. **`date_create()` - Criar um Novo Objeto de Data e Hora**

```php
<?php
$data = date_create("2024-07-20 10:30:00");
echo "Data formatada: " . date_format($data, "d/m/Y H:i:s"); // Output: 20/07/2024 10:30:00
?>
```

### 6. **`file_exists()` - Verificar se um Arquivo ou Diretório Existe**

```php
<?php
$caminho = "exemplo.txt";
if (file_exists($caminho)) {
    echo "O arquivo existe.";
} else {
    echo "O arquivo não existe.";
}
?>
```

### 7. **`gettype()` - Retornar o Tipo de uma Variável**

```php
<?php
$variavel = 123;
echo "Tipo da variável: " . gettype($variavel); // Output: integer
?>
```

### 8. **`preg_replace()` - Substituir Texto em uma String Usando Expressões Regulares**

```php
<?php
$texto = "O preço é R$ 100,00";
$novoTexto = preg_replace("/R\$ (\d+)/", "R$ $1,00", $texto);
echo $novoTexto; // Output: O preço é R$ 100,00
?>
```

### 9. **`http_build_query()` - Construir uma String de Consulta HTTP a partir de um Array**

```php
<?php
$parametros = [
    'nome' => 'João',
    'idade' => 30,
    'cidade' => 'São Paulo'
];
$query = http_build_query($parametros);
echo "Query: " . $query; // Output: nome=João&idade=30&cidade=São+Paulo
?>
```

### 10. **`json_decode()` - Decodificar uma String JSON para um Array ou Objeto PHP**

```php
<?php
$json = '{"nome": "João", "idade": 30}';
$array = json_decode($json, true);
echo "Nome: " . $array['nome']; // Output: Nome: João
?>
```

### Explicação dos Exemplos

1. **`array_filter()`**: Filtra os elementos de um array com base em uma função de callback, retornando apenas os elementos que satisfazem a condição.
2. **`array_map()`**: Aplica uma função a cada elemento de um array e retorna um novo array com os valores modificados.
3. **`array_reduce()`**: Reduz um array a um único valor, aplicando uma função de callback que acumula o resultado.
4. **`strtotime()`**: Converte uma string de data e hora em um timestamp Unix.
5. **`date_create()`**: Cria um objeto de data e hora a partir de uma string e permite manipulação e formatação.
6. **`file_exists()`**: Verifica se um arquivo ou diretório especificado existe.
7. **`gettype()`**: Retorna o tipo de uma variável (por exemplo, integer, string, array).
8. **`preg_replace()`**: Substitui ocorrências de uma expressão regular em uma string por outro valor.
9. **`http_build_query()`**: Constrói uma string de consulta URL a partir de um array associativo.
10. **`json_decode()`**: Decodifica uma string JSON em uma estrutura PHP, como um array associativo ou objeto.

Essas funções são um pouco mais avançadas e permitem realizar operações mais complexas e úteis em PHP.
