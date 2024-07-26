# Funções em JavaScript
 
## O que é uma função?
Uma função é um bloco de código que realiza uma tarefa específica.
Você escreve a função uma vez e pode usá-la várias vezes no seu programa.
 
## Como criar uma função?
Para criar uma função, você usa a palavra-chave function, seguida pelo nome da função, parênteses e um bloco de código entre `chaves { }`.

## Como usar (chamar) uma função
Depois de criar a função, você pode chamá-la pelo nome para executar o código dentro dela.

---
 
### Exemplo função simples:
```
<script>
function saudacao(){
    console.log('Olá');
}
 
saudacao();
</script>
```
 
---

## Funções com parâmetros
Parâmetros são como variáveis que você passa para a função para que ela possa usar esses valores.

### Exemplo:
```
<script>
function saudacao(nome){
    console.log('Olá ' + nome + '!');
}
saudacao('Janete');
 
</script>
```
--- 
## Funções com retorno
Uma função pode retornar um valor usando a palavra-chave return.
Quando a função é chamada, o valor de retorno pode ser usado em outras partes do programa.

### Exemplo:
 
```
<script>
  function soma(a, b) {
    return a + b;
  }
 
  let resultado = soma(5, 8);
  console.log(resultado);
</script>
```
---
### Funções anônimas
 
Uma função anônima em JavaScript é uma função que não possui um nome e é frequentemente atribuída a uma variável. A atribuição permite que você chame a função usando o nome da variável.
As funções anônimas são úteis para criar funções rapidamente sem a necessidade de nomeá-las.
### Exemplo:
 
```
<script>
 
    let saudacao = function(nome){
        return 'Ola ' + nome + '!';
    }
 
    console.log(saudacao('Cristiano'));
    console.log(saudacao('Pedro'));
 
</script>
```
 
---
## Arrow Functions (Funções de seta)
As arrow functions são uma forma mais curta de escrever funções anônimas.
Elas usam a sintaxe () => {}.
### Exemplo:
 
```
<script>
    let saudacao = () =>{
        console.log('Usando uma função de seta!')
    }
 
    saudacao();
</script>
```
---
## Funções como Objetos
Em JavaScript, funções são objetos de primeira classe, o que significa que podem ter propriedades (variáveis associadas) e métodos.

### Exemplo:
 
```
<script>
    function saudacao() {
        console.log("Olá, eu sou a função saudacao()!");
    }
 
    saudacao.propriedade = 'Eu sou uma propriedade da função';
    saudacao.descricao = 'Eu sou uma descrição sobre a função';
 
    console.log(saudacao.propriedade); // Isso vai imprimir - Eu sou uma propriedade da função
 
    console.log(saudacao.descricao); // Isso vai imprimir - Eu sou uma descrição
 
    saudacao(); // Isso vai imprimir - Olá, eu sou a função saudacao()!
 
</script>
```
---
## Funções Imediatamente Invocadas (IIFE)
Uma IIFE (Immediately Invoked Function Expression) ```Função Imediatamente Invocada```. é uma função que é executada assim que é definida. Isso é útil para criar um escopo local.
### Exemplo:
 
```
<script>
    (function(){
        let mensagem = "Olá, mundo!"; // Variável local dentro da IIFE
        console.log(mensagem); // Imprime "Olá, mundo!" no console
    })();
 
    // Tentar acessar `mensagem` fora da IIFE vai dar erro
    console.log(mensagem);
    // Isso vai gerar um erro porque `mensagem` não está definida fora da IIFE
 
 
</script>
```
---
## Função de callback
É uma função que você passa como argumento para outra função.
A função principal executa a função de callback quando termina seu trabalho.
É uma maneira de garantir que alguma ação seja realizada depois que outra tarefa estiver concluída.
 
## Como Funciona?
1. Criação da Função de Callback: Você define uma função que quer usar depois que outra tarefa terminar.
2. Passagem como Argumento: Você passa essa função como um argumento para outra função.
3. Execução do Callback: A função principal faz o trabalho e, quando termina, executa a função de callback.
 
