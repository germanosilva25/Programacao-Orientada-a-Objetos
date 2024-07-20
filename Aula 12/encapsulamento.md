Encapsulamento é um dos princípios fundamentais da programação orientada a objetos (OOP). Ele se refere ao conceito de esconder os detalhes internos de uma classe e expor apenas uma interface pública para interagir com o mundo externo. Isso ajuda a proteger o estado interno da classe e a garantir que os dados sejam manipulados de maneira controlada e segura.

### Conceito de Encapsulamento

1. **Ocultamento de Dados**: Encapsulamento permite que os atributos e métodos internos de uma classe sejam ocultados do acesso externo. Isso impede que partes externas do código modifiquem diretamente os dados internos da classe de forma não autorizada ou indesejada.

2. **Interface Pública**: A classe fornece uma interface pública (métodos públicos) para interagir com seus dados. Esses métodos permitem que usuários da classe acessem e modifiquem os dados de forma controlada.

3. **Controle e Validação**: Encapsulamento permite a implementação de regras de negócios e validações antes de alterar os dados internos. Isso ajuda a manter a integridade dos dados.

### Benefícios do Encapsulamento

1. **Segurança e Proteção**: Protege os dados internos da classe contra acesso e modificações não autorizadas.
2. **Manutenção e Evolução**: Facilita a manutenção e a evolução do código. Mudanças internas podem ser feitas sem afetar o código que usa a classe, desde que a interface pública permaneça consistente.
3. **Modularidade**: Permite a construção de componentes independentes e modulares que podem ser desenvolvidos, testados e atualizados separadamente.
4. **Reutilização**: Facilita a reutilização de código ao fornecer interfaces bem definidas e encapsuladas.

### Exemplo de Encapsulamento em PHP

Aqui está um exemplo básico de como o encapsulamento é aplicado em PHP:

```php
<?php

class ContaBancaria {
    // Atributos privados (ocultos do acesso externo)
    private $saldo;
    private $titular;

    // Construtor para inicializar os atributos
    public function __construct($titular, $saldoInicial) {
        $this->titular = $titular;
        $this->saldo = $saldoInicial;
    }

    // Método público para obter o saldo (interface pública)
    public function getSaldo() {
        return $this->saldo;
    }

    // Método público para depositar dinheiro (controle e validação)
    public function depositar($quantia) {
        if ($quantia > 0) {
            $this->saldo += $quantia;
        } else {
            echo "Quantia para depósito deve ser positiva.\n";
        }
    }

    // Método público para retirar dinheiro (controle e validação)
    public function retirar($quantia) {
        if ($quantia > 0 && $quantia <= $this->saldo) {
            $this->saldo -= $quantia;
        } else {
            echo "Quantia inválida ou saldo insuficiente.\n";
        }
    }
}

// Criando um objeto da classe ContaBancaria
$conta = new ContaBancaria("Maria", 1000.00);

// Usando métodos públicos para interagir com a conta
echo "Saldo inicial: R$ " . $conta->getSaldo() . "\n";

$conta->depositar(500.00);
echo "Saldo após depósito: R$ " . $conta->getSaldo() . "\n";

$conta->retirar(200.00);
echo "Saldo após retirada: R$ " . $conta->getSaldo() . "\n";

$conta->retirar(2000.00); // Mensagem de erro
?>
```

### Resumo dos Conceitos

- **Atributos Privados**: Dados internos da classe que não podem ser acessados diretamente de fora da classe.
- **Métodos Públicos**: Interface pública que permite interagir com os dados da classe de forma controlada.
- **Controle e Validação**: Métodos públicos podem incluir lógica para garantir que as operações realizadas nos dados estejam de acordo com as regras de negócios.

### Conclusão

O encapsulamento é crucial para criar classes robustas e seguras em OOP. Ele ajuda a proteger os dados internos, fornece uma interface clara para interação e permite que as mudanças na implementação interna da classe não impactem o código que utiliza a classe. Aplicar corretamente o encapsulamento leva a um design de software mais limpo, modular e fácil de manter.