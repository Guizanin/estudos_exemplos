# 🏗️ Fundamentos da Orientação a Objetos (OO) em Java

A **Orientação a Objetos (OO)** é um paradigma de programação que organiza o código em **objetos**, permitindo reutilização, modularidade e abstração.

---

## 🔍 1. Classes e Objetos

- **Classe**: Define atributos e métodos.
- **Objeto**: Instância da classe, com estado próprio.

### 💡 Exemplo em Java

```java
class Carro {
    String modelo;
    int ano;

    void exibirInformacoes() {
        System.out.println("Modelo: " + modelo + ", Ano: " + ano);
    }
}

public class Main {
    public static void main(String[] args) {
        Carro meuCarro = new Carro();
        meuCarro.modelo = "Fusca";
        meuCarro.ano = 1970;
        meuCarro.exibirInformacoes();
    }
}
```

## 🔒 2. Encapsulamento

Protege atributos internos da classe.
Usa modificadores de acesso (private, protected, public).

### 💡 Exemplo em Java

```java
class Pessoa {
    private String nome;

    public void setNome(String nome) {
        this.nome = nome;
    }

    public String getNome() {
        return nome;
    }
}

public class Main {
    public static void main(String[] args) {
        Pessoa p = new Pessoa();
        p.setNome("Carlos");
        System.out.println("Nome: " + p.getNome());
    }
}
```

## 🧬 3. Herança

- Permite que uma classe herde características de outra.
- Usa a palavra-chave extends.

### 💡 Exemplo em Java

```java
class Animal {
    void fazerSom() {
        System.out.println("Som genérico de animal");
    }
}

class Cachorro extends Animal {
    @Override
    void fazerSom() {
        System.out.println("Au Au!");
    }
}

public class Main {
    public static void main(String[] args) {
        Cachorro c = new Cachorro();
        c.fazerSom();
    }
}
```

## 🔄 4. Polimorfismo

- Sobrecarga: Mesmo nome, diferentes parâmetros.
- Sobrescrita: Redefinição do método da classe pai.

### 💡 Exemplo de Sobrecarga

```java
class Calculadora {
    int somar(int a, int b) {
        return a + b;
    }

    int somar(int a, int b, int c) {
        return a + b + c;
    }
}

public class Main {
    public static void main(String[] args) {
        Calculadora calc = new Calculadora();
        System.out.println(calc.somar(2, 3));       // 5
        System.out.println(calc.somar(2, 3, 4));    // 9
    }
}
```

### 💡 Exemplo de Sobrescrita

```java
class Veiculo {
    void acelerar() {
        System.out.println("Veículo acelerando...");
    }
}

class Moto extends Veiculo {
    @Override
    void acelerar() {
        System.out.println("Moto acelerando rapidamente!");
    }
}

public class Main {
    public static void main(String[] args) {
        Veiculo v = new Moto();
        v.acelerar(); // Moto acelerando rapidamente!
    }
}
```

## 🎭 5. Abstração

- Modela apenas características essenciais.
- Usa classes abstratas e interfaces.

### 💡 Exemplo de Classe Abstrata

```java
abstract class Forma {
    abstract void desenhar();
}

class Circulo extends Forma {
    @Override
    void desenhar() {
        System.out.println("Desenhando um círculo...");
    }
}

public class Main {
    public static void main(String[] args) {
        Forma f = new Circulo();
        f.desenhar(); // Desenhando um círculo...
    }
}
```
