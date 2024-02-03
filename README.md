# Módulo 6
Conteudo de apoio:
# Exercicio
## Programação procedual
A programação procedural é um paradigma de programação que se baseia na execução sequencial de instruções, organizadas em procedimentos ou funções. Nesse estilo de programação, o código é estruturado de maneira linear, com ênfase nas operações e manipulações de dados. Em geral, as linguagens de programação que seguem esse paradigma utilizam procedimentos, funções ou métodos para organizar o código em blocos de instruções reutilizáveis.

Um exemplo de programação procedural em Java pode ser visto abaixo. Neste exemplo simples, criaremos um programa para calcular a soma de dois números:

      public class Calculadora {
          // Função para calcular a soma de dois números
          public static int somar(int a, int b) {
              return a + b;
          }
      
          // Função principal (método main)
          public static void main(String[] args) {
              // Definindo dois números
              int numero1 = 10;
              int numero2 = 20;
      
              // Chamando a função somar e armazenando o resultado em uma variável
              int resultado = somar(numero1, numero2);
      
              // Exibindo o resultado
              System.out.println("A soma de " + numero1 + " e " + numero2 + " é: " + resultado);
          } }

Neste exemplo, a função somar é definida para realizar a operação de adição de dois números inteiros. O método main é o ponto de entrada do programa, onde dois números são definidos, a função somar é chamada com esses números, e o resultado é exibido na saída padrão.

## Programação orientada a objeto
A programação orientada a objetos (POO) é um paradigma de programação que se baseia na ideia de organizar o código em torno de "objetos", que são instâncias de classes. Cada objeto pode conter dados (atributos) e métodos (funções) que operam sobre esses dados. A POO busca modelar o mundo real, representando entidades e suas interações de forma mais natural.

Aqui está um exemplo simples em Java para ilustrar a programação orientada a objetos. Vamos criar uma classe chamada Carro com atributos como modelo, cor e ano, além de métodos para definir esses atributos e exibir informações sobre o carro:

          public class Carro {
              // Atributos
              private String modelo;
              private String cor;
              private int ano;
          
              // Construtor
              public Carro(String modelo, String cor, int ano) {
                  this.modelo = modelo;
                  this.cor = cor;
                  this.ano = ano;
              }
          
              // Método para exibir informações sobre o carro
              public void exibirInformacoes() {
                  System.out.println("Modelo: " + modelo);
                  System.out.println("Cor: " + cor);
                  System.out.println("Ano: " + ano);
              }
          
              // Métodos para definir atributos
              public void setModelo(String modelo) {
                  this.modelo = modelo;
              }
          
              public void setCor(String cor) {
                  this.cor = cor;
              }
          
              public void setAno(int ano) {
                  this.ano = ano;
              }
          
              // Método principal (método main)
              public static void main(String[] args) {
                  // Criando uma instância da classe Carro
                  Carro meuCarro = new Carro("Fusca", "Azul", 2022);
          
                  // Exibindo informações iniciais do carro
                  System.out.println("Informações iniciais do carro:");
                  meuCarro.exibirInformacoes();

        // Modificando alguns atributos
        meuCarro.setModelo("Civic");
        meuCarro.setAno(2023);

        // Exibindo informações atualizadas do carro
        System.out.println("\nInformações atualizadas do carro:");
        meuCarro.exibirInformacoes();
    } }

Neste exemplo, a classe Carro tem atributos privados (modelo, cor e ano), um construtor para inicializar esses atributos, métodos de acesso para modificar os atributos e um método exibirInformacoes para mostrar detalhes do carro. No método principal (main), criamos uma instância da classe Carro, modificamos alguns atributos e exibimos as informações do carro antes e depois das modificações.

## Principais diferenças entre programação procedural e programação orientada a objeto

### Organização do Código:

- Procedural: O código é estruturado em torno de procedimentos, funções ou rotinas. As operações e manipulações de dados são o foco principal.
- Orientada a Objetos: O código é estruturado em torno de classes e objetos. As entidades do mundo real são modeladas como objetos, que encapsulam dados e comportamentos.

### Exemplo em Java (Procedural):
            java
            Copy code
            // Procedural
            public class Calculadora {
                public static int somar(int a, int b) {
                    return a + b;
                }
            
                public static int subtrair(int a, int b) {
                    return a - b;
                } }

### Exemplo em Java (Orientada a Objetos):

            java
            Copy code
            // Orientada a Objetos
            public class Calculadora {
                public int somar(int a, int b) {
                    return a + b;
                }
            
                public int subtrair(int a, int b) {
                    return a - b;
                } }
    
### Encapsulamento:

- Procedural: Não há uma noção clara de encapsulamento. Dados e funções são geralmente globais ou pertencem a estruturas de dados.
- Orientada a Objetos: Os objetos encapsulam dados e comportamentos, controlando o acesso aos mesmos por meio de modificadores de acesso (como private, public, etc.).

### Exemplo em Java (Orientada a Objetos):

            java
            Copy code
            public class Carro {
                private String modelo;
            
                public String getModelo() {
                    return modelo;
                }
            
                public void setModelo(String novoModelo) {
                    this.modelo = novoModelo;
                } }
### Herança:

- Procedural: Geralmente não há suporte direto para herança de código.
- Orientada a Objetos: Suporta herança, permitindo que uma classe herde atributos e métodos de outra classe.

### Exemplo em Java (Orientada a Objetos):

            java
            Copy code
            public class Animal {
                public void emitirSom() {
                    System.out.println("Som do animal");
                }
            }
            
            public class Cachorro extends Animal {
                // Esta classe herda o método emitirSom da classe Animal
            }

### Polimorfismo:

- Procedural: Geralmente, não há suporte para polimorfismo.
- Orientada a Objetos: Suporta polimorfismo, onde um objeto pode ser tratado como um objeto de sua classe base.

### Exemplo em Java (Orientada a Objetos):

            java
            Copy code
            public interface Animal {
                void fazerSom();
            }
            
            public class Cachorro implements Animal {
                @Override
                public void fazerSom() {
                    System.out.println("Latindo");
                }
            }
            
            public class Gato implements Animal {
                @Override
                public void fazerSom() {
                    System.out.println("Miando");
                } }
