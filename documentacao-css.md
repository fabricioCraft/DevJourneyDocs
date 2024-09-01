# Sumário
- [Representando cores com CSS](#representando-cores-com-css)
- [Harmonia de cores](#harmonia-de-cores)
    - [Círculo Cromático](#círculo-cromático)
        - [Cores Primárias](#cores-primárias)
        - [Cores Secundárias](#cores-secundárias)
        - [Cores Terciárias](#cores-terciárias)
    - [Cores Complementares](#cores-complementares)
    - [Cores Análogas](#cores-análogas)
        - [Cores Análogas Relacionadas](#cores-análogas-relacionadas)
    - [Cores Triádicas](#cores-triádicas)
    - [Cores Quadráticas](#cores-qudráticas)
    - [Cores Tetrádicas](#cores-tetrádicas)
    - [Monocromia](#monocromia)
    - [Gradiente](#gradiente)
    - [Tipografia](#tipografia)
        - [Anatomia do tipo](#anatomia-do-tipo)
            - [Serifa](#serifa)

## Representando cores com CSS

 Exitem 3 formas de fazer a representação de cores em CSS:

 - Representando-as pelos nomes das cores

 ```html
 <h2 style="background-color: blue; color: white;">Exemplo de Cores</h2>
 ```

 - Representando-as por códigos hexadecimais, onde o tom mais baixo é 0 que
 significa tons mais escuros e o tom mais forte é 255 que significa tons mais claros.

 **A denominação RGB vem de: R(Red), G(Green) e B(Blue). Quanto mais baixo, mais escuro é a cor, quanto mais alto, mais claro é a cor**

 ```html
  <h2 style="background-color: rgb(0, 0, 255); color: rgb(255, 255, 255);">Exemplo de Cores</h2>
 ```

 - Representando-as por HSL
    - H(Hue ou Matriz) - Define a cor do objeto. No modelo HSL, o matiz é representado por um ângulo de 0 a 360 graus, onde 0 e 360 correspondem ao vermelho, 120 ao verde e 240 ao azul.

    - S(Saturation) - Define a intensidade da cor. Quanto maior a saturação, mais vibrante e intensa será a cor. No modelo HSL, a saturação é representada por um valor de 0 a 100%, onde 0% corresponde a uma cor completamente desaturada (tons de cinza) e 100% a uma cor totalmente saturada (corestão vibrantes).

    - L(Luminosity) - Define a claridade da cor.No modelo HSL, a luminosidade é representada por um valor de 0 a 100%, onde 0% corresponde ao preto absoluto e 100% ao branco absoluto. Valores intermediários representam diferentes níveis de luminosidade, permitindo criar uma ampla gama de tons e nuances de uma mesma cor.

```html
<h2 style="background-color: hsla(0, 100%, 50%, 0.928); color: hsl(0, 0, 100);">Exemplo de Cores</h2>
```
## Harmonia de cores

Uma paleta de cores tem de 3 à 5 cores.

### Círculo Cromático

Ao fazer um corte central no círculo, entre o vermelho-arroxeado e o amarelo-esverdeado, do lado esquerdo estão as cores frias e do lado direito as cores quentes

#### Cores primárias

- Amarelo
- Vermelho
- Azul

Estão simétricas no círculo cromático e formam um triângulo, formando uma harmonia.

#### Cores Secundárias

- Laranja
- Violeta
- Verde

#### Cores Terciárias

Mistura das cores primárias e secundárias. Elas são de tons pastéis e formam um hexágono no círculo cromático.

### Cores Complementares

Ao escolher as cores para compor um site, depois de escolher uma cor, a cor que mais combina com a cor escolhida está exatamente na sua oposição.

### Cores Análogas

São cores que não tem muito contraste uma com a outra, mas ainda assim são perceptives. Elas se sencontram ao lado uma da outra, ou seja, são cores vizinhas.

#### Cores Análogas Relacionadas

![Cores Análogas Relacionadas](./images/cores-analogas-relacionadas.png)

### Cores Triádicas

Combinação de três cores que estão igualmente espaçadas no círculo cromático, formando um triângulo equilátero.

![Cores Triádicas](./images/cores-triadicas.webp)


### Cores Qudráticas

É uma harmonia semelhante à harmonia de cores triádicas, exceto que neste esquema harmónico existem quatro cores, todas equidistantes no círculo cromático.

![Cores Quadráticas](./images/cores-quadraticas.webp)

### Cores Tetrádicas

Esquema de cores que se caracteriza por uma paelte de quatro cores uniformemente distribuídas no círculo cromático, formando dois pares de cores complementares.

Para obter as cores tetrádicas, é necessário traçar um retângulo comprido no centro do círculo cromático.

![Cores Tetrádicas](./images/cores-tetradicas.png)


### Monocromia

Trabalha somente com uma cor com a mudança de duas características, luminosidade e saturação.

## Gradiente

Para configurar uma cor gradiente em um elemento, é necessário escolher o seletor, que nesse nosso caso é o ``body``, que permite que todo o corpor da página seja configurado de uma mesma forma.

Depois disso, passar a propriedade
`backgroung-image` que recebe o módulo `linear-gradient` ou `radial-gradient` dependendo da forma que vc deseja usar o gradiente.

Esse módulo leva como primeiro parâmetro a direção para onde a cor gradiente irá se deslocar `to right` ou `to left` ou `to up` ou `to down` ou ainda pode receber ângulos como `45deg`.

No caso do primeiro parâmetro, se optar pelo `radial-gradient`, ele deve ser necessariamente `circle`.

Ainda é possível passar porcentagem depois da cor para indicar o quanto daquela cor irá preencher a tela, por exemplo `#F5EE00 10%`. Isso faz com que a referida cor ocupe 10% da página.

```css

body{
    background-image: linear-gradient(to right, #F5EE00, #F5BB00, #E800F5, #6200F5,#A09C35);
}

```

## Tipografia

### Anatomia do tipo

Todas as letras minúsculas de uma fonte é baseada na letra 'x'. A altura das letras minúsculas é conhecida como **altura-x**.

Já a altura das letras maiúsculas é conhecida como **altura das maiúsculas**.

Algumas letras minúsculas vazam da altura, que conhecemos como altura-x, tanto para cima, como as letras 'k' e 'b', quanto para baixo, como a letra 'g'. Esse vazamento das letras para cima é chamado de **ascendente**, já o vazamento das letras para baixo é denominado **descendente**.

A altura total das letras considerando desde a altura das maiúsculas até o vazamento descendente das minúsculas é chamado de **corpo**.

#### Serifa

É um pequeno traço, barra ou prolongamento que se encontra no final das hastes de algumas letras, números e símbolos.

![Letras Serifas](./images/letras-serifa.JPG)

#### Categoria de Fontes

- **Serif** - Esse estilo de fonte é caracterizado por um design mais conservador.

    - **Marcas que usam serifas:** Zara, Tiffany & Co, Abercrombie & Fitch.

    - **Psicologia das fontes serifadas:** são populares entre empresas que buscam retratar uma marca **elegante e sofisticada.** Os logotipos com esses tipos de fontes evocam **tradição, respeito e confiança.** Além disso, as serifas ajudam as empresas a parecerem mais estabelecidas e são ideais para comunicar uma **identidade baseada em autoridade e grandeza.**

- **Sans-Serif -** Essas fontes são definidas pelas suas **linhas retas e simples.** Elas **não apresentam floreios e enfatizam a legibilidade e a simplicidade.**

    - **Marcas que usam fontes não serifadas:** LinkedIn, Calvin Klein e The Guardian.

    - **Psicologia da fonte não serifada:** esses tipos de fontes oferecem um **visual simples e descomplicado.** Elas **enfatizam a clareza**, com uma abordagem progressista – ***mas também podem ser ousadas e usadas para chamar a atenção com seu design refinado e eficiente.** As empresas que escolhem essa família de fontes priorizam um **senso de sensibilidade e honestidade** que não tem necessidade de floreios ou firulas.

- **Monoespaçada:** Se caracteriza por ter todas as letras e caracteres ocupando o mesmo espaço horizontal.



- **Handwritting (Script) -** Esses tipos de fontes também deixam de lado o visual de impressão compacto e **favorecem o estilo cursivo, mais natural.**

    - **Marcas que usam fontes caligráficas:** Coca-Cola, Instagram e Cadillac.

    - **Psicologia das fontes caligráficas:** evocam ideias de ***elegância, criatividade, liberdade e feminilidade.** Seus estilos curvados e floreados também comunicam uma **abordagem comercial mais prática e pessoal.** As empresas que querem transmitir uma emoção específica podem usar fontes caligráficas com um grande impacto. Da mesma forma, fontes caligráficas **são perfeitas para quem deseja transmitir uma sensação de pensamento singular e artístico.**

- **Decorativas (Display) -** As fontes decorativas, ou gráficas, **renunciam às convenções em favor de um corpo tipográfico único e atraente.** A maioria dos tipos decorativos é útil para diversos setores e necessidades, pois essas fontes geralmente são criadas sob medida para empresas específicas.

    - **Marcas que usam fontes decorativas:** Toys R’ Us, Lego e Fanta.

    - **Psicologia das fontes decorativas:** **transmitem singularidade e enfatizam a originalidade.** Além disso, sua flexibilidade permite às empresas decidirem em quais emoções se concentrarem, misturando e combinando diferentes estilos de fontes. Algumas das emoções mais desencadeadas são a sensação de **informalidade, diversão e pensamento criativo.** Elas também podem evocar memes específicos da cultura ou características ou temas que lembram uma determinada época.
![Categoria de Fontes](./images/categoria-de-fontes.JPG)

