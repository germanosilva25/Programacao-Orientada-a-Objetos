Os modificadores de acesso também se aplicam a métodos em orientação a objetos (OOP). Eles controlam como e de onde os métodos de uma classe podem ser acessados e chamados. Assim como para os atributos, os principais modificadores de acesso para métodos são `public`, `private` e `protected`.

### Modificadores de Acesso para Métodos

1. **Público (public)**:
   - **Visibilidade**: Métodos declarados como `public` podem ser acessados de qualquer lugar: dentro da classe, fora da classe e por classes derivadas.
   - **Uso**: Utilizado para métodos que precisam ser acessíveis para outras classes ou para qualquer parte do programa.

2. **Privado (private)**:
   - **Visibilidade**: Métodos declarados como `private` só podem ser acessados de dentro da própria classe.
   - **Uso**: Utilizado para métodos que são internos à classe e não devem ser acessados ou alterados diretamente por outras classes ou instâncias.

3. **Protegido (protected)**:
   - **Visibilidade**: Métodos declarados como `protected` podem ser acessados dentro da própria classe e por classes derivadas (subclasses).
   - **Uso**: Utilizado para métodos que devem ser acessíveis por subclasses, mas não diretamente acessíveis por outras classes.

### Exemplos em PHP

#### Modificador Público

```php
<?php

class Pessoa {
    private $nome;

    public function __construct($nome) {
        $this->nome = $nome;
    }

    // Método público
    public function getNome() {
        return $this->nome;
    }

    // Método público
    public function setNome($nome) {
        $this->nome = $nome;
    }
}

$pessoa = new Pessoa("João");
echo $pessoa->getNome(); // Acesso ao método público

$pessoa->setNome("Maria");
echo $pessoa->getNome(); // Output: Maria

?>
```

#### Modificador Privado

```php
<?php

class Pessoa {
    private $nome;

    public function __construct($nome) {
        $this->nome = $nome;
    }

    // Método privado
    private function validarNome($nome) {
        return !empty($nome);
    }

    // Método público que utiliza o método privado
    public function setNome($nome) {
        if ($this->validarNome($nome)) {
            $this->nome = $nome;
        }
    }

    public function getNome() {
        return $this->nome;
    }
}

$pessoa = new Pessoa("João");
echo $pessoa->getNome(); // Output: João

$pessoa->setNome("");
echo $pessoa->getNome(); // Output: João (nome não alterado devido à validação)

$pessoa->setNome("Maria");
echo $pessoa->getNome(); // Output: Maria

// $pessoa->validarNome("João"); // Erro: Método privado não pode ser acessado diretamente

?>
```

#### Modificador Protegido

```php
<?php

class Pessoa {
    protected $nome;

    public function __construct($nome) {
        $this->nome = $nome;
    }

    // Método protegido
    protected function getNome() {
        return $this->nome;
    }
}

class Funcionario extends Pessoa {
    private $cargo;

    public function __construct($nome, $cargo) {
        parent::__construct($nome);
        $this->cargo = $cargo;
    }

    public function getDetalhes() {
        return "Nome: " . $this->getNome() . ", Cargo: " . $this->cargo;
    }
}

$funcionario = new Funcionario("Maria", "Desenvolvedora");
echo $funcionario->getDetalhes(); // Output: Nome: Maria, Cargo: Desenvolvedora

// $funcionario->getNome(); // Erro: Método protegido não pode ser acessado diretamente

?>
```

### Resumo dos Modificadores de Acesso

| Modificador | Visibilidade                      | Exemplo de Uso                            |
|-------------|-----------------------------------|-------------------------------------------|
| **public**  | Acessível de qualquer lugar       | Métodos que precisam ser acessíveis de fora da classe. |
| **private** | Acessível apenas dentro da classe | Métodos internos que não devem ser acessados diretamente.   |
| **protected** | Acessível na classe e subclasses | Métodos que devem ser compartilhados com subclasses, mas protegidos de acesso externo. |

### Conclusão

Os modificadores de acesso para métodos são essenciais para implementar o encapsulamento em OOP. Eles permitem controlar a visibilidade e o acesso aos métodos de uma classe, garantindo que os métodos internos sejam protegidos e que os métodos públicos estejam acessíveis quando necessário. Usar corretamente os modificadores de acesso ajuda a manter o código mais seguro, modular e fácil de manter.

