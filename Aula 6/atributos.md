Em programação orientada a objetos (OOP), atributos são variáveis definidas dentro de uma classe que armazenam os dados ou o estado de um objeto. Cada instância (objeto) de uma classe tem seu próprio conjunto de valores de atributos, o que permite que objetos diferentes da mesma classe possam ter dados diferentes.

### Características dos Atributos

1. **Definição Dentro da Classe**: Atributos são definidos dentro da classe e representam as propriedades ou características dos objetos criados a partir dessa classe.

2. **Visibilidade**: Atributos podem ter diferentes níveis de visibilidade:
   - `public`: Acessível de qualquer lugar.
   - `protected`: Acessível dentro da classe e por subclasses.
   - `private`: Acessível apenas dentro da própria classe.

3. **Inicialização**: Atributos podem ser inicializados diretamente na sua definição, ou através de um construtor, que é um método especial chamado quando um objeto é instanciado.

### Exemplo Prático

Aqui está um exemplo de uma classe em PHP que demonstra a definição e uso de atributos:

```php
<?php

class Colaborador {
    // Atributos da classe
    private $nome;
    private $salario;
    private $qntDependentes;

    // Construtor da classe
    public function __construct($nome, $salario, $qntDependentes) {
        $this->nome = $nome;
        $this->salario = $salario;
        $this->qntDependentes = $qntDependentes;
    }

    // Método para exibir informações do colaborador
    public function exibirInformacoes() {
        echo "Nome: " . $this->nome . "\n";
        echo "Salário: R$ " . number_format($this->salario, 2, ',', '.') . "\n";
        echo "Quantidade de Dependentes: " . $this->qntDependentes . "\n";
    }

    // Método para calcular bônus baseado no salário
    public function calcularBonus($percentual) {
        return $this->salario * ($percentual / 100);
    }

    // Métodos getters e setters para acessar e modificar os atributos
    public function getNome() {
        return $this->nome;
    }

    public function setNome($nome) {
        $this->nome = $nome;
    }

    public function getSalario() {
        return $this->salario;
    }

    public function setSalario($salario) {
        $this->salario = $salario;
    }

    public function getQntDependentes() {
        return $this->qntDependentes;
    }

    public function setQntDependentes($qntDependentes) {
        $this->qntDependentes = $qntDependentes;
    }
}

// Criando um novo objeto Colaborador
$colaborador = new Colaborador("João Silva", 5000.00, 2);

// Exibindo as informações do colaborador
$colaborador->exibirInformacoes();

// Modificando os atributos usando setters
$colaborador->setNome("Maria Oliveira");
$colaborador->setSalario(6000.00);
$colaborador->setQntDependentes(3);

// Exibindo as informações atualizadas do colaborador
$colaborador->exibirInformacoes();

// Calculando e exibindo o bônus
$bonus = $colaborador->calcularBonus(10);
echo "Bônus: R$ " . number_format($bonus, 2, ',', '.') . "\n";

?>
```

### Explicação do Exemplo

1. **Classe Colaborador**:
   - A classe `Colaborador` possui três atributos privados: `nome`, `salario` e `qntDependentes`.

2. **Construtor `__construct()`**:
   - O construtor inicializa os atributos com os valores fornecidos quando um novo objeto é criado.

3. **Método `exibirInformacoes()`**:
   - Um método público que exibe as informações do colaborador.

4. **Método `calcularBonus()`**:
   - Um método público que calcula o bônus do colaborador com base em um percentual fornecido.

5. **Métodos Getters e Setters**:
   - Métodos `getNome()`, `setNome()`, `getSalario()`, `setSalario()`, `getQntDependentes()`, `setQntDependentes()` são usados para acessar e modificar os atributos da classe.

6. **Criação e Uso de Objetos**:
   - Um objeto `Colaborador` é criado com o nome "João Silva", salário de 5000.00 e 2 dependentes.
   - As informações do colaborador são exibidas usando `exibirInformacoes()`.
   - Os atributos do colaborador são modificados usando os métodos setters.
   - As informações atualizadas são exibidas novamente.
   - O bônus é calculado e exibido.

### Benefícios dos Atributos

- **Encapsulamento**: Atributos permitem encapsular os dados dentro de uma classe, protegendo-os de acesso direto e não autorizado.
- **Organização**: Facilita a organização do código, tornando-o mais legível e manutenível.
- **Reutilização**: Permite a reutilização de código, pois os atributos podem ser usados por vários métodos dentro da classe.
- **Flexibilidade**: Atributos podem ser facilmente modificados e acessados usando métodos getters e setters, promovendo a flexibilidade no design do software.

Em resumo, atributos são fundamentais na programação orientada a objetos, pois representam as propriedades dos objetos e permitem encapsular dados dentro de uma classe, promovendo uma estrutura de código organizada, segura e reutilizável.