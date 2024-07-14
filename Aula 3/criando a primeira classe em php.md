Vamos criar uma classe em PHP que representa um aluno, incluindo atributos para armazenar suas informações pessoais e métodos para manipular esses dados.

### Exemplo: Classe Aluno em PHP

#### Definindo a Classe

```php
<?php

class Aluno {
    // Atributos
    private $nome;
    private $idade;
    private $matricula;
    private $notas = [];

    // Construtor
    public function __construct($nome, $idade, $matricula) {
        $this->nome = $nome;
        $this->idade = $idade;
        $this->matricula = $matricula;
    }

    // Métodos para acessar e modificar os atributos
    public function getNome() {
        return $this->nome;
    }

    public function setNome($nome) {
        $this->nome = $nome;
    }

    public function getIdade() {
        return $this->idade;
    }

    public function setIdade($idade) {
        $this->idade = $idade;
    }

    public function getMatricula() {
        return $this->matricula;
    }

    public function setMatricula($matricula) {
        $this->matricula = $matricula;
    }

    // Método para adicionar uma nota
    public function adicionarNota($nota) {
        $this->notas[] = $nota;
    }

    // Método para calcular a média das notas
    public function calcularMedia() {
        if (count($this->notas) === 0) {
            return 0;
        }
        $soma = array_sum($this->notas);
        return $soma / count($this->notas);
    }

    // Método para exibir as informações do aluno
    public function exibirInformacoes() {
        echo "Nome: " . $this->getNome() . "\n";
        echo "Idade: " . $this->getIdade() . "\n";
        echo "Matrícula: " . $this->getMatricula() . "\n";
        echo "Média das Notas: " . $this->calcularMedia() . "\n";
    }
}

// Exemplo de uso da classe
$aluno1 = new Aluno("João Silva", 20, 123456);
$aluno1->adicionarNota(8.5);
$aluno1->adicionarNota(9.0);
$aluno1->adicionarNota(7.5);
$aluno1->adicionarNota(8.0);
$aluno1->adicionarNota(9.2);

$aluno1->exibirInformacoes();

?>
```

#### Explicação do Código

1. **Definição da Classe**:
   - A classe `Aluno` é definida com quatro atributos: `nome`, `idade`, `matricula` e `notas`.
   - Os atributos são definidos como `private` para garantir o encapsulamento, permitindo o acesso apenas através de métodos específicos.

2. **Construtor**:
   - O método `__construct` é usado para inicializar os atributos `nome`, `idade` e `matricula` quando um novo objeto `Aluno` é criado.

3. **Métodos de Acesso e Modificação**:
   - Métodos `get` e `set` são definidos para cada atributo, permitindo acessar e modificar seus valores de forma controlada.

4. **Método para Adicionar Nota**:
   - O método `adicionarNota` adiciona uma nova nota ao array `notas`.

5. **Método para Calcular Média das Notas**:
   - O método `calcularMedia` calcula e retorna a média das notas armazenadas no array `notas`.

6. **Método para Exibir Informações do Aluno**:
   - O método `exibirInformacoes` exibe os dados do aluno, incluindo a média das notas.

7. **Exemplo de Uso**:
   - Um objeto `Aluno` é criado e inicializado com `nome`, `idade` e `matricula`.
   - Notas são adicionadas ao aluno.
   - As informações do aluno, incluindo a média das notas, são exibidas.

#### Executando o Código

Salve o código em um arquivo com a extensão `.php`, por exemplo, `aluno.php`, e execute-o em um ambiente de servidor PHP (como o Apache com PHP instalado, ou diretamente pelo terminal usando o PHP CLI):

```bash
php aluno.php
```

### Saída Esperada

```
Nome: João Silva
Idade: 20
Matrícula: 123456
Média das Notas: 8.44
```

### Conclusão

Este exemplo demonstra a criação de uma classe em PHP com atributos privados, métodos de acesso, e métodos para manipular dados. A utilização de métodos `get` e `set` permite um controle adequado sobre o acesso e a modificação dos atributos, enquanto métodos adicionais fornecem funcionalidades específicas, como adicionar notas e calcular a média. A POO facilita a organização e a manutenção do código, promovendo a reutilização e a modularidade.