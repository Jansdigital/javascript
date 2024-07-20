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

