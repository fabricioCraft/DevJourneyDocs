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

