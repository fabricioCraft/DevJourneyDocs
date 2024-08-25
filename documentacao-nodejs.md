# Sumário

- [Utilidade do node.js](#utilidade-do-nodejs)
- [NPM](#npm)
    - [NPM init](#npm-init)
- [Require x Import](#require-x-import)
- [Biblioteca Externa](#biblioteca-externa)
- [Biblioteca de desenvolvimento x produção](#biblioteca-de-desenvolvimento-x-produção)



# Utilidade do node.js

O node.js permite que os desenvolvedores utilizem JavaScript para programar no lado do servidor, ampliando as possibilidades de uso da linguagem para além do ambiente do navegador.

# NPM

O npm (Node Package Manager) é o gerenciador de pacotes padrão para o ecossistema Node.js. Ele facilita a instalação, gerenciamento e atualização de bibliotecas e dependências de um projeto em Node.js. 

Ao utilizar o npm, os desenvolvedores podem facilmente adicionar pacotes de terceiros aos seus projetos, além de gerenciar versões e atualizações de forma eficiente. Isso é importante, pois permite a reutilização de código e a integração de funcionalidades prontas para uso em um projeto, acelerando o desenvolvimento.

Além disso, o npm também possibilita a definição de scripts personalizados no arquivo `package.json`, permitindo a execução de tarefas automatizadas, como a compilação de código, execução de testes, entre outras ações, através do comando `npm run`.

Um exemplo de uso do npm é a instalação de uma biblioteca de utilitários como o Lodash. Para isso, basta executar o comando `npm install lodash`. Dessa forma, o Lodash será baixado e adicionado como uma dependência do projeto, podendo ser importado nos arquivos JavaScript conforme necessário.

Em resumo, o npm é uma ferramenta essencial no desenvolvimento de aplicações em Node.js, pois simplifica a gestão de dependências e facilita a integração de pacotes externos, contribuindo para a eficiência e qualidade dos projetos de software.

## NPM init

O comando `npm init` é utilizado para iniciar o processo de criação de um novo projeto Node.js e criar um arquivo `package.json` que contém as informações do projeto, como nome, versão, descrição, scripts personalizados, dependências, entre outros detalhes.

Ao executar o comando `npm init`, o npm fará uma série de perguntas interativas para coletar essas informações e gerar o arquivo `package.json` com base nas respostas fornecidas. 

Isso é útil para garantir a organização e padronização do projeto, além de facilitar o versionamento, distribuição e colaboração com outros desenvolvedores.

Por exemplo, ao executar o `npm init`, você será solicitado a fornecer o nome do projeto, a versão, a descrição, o ponto de entrada (entry point), os scripts que deseja adicionar, o autor, as licenças utilizadas, entre outras informações relevantes.

Ao final do processo, o arquivo `package.json` será gerado com base nas respostas fornecidas, refletindo as configurações iniciais do projeto. Você pode editar manualmente o arquivo `package.json` posteriormente, caso deseje adicionar mais informações ou fazer ajustes. 

Dessa forma, o `npm init` é o ponto de partida para criar e configurar um novo projeto Node.js, garantindo uma estrutura organizada e bem definida desde o início do desenvolvimento.

```bash
npm init

```
Caso queira marcar todas as perguntas como padrão e responder "sim" para todas as perguntas, você pode passar o comando abaixo.

```bash
npm init -y
```

# Require x Import

Em JavaScript, `import` e `require` são utilizados para trazer funcionalidades de módulos externos para o seu código, porém cada um é utilizado em um contexto diferente.

- `require`: É uma função utilizada em ambientes que suportam o sistema de módulos CommonJS, como o Node.js. Com `require`, você pode trazer módulos para o seu código de forma síncrona.

- `import`: É uma declaração do ECMAScript 6 utilizada em ambientes que suportam o sistema de módulos ES6, como os navegadores modernos com suporte a módulos. Com `import`, você pode trazer módulos para o seu código de forma assíncrona e também possui suporte a importações nomeadas.

Um exemplo de uso do `require` em Node.js é trazer o módulo `fs` para manipulação de arquivos:

```javascript
const fs = require('fs');
```

Já um exemplo de uso do `import` em um arquivo JavaScript com suporte a módulos ES6 poderia ser:

```javascript
import { nomeDaFuncao } from './meuModulo.js';
```

Em resumo, `require` é utilizado em ambientes CommonJS, como Node.js, enquanto `import` é utilizado em ambientes ES6, como navegadores modernos com suporte a módulos. A escolha entre um ou outro depende do ambiente em que está desenvolvendo e das especificações de módulos que está utilizando em seu projeto.

# Biblioteca Externa

Para fazer a instalação de uma biblioteca externa em um projeto JavaScript, você pode utilizar o Node Package Manager (NPM) no caso de um projeto Node.js. Primeiramente, é importante ter o Node.js instalado na sua máquina. 

Para instalar uma biblioteca, você pode utilizar o comando `npm install nome-da-biblioteca`. Por exemplo, se você quer instalar o pacote `axios` para fazer requisições HTTP em seu projeto, você pode executar o seguinte comando no terminal:

```bash
npm install axios
```

Isso vai baixar a biblioteca `axios` e adicioná-la como uma dependência no arquivo `package.json` do seu projeto.

Após a instalação, você pode utilizar a biblioteca em seu código importando-a com `require` (em ambientes CommonJS) ou `import` (em ambientes ES6).

Lembre-se de que é importante verificar a documentação da biblioteca que você está instalando para entender como utilizá-la corretamente em seu projeto e quais dependências ela pode ter.

Por fim, é sempre recomendado manter um arquivo `package.json` atualizado com todas as dependências do seu projeto, facilitando a gestão das bibliotecas instaladas e suas versões.

# Biblioteca de desenvolvimento x produção

As bibliotecas de desenvolvimento são aquelas utilizadas durante o desenvolvimento da aplicação, como ferramentas para testes, linters, entre outras. Elas não são essenciais para o funcionamento da aplicação em produção, por isso são instaladas com a flag "-D" quando utilizamos o npm, como por exemplo: `npm install -D nome_da_biblioteca`.

Já as bibliotecas de produção são aquelas necessárias para o funcionamento correto da aplicação em ambiente de produção. Elas são as dependências principais do projeto e devem ser instaladas sem a flag "-D", apenas com `npm install nome_da_biblioteca`.

Um exemplo prático seria a instalação do framework Express em uma aplicação Node.js. Se estamos desenvolvendo a aplicação e precisamos utilizar o Express apenas durante o desenvolvimento, podemos instalá-lo como biblioteca de desenvolvimento. Já se o Express é essencial para o funcionamento da aplicação em produção, ele deve ser instalado como uma biblioteca de produção.
