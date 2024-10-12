# Sumário

- [Testes automatizados](#testes-automatizados)
- [Agrupamento de testes](#agrupamento-de-testes)

# Testes automatizados

Os teste automatizados servem para garantir que a aplicação funcione corretamente ao longo do tempo permitindo que desenvolvedores testem funcionalidades de forma automatizada em ambiente de desenvolvimento.

Para criar um teste automatizado, primeiro é necessário instalar o framework `jest` no seu projeto, como mostrado abaixo:

```bash
npm install -D jest
```
Após, é necessário criar um arquivo `.test.js` para cada arquivo `.js` que deseja testar.

Em seguida, basta escrever o teste a ser testado no arquivo `.test.js`, é importante lembrar que o jest usa por padrão o commonjs, ou seja, é necessário importar o arquivo que deseja testar com `require()` para o teste funcionar de maneira adequada:

```js
// soma.js

function soma(a, b) {
    return a + b
}

module.exports = soma

//soma.test.js

const soma = require('./soma')

test('Verifica a soma entre dois números', () => {
    expect(soma(3, 4)).toBe(7)
})

// Esse código deve testar se a soma dos números 3 e 4 é igual a 7.
```

Para executar os testes automatizados, basta digitar no terminal:

```bash
npm jest
```

# Agrupamento de testes

O agrupamento de testes serve para organizar os testes de forma mais clara e intuitiva.

Quando você agrupa testes, você pode executar todos os testes de um grupo específico de uma só vez, em vez de executar todos os testes do projeto. Isso é útil durante a fase de desenvolvimento, quando você está focado em uma parte específica do código.

Para agrupar os testes em um grupo, basta adicionar o comando `describe()` com o nome do grupo e o comando `it()` ou `test()`para cada teste.

```js
describe('Teste de soma', () => {
    test('Verifica a soma entre dois números', () => {
        expect(soma(3, 4)).toBe(7)
    })
})
```

Quando você quiser verificar que um resultado não seja igual ao esperado, basta você utilizar o método `not.toBe()`.

```js
describe('Teste de soma', () => {
    test('Verifica a soma entre dois números', () => {
        expect(soma(3, 4)).not.toBe(8)
    })
})