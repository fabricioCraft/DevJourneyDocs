# Desmitificando Git

## Sumário
- [Branch](#branch)
- [Mudança de Branch](#mudança-de-branch)
- [Publicando alterações no GitHub](#publicando-alterações-no-github)
- [Inicializando o Git local](#inicializando-o-git-local)
- [Como verificar se houve alguma modificação em algum documento ou pasta](#como-verificar-se-houve-alguma-modificação-em-algum-documento-ou-pasta)
- [Como adicionar as alterações realizadas em uma pasta ou documento no repositório](#como-adicionar-as-alterações-realizadas-em-uma-pasta-ou-documento-no-repositório)



## Branch
Branches (ramificações) são utilizadas no Git para criar linhas de desenvolvimento paralelas. 

Nas empresas, o uso de branches é essencial para separar novas funcionalidades, correções de bugs ou qualquer outra modificação no código, sem impactar diretamente a branch principal (normalmente chamada de "master" ou "main").

Cada branch pode ter suas próprias alterações, commits e histórico de desenvolvimento, permitindo que diferentes equipes ou desenvolvedores trabalhem em funcionalidades distintas sem interferir no trabalho uns dos outros. 

Após finalizar o desenvolvimento em uma branch, é possível integrar as alterações na branch principal por meio de um processo chamado de "merge".


Por exemplo, imagine que uma equipe está trabalhando em uma nova funcionalidade para um aplicativo e outra equipe está corrigindo bugs na versão atual. Cada equipe pode criar suas próprias branches para realizar as alterações necessárias. Quando as implementações estiverem prontas, as branches podem ser mescladas de volta à branch principal de forma organizada e sem conflitos.

### Vantagens

- Ajuda a manter um histórico claro do que foi desenvolvido;
- Facilita a revisão de código;
- Facilita a identificação de possíveis problemas;
- Facilita a manutenção do projeto de forma mais eficiente.

## Mudança de Branch

Quando se faz uma mudança de branch, todas as informações da branch que está selecionada são copiadas para a nova. Sendo assim, todas as funcionalidades da branch anteriormente selecionada podem ser usadas na nova branch.

```bash
git checkout -b nome-da-nova branch
```
## Publicando alterações no GitHub


```bash
git push origin nome-da-branch
```
Caso tenha mais de uma branch e queira fazer um `push` pro GitHub, é necessário passar o comando abaixo para transformar todas as branchs em rastreáveis para que seja aceito.

``` bash
git push -u --all
```

## Inicializando o Git local

Usado para inicializar o git em um pasta no computador.

```bash
git init
```

## Como verificar se houve alguma modificação em algum documento ou pasta

Comando que serve para ver os arquivos existentes no repositório e se há alguma modificação

```bash
git status
```

## Como adicionar as alterações realizadas em uma pasta ou documento no repositório

O comando abaixo faz com que o repositório rastreie todos os arquivos que foram feitas alterações.

```bash
git add .
```

Já esse comando faz com que o repositório rastreie somente o arquivo que foi passado no comando.

``` bash
git add nome-do-arquivo-alterado
```

## Remover arquivos do rastreiamento do repositório

```bash
git reset nome-do-arquivo

```

