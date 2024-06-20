# Criando-Seu-Primeiro-Projeto-Prático-com-Orientação-a-Objetos-em-Java

Para criar o primeiro projeto prático com Orientação a Objetos em Java, vou te guiar através de um exemplo simples e prático. Vou criar um sistema básico de gestão de funcionários, onde cada funcionário terá nome, salário e cargo.

### Descrição do Projeto:
Desenvolver um sistema em Java para gerenciar funcionários, aplicando os conceitos de POO como encapsulamento, herança e polimorfismo.

### Passos para Implementação:

#### Passo 1: Definição das Classes
Vamos criar três classes principais: `Funcionario`, `Gerente` (que é um tipo específico de funcionário) e a classe principal `Main` para testar nosso sistema.

1. **Classe `Funcionario`:**
   - Atributos: `nome` (String), `salario` (double).
   - Métodos: Construtor, getters e setters para os atributos.

```java
// Funcionario.java
public class Funcionario {
    private String nome;
    private double salario;

    public Funcionario(String nome, double salario) {
        this.nome = nome;
        this.salario = salario;
    }

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public double getSalario() {
        return salario;
    }

    public void setSalario(double salario) {
        this.salario = salario;
    }
}
```

2. **Classe `Gerente` (subclasse de `Funcionario`):**
   - Além dos atributos herdados (`nome` e `salario`), o `Gerente` terá um atributo adicional `departamento` e métodos específicos.

```java
// Gerente.java
public class Gerente extends Funcionario {
    private String departamento;

    public Gerente(String nome, double salario, String departamento) {
        super(nome, salario);
        this.departamento = departamento;
    }

    public String getDepartamento() {
        return departamento;
    }

    public void setDepartamento(String departamento) {
        this.departamento = departamento;
    }
}
```

3. **Classe `Main`:**
   - Nesta classe, faremos a instância de alguns objetos do tipo `Funcionario` e `Gerente` para testar nosso sistema.

```java
// Main.java
public class Main {
    public static void main(String[] args) {
        Funcionario funcionario1 = new Funcionario("João", 3000.0);
        Gerente gerente1 = new Gerente("Maria", 6000.0, "Financeiro");

        System.out.println("Dados do Funcionário:");
        System.out.println("Nome: " + funcionario1.getNome());
        System.out.println("Salário: R$" + funcionario1.getSalario());

        System.out.println("\nDados do Gerente:");
        System.out.println("Nome: " + gerente1.getNome());
        System.out.println("Salário: R$" + gerente1.getSalario());
        System.out.println("Departamento: " + gerente1.getDepartamento());
    }
}
```

### Explicação do Código:
- **Classe `Funcionario`:** Define um funcionário básico com nome e salário.
- **Classe `Gerente`:** Herda de `Funcionario` e adiciona um atributo `departamento`.
- **Classe `Main`:** Testa a criação de objetos `Funcionario` e `Gerente`, demonstrando polimorfismo ao usar métodos específicos de cada classe.

### Observações Finais:
Este exemplo é bastante simples para ilustrar os conceitos básicos de POO em Java. Podemos expandir este projeto adicionando mais funcionalidades, como cálculo de bonificações, métodos para aumento de salário, entre outros. É importante praticar criando novas classes e explorando diferentes relações de herança e polimorfismo para consolidar seu conhecimento em POO.
