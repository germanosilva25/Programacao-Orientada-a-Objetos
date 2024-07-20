Em programação orientada a objetos (OOP), métodos são funções definidas dentro de uma classe que descrevem os comportamentos que os objetos da classe podem realizar. Eles permitem que os objetos interajam com seus dados e realizem ações específicas. Métodos são fundamentais para encapsular a lógica dentro de uma classe, promovendo a reutilização de código e a organização do software.

### Características dos Métodos

1. **Definição Dentro da Classe**: Métodos são definidos dentro da classe e podem acessar e modificar os dados da classe (as propriedades).

2. **Acesso aos Dados da Classe**: Métodos podem acessar e manipular as propriedades da classe, permitindo a interação e modificação dos dados do objeto.

3. **Visibilidade**: Métodos podem ter diferentes níveis de visibilidade, como `public`, `protected` e `private`, controlando o acesso aos métodos fora da classe.

4. **Métodos Estáticos**: Além dos métodos de instância (que operam em objetos específicos), uma classe também pode ter métodos estáticos, que podem ser chamados sem criar uma instância da classe.

### Exemplo Prático

Aqui está um exemplo de uma classe em PHP que demonstra a definição e uso de métodos:

```php
<?php

class Colaborador {
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

    // Método estático
    public static function exibirMensagem() {
        echo "Bem-vindo ao sistema de gestão de colaboradores!\n";
    }
}

// Criando um novo objeto Colaborador
$colaborador = new Colaborador("João Silva", 5000.00, 2);

// Exibindo as informações do colaborador
$colaborador->exibirInformacoes();

// Calculando e exibindo o bônus
$bonus = $colaborador->calcularBonus(10);
echo "Bônus: R$ " . number_format($bonus, 2, ',', '.') . "\n";

// Chamando o método estático
Colaborador::exibirMensagem();

?>
```

### Explicação do Exemplo

1. **Classe Colaborador**:
   - A classe `Colaborador` possui três propriedades privadas: `nome`, `salario` e `qntDependentes`.

2. **Construtor `__construct()`**:
   - Um construtor é definido para inicializar as propriedades do objeto `Colaborador`.

3. **Método `exibirInformacoes()`**:
   - Um método público que exibe as informações do colaborador.

4. **Método `calcularBonus()`**:
   - Um método público que calcula o bônus do colaborador com base em um percentual fornecido.

5. **Método Estático `exibirMensagem()`**:
   - Um método estático que pode ser chamado sem criar uma instância da classe `Colaborador`.

6. **Criação e Uso de Objetos**:
   - Um objeto `Colaborador` é criado e os métodos `exibirInformacoes()` e `calcularBonus()` são chamados no objeto.
   - O método estático `exibirMensagem()` é chamado diretamente na classe `Colaborador`.

### Benefícios dos Métodos

- **Encapsulamento**: Métodos permitem encapsular a lógica dentro da classe, protegendo os dados e fornecendo uma interface clara para interagir com o objeto.
- **Reutilização de Código**: Métodos podem ser reutilizados em diferentes partes do programa, promovendo a DRY (Don't Repeat Yourself) principle.
- **Organização**: Facilita a organização do código, tornando-o mais legível e manutenível.
- **Modularidade**: Métodos permitem dividir o código em módulos funcionais, facilitando a manutenção e a compreensão.

Em resumo, métodos são essenciais na programação orientada a objetos, pois definem as ações que os objetos podem realizar e como eles interagem com seus dados. Eles promovem a encapsulação, reutilização e organização do código, tornando-o mais robusto e fácil de manter.