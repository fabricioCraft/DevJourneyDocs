# Tabela de conteúdo
- [HTML](#html)
    - [Código Base do HTML](#código-base-do-html)
        - [Configuração do site](#configuração-do-site)
        - [Conteúdo do site](#conteudo-do-site)
    - [Tags HTMl](#tags)
        - [Parágrafos e Quebras](#paragrafos-e-quebras)
        - [Simbolos no site](#simbolos-no-site)
        - [Emoji no site](#emoji-no-site)
        - [Como evitar danos com direitos autorais?](#como-evitar-danos-com-direitos-autorais)
        - [Formatos para imagens na web](#formatos-para-imagens-na-web)
        - [Por que o tamanho das imagens de um site importa?](#por-que-o-tamanho-das-imagens-importa)
        - [Tags img para inserir imagens no site](#tags-img-para-inserir-imagens-no-site)
        - [Como mudar o favicon de um site?](#como-mudar-o-favicon-de-um-site)
        - [Hierarquia de Títulos](#hieraquia-de-titulos)
        - [Semântica em HTML5 é importante](#semântica-em-html5-é-importante)
        - [Negrito e Itálico do jeito certo](#negrito-e-itálico-do-jeito-certo)
        - [Colocação de Tags de forma produtiva](#colocação-de-tags-de-forma-produtiva)
        - [Formatações adicionais em HTML](#formatações-adicionais-em-html)
        - [Citações e Códigos](#citações-e-códigos)
        - [Listas](#listas)
            - [Ordenadas](#ordenadas)
            - [Não Ordenadas](#não-ordenadas)`
            - [Listas de Definições](#listas-de-definições)
        - [Links](#links)
            - [Links e Âncoras](#links-e-âncoras)
            - [Links Internos](#links-internos)
            - [Links para download](#links-para-download)
        - [Mídias](#mídias)
            -[Imagens Dinãmicas](#imagens-dinâmicas)
            - [Colocando áudio no site](#colocando-audio-no-site)
            - [Vídeo em hospedagem própria](#video-em-hospedagem-própria)

# HTML

## Código Base do HTML

### Configuração do site

```html

<!DOCTYPE html> <!--Indica que estamos tabalhando com html 5-->
<html lang="en"> <!--Define a linguagem do site-->
<head> 
    <meta charset="UTF-8"> <!-- Codificação de caracteres que dá suporte a acentuação do site-->
    <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!--Indica que o site ocupará 100% do espaço disponível na tela-->
    <title>Meu primeiro exercício</title> <!--Título do site-->
</head>

```

### Conteudo do site

```html
<body>
    <h1>Olá Mundo!</h1>
    <hr>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis, quibusdam.</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis, quibusdam.</p>
    
</body>
</html>

```


## Tags
```html
<h1></h1> <!--Título de nível 1-->
<hr> <!--Cria uma linha horizontal-->
``` 

### Paragrafos e Quebras

```html

<br> <!--Quebra a linha-->
<p></p> <!--Parágrafo-->
&lt; <!--Significa menor que "em inglês". Possibilita a impressão no navegador do símbolo "<"-->
&gt; <!--Significa maior que "em inglês". Possibilita a impressão no navegador do símbolo ">"-->
```

### Simbolos no site

```html
&reg; <!--Simbolo de marca registrada-->
&copy; <!--Simbolo de copyright-->
&trade; <!--Simbolo de Trade Mark-->
&euro; <!--Simbolo do euro-->
&pound; <!--Simbolo da libra (pound)-->
&yen; <!--Simbolo do Yen-->
&cent; <!--Simbolo de centavos em dólar-->
&delta; <!--Simbolo do delta minúsculo-->
&Delta; <!--Simbolo do Delta maiúsculo-->
&empty; <!--Simbolo de vazio-->
&uarr; <!--Simbolo de seta para cima-->
&larr; <!--Simbolo de seta para a esquerda-->
&rarr; <!--Simbolo de seta para a direita-->
&darr; <!--Simbolo de seta para baixo-->
```

### Emoji no site
Para saber o código do emoji:
- Acessar [emojipedia](https://emojipedia.org/)
- Encontrar o emoji desejado
- Procurar por Codepoints
- Copiar o código após o sinal de mais(+)
- No html, adicionar antes do código do emoji **&#x**

### Como evitar danos com direitos autorais?
- Se for procurar imagens no google, colocar o filtro de **Marcadas para reutilização** (Creative Comuns)
- Ou acessar banco de imagens:
    - Unsplash
    - Pexels
    - Freepik

### Formatos para imagens na web
Normalmente são usados os formados: **JPEG** e **PNG**

**JPEG** é um formato para alto compactação de imagens. As imagens JPEG tem extensão JPG

**PNG** permite trabalhar com imagens transparentes no site. As imagens PNG possui uma maior qualidade do que imagens JPEG, permitindo que o Zoom in não distorça as imagens.

### Por que o tamanho das imagens importa?
O tamanho certo para utilizar em um site é 1500 no máximo.

O tamanho da imagem é importante para a velocidade do site. Imagens grandes deixam o site mais pesado fazendo com que não hanckeie bem no google, deixando seu site fora da busca de pesquisas.

### Tags img para inserir imagens no site

```html
<img src="logo-html.png" alt="Logo HTML 5">

<!--src - É o local onde sua imagem está guardada, seja ela em uma pasta local no computador ou em um site. Caso a imagem esteja em um site, o src usado para fazer referência a imagem será o link da imagem.

alt - É o nome que faz referência a imagem. Se por algum motivo a imagem não aparecer, o texto escrito nele irá aparecer. É um bom recurso de acessibilidade.-->
```
### Como mudar o favicon de um site?
Para gerar o favicon, é melhor e mais compatível gerar com a extensão .ico.

 - Sites para gerar o favicon:
    - [icon archive](https://www.iconarchive.com/)
    - [favicon](https://favicon.io/)

### Hieraquia de Titulos
São titulos e subtítulos para organização do texto, indo de h1 até h6.

```html
<h1></h1> <!--Título de nível 1-->
<h2></h2> <!--Título de nível 2-->
<h3></h3> <!--Título de nível 3-->
<h4></h4> <!--Título de nível 4-->
<h5></h5> <!--Título de nível 5-->
<h6></h6> <!--Título de nível 6-->
```

### Semântica em HTML5 é importante
O HTML5  é focado no significado, ou seja, no conteúdo do site. A forma ou estilo do site é de responsabilidade do CSS3.

### Negrito e Itálico do jeito certo

```html
<strong></strong> <!--Negrito-->
<em></em> <!--Itálico-->
```

### Colocação de Tags de forma produtiva

Para colocar tags no meio de um texto de forma produtiva:

    Passo 1 -Selecione o texto que deseja que fique entre as tags;

    Passo 2 - Pressione o conjunto de teclas: CTRL + Shift + p

    Passo 3 - Procure por **Wrap with abreviation** e selecione;

    Passo 4 - Digite a tag que deseje.

### Formatações adicionais em HTML


```html
<mark></mark> <!--Marcador de texto.-->
<small></small> <!--Faz a letra ficar pequena.-->
<del></del> <!--Marca o texto como excluído.-->
<ins><ins> <!--Marca o texto como inserido (Sublina o texto).-->
<sup></sup> <!--Sobrescreve o texto (Coloca parte do texto mais acima).-->
<sub></sub> <!--Subescreve o texto (Coloca parte do texto mais abaixo).--> 
```

### Citações e Códigos

```html
<code></code> <!--Usado para imprimir na tela web um código.-->
<pre></pre> <!--Usado para identar o código impresso na tela da mesma maneira 
como está no código desenvolvido.-->
<q></q> <!--Usado para citação de frase, coloca aspas ("") na frase citada.-->
<blockquote></blockquote> <!--Usado para citação de um bloco completa, 
tem uma quebra de linhas e um desolocamento horizontal do bloco citação. 
(Normalmente usado em parágrafos ou fases com mais de uma linha).-->
<abbr title="Nome completo da palavra">Palavra abreviada<abbr> <!--Usado para abreviações no texto.

Quando o usuário passa o mouse em cima ele informa o que a sigla significa.-->
<bdo><bdo> <!--Mostra o texto invertido, de trás para frente.-->
```

## Listas

### Ordenadas

As listas ordenadas são aquelas enuremadas fazendo a contagem do primeiro elemento da lista até o último.

``` html

<!--Elas podem ser do tipo: 1, A, a, I e i.-->

<ol type="1"></ol>
<ol type="A"></ol>
<ol type="a"></ol>
<ol type="I"></ol>
<ol type="i"></ol>

<!--Exemplo:-->

<ol type="1">
    <li>Acordar</li>
    <li>Ligar para o João</li>
    <li>Tomar café</li>
    <li>Escovar os dentes</li>

</ol>
```

### Não Ordenadas

As listas não ordenadas são aquelas que não seguem uma ordem.

``` html
<ul type = "disc"></ul>
<ul type = "circle"></ul>
<ul type = "square"></ul>

<!--Exemplo:-->

<ul type="disc">
        <li>Pão</li>
        <li>Leite</li>
        <li>Tomate</li>
        <li>Manteiga</li>
        <li>Arroz</li>
        <li>Feijão</li>
    </ul>

```

### Listas de Definições

As listas de definições são usadas como se fosse um dicionário com termos e descrição desses termos.

```html
<dl>
    <dt>HTML</dt> <!--Definição de termo-->
    <dd>Linguagem de marcação para a criação de um site.</dd> <!--Definição de descrição-->
</dl>
```
## Links

### Links e Âncoras

href - se refere ao link que será aberto quando o visitante clica-lo.

Ao usar o "target= '_blank' e o "rel='external'"" você está dizendo que esse link abre um o site externo e para isso ele deve abrir uma nova aba em branco para carregar a página.

Sem esses dois comandos, a página externa é aberta na msm página e faz com que o visitante saia do seu site. 
```html
    <p>Você pode acessar meu <a href="https://github.com/fabricioCraft" target="_blank" rel="external">repositório público no github</a></p>
```

### Links internos

Os links internos servem para fazer referência entre uma página e outra dentro do mesmo site.

```html
<!--Exemplos-->

<p>Esta é a primeira página do site. Se você quiser, pode acessar também a minha <a href="pag2.html" rel="next">segunda página</a></p>

<!--No exemplo, foi criado um link no conjunto de palavras "segunda página", onde ao clicar nela o usuário é redirecionado para a segunda página do site-->

<!--Ainda no exemplo, o parâmetro "next" faz referência à próxima página do site, assim como o parâmetro "prev" faz referência à página anterior. -->
```

### Links para download

Para permitir que o visitante possa baixar um arquivo do site:

- Basta fazer o link diretamente para o arquivo que se deseja efetuar o download. 
- Adicionar o atributo "download" com o valor configurado para o nome do arquivo.
- E adicionar o atributo "type" para indicar ao navegador que tipo de arquivo está sendo baixado.

Para saber o valor a ser colocado no "type", você pode visitar a página [iana](#https://www.iana.org/assignments/media-types/media-types.xhtml)

Alguns media types bem usados no dia-a-dia:
- application/zip
- text/html
- text/css
- text/javascript
- video/mp4
- video/H264
- video/JPEG
- audio/acc
- audio/mpeg
- font/ttf
- image/jpeg
- image/png

```html
<a href="exemplo.pdf" download ="exemplo.pdf" type="application/pdf">Baixar livro em PDF</a>
```
## Mídias

### Imagens Dinâmicas

Seu site deve se adaptar ao tamanho da tela do dispositivo em que estiver utilizando.

**Cuidado:** Sites lentos diminuem a taxa de retenção dos usuários, que ficam menos tempo no seu site, prejudicando a indexação da sua página no mecanismo de busca do google.

A tag ```<source>``` possui três atributos:
- type que vai indicar o media type da imagem que usamos.
- srcset que vai configurar o nome da imagem que será carregada quando o tamanho for atingido.
- media que indica o tamanho máximo a ser considerado para carregar a imagem indicada.

***Atenção:** Existem uma ordem entre os ```<source>``` que deve ser respeitada e na configuração do exemplo abaixo, os itens mais acima devem ser os de menores tamanhos para o max-width e que os seguintes sejam maiores, de forma crescente.

```html
    <picture>
        <source media="(max-width:750px )" srcset="./imagens/foto-p.png">
        <source media="(max-width:1050px )" srcset="./imagens/foto-m.png" type="image/png">
        <img src="./imagens/foto-g.png" alt="Imagem flexível">
    </picture>
```
### Colocando audio no site

Existe basicamente duas maneiras de colocar audio no seu site, como descritas nos exemplos abaixo:

No primeiro exemplo, você pode colocar o áudio diretamente na tag ```<audio>```.

No segundo exemplo, você pode colocar os ```<source>```
dentro da tag ```<audio>``` e então colocar os tipos de áudios. Caso o navegador não consiga acessar um arquivo ele tentará acessar o outro e assim sucessivamente.

- O parâmetro **autoplay** faz com que o áudio comece a tocar.
- O parâmetro **controls** faz com que o áudio apareça na página e seja possível pausar e dar play no áudio.
- O parâmetro **loop** faz com que o áudio volte ao início quando ele chegar ao fim, ou seja, continua tocando em loop.

```html
    <!--Exemplo 1-->
    <audio src="./midia/east-west.mp3" autoplay ></audio>
    <!--Exemplo 2-->
    <audio preload="auto"  autoplay controls loop>
        <source src="./midia/east-west.mp3" type="audio/mpeg">
    </audio>
```
### Video em hospedagem própria

Para colocar vídeos no site, é a mesma ideia do áudio.

- O parâmetro **poster** coloca uma capa no vídeo.

```html
    <video poster = "./imagens.jpg" auplay controls>
        <source src="./midia/meu-video.mp4" type="video/mp4">
        <source src="./midia/meu-video.mp4.m4v" type="video/mp4">
        <source src="./midia/meu-video.webm" type="video/mp4">
    </video>
```