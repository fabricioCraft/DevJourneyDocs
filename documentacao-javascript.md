# Sumário

- [Variáveis](#variáveis)
    - [Tipos de Variáveis](#tipos-de-variáveis)
    - [Escopo](#escopo)
- [Operadores](#operadores)
- [Template Strings](#template-strings)
- [Condicionais IF e Else](#condicionais-if-e-else)
- [Condicionais IF, ELSE e ELSE IF](#condicionais-if-else-e-else-if)
- [Truthy e Falsy](#truthy-e-falsy)
- [Ternário](#ternário)
- [Operador de Negação ``!`` (NOT)](#operador-de-negação--not)
- [Operador lógico AND ``&&``](#operador-lógico-and-)
- [Operador lógico OR ``||``](#operador-lógico-or-)
- [Arrays](#arrays)
    - [Como acessar itens do array](#como-acessar-itens-do-array)
    - [Como alterar itens do array](#como-alterar-itens-do-array)
    - [Como adicionar itens ao array](#como-adicionar-itens-ao-array)
    - [Como saber o tamanho do array](#como-saber-o-tamanho-do-array)
- [Loop While](#loop-while)
- [Loop For](#loop-for)
- [Loop For...of](#loop-forof)
- [Break](#break)
- [Continue](#continue)
- [Loop for em Strings](#loop-for-em-strings)
- [Objetos](#objetos)
    - [Como criar objetos](#como-criar-objetos)
    - [Como acessar propriedades de um objeto](#como-acessar-propriedades-de-um-objeto)
    - [Como alterar e adicionar propriedades de um objeto](#como-alterar-e-adicionar-propriedades-de-um-objeto)
    - [Array de Objetos](#array-de-objetos)
    - [Tipagem de Objetos em TypeScript](#tipagem-de-objetos-em-typescript)
    - [Desestruturação de Objetos](#desestruturação-de-objetos)
    - [Rest Operator](#rest-operator)
    - [Spread Operator](#spread-operator)
- [Função](#função)
    - [SetTimeout](#settimeout)
    - [SetInterval](#setinterval)
    - [Arrow Functions](#arrow-functions)
    - [Parâmetros da função](#parâmetros-da-função)
- [Método de String](#método-de-string)
    - [Trim](#trim)
    - [TrimStart](#trimstart)
    - [TrimEnd](#trimend)
    - [toUpperCase e toLowerCase](#touppercase-e-tolowercase)
    - [substring](#substring)
    - [slice](#slice)
    - [split](#split)
    - [replace e replaceAll](#replace-e-replaceall)
    - [padStart e padEnd](#padstart-e-padend)
    - [indexOf e includes](#indexof-e-includes)
- [Métodos de Array](#métodos-de-array)
    - [push](#push)
    - [pop](#pop)
    - [shift](#shift)
    - [unshift](#unshift)
    - [indexOf](#indexof)
    - [includes](#includes)
    - [reverse](#reverse)
    - [join](#join)
    - [slice](#slice)
    - [splice](#splice)
    - [every](#every)
    - [some](#some)
    - [find](#find)
    - [findIndex](#findindex)
    - [filter](#filter)
    - [map](#map)
- [Importação e Exportação de módulos](#importação-e-exportação-de-módulos)
- [Exportação Individual com ES modules](#exportação-individual-com-es-modules)
- [Export default](#export-default)
- [Criando um servidor](#criando-servidor)
 - [Com fastify](#com-fastify)
 - [Com express](#com-express)
 - [Nodemon](#nodemon)
 - [Parâmetros de rota](#parâmetros-de-rotas)
 - [Parâmetros de pesquisa](#parâmetros-de-pesquisa)
 - [Intermediários](#intermediários)
 - [Intermediários gerais](#intermediários-gerais)
 - [Controladores](#controladores)
 - [API REST](#api-rest)
 - [Métodos HTTP](#métodos-http)
 = [Código de Resposta HTTP](#código-de-resposta-http)


# Variáveis

Identificadores que recebem nome e são usadas para armazenar dados.

As variáveis são fundamentais para a programação, pois fornecem um meio de lidar com informações dinâmicas, permitindo que você armazene, manipule e recupere dados dentro de um programa.

## Tipos de variáveis

Os tipos de variáveis existentes são `var`, `let`, `const`.

- `var` - é o tipo de variável que possui o escopo global. Isso significa que ela é visível em qualquer lugar em que é chamada, independente do seu valor.

- `let` - Foi implementado a partir do EcmaScript 6 (ES6) e possui escopo local. Diferente do `var`, ela **só é válida dentro do bloco em que foi declarada**. Tanto `var` quanto `let` podem ter seus valores **reatribuidos**.

-`const` - Também foi implementado a partir do EcmaScript 6 (ES6) e possui o mesmo escopo do `let`, porém o valor definido inicialmente para uma `const` **não pode ser reatribuido.** **Representa uma constante.**

## Escopo

**O escopo refere-se ao contexto em que uma variável é acessível.** Ele determina onde a variável pode ser usada dentro de um programa. Um escopo pode ser **global**, acessível a todo o programa, ou **local**, acessível apenas dentro de um determinado bloco de código.

Por exemplo, se declaramos uma variável dentro de uma função em JavaScript, essa variável terá escopo local e só poderá ser acessada dentro dessa função. Já se declaramos uma variável fora de qualquer função, ela terá escopo global e poderá ser acessada em qualquer parte do código.

O escopo serve para garantir a integridade e segurança do código, evitando conflitos de nomes entre variáveis e facilitando a organização do programa. Além disso, o escopo ajuda a otimizar o uso de memória, pois variáveis locais são liberadas da memória assim que o bloco de código em que estão é finalizado.

Portanto, entender e utilizar corretamente o escopo é fundamental para escrever códigos mais limpos, seguros e eficientes em programação. 

# Operadores

Os operadores são símbolos que representam ações a serem realizadas em operandos, como variáveis, valores ou expressões. Em programação, os operadores são utilizados para realizar operações matemáticas, lógicas, de comparação, entre outras.

Alguns exemplos de operadores comuns em linguagens de programação são:

- Operadores aritméticos: como adição (+), subtração (-), multiplicação (*), divisão (/) e módulo (%), que realizam operações matemáticas básicas.

- Operadores de atribuição: como igual (=), que atribui um valor a uma variável, e operadores combinados de atribuição, como +=, que adiciona um valor à variável e atribui o resultado de volta à variável.

- Operadores de comparação: como igualdade (==), desigualdade (!=), maior que (>), menor que (<), maior ou igual (>=), menor ou igual (<=), que são utilizados para comparar valores.

- Operadores lógicos: como AND (&&), OR (||), NOT (!), que são utilizados para combinar expressões lógicas e tomar decisões condicionais.

- Operadores de incremento e decremento: como ++ e --, que incrementam e decrementam o valor de uma variável, respectivamente.

Os operadores são essenciais para realizar diversas tarefas em programação, desde cálculos matemáticos simples até tomadas de decisão mais complexas com base em condições lógicas. É importante compreender o funcionamento e a precedência dos operadores para escrever códigos corretos e eficientes.

Em programação, especialmente em linguagens como JavaScript, a diferença entre os operadores de comparação "==" e "===" é fundamental.

O operador "==" compara dois valores, permitindo a conversão de tipos durante a comparação. Isso significa que, ao utilizar o operador "==", os valores são convertidos para um mesmo tipo antes da comparação ser realizada. Por exemplo, ao comparar um número com uma string que represente o mesmo número utilizando "==", o JavaScript irá converter o tipo da string para número antes de realizar a comparação.

Por outro lado, o operador "===" realiza uma comparação estrita, também conhecida como comparação de identidade. Nesse caso, além de comparar os valores, o JavaScript verifica se os tipos dos valores são iguais. Isso significa que os valores devem ser do mesmo tipo e ter o mesmo valor para que a comparação retorne verdadeira.

Em resumo, o operador "==" é mais flexível, permitindo a conversão automática de tipos durante a comparação, enquanto o operador "===" é mais rigoroso, exigindo que os valores sejam do mesmo tipo e tenham o mesmo valor para que a comparação seja verdadeira.

Portanto, é recomendável utilizar o operador "===" para comparações mais seguras e precisas, evitando comportamentos inesperados devido à conversão automática de tipos.

# Template Strings

Template strings, ou strings de modelo, são uma funcionalidade comum em linguagens modernas de programação, como JavaScript. Elas permitem a criação de strings mais legíveis e com mais funcionalidades do que as strings tradicionais delimitadas por aspas simples ou duplas.

Em JavaScript, as template strings são delimitadas por crases (`) e podem conter expressões embutidas dentro de ${}. Isso permite a interpolação de variáveis e a execução de códigos dentro da própria string.

As template strings facilitam a concatenação de strings e a formatação de texto de uma maneira mais intuitiva e limpa. Além disso, elas permitem a quebra de linha e a formatação de texto de forma mais visualmente agradável, o que é especialmente útil para a criação de mensagens ou blocos de texto extensos.

Por exemplo, em JavaScript, podemos usar template strings para criar mensagens dinâmicas que incluam variáveis:

```javascript
const nome = "Emily";
const idade = 30;

const mensagem = `Olá, meu nome é ${nome} e tenho ${idade} anos.`;
```

Dessa forma, as template strings oferecem uma maneira mais versátil e legível de manipular strings em comparação com as strings tradicionais. Elas são amplamente utilizadas em aplicações web e têm se tornado uma prática comum em linguagens de programação modernas.

# Condicionais IF e ELSE

É usada executar uma afirmação verificando se uma condição é verdadeira ou falsa.

```js
if (condição) {
    // código a ser executado se a condição for verdadeira
} else {
    // código a ser executado se a condição for falsa
}

```

# Condicionais IF, ELSE e ELSE IF

Quando for necessário verificar mais de uma condição, podemos usar a condicional `else if`.

```js
if (condição) {
    // código a ser executado se a condição 1 for verdadeira
} else if (condição) {
    // código a ser executado se a condição 2 for verdadeira
} else {
    // código a ser executado se nenhuma das condições anteriores for verdadeira
}
```

# Truthy e Falsy

Diferença entre Truthy e Falsy:

- Truthy: Qualquer valor que não é Falsy é considerado Truthy.
- Falsy: Valores que são considerados falsos em contextos que esperam um booleano.

```js
console.log(Boolean(0)); // falshy
console.log(Boolean(null)); // falshy
console.log(Boolean(undefined)); // falshy
console.log(Boolean("")); // falshy
console.log(Boolean(NaN)); // falshy
console.log(Boolean(false)); // falshy
```

# Ternário

Operador que permite realizar uma operação condicional de forma mais compacta.

```js
condição ? expressão1 /*se a condição for verdadeira*/ : expressão2 /*se a condição for falsa*/
```

Exemplo:

```js
const idade = 18;
const resultado = idade >= 18 ? "Maior de idade" : "Menor de idade";
console.log(resultado); // Maior de idade
```

# Operador de Negação ``!`` (NOT)

O operador de negação ``!`` é um operador  que inverte o valor de uma expressão. Se a expressão for verdadeira, o operador de negação a tornará falsa, e vice-versa.

```js
const valor = true;
const resultado = !valor;
console.log(resultado); // false
```

Podemos usar, por exemplo, quando queremos verificar se o nome foi digitado pelo usuário no formulário.

# Operador lógico AND ``&&``

O operador lógico AND ``&&`` é um operador que retorna true se ambas as expressões forem verdadeiras.

```js
const valor1 = true;
const valor2 = true;
const resultado = valor1 && valor2;
console.log(resultado); // true
```

# Operador lógico OR ``||``

O operador lógico OR ``||`` é um operador que retorna true se uma das expressões for verdadeira.

```js
const valor1 = true;
const valor2 = false;
const resultado = valor1 || valor2;
console.log(resultado); // true
```

# Arrays

Arrays são estruturas de dados que permitem armazenar uma coleção de valores em uma única variável. Cada valor dentro do array é identificado por um índice, ou index, que começa do zero. Também pode ser chamado de lista.

```js
const array = [1, 2, 3, 4, 5];
console.log(array[0]); // 1
console.log(array[1]); // 2
```
## Como acessar itens do array

Para acessar um item específico do array, usamos a propriedade `[]` e o índice do item que queremos acessar.

```js
const array = [1, 2, 3, 4, 5];
console.log(array[0]); // 1
console.log(array[1]); // 2
```

## Como alterar itens do array

Para adicionar ou alterar um item específico do array, usamos a propriedade `[]` e o índice do item que queremos adicionar ou alterar.

```js
const array = [1, 2, 3, 4, 5];
array[0] = 10;
console.log(array); // [10, 2, 3, 4, 5]
```

## Como adicionar itens ao array

Para adicionar um item na última posição do array, usamos o método `push()`.

```js
const array = [1, 2, 3, 4, 5];
array.push(6);
console.log(array); // [1, 2, 3, 4, 5, 6]
```

outra forma de adicionar um item, é chamar a variável e passar o índice do item que queremos adicionar e o valor do item.

```js
const array = [1, 2, 3, 4, 5];
array[6] = 10;
console.log(array); // [1, 2, 3, 4, 5, 10]
```

## Como saber o tamanho do array

Para saber o tamanho do array, usamos a propriedade `length`.

```js
const array = [1, 2, 3, 4, 5];
console.log(array.length); // 5
```

# Loop While

O loop `while` é uma estrutura de repetição que executa um bloco de código enquanto uma condição for verdadeira.

```js
let i = 0;
while (i < 5) {
    console.log(i);
    i++;
}
```

# Loop For

O loop `for` é uma estrutura de repetição que executa um bloco de código um número determinado de vezes.

```js
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```

# Loop For...of

O loop `for...of` é uma estrutura de repetição que executa um bloco de código para cada elemento de um array.

```js
const array = [1, 2, 3, 4, 5];
for (const item of array) {
    console.log(item);
}
```

# Break

O break é uma palavra reservada que interrompe o loop.

```js
for (let i = 0; i < 5; i++) {
    if (i === 3){ 
        break
    };
    console.log(i);
}
```

# Continue

O continue é uma palavra reservada que interrompe a iteração atual do loop e continua para a próxima iteração.

```js
for (let i = 0; i < 5; i++) {
    if (i === 3){ 
        continue
    };
    console.log(i);
}
```
# Loop for em Strings

O loop `for` pode ser usado para iterar sobre os caracteres de uma string.

```js
const string = "Hello";
for (let i = 0; i < string.length; i++) {
    console.log(string[i]);
}
```

# Objetos

É uma estrutura de dados que permite armazenar uma coleção de dados em uma **única variável.**

Exemplo:

```js
const objeto = {
    nome: "João",
    idade: 20,
    cidade: "São Paulo"
};
```

Cada informação dentro do objeto é uma **propriedade (membro)** e o valor da propriedade é o valor que queremos armazenar.

## Como criar objetos

Para criar um objeto, usamos as chaves `{}`, como exemplificado abaixo:

```js
const objeto = {
    nome: "João",
    idade: 20,
    cidade: "São Paulo"
};
```

## Como acessar propriedades de um objeto

Para acessar uma propriedade de um objeto, usamos o nome do objeto seguido da propriedade que queremos acessar.

```js
const objeto = {
    nome: "João",
    idade: 20,
    cidade: "São Paulo"
};
console.log(objeto.nome); // João
console.log(objeto.idade); // 20
console.log(objeto.cidade); // São Paulo
```
## Como alterar e adicionar propriedades de um objeto

Para alterar ou adicionar uma propriedade de um objeto, usamos o nome do objeto, a propriedade que queremos alterar e o novo valor.

```js
const objeto = {
    nome: "João",
    idade: 20,
    cidade: "São Paulo" 
};
objeto.nome = "Maria";
console.log(objeto.nome); // Maria
```
## Array de Objetos

Podemos criar um array de objetos, como por exemplo:

```js
const arrayDeObjetos = [
    { nome: "João", idade: 20, cidade: "São Paulo" },
    { nome: "Maria", idade: 30, cidade: "Rio de Janeiro" }
];
```

Para que possamos acessar os dados de um array de objetos, podemos usar o loop `for...of`.

```js
for (const item of arrayDeObjetos) {
    console.log(item.nome);
}
```

## Tipagem de Objetos em TypeScript

Em TypeScript, os objetos são tipados estaticamente, o que significa que o tipo de dado de um objeto deve ser definido no momento da criação do objeto.

```ts
type TPessoa = {
    nome: string;
    idade: number;
};

const pessoa: Pessoa = {
    nome: "João",
    idade: 20
};
```

Podemos também definir o tipo de um objeto como sendo opcional, utilizando o `?`.

```ts
type TPessoa = {
    nome: string;
    idade?: number;
};

```

## Desestruturação de Objetos

A desestruturação de objetos é uma funcionalidade que permite extrair valores de um objeto e atribuí-los a variáveis individuais.

Sua funcionalidade prática é que ela permite que você pegue apenas os valores que você precisa de um objeto, sem precisar criar uma variável para cada valor.

A desestruturação de objetos tem várias utilizações práticas:

1. Simplificação de código: Permite extrair múltiplas propriedades de um objeto de forma concisa.

2. Atribuição de variáveis: Facilita a criação de variáveis locais a partir de propriedades de objetos.

3. Parâmetros de funções: Pode ser usada para extrair valores específicos de objetos passados como argumentos.

4. Renomeação de variáveis: Permite atribuir nomes diferentes às variáveis extraídas.

5. Valores padrão: Possibilita definir valores padrão para propriedades que podem não existir no objeto.

6. Aninhamento: Pode ser usada para desestruturar objetos aninhados.

Exemplos:


```ts
const pessoa = {
    nome: "João",
    idade: 20
};

const { nome, idade } = pessoa;
console.log(nome); // João
console.log(idade); // 20
```
## Rest Operator

O rest operator é uma funcionalidade que permite que você pegue os valores restantes de um objeto e atribuia a uma nova variável.

```ts
const pessoa = {
    nome: "João",
    idade: 20,
    cidade: "São Paulo"
};

const { nome, ...resto } = pessoa;
console.log(nome); // João
console.log(resto); // { idade: 20, cidade: "São Paulo" }
```

## Spread Operator

O spread operator é uma funcionalidade que permite espalhar (spread) os elementos de um objeto ou array em outro objeto ou array. Sua sintaxe é representada por três pontos (...) seguidos do objeto ou array que se deseja espalhar.

A funcionalidade prática do spread operator inclui:

1. Cópia de arrays ou objetos: Permite criar uma cópia superficial de arrays ou objetos, permitindo a criação de novas instâncias com valores idênticos.

2. Concatenação de arrays: Simplifica a concatenação de arrays, permitindo a adição de elementos de um array a outro sem a necessidade de loops manuais.

3. Passagem de argumentos em funções: Permite passar elementos de um array como argumentos para uma função, evitando a necessidade de listar cada elemento separadamente.

4. Combinação de arrays ou objetos: Permite combinar facilmente arrays ou objetos em um único array ou objeto, facilitando a manipulação de dados.

Exemplos:

```ts
const array1 = [1, 2, 3];
const array2 = [4, 5, 6];
const array3 = [...array1, ...array2];
console.log(array3); // [1, 2, 3, 4, 5, 6]
```
# Função

As funções são blocos de código reutilizáveis que executam uma tarefa específica. Elas são fundamentais na programação, pois permitem organizar o código, evitar repetições e tornar o programa mais modular e fácil de manter.

Características principais das funções:

1. Podem receber parâmetros (dados de entrada)
2. Podem retornar um valor (resultado)
3. Podem ser chamadas várias vezes no programa
4. Ajudam a organizar e estruturar o código

Exemplo básico de uma função em JavaScript:

```js
function nomeDaFuncao(parametros) {
    // corpo da função
}
```
## setTimeout()

O método `setTimeout()` executa uma função depois de um tempo especificado.

O método recebe os parâmetros da função e o tempo em milissegundos como argumentos.

O parâmetro da função, é passado sem os `()`, pois o objetivo não é executar a função imediatamente e sim após um tempo especificado.

Também pode ser criada uma função dentro da função `setTimeout()`, nesse caso não é necessário passar o nome da função.

A prática de chamar uma função dentro da outra é chamado de **callback functions**.

Exemplo:

```js
function olaMundo (){
    console.log("Ola mundo!");
}

setTimeout(olaMundo, 3000);

setTimeout(function () {
    console.log("Ola mundo!");
}, 3000); 

// A função será executada em 3 segundos.
```

## setInterval()

O método `setInterval()` executa uma função em um intervalo de tempo especificado.

O método recebe os parâmetros da função e o tempo em milissegundos como argumentos. 

Para fazer com que a função pare de ser executada, o método `clearInterval()` deve ser chamado.

Exemplo:

```js
let contador = 10 // inicia a contagem em 10
const id = setInterval(() => {
    // imprime a contagem
    console.log(contador)
    // diminui a contagem em 1 a cada intervalo especificado
    contador-- 

    // verifica se a contagem chegou a zero
    if(contador === 0){
        console.log(contador)
        console.log('Boooooooooom!')
        // interrompe a função
        clearInterval(id)
    }

}, 1000) // Faz com que a função seja executada a cada 1 segundo
```

## Parâmetros da função

Os parâmetros da função são valores que podem ser passados para a função quando ela é chamada. Eles permitem que a função receba dados externos e os utilize em seu processamento interno.

Características dos parâmetros de função:

1. Podem ser de qualquer tipo de dado (números, strings, objetos, arrays, etc.)
2. São opcionais, uma função pode não ter parâmetros
3. Podem ter valores padrão definidos

Exemplos de funções com parâmetros:

```js
function soma(a, b) {
    return a + b;
}

console.log(soma(1, 2)); // 3
```



## Arrow Functions

São uma forma mais curta de escrever funções.

As Arrow Functions são uma sintaxe mais concisa para escrever funções em JavaScript, introduzidas no ECMAScript 6 (ES6). Elas oferecem uma maneira mais curta de definir funções, especialmente útil para funções anônimas e callbacks.

Características principais das Arrow Functions:

1. Sintaxe mais curta
2. Não podem ser usadas como construtores
3. Melhor para funções de callback e funções anônimas

Exemplos de Arrow Functions:

```js
const nomeDaFuncao = (parametros) => {
    // corpo da função
}
```

# Métodos de String

## Trim

O método `trim` remove todos os espac	os iniciais e finais de uma string.

Para utilizá-lo é necessario armazená-lo em uma variável e passar a variável que deseja eliminar os espaços dentro do parenteses.

Exemplo:

`````js
const string = '   Ola, mundo!   ';

console.log(string) // Saída esperada:
//'   Ola, mundo!   '

console.log(string.trim()) // Saída esperada: 'Ola, mundo!'
`````

### trimStart

Remove todos os espaços iniciais de uma string.

### trimEnd

Remove todos os espaços finais de uma string.

## toUpperCase e toLowerCase

O método `toUpperCase` converte uma string para maiúsculas e o `toLowerCase` converte uma string para minúsculas.

Exemplo:

````js
const texto = 'bEM ViNdO, mUNdO'

console.log(texto.toUpperCase()) // 'BEM VINDO, MUNDO'

console.log(texto.toLowerCase()) // 'bem vindo, mundo'
````
## Substring

O método `substring` retorna uma parte de uma string.

Caso um índice seja negativo, o ``substring`` converterá o índice para zero.

No caso do primeiro índice for maior do que o segundo, o ``substring`` muda a posição dos índices.


Exemplo:

````js
const texto = 'Bem vindo, mundo'

const parteDaString = texto.substring(4, 9)
const parteDaString2 = texto.substring(texto.length - 5)

console.log(parteDaString) //vindo
console.log(parteDaString2) //mundo
````

## Slice

O método `slice` retorna uma parte de uma string.

A diferença do `slice` para o `substring` é o tratamento de índices negativos.

O `slice` te permite utilizar índice negativo para selecionar uma parte da string e nesse caso ele começa a contagem do final da string para o início.

Exemplo:

````js
const texto = 'Bem vindo, mundo'

const parteDaString = texto.slice(-5, -1) // 'mund'
````
## Split

O método ``split()`` divide uma String em um array de strings. A divisão é feita procurando um padrão, onde o padrão é fornecido como o primeiro parâmetro na chamada do método.

Exemplo:

````js
const texto = 'Bem vindo, mundo'

const parteDaString = texto.split(' ')

console.log(parteDaString) // ['Bem', 'vindo,', 'mundo']
````
## Replace e ReplaceAll

O método `replace` substitui uma string por outra. O método `replaceAll` substitui todas as ocorências de uma string por outra.

Exemplo:

````js
const texto = 'Bem vindo, mundo. O mundo está belo hoje.'

const parteDaString = texto.replace('mundo', 'planeta')

console.log(parteDaString) // 'Bem vindo, planeta. O mundo está belo hoje'

const parteDaString = texto.replaceAll('mundo', 'planeta')

console.log(parteDaString) // 'Bem vindo, planeta. O planeta está belo hoje.'
````
## PadStart e PadEnd

O método `padStart()` preenche a string no começo com um caractere ou string de substituição  e `padEnd()` será usado para preencher a string no final.

Exemplo:

````js
const texto = 'Bem vindo, mundo. O mundo está belo hoje.'

const parteDaString = texto.padStart(50, '.')

console.log(parteDaString) // '.........Bem vindo, mundo. O mundo está belo hoje.'

const parteDaString = texto.padEnd(50, '.')

console.log(parteDaString) // 'Bem vindo, mundo. O mundo está belo hoje.........'
````

## indexOf e includes

O método `indexOf` retorna o índice de um caractere ou string dentro de uma string. O método `includes` retorna um valor booleano que indica se um caractere ou string está dentro de uma string.

Exemplo:

````js
const texto = 'Bem vindo, mundo. O mundo está belo hoje.'

const parteDaString = texto.indexOf('mundo')

console.log(parteDaString) // 11

const parteDaString = texto.includes('mundo')

console.log(parteDaString) // true
````
# Métodos de array

## push()

O método `push()` adiciona um ou mais elementos ao final de um array e retorna o novo comprimento do array.

A diferença da utilização do método `push()` para `array[array.length]` é que o `push()` te permite adicionar mais de um elemento ao mesmo tempo.

Para retornar o tamanho do array utilizando o método `push()`, é necessário atribuir a uma variável.

Exemplo:

````js
const array = [1, 2, 3, 4, 5]

array.push(6, 7, 8)

console.log(array) // [1, 2, 3, 4, 5, 6, 7, 8]

const tamanhoArray = array.push(6,7,8)

console.log(tamanhoArray) // 10
````

## pop()

O método `pop()` remove e retorna o último elemento de um array.

Para retornar o elemento removido, basta atribuir a uma variável.

Exemplo:

````js
const array = [1, 2, 3, 4, 5]

array.pop()

console.log(array) // [1, 2, 3, 4]

const elementoRemovido = array.pop()

console.log(elementoRemovido) // 5
````

## shift()

O método `shift()` remove e retorna o primeiro elemento de um array.

Para retornar o elemento removido, basta atribuir a uma variável.

Exemplo:

````js
const array = [1, 2, 3, 4, 5]

array.shift()

console.log(array) // [2, 3, 4, 5]

const elementoRemovido = array.shift()

console.log(elementoRemovido) // 1
````

## unshift()

O método `unshift()` adiciona um ou mais elementos no comeco de um array e retorna o novo comprimento do array.

Para retornar o tamanho do array utilizando o método `unshift()`, é necessário atribuir a uma variável.

Exemplos:

````js
const array = [1, 2, 3, 4, 5]

array.unshift(0)

console.log(array) // [0, 1, 2, 3, 4, 5]

const tamanhoArray = array.unshift(0)

console.log(tamanhoArray) // 6
````

## indexOf()

O método `indexOf()` retorna o índice de um elemento dentro de um array e retorna `-1` caso o elemento não esteja no array.

É necessário tomar cuidado quando utilizá-lo com array de objetos, pois ele faz uma comparação entre os objetos tratando o objeto como novo e isso retorna `-1`, mesmo se o objeto tiver as mesmas propriedades e os mesmos valores.

Exemplo:

````js
const array = [1, 2, 3, 4, 5]

const indice = array.indexOf(3)

console.log(indice) // 2
````

## includes()

O método `includes()` retorna um valor booleano que retorna `true` se um elemento estiver no array e `false` caso contrário.

É necessário tomar cuidado quando utilizá-lo com array de objetos, pois ele faz uma comparação entre os objetos tratando o objeto como novo e isso retorna `false`, mesmo se o objeto tiver as mesmas propriedades e os mesmos valores.

Exemplo:

````js
const array = [1, 2, 3, 4, 5]

const inclui = array.includes(3)

console.log(inclui) // true
````

## reverse()

O método `reverse()` inverte a ordem dos elementos de um array.

Exemplo:

````js
const array = [1, 2, 3, 4, 5]

array.reverse()

console.log(array) // [5, 4, 3, 2, 1]
````

## join()

O método `join()` junta todos os elementos de um array em uma string separados pelo caractere passado como parâmetro.

Exemplo:

````js
const array = [1, 2, 3, 4, 5]

const string = array.join('-')

console.log(string) // 1-2-3-4-5
````

## slice()

O método `slice()` seleciona uma parte de uma string e retorna uma nova string.

Exemplo:

````js
const paises = ['Brasil', 'Argentina', 'Chile']

const novoArray = paises.slice(1)

console.log(novoArray) // ['Argentina', 'Chile']

const novoArray = paises.slice(1, 3)

console.log(novoArray) // ['Argentina', 'Chile']
````

## splice()

O método `splice()` remove elementos do array e adiciona novos elementos no lugar do elemento removido.

Exemplo:

````js
const paises = ['Brasil', 'Argentina', 'Chile']

paises.splice(1, 1, 'Paraguai', 'Uruguai')

console.log(paises) // ['Brasil', 'Paraguai', 'Uruguai', 'Chile']
````
## every()

O método `every()` verifica cada item dentro do array e retorna `true` caso todos os itens sejam verdadeiros e `false` caso contrário a partir de uma condição especificada.

O método `every()` recebe uma função como parâmetro.

Exemplo:

````js
const array = [1, 2, 3, 4, 5]

const todosPositivos = array.every((item) => item > 0)

console.log(todosPositivos) // true
````
## some()

O método `some()` verifica cada item dentro do array e retorna `true` caso pelo menos um item seja verdadeiro e `false` caso contrário a partir de uma condição especificada.

O método `some()` recebe uma função como parâmetro.

Exemplo:

````js
const array = [-1, -2, -3, 4, -5]

const peloMenosUmPositivo = array.some((item) => item > 0)

console.log(peloMenosUmPositivo) // true
````

## find()

O método `find()` verifica cada item dentro do array e retorna o primeiro item que satisfaz a condição.

O método `find()` recebe uma função como parâmetro.

Exemplo:

````js
const array = [-1, -2, -3, -4, 5]

const primeiroPositivo = array.find((item) => item > 0)

console.log(primeiroPositivo) // 5
````

## findIndex()

O método `findIndex()` verifica cada item dentro do array e retorna o índice do primeiro item que satisfaz a condição.

O método `findIndex()` recebe uma função como parâmetro.

Exemplo:

````js
const array = [-1, -2, -3, -4, 5]

const primeiroPositivo = array.findIndex((item) => item > 0)

console.log(primeiroPositivo) // 4
````

## filter()

O método `filter()` verifica cada item dentro do array e retorna um novo array com os itens que satisfazem a condição.

O método `filter()` recebe uma função como parâmetro.

Exemplo:

````js
const array = [{
    nome: 'João',
    idade: 16
}, {
    nome: 'Maria',
    idade: 30

},
{
    nome: 'Pedro',
    idade: 40
},
{
    nome: 'Ana',
    idade: 10
}
]

const adultos = array.filter((item) => item.idade >= 18)

console.log(adultos) // [{ nome: 'Maria', idade: 30 }, { nome: 'Pedro', idade: 40 }]
````
## map()

O método `map()` verifica cada item dentro do array e retorna um novo array com os itens modificados.

O método `map()` recebe uma função como parâmetro.

Exemplo:

````js
const array = [1, 2, 3, 4, 5]

const arrayModificado = array.map((item) => item * 2)

console.log(arrayModificado) // [2, 4, 6, 8, 10]
````

## sort()

O método `sort()` ordena os itens de um array de acordo com o código unicode.

Diferente de outros métodos, ele não cria um novo array, mas sim, modifica o array original.

Para fazer a ordenação, ele faz a comparação entre dois argumentos e retorna um valor negativo, 0 ou positivo.

Caso seu retorno seja negativo, o primeiro elemento é menor que o segundo e por isso vem antes.

Caso seu retorno seja positivo, o primeiro elemento é maior que o segundo e por isso vem depois.

Caso seu retorno seja 0, o primeiro elemento é igual ao segundo e por isso não há ordenação de posição. 

Exemplo:

````js
const array = [25, 9, 50, 35, 11, 6, 10]

// ordenação crescente
array.sort((num1, num2) => {

    if (num1 > num2) {
        return 1
    }

    if (num1 < num2) {
        return -1
    }

    return 0

})

//Ou ainda

array.sort((num1, num2) => {
    return num1 - num2
    })

console.log(array) // [6, 9, 10, 11, 25, 35, 50]

// Todas as duas formas acima irão retornar o array ordenado de forma crescente

// ordenação decrescente

const array = [25, 9, 50, 35, 11, 6, 10]

array.sort((num1, num2) => {

    if (num1 > num2) {
        return -1
    }

    if (num1 < num2) {
        return 1
    }

    return 0

})

//Ou ainda

array.sort((num1, num2) => {
    return num2 - num1
    })

console.log(array) // [50, 35, 25, 11, 10, 9, 6]

// Todas as duas formas acima irão retornar o array ordenado de forma decrescente
````

## Ordenação de strings

Para ordenar uma string, além de utilizar o método `sort()`, é necessário utilizar também o método `localeCompare()`.

O método `localeCompare()` faz uma comparação entre duas strings e retorna um valor negativo, 0 ou positivo.

Assim como na ordenação de numerais, o método `localeCompare()` irá retornar um valor negativo, 0 ou positivo e fará a ordenação de acordo com seu retorno.

Se negativo, o primeiro elemento vem antes, positivo o primeiro elemento vem depois e 0 se o primeiro elemento é igual ao segundo.

Exemplo:

````js
const array = ['b', 'd', 'a', 'c', 'e']

// ordenação crescente

array.sort((a, b) => {
    return a.localeCompare(b)
})

console.log(array) // ['a', 'b', 'c', 'd', 'e']

// ordenação decrescente

array.sort((a, b) => {
    return b.localeCompare(a)
})

console.log(array) // ['e', 'd', 'c', 'b', 'a']
````

## Reduce()

O método `reduce()` executa uma função callback e retorna um único valor.

Ele recebe uma função como parâmetro e essa função recebe 4 argumentos:

1. Acumulador
2. Valor atual
3. Índice
4. Array

Exemplo:

````js

const array = [1, 2, 3, 4, 5]

const resultado = array.reduce((acumulador, valorAtual, indice, array) => {

    return acumulador + valorAtual
})

console.log(resultado) // 15

// A função acima retona a soma de todos os elementos do array
````

O método `reduce()` também pode receber um outro parâmetro que é opcional.

Quando ele recebe esse parâmetro que é um número, ele se torna o ``acumulador`` da primeira iteração e o número da primeira posição do array o ``valor atual``.

Exemplo:

````js

const array = [1, 2, 3, 4, 5]

const resultado = array.reduce((acumulador, valorAtual, indice, array) => {

    return acumulador + valorAtual
}, 10)

console.log(resultado) // 25

// A função acima tem o número 10 como o primeiro acumulador e o valor 1 como valor atual na primeira iteração.
````
# Importação e exportação de módulos

Para importar um módulo de um arquivo para ser utilizado em outro arquivo é necessário primeiro exportá-lo da seguinte maneira:

````js

function soma (num1, num2) {
    return num1 + num2
}

const nome = 'Fabrício'

module.exports = {
    soma,
    nome
} // Exportação utilizando o commonJS 

export {
    soma,
    nome
} // Exportação utilizando o ES6
````
E depois importá-lo para o arquivo desejado:

````js
const {soma, nome} = require('./soma')
import {soma, nome} from './soma.js'


console.log(soma(1, 2)) // 3
console.log(nome) // Fabrício
````

# Exportação individual com ES Modules

Para exportar um módulo individualmente, basta utilizar o método `export` na linha de cima do módulo.

````js
export function soma (num1, num2) {
    return num1 + num2
}

export const nome = 'Fabrício'
````

# Export default

O ``export default`` te permite exportar um único valor por arquivo, que pode ser uma função, classe ou objeto.

Ao importá-lo, você pode dar qualquer nome ao que está sendo importado, pois não está atrelado ao nome original.

cada arquivo pode ter apenas um `export default`.

````js
// soma.js
export default function soma(a, b) {
    return a + b;
}

// index.js
import minhaSoma from './soma.js';
console.log(minhaSoma(2, 3)); // Saída: 5
````
# Criando servidor

## Com fastify

O primeiro passo para criar um servidor utilizando a biblioteca fastify é instalá-lo e importá-lo.

Depois que o fastify tiver importado, é necessário instanciar o servidor, ou seja, inicializá-lo, da seguinte forma:

````js
import fastify from 'fastify'
const app = fastify({
    logger: true
})
````

Agora, é necessário criar uma rota, um caminho para o qual o servidor responderá.

A rota recebe dois parâmetros: o caminho e a função que será executada quando o caminho for acessado:

````js
app.get('/', (request, res) => {
   const saudacao = 'Ola mundo!'

   return res.send(saudacao) 
})
````

Feito isso, é necessário passar a porta pela qual o servidor será executado e isso é feito com o método `listen()`.

````js
app.listen({
    port: 3000
})
````

# Com express

````js
import express from 'express'

const app = express()

app.get('/', (request, res) => {
    const saudacao = 'Ola mundo!'

    return res.send(saudacao)
})

ap.listen(3000)
````
# nodemon

O nodemon é uma biblioteca que permite que o servidor seja executado automaticamente quando houver alterações em arquivos.

Para usá-lo, é necessário primeiro instalar a biblioteca.

````js
npm install -D nodemon
````
Em seguida adicioná-lo a lista de scripts do arquivo `package.json`.

Como o nodemon roda o node e o node não entende arquivos .ts, é necessário configurá-lo para que o nodemon execute o `ts-node` para que o node entenda arquivos .ts.
````json

"scripts": {

    "dev": "nodemon --exec ts-node src/server.ts"    
}
````

# Parâmetros de rotas

Os parâmetros de rota são partes dinâmicas da URL que permitem criar rotas flexíveis em uma aplicação. 

Eles são utilizados para passar informações através de uma URL e recuperá-las no servidor para processamento.

````js
// Exemplos de parâmetros de rota
// Rota com parâmetro dinâmico
app.get('/usuario/:id', (req, res) => {
    const userId = req.params.id;
    res.send(`ID do usuário: ${userId}`);
});

// Rota com parâmetros múltiplos
app.get('/produto/:categoria/:id', (req, res) => {
    const { categoria, id } = req.params;
    res.send(`Categoria: ${categoria}, ID do produto: ${id}`);
});
````

# Parâmetros de pesquisa

Os parâmetros de pesquisa servem para filtrar resultados de uma pesquisa.

````js
// Rota com parâmetro de pesquisa
app.get('/produtos', (req, res) => {
    const { categoria } = req.query;
    res.send(`Produtos da categoria: ${categoria}`);
});  
````


# Intermediários

Os intermediários são funções que podem ser chamadas antes que o fluxo de requisição seja passado para o próximo middleware ou para o controlador. 

Eles são utilizados para:
- Verificar se o usuário está autenticado
- Verificar se o usuário tem permissão para acessar a rota
- Adicionar propriedades ao objeto de requisição
- Executar uma lógica de negócios

Exemplo:

````js
// intermediarios.ts

import { NextFunction, Request, Response } from "express";

export const meuPrimeiroIntermediario = (req: Request, res: Response, next: NextFunction) => {
    console.log('Passei pelo intermediário');

    if(req.params.item === 'sair'){
        res.send('A requisição foi respondida pelo intermediário, antes de chegar no controlador')
        return
    }
    
    next()
}

// contoladores.ts

export const itemProdutos = (req: Request, res: Response) => {
    console.log(req.params.item);        
    res.send('Cheguei no controlador')
}

//index.ts
import express, { NextFunction, Request, Response } from 'express'
import {  itemProdutos } from './controladores'
import { meuPrimeiroIntermediario } from './intermediarios'

app.get('/produtos/:item', meuPrimeiroIntermediario ,itemProdutos)
````

# Intermediários Gerais

Os intermediários gerais são funções que são chamadas antes que o fluxo de requisição seja passado para o controlador.

````js
// intermediarios.ts

import { NextFunction, Request, Response } from "express";

export const intermediariosGerais = (req: Request, res: Response, next: NextFunction) => {
    
       console.log('Passou no intermediario geral');
    
    next()
}

// index.ts

app.use(intermediarioGeral)

app.get('/produtos/:item', meuPrimeiroIntermediario ,itemProdutos)

app.get('/usuarios/:email', buscarUsuario)

app.use(intermediarioGeral)

app.get('/usuarios', buscarUsuarioQuery)

````
O intermediário geral fará a verificação para todas as rotas antes de acessá-la.


# Controladores

Os controladores são as rotas que serão processadas pelo servidor.

````js
// controladores.ts

export const itemProdutos = (req: Request, res: Response) => {
    console.log(req.params.item);        
    res.send('Cheguei no controlador')
}

//index.ts
import express, { Request, Response } from 'express'

import { itemProdutos } from './controladores'

app.get('/produtos/:item', itemProdutos)
````

# API REST

API é um conjunto de instruções que determina como se comunicar com um sistema. Diversos sistemas disponibilizam API's para que sejam integradas com outros sistemas.

REST (Representational State Transfer) é um conjunto de restrito de arquitetura que podem ser utilizadas para o desenvolvimento de APIs.

Por exemplo, numa API de um sistema para um biblioteca, livro é um recurso e a listagem de livros é a coleção.

A comunicação ocorre através de requisições e respostas, onde um cliente (por exemplo, um aplicativo) envia uma requisição ao servidor e recebe uma resposta. Essa interação é baseada no protocolo HTTP.

APIs REST trabalham com recursos, que são entidades que o cliente pode manipular. Cada recurso possui um identificador único e é acessado através de endpoints.

Esses dados de requisição e resposta podem ser representados no formato JSON.

O JSON (Javascript Object Notation) é uma notação que utiliza uma estrutura de pares chave-valor, semelhante a um objeto JavaScript, e é amplamente usado para a troca de dados na web.

Por exemplo, se tivermos um objeto representando um usuário, ele poderia ser estruturado da seguinte forma em JSON:

````json
{
  "nome": "Pedro",
  "email": "pedro@arrobaemail.com",
  "idade": 30,
  "curso": {
    "nome": "Desenvolvimento Web",
    "id": 1
  },
  "termosAceitos": true
}
````
Neste exemplo, temos um objeto com várias propriedades, onde cada chave está entre aspas duplas e os valores podem ser strings, números, objetos ou booleanos. Essa estrutura é essencial para a comunicação entre cliente e servidor, especialmente ao enviar dados através de requisições.

## Métodos HTTP

As operações sobre os recursos são realizadas utilizando métodos HTTP, conhecidos como verbos. Os principais verbos incluem:

**GET:** Para obter dados.

**POST:** Para criar novos recursos.

**PUT:** Para atualizar um recurso inteiro.

**PATCH:** Para atualizar parcialmente um recurso.

**DELETE:** Para remover um recurso.

## Código de Resposta HTTP

Em cada resposta de uma requisição HTTP, a API devolve um código numérico para informar o status do que foi solicitado na requisição.

Uma requisição HTTP pode ser bem sucedida ou não, sendo assim, o código devolvido representa sucesso ou erro da requisição.

**Principais grupos de códigos de resposta:**

2xx - Sucesso

    Indica que a requisição foi aceita e processada com sucesso.

4xx - Erro do cliente

    Indica que a requisição foi recebida, porém, possui erros.

5xx - Erro do servidor

    Indica que houve erro interno inesperado do servidor.

**Principais códigos:**

200 - OK

    Requisição bem sucedida.

201 - Created

    Requisição bem sucedida e recurso criado.

204 - No content

    Requisição bem sucedida, sem conteúdo no corpo da resposta.

400 - Bad request

    O servidor não entendeu a requisição pois está com uma sintaxe inválida.

401 - Unauthorized

    O cliente não está autenticado.

403 - Forbidden

    O cliente não tem permissão para acessar o recurso solicitado.

404 - Not found

    O servidor não pode encontrar o recurso solicitado.

500 - Internal server error

    O servidor encontrou um erro inesperado.

# Programação Orientada a Objetos

Programação Orientada a Objetos (POO) é uma abordagem de programação baseada em classes e métodos.

Consiste em implementar estruturas que representam entidades do mundo real.

Existem 4 pilares de POO:

**Abstração:** Simplifica focaando nos aspectos essenciais da implementação.

**Encapsulamento:** Protege os detalhes expondo apenas o necessário. 

**Heranças:** Reutiliza estruturas de outras implementações.

**Polimorfismo:** Permite que uma estrutura tenha diferentes comportamentos.

## Classe

Uma classe define a estrutura e o comportamento de um objeto. Ela serve como um molde para a criação de objetos.

Uma classe pode ter atributos e métodos. Os atributos representam os dados do objeto e os métodos representam as ações que podem ser feitas com o objeto.

Uma classe pode ter uma ou mais instâncias, que são objetos criados a partir da classe. Cada instância tem seus próprios valores para os atributos e os métodos podem ser chamados independentemente em cada instância.

Classes podem ter heranças, o que permite que uma classe herde atributos e métodos de outra classe. Isso permite que as classes sejam reutilizadas e que as funcionalidades sejam estendidas.

Exemplo:

````js
class Carro {
    cor: string =''
    marca: string=''
    modelo: string=''
    ano: number=0
    potencia: number=0
}

const fusca = new Carro()

fusca.ano = 1960
console.log(fusca) // Carro { cor: '', marca: '', modelo: '', ano: 1960, potencia: 0 }
````

## Constructor

Um construtor é um método especial dentro de uma classe que é executado automaticamente quando uma instância da classe é criada.

O construtor tem o nome da classe e não tem um tipo de retorno explícito. Ele sempre retorna a instância da classe.

O construtor é usado para inicializar os atributos da classe com valores padrão.

Exemplo:

````js
class Carro {
    cor: string =''
    marca: string=''
    modelo: string=''
    ano: number=0
    potencia: number=0

    constructor(cor: string, marca: string, modelo: string, ano: number, potencia: number) {
        this.cor = cor
        this.marca = marca
        this.modelo = modelo
        this.ano = ano
        this.potencia = potencia
    
    }
}
````	
## Abstração

A abstração é um conceito fundamental na programação orientada a objetos que permite simplificar a complexidade, focando apenas nos aspectos essenciais de um objeto.

````js
class ContaBancaria {
  private saldo; 
  private titular; // Variável privada, não acessível fora da classe

  constructor(titular) {
    this.titular = titular;
    this.saldo = 0; // Saldo começa em zero
  }

  // Método para depositar dinheiro
  depositar(valor) {
    if (valor > 0) {
      this.saldo += valor;
      console.log(`Depósito de R$${valor} realizado.`);
    } else {
      console.log("Valor inválido para depósito.");
    }
  }

  // Método para sacar dinheiro
  sacar(valor) {
    if (valor > 0 && valor <= this.saldo) {
      this.saldo -= valor;
      console.log(`Saque de R$${valor} realizado.`);
    } else {
      console.log("Saldo insuficiente ou valor inválido.");
    }
  }

  // Método para exibir o saldo
  exibirSaldo() {
    console.log(`Saldo atual: R$${this.#saldo}`);
  }
}

// Exemplo de uso
const conta = new ContaBancaria("João");
conta.depositar(1000);
conta.sacar(300);
conta.exibirSaldo(); // Saldo atual: R$700
````

## Encapsulamento

Encapsulamento em JavaScript é uma técnica que ajuda a proteger e controlar o acesso aos dados de uma classe, limitando a exposição das propriedades e métodos apenas ao que é necessário. Essa prática ajuda a manter o código mais seguro, organizado e fácil de manter, evitando que partes externas possam modificar diretamente os dados internos de uma classe.

# Assincronismo

## Síncrono e Assíncrono

Em programação, temos dois tipos de processamentos: síncrono e assíncrono.

**Síncrono:** Um processamento síncrono executa as operações sequencialmente, esperando que a operação anterior seja concluída antes de executar a próxima. Isso significa que o código espera a resposta do servidor antes de continuar.

**Assíncrono:** Um processamento assíncrono executa as operações em paralelo, sem esperar que a operação anterior seja concluída. Isso significa que o código pode fazer outras coisas enquanto aguarda a resposta do servidor.
## Async e Promises

Em JavaScript, temos dois modos de trabalhar com processamentos assíncronos: `async/await` e `promises`.

**Promises:** Uma Promise é um objeto que representa uma operação assíncrona. Uma Promise pode ter um dos seguintes estados:

- **Pending** (pendente): estado inicial, quando a operação ainda não foi concluída.
- **Fulfilled** (concluída): estado quando a operação foi concluída com sucesso.
- **Rejected** (rejeitada): estado quando a operação falhou.

**Async/Await:** Async/await é uma forma de trabalhar com promises de forma mais legível e fácil de entender. O `async` define uma função que retorna uma Promise, enquanto o `await` suspende a execução da função até que a Promise seja resolvida.

````js
// Exemplo usando Promises

const promessaDeCompra = new Promise((resolve, reject) => {
  const temDinheiro = true;
  
  if (temDinheiro) {
    resolve("Compra realizada com sucesso!");
  } else {
    reject("Saldo insuficiente para compra.");
  }
});

promessaDeCompra
  .then((mensagem) => console.log(mensagem))
  .catch((erro) => console.log(erro));

// Exemplo usando Async/Await

async function fazerCompra(valor) {
  try {
    const saldo = 1000;
    
    if (valor <= saldo) {
      return "Compra realizada com sucesso!";
    } else {
      throw new Error("Saldo insuficiente");
    }
  } catch (erro) {
    console.log(`Erro na compra: ${erro.message}`);
  }
}

// Usando a função async

async function executarCompra() {
  const resultado = await fazerCompra(500);
  console.log(resultado); // "Compra realizada com sucesso!"
  
  const resultadoErro = await fazerCompra(1500);
  // Vai imprimir: "Erro na compra: Saldo insuficiente"
}

executarCompra();

````
### Capturando Promessas Rejeitadas

Quando uma promessa é rejeitada (rejected), significa que ocorreu algum erro durante a execução da operação assíncrona. Para tratar esses erros, podemos usar:

1. O método `.catch()` em Promises
2. O bloco `try/catch` com async/await

Exemplo:
````js
const minhaPromessa = new Promise((resolve, reject) => {
  const operacaoComErro = true;
  
  if (operacaoComErro) {
    reject("Algo deu errado!");
  } else {
    resolve("Operação bem sucedida!");
  }
});

minhaPromessa
  .then(resultado => console.log(resultado))
  .catch(erro => console.log(`Erro capturado: ${erro}`));
````
# Manipulação de Arquivos

## File System

A biblioteca fs (File System) do Node.js é uma ferramenta nativa que permite a manipulação de arquivos de forma eficiente. Ela já vem instalada com o Node.js, o que significa que você pode começar a usá-la imediatamente em seus projetos. 


Ela permite realizar diversas operações em arquivos, incluindo:

- **Leitura de arquivos:** Você pode acessar o conteúdo de arquivos existentes.

- **Escrita de arquivos:** É possível criar novos arquivos ou modificar arquivos existentes.

- **Remoção de arquivos:** Você pode excluir arquivos do sistema.

- **Renomeação de arquivos:** É possível alterar o nome de arquivos já existentes.


A leitura de arquivos pode ser feita de duas maneiras: síncrona e assíncrona.

**Leitura Síncrona**

Para ler um arquivo de forma síncrona, você pode usar o método `fs.readFileSync()`. Esse método bloqueia a execução do código até que a leitura do arquivo seja concluída. Aqui está um exemplo:

````js
const fs = require('fs');

// Lendo o arquivo de forma síncrona
const data = fs.readFileSync('a.txt', 'utf8');
console.log(data); // O conteúdo do arquivo será impresso aqui.

````
Neste exemplo, o código aguarda a leitura do arquivo a.txt antes de prosseguir.

**Leitura Assíncrona**

A leitura assíncrona é feita com o método `fs.readFile()`, que não bloqueia a execução do código. Em vez disso, você passa uma função callback que será chamada quando a leitura for concluída. Veja um exemplo:

````js
const fs = require('fs');

// Lendo o arquivo de forma assíncrona
fs.readFile('a.txt', 'utf8', (err, data) => {
    if (err) {
        console.error(err); // Captura e exibe erros, se houver
        return;
    }
    console.log(data); // O conteúdo do arquivo será impresso aqui.
});
````
Nesse caso, enquanto o arquivo está sendo lido, o código pode continuar executando outras operações.

**Tratamento de Erros**

É importante sempre tratar erros ao lidar com arquivos. Se você tentar ler um arquivo que não existe, por exemplo, o Node.js retornará um erro. No exemplo acima, o erro é capturado e exibido no console.

**Buffers**

Quando você lê um arquivo, o Node.js retorna um "buffer", que é uma área de memória que armazena dados binários do arquivo. Esses dados podem ser convertidos para strings ou outros formatos, dependendo de como você deseja utilizá-los. Por exemplo, se um arquivo contém a palavra "teste", o buffer desse arquivo será uma sequência de números que representam esses dados binários.
