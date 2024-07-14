### Apostila de Programação Orientada a Objetos em PHP

---

## 1. Introdução à Programação Orientada a Objetos (POO)
A Programação Orientada a Objetos (POO) é um paradigma de programação que utiliza "objetos" – entidades que combinam dados e comportamento. A POO ajuda a organizar e estruturar o código de uma maneira mais natural, intuitiva e escalável. Este paradigma é amplamente utilizado em linguagens como PHP, Java, C++, Python, entre outras.

### Vantagens da POO:
- **Reutilização de Código:** Facilita a reutilização de código através da herança.
- **Modularidade:** Divide programas complexos em partes menores e mais gerenciáveis.
- **Manutenibilidade:** Torna o código mais fácil de entender e manter.
- **Escalabilidade:** Facilita a adição de novas funcionalidades sem alterar o código existente.

---

## 2. Classes
Uma classe é um molde ou uma estrutura que define um conjunto de propriedades e métodos comuns a um determinado tipo de objeto.

### Estrutura Básica:
```php
class NomeDaClasse {
    // Atributos
    // Métodos
}
```
### Exemplo:
```php
class Carro {
    public $cor;
    public $modelo;
    public $ano;
}
```

---

## 3. Atributos
Os atributos são variáveis que pertencem à classe e representam as características dos objetos criados a partir da classe.

### Declaração de Atributos:
```php
class Carro {
    public $cor;
    public $modelo;
    public $ano;
}
```

---

## 4. Métodos
Os métodos são funções que definem os comportamentos dos objetos. Eles podem manipular os atributos da classe e realizar ações.

### Exemplo de Método:
```php
class Carro {
    public $cor;
    public $modelo;
    public $ano;

    public function acelerar() {
        echo "O carro está acelerando.";
    }
}
```

---

## 5. Objetos
Um objeto é uma instância de uma classe. Ele é criado a partir de uma classe e possui seus próprios valores de atributos.

### Criação de um Objeto:
```php
$meuCarro = new Carro();
$meuCarro->cor = "Vermelho";
$meuCarro->modelo = "Fusca";
$meuCarro->ano = 1965;
```

---

## 6. Modificadores de Acesso
Os modificadores de acesso definem a visibilidade dos atributos e métodos da classe. Os mais comuns são:

- **public:** Acesso livre de qualquer classe.
- **private:** Acesso restrito apenas à própria classe.
- **protected:** Acesso permitido às subclasses e classes do mesmo pacote.

### Exemplo:
```php
class Carro {
    private $cor;
    public $modelo;
    protected $ano;
}
```

---

## 7. Métodos

### 7.1 Tipos de Retorno
O tipo de retorno de um método define o tipo de valor que o método irá retornar após sua execução. Se o método não retornar nada, utiliza-se o tipo `void`.

### Exemplo:
```php
class Calculadora {
    public function somar($a, $b) {
        return $a + $b;
    }

    public function exibirMensagem() {
        echo "Olá, mundo!";
    }
}
```

### 7.2 Parâmetros
Os parâmetros são valores passados para os métodos para que eles possam realizar suas operações.

### Exemplo:
```php
class Carro {
    private $cor;

    public function setCor($cor) {
        $this->cor = $cor;
    }

    public function getCor() {
        return $this->cor;
    }
}
```

---

## 8. Encapsulamento
Encapsulamento é o princípio de esconder os detalhes internos dos objetos e expor apenas o que é necessário. Isso é feito utilizando modificadores de acesso e métodos getters e setters.

### Exemplo:
```php
class Carro {
    private $cor;

    public function getCor() {
        return $this->cor;
    }

    public function setCor($cor) {
        $this->cor = $cor;
    }
}
```

---

## 9. Herança
Herança é um mecanismo onde uma classe herda os atributos e métodos de outra classe. A classe que herda é chamada de subclasse, e a classe herdada é chamada de superclasse.

### Exemplo:
```php
class Veiculo {
    public $tipo;
}

class Carro extends Veiculo {
    public $modelo;
}
```

---

## 10. Polimorfismo
Polimorfismo permite que um objeto seja tratado de várias formas. Existem dois tipos principais: 

- **Polimorfismo de sobrecarga:** Vários métodos com o mesmo nome, mas diferentes assinaturas.
- **Polimorfismo de sobrescrita:** Uma subclasse fornece uma implementação específica de um método que já é definido em sua superclasse.

### Exemplo de Sobrecarga:
```php
class Calculadora {
    public function somar($a, $b) {
        return $a + $b;
    }

    public function somar($a, $b, $c) {
        return $a + $b + $c;
    }
}
```

### Exemplo de Sobrescrita:
```php
class Animal {
    public function fazerSom() {
        echo "O animal faz um som";
    }
}

class Cachorro extends Animal {
    public function fazerSom() {
        echo "O cachorro late";
    }
}
```

---

### Conclusão
A Programação Orientada a Objetos é uma poderosa ferramenta para desenvolver software de maneira modular, reutilizável e escalável. Compreender e aplicar os conceitos de classes, objetos, encapsulamento, herança e polimorfismo é fundamental para qualquer programador.