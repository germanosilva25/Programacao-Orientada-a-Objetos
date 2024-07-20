Em programação orientada a objetos (OOP), herança é um mecanismo que permite que uma classe (chamada de subclasse ou classe derivada) herde as propriedades e métodos de outra classe (chamada de superclasse ou classe base). Herança promove a reutilização de código e permite criar uma hierarquia de classes que compartilham uma interface comum e funcionalidade.

### Características da Herança

1. **Reutilização de Código**: Herança permite que classes reutilizem o código de outras classes, evitando duplicação e promovendo a manutenção do código.

2. **Hierarquia de Classes**: Cria uma relação hierárquica entre classes, onde uma subclasse herda os atributos e métodos de uma superclasse.

3. **Sobrescrita de Métodos**: Subclasses podem sobrescrever métodos da superclasse para fornecer uma implementação específica.

4. **Extensibilidade**: Facilita a extensão de classes existentes para adicionar novas funcionalidades sem modificar o código original.

### Exemplo Prático em PHP

Aqui está um exemplo de herança em PHP:

```php
<?php

// Superclasse ou Classe Base
class Colaborador {
    protected $nome;
    protected $salario;

    public function __construct($nome, $salario) {
        $this->nome = $nome;
        $this->salario = $salario;
    }

    public function exibirInformacoes() {
        echo "Nome: " . $this->nome . "\n";
        echo "Salário: R$ " . number_format($this->salario, 2, ',', '.') . "\n";
    }

    public function calcularBonus($percentual) {
        return $this->salario * ($percentual / 100);
    }
}

// Subclasse ou Classe Derivada
class Gerente extends Colaborador {
    private $departamento;

    public function __construct($nome, $salario, $departamento) {
        // Chama o construtor da superclasse
        parent::__construct($nome, $salario);
        $this->departamento = $departamento;
    }

    // Sobrescrevendo o método exibirInformacoes
    public function exibirInformacoes() {
        parent::exibirInformacoes();
        echo "Departamento: " . $this->departamento . "\n";
    }

    // Novo método exclusivo da subclasse
    public function exibirDepartamento() {
        echo "Departamento: " . $this->departamento . "\n";
    }
}

// Criando objetos
$colaborador = new Colaborador("João Silva", 5000.00);
$gerente = new Gerente("Maria Oliveira", 8000.00, "TI");

// Exibindo informações
$colaborador->exibirInformacoes();
echo "\n";
$gerente->exibirInformacoes();
echo "\n";

// Exibindo bônus
echo "Bônus do colaborador: R$ " . number_format($colaborador->calcularBonus(10), 2, ',', '.') . "\n";
echo "Bônus do gerente: R$ " . number_format($gerente->calcularBonus(15), 2, ',', '.') . "\n";

?>
```

### Explicação do Exemplo

1. **Superclasse Colaborador**:
   - A classe `Colaborador` define dois atributos (`nome` e `salario`), um construtor, um método `exibirInformacoes()` e um método `calcularBonus()`.

2. **Subclasse Gerente**:
   - A classe `Gerente` estende `Colaborador` usando a palavra-chave `extends`.
   - O construtor da subclasse chama o construtor da superclasse usando `parent::__construct()`.
   - O método `exibirInformacoes()` é sobrescrito para incluir o departamento do gerente.
   - Um novo método `exibirDepartamento()` é adicionado à subclasse.

3. **Criação e Uso de Objetos**:
   - Objetos das classes `Colaborador` e `Gerente` são criados.
   - Os métodos `exibirInformacoes()` e `calcularBonus()` são chamados nos objetos, demonstrando a herança e sobrescrita de métodos.

### Vantagens da Herança

- **Reutilização de Código**: Reduz a duplicação de código, permitindo que classes reutilizem atributos e métodos de outras classes.
- **Organização e Hierarquia**: Facilita a organização do código em uma hierarquia lógica de classes, promovendo a compreensão e manutenção.
- **Extensibilidade**: Permite a extensão de funcionalidades sem modificar as classes base, promovendo a escalabilidade e flexibilidade do código.
- **Polimorfismo**: Suporta o polimorfismo, permitindo que objetos de diferentes classes sejam tratados de maneira uniforme.

### Desvantagens da Herança

- **Aumento da Complexidade**: Pode aumentar a complexidade do sistema devido à profundidade da hierarquia de classes.
- **Acesso Inadequado**: Pode levar a um acesso inadequado a atributos e métodos que deveriam ser encapsulados.
- **Dependência Forte**: Cria uma dependência forte entre a subclasse e a superclasse, tornando difícil modificar a superclasse sem impactar as subclasses.

Em resumo, herança é um dos pilares da programação orientada a objetos que permite a reutilização de código, organização em hierarquia, e extensão de funcionalidades, mas deve ser usada com cuidado para evitar aumento de complexidade e dependências inadequadas.
