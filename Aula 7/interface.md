Em programação orientada a objetos (OOP), uma interface é um tipo de contrato que define um conjunto de métodos que uma classe deve implementar. Interfaces não contêm a implementação dos métodos, apenas a assinatura, o que permite que diferentes classes implementem esses métodos de maneiras variadas. Interfaces são usadas para definir um comportamento comum que pode ser compartilhado entre classes não relacionadas, promovendo a flexibilidade e a extensibilidade do código.

### Características das Interfaces

1. **Definição de Métodos**: Interfaces definem apenas a assinatura dos métodos, sem a implementação.
2. **Implementação Obrigatória**: Qualquer classe que implementar uma interface deve fornecer a implementação de todos os métodos definidos na interface.
3. **Multipla Implementação**: Diferente da herança de classes (que permite herança simples na maioria das linguagens), uma classe pode implementar múltiplas interfaces.
4. **Sem Estado**: Interfaces não podem conter atributos (variáveis de instância), apenas métodos.

### Exemplo Prático em PHP

Aqui está um exemplo de como definir e usar interfaces em PHP:

```php
<?php

// Definindo a interface
interface Trabalhador {
    public function trabalhar();
    public function receberSalario();
}

// Classe que implementa a interface
class Programador implements Trabalhador {
    private $nome;
    private $salario;

    public function __construct($nome, $salario) {
        $this->nome = $nome;
        $this->salario = $salario;
    }

    public function trabalhar() {
        echo $this->nome . " está programando.\n";
    }

    public function receberSalario() {
        echo $this->nome . " recebeu o salário de R$ " . number_format($this->salario, 2, ',', '.') . ".\n";
    }
}

// Outra classe que implementa a interface
class Designer implements Trabalhador {
    private $nome;
    private $salario;

    public function __construct($nome, $salario) {
        $this->nome = $nome;
        $this->salario = $salario;
    }

    public function trabalhar() {
        echo $this->nome . " está desenhando.\n";
    }

    public function receberSalario() {
        echo $this->nome . " recebeu o salário de R$ " . number_format($this->salario, 2, ',', '.') . ".\n";
    }
}

// Criando objetos e chamando os métodos
$programador = new Programador("João Silva", 5000.00);
$designer = new Designer("Maria Oliveira", 4000.00);

$programador->trabalhar();
$programador->receberSalario();

$designer->trabalhar();
$designer->receberSalario();

?>
```

### Explicação do Exemplo

1. **Definição da Interface Trabalhador**:
   - A interface `Trabalhador` define dois métodos: `trabalhar()` e `receberSalario()`.
   - Estes métodos não têm implementação, apenas a assinatura.

2. **Classe Programador**:
   - A classe `Programador` implementa a interface `Trabalhador`.
   - Ela deve fornecer a implementação dos métodos `trabalhar()` e `receberSalario()`.
   - A classe também define atributos privados `nome` e `salario` e os inicializa no construtor.

3. **Classe Designer**:
   - A classe `Designer` também implementa a interface `Trabalhador`.
   - Similar à classe `Programador`, ela fornece a implementação dos métodos `trabalhar()` e `receberSalario()`.

4. **Criação e Uso de Objetos**:
   - Objetos das classes `Programador` e `Designer` são criados e os métodos `trabalhar()` e `receberSalario()` são chamados em cada um dos objetos.

### Benefícios das Interfaces

- **Definição Clara de Contratos**: Interfaces definem claramente quais métodos uma classe deve implementar, promovendo a consistência.
- **Flexibilidade**: Classes não relacionadas podem implementar a mesma interface, permitindo que diferentes tipos de objetos sejam tratados de maneira uniforme.
- **Desacoplamento**: Promove o desacoplamento, já que o código pode depender de interfaces em vez de classes concretas.
- **Multipla Implementação**: Classes podem implementar múltiplas interfaces, permitindo a combinação de diferentes comportamentos.

### Quando Usar Interfaces

- **Definir Comportamentos Comuns**: Quando várias classes diferentes precisam implementar um conjunto comum de métodos.
- **Desacoplamento**: Quando deseja reduzir a dependência entre partes do sistema.
- **Plugabilidade**: Quando deseja que diferentes implementações possam ser facilmente substituídas.

### Limitações das Interfaces

- **Sem Implementação Compartilhada**: Não podem fornecer implementação comum para métodos, apenas definem a assinatura.
- **Aumento da Complexidade**: Pode aumentar a complexidade do design, especialmente em sistemas grandes com muitas interfaces.

Em resumo, interfaces são uma ferramenta poderosa na programação orientada a objetos, permitindo a definição de contratos que diferentes classes podem implementar, promovendo a flexibilidade, reutilização de código e desacoplamento.
