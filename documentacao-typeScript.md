# Sumário
- [TypeScript](#typescript)
- [Tipagem Dinâmica](#tipagem-dinâmica)
- [Typagem Estática](#tipagem-estática)
- [Instalação do TypeScript](#instalação-do-typescript)
- [Rodando um arquivo TS](#rodando-um-arquivo-ts)
- [Transformação do código TS em JS](#transformando-código-ts-em-js)
- [Tipagem de Arrays no Typescript](#tipagem-de-arrays-no-typescript)
- [Tipagem](#tipagem)
    - [Tipos Literais](#tipos-literais)
    - [União de tipos](#união-de-tipos)
    - [Tuplas](#tuplas)
        - [Diferença entre tuplas e tipagem de objetos](#diferença-entre-tuplas-e-tipagem-de-objetos)
    - [Tipos de Conjuntos](#tipos-de-conjuntos)
    


# TypeScript

É um supercojunto do JavaScript, criado pela Microsoft, que permite desenvolver aplicações JavaScript utilizando conceitos e arquiteturas mais sólidas

O TypeScript é usado somente para desenvolvimento do código e não para execução, sendo necessário fazer uma **transpilação** para transformar o código em JavaScript.

Uma grande vantagem do TypeScript é apontar problemas durante o desenvolvimento da aplicação.

Para iniciar um projeto em TypeScript, digite o comando abaixo no terminal. Esse comando irá criar um arquivo de configuração do TypeScript chamado ``ts.config``.

```bash
npx tsc --init
```

# Tipagem Dinâmica

A Tipagem dinâmica permite que uma mesma variável receba uma reatribuição de tipos diferentes.

```js
let nome = 'Guido Cerqueira'
let idade = 33
let estaCadastrado = true //boolean
estaCadastrado = 'sim' //string
```

# Tipagem Estática

O TypeScript possui uma tipagem estática, isso significa que quando uma variável é declarada é necessário definir um tipo para a variável e não é possível fazer uma reatribuição com um outro tipo para a mesma variável.

```ts
let nome : string = 'Guido Cerqueira' // tipagem explícita
let idade : number = 33 // tipagem explícita
let altura = true // tipagem inferida
let estaCadastrado = 'sim' // erro antes de executar
```

Repare que quando não é definido o tipo da variável, o seu tipo é inferido pelo próprio ts, ou seja, o tipo de valor que for atribuída na primeira vez será o tipo definido pelo próprio ts e não será possível mudar o seu tipo. 

# Instalação do TypeScript

Primeiro inicie o projeto no node:

```bash
npm init -y
```

Depois, instale o TypeScript:

```bash
npm install -D typescript
```

# Rodando um arquivo TS

Para rodar um arquivo TS, é necessário instalar a dependência ts-node:

```bash
npm install -D ts-node
```

Feito isso, rode o arquivo com o seguinte comando:

```bash
npx ts-node 'nome-do-arquivo.ts'
```
# Transformando código TS em JS

Ao finalizar o desenvolvimento da aplicação, é necessário fazer a transpilação do código:

```bash
npx tsc 'nome-do-arquivo.ts'
```

# Tipagem de arrays no TypeScript   

Para criar um array no typescript definindo o tipo de variável, podemos usar a tipagem `Array[]`.

```ts
let array : number[] = [1, 2, 3, 4, 5]
```

# Tipagem

## Tipos Literais

Tipos literais, é um tipo que representa um valor específico. 

Eles são úteis quando você deseja criar tipos que são mais restritos do que os tipos genéricos.

Aqui estão alguns exemplos de tipos literais em TypeScript:

````ts
type NumeroQuarentaDois = 42;
type StringHello = 'hello';
type BooleanTrue = true;
````
## União de tipos

A união de tipos (Union Types) no TypeScript permite que uma variável ou parâmetro possa ter mais de um tipo. Isso é útil quando você quer permitir que um valor seja de diferentes tipos.


Abaixo temos exemplos de tuplas em TypeScript:

```ts
type ResultadoOperacao = number | string;
```

No exemplo acima, a definição de tipos permite que a variável receba tanto valores do tipo numéricos quanto do tipo string.

## Tuplas

Tuplas são estruturas de dados semelhantes a arrays, mas com um número fixo de elementos e tipos específicos para cada posição. Elas são úteis quando você precisa representar um conjunto de valores com tipos diferentes, mas em uma ordem específica e com um tamanho predefinido. As tuplas permitem maior controle sobre a estrutura dos dados e fornecem verificação de tipo mais rigorosa em comparação com arrays comuns.

### Diferença entre tuplas e tipagem de objetos

**Tuplas são geralmente preferíveis quando:**

1 - Você tem um número fixo e pequeno de elementos.

2 - A ordem dos elementos é importante.

3 - Os tipos dos elementos são diferentes.

4 - Você não precisa nomear os elementos.

**Objetos são geralmente melhores quando:**

1 - Você tem muitos elementos ou um número variável deles.

2 - A ordem dos elementos não é importante.

3 - Você precisa nomear os elementos para maior clareza.

4 - Você quer adicionar métodos ou comportamentos aos dados.

Exemplos:

```typescript
// Exemplo de tupla
type Coordenada = [number, number];
let ponto: Coordenada = [10, 20];

// Exemplo de objeto
type Ponto = {
  x: number;
  y: number;
};
let pontoObj: Ponto = { x: 10, y: 20 };

// Tupla para representar uma pessoa (nome, idade, ativo)
type Pessoa = [string, number, boolean];
let pessoa: Pessoa = ["João", 30, true];

// Objeto para representar uma pessoa
type PessoaObj = {
  nome: string;
  idade: number;
  ativo: boolean;
};
let pessoaObj: PessoaObj = { nome: "João", idade: 30, ativo: true };

```

Use tuplas quando a estrutura for simples e a ordem for importante. Use objetos quando precisar de mais flexibilidade ou clareza nos nomes dos campos.

## Tipos de conjuntos

Os tipos de conjuntos permitem concatenar dois tipos complementares em uma única variável utilizando o identificador `&`.

Exemplo:

```ts
type TUsuario = {
    nome: string
    email: string
    idade: number
    numero: string | number
}

type TEndereco = {
    rua: string
    numero: number | string
    cidade: string
}

type TUsuarioEndereco = TUsuario & TEndereco

const usuarios: TUsuarioEndereco[] = [
    {
        nome: 'Fabrício',
        email: 'fabricio@email.com',
        idade: 33,
        rua: 'Rua 1',
        numero: 123,
        cidade: 'Cidade 1'
    }
]
```

**Obs.:** Não é possível utilizá-lo para concatenar tipos diferentes para a mesma variável, parâmetro ou propriedade, pois vai retornar um erro dizendo que é impossível uma variável ter dois tipos de valores ao mesmo tempo.