### Exemplo:
Vamos fazer um exemplo que simula preparar um lanche e, depois, exibir uma mensagem quando o lanche estiver pronto.
[21:26] CRISTIANO BEZERRA MAIA
```
<script>
    // Função que prepara o lanche e usa uma função de callback
function prepararLanche(callback) {
    console.log("Preparando o lanche...");
   
    // Simula o tempo de preparo com setTimeout
    setTimeout(() => {
        console.log("Lanche pronto!");
        callback(); // Chama a função de callback
    }, 4000); // Espera 4 segundos
}
// Função de callback que exibe uma mensagem
function mensagemDePronto() {
    console.log("Agora você pode comer seu lanche.");
}
// Usar a função prepararLanche com mensagemDePronto como callback
prepararLanche(mensagemDePronto); // Depois de 4 segundos, exibe a mensagem
 
</script>
```
### O que está acontecendo?
1. Função prepararLanche:
* Simula o preparo de um lanche.
* Usa setTimeout para esperar 4 segundos e depois chama a função de callback.
 
2. Função mensagemDePronto:
* Esta é a função de callback que será chamada quando o lanche estiver pronto.
 
3. Chamada da Função prepararLanche:
* Passamos a função mensagemDePronto como argumento.
* Depois que a espera de 4 segundos terminar, a mensagem "Agora você pode comer seu lanche." será exibida.
 
### Resumindo:
* Função de Callback: É uma função que você passa para outra função.
* Como Funciona: A função principal faz algo e depois usa a função de callback para realizar uma ação adicional.
 
---
 
## O que são Objetos em JavaScript?
* Um objeto é uma coleção de dados e ações.
* Dados são chamados de propriedades.
* Ações são chamadas de métodos.
 
### Exemplo de Objeto
Imagine um objeto chamado pessoa:
 
let pessoa = {
  nome: "Ana",
  idade: 25
};
 
#### Neste exemplo:
 
* nome e idade são propriedades do objeto pessoa.
* pessoa tem um nome (Ana) e uma idade (25).
 
```
<script>
    // Criando um objeto chamado 'pessoa' com propriedades 'nome' e 'idade'
    let pessoa = {
      nome: "Ana",
      idade: 25
    };
 
    // Imprimindo o objeto 'pessoa' no console
    console.log(pessoa);
  </script>
 
```
 
---
 
## O que são Métodos?
* Métodos são ações que os objetos podem realizar.
Pense nos métodos como "coisas que os objetos podem fazer".
 
### Adicionando e chamando um Método de um Objeto
#### Exemplo:
```
 
<script>
    let pessoa = {
        nome: 'Ana',
        idade: 25,
        // Ação que o objeto pessoa pode fazer
        cumprimentar: function () {
            console.log('Olá, meu nome é ' + this.nome);
 
            // this é uma palavra que significa "este objeto"
           
            console.log('Eu tenho '+ this.idade + ' anos')
        }
    };
 
    pessoa.cumprimentar();
 
</script>
```
 
#### Resumo
Objetos são coleções de dados (propriedades) e ações (métodos).
* ``Propriedades`` são os dados do objeto.
* ``Métodos`` são as ações que os objetos podem realizar.
* ``this`` dentro dos métodos se refere ao próprio objeto.
 
 
#### Mais um Exemplo
Vamos criar um objeto animal que pode falar a sua espécie e aumentar a idade:
 
```
<script>
    let animal = {
        nome: 'Rex',
        especie: 'Cachorro',
        idade: 5,
        // Método "Ação" que o objeto animal pode fazer
        descrever: function () {
            console.log('Animal: ' + this.nome + ', Espécie: ' + this.especie + ', Idade: ' + this.idade);
        },
        // Outro método "ação" que o objeto animal pode fazer
        fazerAniversario: function () {
            this.idade += 1;
            console.log(this.nome + ' agora tem ' + this.idade + ' anos.');
        }
    };
 
    // Chamando métodos
    animal.descrever(); // Saída: Animal: Rex, Espécie: Cachorro, Idade: 5
    animal.fazerAniversario(); // Saída: Rex agora tem 6 anos.
 
</script>
 
```
 
---