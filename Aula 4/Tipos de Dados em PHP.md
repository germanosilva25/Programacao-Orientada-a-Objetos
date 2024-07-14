Em PHP, existem vários tipos de variáveis que podem ser usados para armazenar diferentes tipos de dados. Aqui estão os principais tipos de variáveis em PHP, cada um com exemplos para ilustrar seu uso:

### 1. Integer (Inteiro)

Variáveis do tipo inteiro são usadas para armazenar números inteiros sem casas decimais.

```php
$idade = 30;
$ano_nascimento = 1994;
$num_alunos = 1000;
```

### 2. Float (Ponto Flutuante)

Variáveis do tipo ponto flutuante (ou float) são usadas para armazenar números com casas decimais.

```php
$peso = 68.5;
$altura = 1.75;
$preco_produto = 19.99;
```

### 3. String

Variáveis do tipo string são usadas para armazenar sequências de caracteres (texto).

```php
$nome = "João";
$cidade = 'São Paulo';
$texto = "Bem-vindo ao meu site!";
```

### 4. Boolean

Variáveis do tipo boolean são usadas para armazenar valores verdadeiro ou falso.

```php
$tem_permissao = true;
$usuario_logado = false;
$aceitou_termos = true;
```

### 5. Array

Arrays são usados para armazenar múltiplos valores em uma única variável.

```php
$cores = array("vermelho", "verde", "azul");
$numeros = [1, 2, 3, 4, 5]; // Sintaxe alternativa a partir do PHP 5.4
$aluno = [
    "nome" => "Maria",
    "idade" => 25,
    "curso" => "Engenharia"
];
```

### 6. Object (Objeto)

Variáveis do tipo objeto são usadas para armazenar instâncias de classes definidas pelo usuário.

```php
class Pessoa {
    public $nome;
    public $idade;
}

$pessoa1 = new Pessoa();
$pessoa1->nome = "João";
$pessoa1->idade = 30;
```

### 7. Null

Variáveis do tipo null representam uma variável sem valor atribuído.

```php
$variavel_nula = null;
```

### 8. Resource

Variáveis do tipo resource são usadas para armazenar referências a recursos externos, como conexões de banco de dados.

```php
$bd_conexao = mysqli_connect("localhost", "usuario", "senha", "banco");
```

### 9. Callable

Variáveis do tipo callable são usadas para armazenar callbacks ou funções que podem ser chamadas dinamicamente.

```php
function somar($a, $b) {
    return $a + $b;
}

$funcao = 'somar';
echo $funcao(10, 5); // Saída: 15
```

### Conclusão

Estes são os principais tipos de variáveis em PHP, cada um adequado para diferentes tipos de dados e usos. É importante entender cada tipo e saber quando e como usá-los adequadamente em seus programas PHP.
