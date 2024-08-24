# Desmitificando Git

## Sumário
- [Branch](#branch)
- [Mudança de Branch](#mudança-de-branch)
- [Git push](#git-push)
- [Git init](#git-init)
- [Git status](#git-status)
- [Git add .](#git-add-)
- [Git reset](#git-reset)
- [Git commit](#git-commit)
- [Git restore](#git-restore)
- [Git log](#git-log)
- [Git remote add origin](#git-remote-add-origin)
- [Git pull](#git-pull)

## Antes de passar qualquer comando git pela primeira vez, faça isso.

Configure o seu nome de usuário e endereço de e-mail globalmente no Git para garantir que todos os commits que você realizar tenham essas informações corretas e para linkar o repositório local ao repositório remoto.

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"

```

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
## Git push

O comando `git push` no Git é utilizado para enviar, ou "empurrar", as alterações do repositório local para o repositório remoto. Ao executar o `git push`, você está enviando os commits que foram feitos no seu repositório local para o repositório remoto, mantendo assim ambos sincronizados.

É importante realizar o `git push` após ter realizado alterações locais e feito commits para garantir que as atualizações feitas por você estejam disponíveis para os outros colaboradores do projeto no repositório remoto. Dessa forma, você contribui para o progresso do projeto e disponibiliza as suas alterações para que a equipe possa trabalhar com base nelas.

O `git push` é uma ação fundamental no fluxo de trabalho com o Git, pois permite que você compartilhe o seu trabalho e colabore de forma eficiente com os demais membros da equipe. Certifique-se de estar com o repositório local atualizado e sem conflitos antes de realizar o `git push` para evitar possíveis problemas de integração com o repositório remoto.

Use esse código na primeira vez que estiver dando um push no repositório
```bash
git push origin nome-da-branch
```
Caso não seja a primeira vez que esteja dando o push, você pode usar o seguinte comando.

```bash
git push
```

Caso tenha mais de uma branch e queira fazer um `push` pro GitHub, é necessário passar o comando abaixo para transformar todas as branchs em rastreáveis para que seja aceito.

``` bash
git push -u --all
```

## Git init

O comando `git init` é utilizado para iniciar um repositório Git em um diretório local. Ao executar o `git init`, o Git cria uma estrutura de controle de versão no diretório especificado, permitindo que você comece a versionar e rastrear as mudanças nos arquivos do seu projeto.

Quando você executa o `git init`, o Git cria uma pasta oculta chamada ".git" dentro do diretório, onde são armazenadas as informações do repositório, como o histórico de commits, branches, configurações e outros dados relacionados ao controle de versão.

**IMPORTANTE: É importante lembrar que o `git init` deve ser executado apenas uma vez no diretório raiz do seu projeto. Uma vez que o repositório Git foi inicializado, você pode começar a utilizar os comandos do Git para versionar o seu código e colaborar com outras pessoas de forma eficiente e segura.**

```bash
git init
```

## Git status

O comando `git status` é utilizado no Git para verificar o estado dos arquivos no seu repositório. Ao executar o `git status`, o Git exibe informações como arquivos modificados, arquivos prontos para serem commitados, branches em uso e outras informações relevantes sobre o estado do seu projeto.

O `git status` é uma ferramenta útil para verificar o que foi alterado no seu repositório desde o último commit, permitindo que você saiba quais arquivos foram modificados, adicionados ou removidos. Isso ajuda a manter o controle sobre as mudanças no código e a decidir quais alterações devem ser commitadas.

Por exemplo, ao realizar algumas modificações em arquivos do seu projeto, você pode executar o `git status` para ver quais arquivos foram alterados e se estão prontos para serem commitados. O `git status` mostrará a lista de arquivos modificados e indicará se eles foram ou não adicionados ao stage para o próximo commit.

Dessa forma, o `git status` é uma ferramenta fundamental para manter o controle e a organização do seu repositório Git, permitindo que você saiba o status atual do código e o que precisa ser feito antes de criar um novo commit.

```bash
git status
```

## Git add .

O comando `git add .` no Git é utilizado para adicionar todas as modificações e novos arquivos do diretório de trabalho ao stage, preparando-os para serem commitados no próximo commit. Ao executar o `git add .`, você está selecionando todas as alterações realizadas nos arquivos para serem incluídas no próximo snapshot (commit).

Isso é útil quando você fez várias alterações em diferentes arquivos e deseja incluir todas essas modificações em um único commit. O `git add .` simplifica o processo de adicionar todas as mudanças de uma vez, sem a necessidade de adicionar manualmente cada arquivo individualmente.

Por exemplo, se você fez alterações em vários arquivos após realizar uma funcionalidade no seu projeto e deseja commitar todas essas mudanças de uma única vez, o `git add .` é uma maneira prática de incluir todas essas alterações no stage.

Lembre-se de sempre revisar as modificações adicionadas com o `git status` após executar o `git add .`, para garantir que apenas as alterações desejadas estejam preparadas para o commit e que nada tenha sido adicionado indevidamente. Essa prática ajuda a manter um histórico de commits organizado e coeso no seu repositório Git.

```bash
git add .
```

Caso queira adicionar modificações de um arquivo específico do diretório de trabalho ao stage, basta passar o comando abaixo.

``` bash
git add nome-do-arquivo-alterado
```

## Git reset

O comando git reset no Git é utilizado para desfazer alterações no repositório, seja desfazendo commits, alterando o HEAD ou desfazendo o stage de arquivos preparados para commit.

```bash
git reset nome-do-arquivo

```
Caso queira remover o rastreio de todos os arquivos, basta passar o comando abaixo.

```bash
git reset .
```

## Git commit

O `commit` no Git é uma operação fundamental que salva as alterações feitas nos arquivos do seu projeto.`

Ao realizar um `commit`, você está registrando de forma permanente as modificações realizadas desde o último commit, gerando um ponto na história do projeto.

Ao realizar um `commit`, é importante escrever uma mensagem clara e descritiva que explique as mudanças feitas no código. Isso ajuda a manter um histórico claro e compreensível do desenvolvimento do projeto, facilitando a colaboração com outros membros da equipe e a identificação de alterações específicas no código.

Por exemplo, ao adicionar uma nova funcionalidade em uma aplicação, você pode realizar um `commit` com uma mensagem como **"Adicionar funcionalidade de login de usuário"**. Dessa forma, qualquer pessoa que revisar o histórico de commits poderá entender rapidamente as mudanças feitas e o motivo por trás delas.

É importante fazer ``commit`` com frequência e de forma organizada, separando as alterações em unidades lógicas e coesas. 

Isso ajuda a manter o histórico do projeto limpo e fácil de entender, além de facilitar a identificação de possíveis erros e a reversão de mudanças, se necessário.

```bash
git commit -m "descricao-do-que-foi-alterado"
```

Você pode utilizar o site abaixo para realizar commits semânticos e padronizá-los. (Verifique a especificação do site.)

<div>
    <a href= "https://www.conventionalcommits.org/pt-br/v1.0.0-beta.4/" >
</div>

## Git restore

O comando `git restore` no Git é utilizado para descartar modificações feitas nos arquivos do projeto e restaurá-los para o estado mais recente registrado no último commit.

Isso significa que o `git restore` permite reverter alterações **não commitadas nos arquivos**, trazendo-os de volta ao estado em que estavam antes das alterações serem feitas.

Ao utilizar o `git restore`, é possível desfazer modificações indesejadas nos arquivos e retornar ao estado anterior sem a necessidade de fazer um novo commit. 

Isso pode ser útil em situações em que você fez mudanças não intencionais ou erroneamente nos arquivos e deseja descartá-las.

Por exemplo, imagine que você tenha feito algumas alterações em um arquivo e percebeu que essas mudanças não eram necessárias. Utilizando o `git restore`, você pode descartar essas modificações e restaurar o arquivo para o estado em que estava no último commit, evitando que essas alterações não intencionais sejam commitadas.

**Obs.: É importante ter cautela ao usar o `git restore`, pois ele descarta as alterações de forma definitiva e não é possível recuperá-las facilmente após a execução do comando. Por isso, é recomendado fazer um backup ou verificar as alterações antes de utilizar o `git restore` para evitar a perda de dados importantes.**

```bash
git restore nome-do-arquivo
```
## Git log

O comando `git log` é utilizado no Git para visualizar o histórico de commits do repositório. Ao executar o `git log`, são exibidas informações como o autor do commit, a data e hora em que o commit foi realizado, o hash SHA do commit, e a mensagem associada a cada commit.

O `git log` mostra os commits em ordem cronológica reversa, ou seja, do commit mais recente para o mais antigo. Isso permite que você acompanhe a evolução do código, veja quem realizou alterações e revise as mensagens de commit associadas a cada mudança.

Você também pode usar algumas opções adicionais com o `git log`, como por exemplo `--oneline` para exibir cada commit em uma única linha, `--graph` para mostrar o histórico de commits de forma gráfica incluindo as ramificações, e `--author` para filtrar os commits por autor específico.

Ao visualizar o `git log`, você pode identificar quais foram as alterações realizadas no projeto ao longo do tempo, revisar as mensagens de commit para entender o contexto de cada mudança e rastrear a autoria de cada modificação no código-fonte. Isso é útil para ajudar na colaboração em equipe, no gerenciamento de versões do software e na análise de problemas ou bugs que possam ter surgido em etapas anteriores do desenvolvimento.

```bash
git log
```

## git remote add origin

O comando `git remote add origin` no Git é utilizado para adicionar um repositório remoto como origem do seu repositório local. A palavra "origin" é um nome convencional utilizado para se referir ao repositório remoto padrão onde você enviará as alterações do seu repositório local.

Ao executar o `git remote add origin`, você está configurando o seu repositório local para se comunicar com um repositório remoto (como o GitHub, GitLab, Bitbucket, entre outros). Isso estabelece uma conexão entre o repositório local e o remoto, permitindo que você envie (push) e receba (pull) alterações entre esses repositórios.

Por exemplo, ao criar um novo repositório no GitHub e desejar vincular o seu repositório local a esse repositório remoto, você pode utilizar o `git remote add origin` seguido do URL do repositório remoto do GitHub. Isso define o repositório remoto como a origem padrão para envio e recebimento de alterações.

A utilização do `git remote add origin` é parte do processo de configuração inicial de um repositório Git e é especialmente útil quando você deseja trabalhar de forma colaborativa em um projeto com outras pessoas ou sincronizar o seu código entre múltiplos computadores. A partir desse momento, você pode utilizar os comandos `git push` e `git pull` para interagir com o repositório remoto, enviar e receber alterações e colaborar de forma eficiente com outros desenvolvedores.

```bash
git remote add origin link-do-repositorio
```

## Git pull

O comando `git pull` no Git é utilizado para buscar e incorporar as alterações do repositório remoto no seu repositório local. Ao executar o `git pull`, você está essencialmente mesclando as alterações feitas no repositório remoto com o seu repositório local, mantendo o histórico de commits sincronizado entre ambos.

O `git pull` combina dois passos em um só: ele primeiro faz um `git fetch` para buscar as alterações do repositório remoto para o seu repositório local e, em seguida, ele realiza um `git merge` para mesclar essas alterações no seu branch atual.

Por exemplo, ao colaborar em um projeto com outros desenvolvedores e eles realizam alterações no código que são pushadas para o repositório remoto, você pode utilizar o `git pull` para trazer essas alterações para o seu repositório local e manter o seu código atualizado com o trabalho em equipe.

O `git pull` é útil para evitar conflitos entre as versões do código e garantir que o seu repositório local esteja alinhado com o repositório remoto. Dessa forma, você pode trabalhar de forma colaborativa, acompanhar as mudanças no projeto e garantir que esteja sempre atualizado com o progresso do desenvolvimento.

```bash
git pull
```