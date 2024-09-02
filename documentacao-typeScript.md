# Sumário
- [TypeScript](#typescript)
- [Tipagem Dinâmica](#tipagem-dinâmica)
- [Typagem Estática](#tipagem-estática)

# TypeScript

É um supercojunto do JavaScript, criado pela Microsoft, que permite desenvolver aplicações JavaScript utilizando conceitos e arquiteturas mais sólidas

O TypeScript é usado somente para desenvolvimento do código e não para execução, sendo necessário fazer uma **transpilação** para transformar o código em JavaScript.

Uma grande vantagem do TypeScript é apontar problemas durante o desenvolvimento da aplicação.

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

```git
npm init -y
```

Depois, instale o TypeScript:

```git
npm install -D typescript
```

Ao finalizar o desenvolvimento da aplicação, é necessário fazer a transpilação do código:

```git
npx tsc 'nome-do-arquivo.ts'
```


