# Instruções
- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 8 questões objetivas assinalando a alternativa correta e **justificando sua resposta.**
- Resolva as 2 questões dissertativas escrevendo no próprio arquivo .md
- Lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com o uso de ChatGPT (e similares), pois entregar algo só para ganhar nota não fará você aprender. Não seja dependente da máquina!
- Ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas
**1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.**
```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
a) A saída será undefined seguido de erro e a alternativa correta, porque a varíavel "VAR" deveria estar acima do console.log()

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log


**2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.**

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```

a) Substituir if (a || b === 0) por if (a === 0 || b === 0)

b) Substituir if (a || b === 0) por if (a === 0 && b === 0) A alternativa B e a correta, porque ao rodar o codigo esta resultando em 2 diferente de antes, que não era possivel obter um numero.

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

______
**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

b) O código imprime 200.   No código, quando o valor de tipo é "eletrônico", o switch entra no case "eletrônico" e define o valor de preco como 1000. Porém, como não tem um break depois desse case, o código continua e vai para o próximo case, que é o case "vestuário". Nesse case, o valor de preco é atualizado para 200.

Como o break só aparece depois do case "vestuário", o código sai do switch e retorna o valor final de preco, que agora é 200.

Portanto, o código vai imprimir 200 no console.

A resposta correta é b) O código imprime 200.

c) O código imprime 50.

d) O código gera um erro.

______
**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

d) 24 A alternativa correta e a letra D, pois O código retorna 24 porque:

O map(x => x * 2) multiplica cada número do array por 2, gerando [2, 4, 6, 8, 10].
O filter(x => x > 5) filtra os números maiores que 5, resultando em [6, 8, 10].
O reduce((a, b) => a + b, 0) soma os valores 6 + 8 + 10, resultando = 24.
______
**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

c) ["banana", "abacaxi", "manga", "laranja"]  e a resposta correta, pois O método splice começa a partir do índice 1, remove dois elementos ("maçã" e "uva") e adiciona "abacaxi" e "manga". O array final é ["banana", "abacaxi", "manga", "laranja"].

d) ["banana", "maçã", "uva", "abacaxi", "manga"]
______
**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.


a) As duas afirmações são verdadeiras, e a segunda justifica a primeira. E a resposta correta, pois Ambas as afirmações estão corretas, e a segunda afirmação (uso da palavra-chave extends) realmente justifica a primeira, pois é a maneira como a herança é implementada em JavaScript.


b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.
______
**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```


I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

a) I e II são verdadeiras.   A alternativa correta é a) I e II são verdadeiras.

Justificativa resumida:

I: A classe Funcionario herda de Pessoa, portanto, pode acessar os atributos nome e idade diretamente, já que esses são definidos no construtor da classe pai.
II: O método apresentar() da classe Funcionario sobrepõe o método da classe Pessoa e chama o método da classe pai usando super.apresentar().
III: O JavaScript suporta herança de classes a partir do ES6, então a afirmação é falsa.

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

______

**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

b) A asserção é verdadeira e a razão é falsa.  A alternativa correta é b) porque A asserção é verdadeira e a razão é falsa.
Asserção: O polimorfismo realmente permite que objetos de diferentes tipos respondam de maneiras diferentes à mesma mensagem. Isso é verdadeiro.
Razão: A afirmação de que o polimorfismo é implementado por sobrecarga de métodos está errada, pois JavaScript não suporta sobrecarga de métodos.
Portanto, a asserção é verdadeira e a razão é falsa.

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

______

# Questões dissertativas
9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

function somaArray(numeros) {
    let soma = 0;  // Inicializa a variável soma
    for (let i = 0; i < numeros.length; i++) {  // Usar .length para o tamanho do array
        soma += numeros[i];  // Soma cada elemento ao total
    }
    return soma;  // Retorna o valor total
}

console.log(somaArray([1, 2, 3, 4]));  // Saída: 10

______
10) Crie um exemplo prático no qual você tenha duas classes:
// Função para criar um Produto
function criarProduto(nome, preco) {
    return {
        nome: nome,
        preco: preco,
        calcularDesconto: function() {
            return this.preco * 0.9; // Aplica 10% de desconto
        }
    };
}

// Função para criar um Livro (modificando o desconto)
function criarLivro(nome, preco) {
    let produto = criarProduto(nome, preco); // Cria um Produto
    produto.calcularDesconto = function() {
        return this.preco * 0.8; // Aplica 20% de desconto para livros
    };
    return produto;
}

// Exemplo de uso:
const produto1 = criarProduto("Camiseta", 100);
console.log(`Preço do produto com desconto: R$ ${produto1.calcularDesconto()}`); // Esperado: 90

const livro1 = criarLivro("JavaScript para Iniciantes", 80);
console.log(`Preço do livro com desconto: R$ ${livro1.calcularDesconto()}`); // Esperado: 64


A parte da herança: Herança: Em vez de usar a herança com extends, modifiquei diretamente o método calcularDesconto() no objeto livro1.
