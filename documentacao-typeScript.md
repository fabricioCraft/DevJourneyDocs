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
    - [Type Narrowing](#type-narrowing-estreitamento-de-tipos)
    - [Type Assertion](#type-assertion)
    - [Verificação de existência de propriedades em objetos](#verificação-de-existência-de-propriedades-em-objetos)
    - [Tipo Unknown](#tipo-unknown)
    


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


## Type Narrowing (Estreitamento de Tipos)

O Type Narrowing é uma técnica útil no TypeScript que permite refinar o tipo de uma variável dentro de um bloco de código específico. Isso é particularmente útil quando se trabalha com tipos de união ou tipos mais amplos.

Principais utilidades do Type Narrowing:

1. **Segurança de tipos**: Ajuda a evitar erros em tempo de execução, garantindo que você esteja usando o tipo correto em um contexto específico.

2. **Melhor IntelliSense**: O editor pode fornecer sugestões mais precisas baseadas no tipo refinado.

3. **Código mais limpo**: Evita a necessidade de type assertions frequentes.

4. **Lógica condicional mais clara**: Permite escrever código que se comporta de maneira diferente com base no tipo real de uma variável.

Exemplo de Type Narrowing:

```ts
function soma(num1: number | string, num2: number | string){
    if(typeof num1 === 'number' && typeof num2 === 'number'){
        // return num1 + num2
        console.log(typeof num1, typeof num2);
          
    }else if(typeof num1 === 'number' && typeof num2 ===     'string'){
        console.log(typeof num1, typeof num2);
        
    }else if(typeof num1 === 'string' && typeof num2 ===     'number'){
        console.log(typeof num1, typeof num2);
    }else{
        console.log(typeof num1, typeof num2);
        
    }  
}

soma('123', 123)
```

## Type Assertion

A utilização de type assertion no TypeScript serve para informar ao compilador que uma variável deve ser tratada como um tipo específico. Esse recurso é útil em diversas situações, especialmente quando lidamos com dados que podem não ter um tipo bem definido.

**Como o Type Assertion Ajuda no Código:** 

**1 - Forçar Tipos:** Quando você tem uma variável que pode ser de um tipo mais genérico ou indefinido, o type assertion permite que você declare explicitamente qual tipo deseja que o compilador considere. Por exemplo, se você tem um objeto que pode ter uma propriedade opcional, você pode usar type assertion para garantir que o TypeScript trate essa propriedade como um tipo específico.

**2 - Evitar Erros de Tipo:** Ao usar type assertion, você pode evitar erros de tipo que poderiam ocorrer durante a execução do código. Isso é especialmente útil quando você sabe que a variável terá um tipo específico em um determinado contexto, mas o compilador não consegue inferir isso.

**3 - Interoperabilidade com APIs Externas:** Muitas vezes, ao trabalhar com dados de APIs externas, a estrutura dos dados pode não ser clara. O type assertion permite que você converta esses dados em tipos que você definiu, facilitando o trabalho com eles no seu código.

Exemplo Prático

Imagine que você tenha um objeto do tipo T-Pessoa, que possui uma propriedade opcional idade. Se você tentar acessar essa propriedade diretamente, pode ocorrer um erro se ela não estiver definida. Veja como utilizar type assertion:

````ts
type TPessoa = {
    nome: string;
    idade?: number; // idade é opcional
};

const guido: TPessoa = { nome: "Guido" };

// Tentando passar guido.idade para uma função que espera um number
function saudacao(nome: string, idade: number) {
    console.log(`Olá, ${nome}. Você tem ${idade} anos.`);
}

// Aqui o TypeScript dará erro, pois idade pode ser undefined saudacao(guido.nome, guido.idade as number); // 
````
Forçando a idade a ser tratada como number
No exemplo acima, usamos guido.idade as number para informar ao TypeScript que queremos tratar idade como um número, mesmo que ela possa ser undefined. No entanto, é importante ter certeza de que a propriedade realmente tem um valor, pois se idade for undefined, isso pode causar erros em tempo de execução.

**Os riscos de usar type assertion no TypeScript incluem:**

**1 - Erros em Tempo de Execução:** Quando você força o TypeScript a tratar um valor como um tipo específico, pode acabar com um erro em tempo de execução se o valor não for realmente desse tipo. Por exemplo, se você usar guido.idade as number e idade for undefined, isso pode causar um erro na aplicação.

**2 - Perda da Segurança de Tipo:** O uso de type assertion pode levar à perda da segurança de tipo que o TypeScript oferece. Isso acontece porque o compilador não verifica se o valor realmente corresponde ao tipo que você está afirmando.

**3 - Dificuldade na Manutenção do Código:** Se você usar type assertion de maneira excessiva, pode tornar o código mais difícil de entender e manter, já que outras pessoas (ou você mesmo no futuro) podem não saber se a asserção é realmente válida.

**4 - Dependência de Dados Externos:** Muitas vezes, a necessidade de usar type assertion surge quando lidamos com dados de sistemas externos. Se esses dados não forem confiáveis, a asserção pode levar a comportamentos inesperados.

**5 - Confusão com Tipos Complexos:** Quando se trabalha com tipos complexos, como objetos aninhados, usar type assertion pode criar confusão, especialmente se a estrutura do objeto não for bem definida ou documentada.

**Considerações Finais**

O uso de type assertion deve ser feito com cautela, pois pode levar a erros se não for utilizado corretamente. É recomendado usá-lo apenas quando você tem certeza de que o valor será do tipo esperado.


## Verificação de Existência de Propriedades em Objetos

Verificar a existência de uma propriedade dentro de um objeto no TypeScript é uma prática muito útil e traz diversas vantagens no desenvolvimento de aplicações. Aqui estão algumas utilidades práticas dessa verificação:

**1. Evitar Erros em Tempo de Execução**

Ao verificar se uma propriedade existe antes de acessá-la, você evita erros que podem ocorrer quando tenta acessar uma propriedade que não está definida. Isso é especialmente importante em situações em que os dados podem vir de fontes externas, como APIs.

Exemplo:

````ts
const usuario = { nome: "Maria" };

// Verificando se a propriedade 'idade' existe antes de acessá-la
if ("idade" in usuario) {
    console.log(`Idade: ${usuario.idade}`);
} else {
    console.log("A idade não está definida.");
}
````
**2. Facilidade na Manipulação de Objetos Opcionais**

Em muitos casos, as propriedades de um objeto podem ser opcionais. Verificar a existência dessas propriedades permite que você escreva código mais robusto e flexível.

Exemplo:

````ts
type Usuario = {
    nome: string;
    idade?: number; // idade é opcional
};

const usuario: Usuario = { nome: "João" };

// Verificando se a idade existe antes de usá-la
if ("idade" in usuario) {
    console.log(`Idade: ${usuario.idade}`);
} else {
    console.log("Idade não informada.");
}
````
**3. Type Narrowing**

A verificação da existência de uma propriedade pode ajudar no processo de type narrowing. Ao confirmar que uma propriedade existe, o TypeScript pode inferir que o tipo dessa propriedade é o esperado, permitindo operações seguras.

Exemplo:

````ts
type Produto = {
    nome: string;
    preco?: number; // opcional
};

const produto: Produto = { nome: "Camiseta" };

// Verificando a existência da propriedade 'preco'
if ("preco" in produto) {
    // Aqui, TypeScript sabe que 'preco' é um number
    console.log(`Preço: ${produto.preco}`);
}
````
**4. Melhorar a Legibilidade do Código**

Verificações explícitas de propriedades ajudam a tornar o código mais claro e fácil de entender. Outros desenvolvedores que lerem seu código poderão compreender rapidamente quais propriedades são esperadas e como elas são usadas.

**Conclusão**

A verificação da existência de propriedades em objetos é uma prática recomendada em TypeScript, pois ajuda a evitar erros, facilita a manipulação de dados opcionais e melhora a legibilidade do código.

## Tipo Unknown

O tipo unknown no TypeScript é utilizado para representar dados cujo tipo exato não é conhecido em um determinado ponto do código. Isso oferece uma maneira mais segura de lidar com dados que podem vir de fontes externas, como APIs, onde a estrutura dos dados pode não ser clara.

**Utilidade Prática do Tipo Unknown**

**Segurança ao Manipular Dados Desconhecidos**

O uso de unknown força o desenvolvedor a validar os dados antes de usá-los, ao contrário do tipo any, que é mais permissivo. Isso ajuda a evitar erros que podem ocorrer ao acessar propriedades ou métodos de um tipo que não corresponde ao que se esperava.

Exemplo:

````ts
function processarDados(dados: unknown) {
if (typeof dados === 'string') {

console.log(dados.toUpperCase()); // Seguro, pois sabemos que é uma string

} else {

console.error('Dados não são uma string');

}

}
````

**Manipulação de Dados JSON**

Quando você recebe dados em formato JSON, pode não saber ao certo como esses dados estão estruturados. Usar unknown permite que você faça uma validação antes de tentar acessar as propriedades.

Exemplo:
````ts
function converterJSON(jsonString: string): unknown {
return JSON.parse(jsonString);

}

const resultado = converterJSON('{"nome": "Maria"}');

if (typeof resultado === 'object' && resultado !== null && 'nome' in resultado) {

console.log((resultado as { nome: string }).nome); // Acessando com type assertion

} else {

console.error('Formato de JSON inválido');

}

````
**Tratamento de Erros**

Quando um erro é capturado em um bloco ``try/catch``, o erro é tipado como unknown. Isso significa que você deve verificar o tipo do erro antes de acessar suas propriedades, o que aumenta a segurança do seu código.

Exemplo:
````ts
try {
// Código que pode gerar um erro

} catch (error: unknown) {

if (error instanceof Error) {

console.error(error.message); // Acessando a mensagem do erro

} else {

console.error('Erro desconhecido');

}

}

````
**Integração com APIs**

Ao trabalhar com APIs, você pode receber dados que não têm uma estrutura fixa. O uso de ``unknown`` permite que você faça uma verificação rigorosa antes de manipular esses dados, garantindo que seu código funcione corretamente independentemente da estrutura dos dados recebidos.

Exemplo:

````ts
async function buscarDados() {
const resposta = await fetch('https://api.exemplo.com/dados');

const dados: unknown = await resposta.json();

if (typeof dados === 'object' && dados !== null && 'id' in dados) {

console.log((dados as { id: number }).id); // Acessando com type assertion

} else {

console.error('Dados recebidos em formato inesperado');

}

}
````
**Conclusão**

O tipo ``unknown`` é uma ferramenta poderosa para lidar com dados que não têm um tipo definido. Ele promove boas práticas de programação ao forçar a validação dos dados antes de serem utilizados, aumentando a segurança e a robustez do código.

# Tipos Utilitários

Tipos utilitários são tipos nativos do typescript que permitem a trasformação de um tipo em outro.

É útil quando você estiver trabalhando com um tipo e precisar criar outro tipo similar, mas com algumas pequenas modificações.

## Partial<Tipo>

Transforma todos os campos de um tipo em opcionais.

Exemplo:

```ts
type Pessoa = {
    nome: string
    email: string
    idade: number
}

function atualizarPessoa (pessoa: Partial<Pessoa>) {

}

atualizarPessoa({
    nome: 'Fabricio',
    idade: 33
})

// Todas as propriedades no tipo Pessoa são opcionais.
```

## Required<Tipo>

Torna todas as propriedades de um tipo obrigatórias.

Para usar é necessário passar o tipo como parâmetro.

Exemplo:

````ts
type Pessoa = {
    nome: string
    email: string
    idade: number
}
Required<Pessoa>

// Todas as propriedades no tipo Pessoa são obrigatórias.
````
## Readonly<Tipo>

Permite que os campos de um tipo sejam apenas leitura.

Exemplo:
```ts
type Todo = {
    titulo: string
}

const todo: Readonly<Todo> = {
    titulo: 'Deletar usuários inativos'
}

todo.titulo = 'Olá'

// O campo 'titulo' é somente leitura e por isso vai dar um erro quando você tenta alterar o valor.
```

## Pick<Tipo, Propriedades>

Permite que você crie novos tipos somente com as propriedades que deseja utilizar.

Exemplo:

````ts
type Usuario = {
    nome: string
    email: string
    senha: string
}

type UsuarioSemSenha = Pick<Usuario, 'nome' | 'email'>
````

## Omit<Tipo, Propriedades>

Permite que você crie novos tipos omitindo as propriedades que você não deseje utilizar.

Exemplo:

````ts
type Usuario = {
    nome: string
    email: string
    senha: string
}

type UsuarioSemSenha = Omit<Usuario, 'senha'>
````
## Record<Chave(s), Tipo>

Permite que você crie tipos de um objeto de forma personalizável quando as propriedades são do mesmo tipo.

Exemplo:

````ts
type Pessoa = Record<'nome' | 'email' | 'senha', string>
````

## Exclude<Tipo, Propriedades>

Permite que você exclua propriedades de um tipo.

É utilizado quando você tem uma união de tipos

Exemplo:

````ts
type Transacao = 'Credito' | 'Debito' | 'Boleto' | 'Pix'

type Banco1 = Exclude<Transacao, 'Credito'>
type Banco2 = Exclude<Transacao, 'Boleto' | 'Pix'>
````

## Extract<Tipo, Propriedades>

Permite que você extraia propriedades de uma união de tipos e mantenha apenas aquelas que desejar utilizar.


Exemplo:

````ts
type Transacao = 'Credito' | 'Debito' | 'Boleto' | 'Pix'

type Banco1 = Extract<Transacao, 'Debito' | 'Boleto' | 'Pix'>
type Banco2 = Extract<Transacao, 'Credito' | 'Debito'>
````

## Tipos de Manipulação de Strings

### Uppercase<Tipo>

Transforma uma string em letras maiúsculas.

Exemplo:

````ts
type TransacaoCredito = 'creDITO'
type TransacaoDebito = 'dEbItO'

type Transacao = Uppercase<TransacaoCredito> |Uppercase<TransacaoDebito>

const tipo1: Transacao = 'CREDITO'
````

### Lowercase<Tipo>

Transforma uma string em letras minúsculas.

Exemplo:

````ts
type TransacaoCredito = 'creDITO'
type TransacaoDebito = 'dEbItO'

type Transacao2 = Lowercase<TransacaoCredito> | Lowercase<TransacaoDebito>

const tipo2: Transacao2 = 'debito'
````

### Capitalize<Tipo>

Transforma a primeira letra de uma string em maiúscula.

Exemplo:

````ts
type TransacaoCredito = 'creDITO'
type TransacaoDebito = 'dEbItO'

type Transacao3 = Capitalize<TransacaoCredito> | Capitalize<TransacaoDebito>

const tipo3: Transacao3 = 'Credito'
````








